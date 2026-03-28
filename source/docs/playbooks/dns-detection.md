# Detect stalkerware using DNS monitoring

This playbook describes using DNS-level monitoring to identify connections consistent with stalkerware and spyware. When a device runs stalkerware, the software must contact its servers to deliver the data it collects. Before it can contact those servers, it must look up their addresses in the domain name system. That lookup is visible to whoever controls the DNS resolver the device is using.

This approach requires neither specialised hardware beyond a computer or a router, nor any modification to the device being checked. It is less detailed than full traffic capture but substantially easier to set up and run continuously.

Before checking anyone else's device, confirm you have their informed consent and that they understand what the process involves. The person whose device is being checked should be present and in control of the decision.

## How it works

Every device on a network, by default, uses a DNS resolver to translate domain names into IP addresses. Stalkerware that phones home to a command-and-control server must resolve that server's domain name. If you control the DNS resolver, you can log every domain the suspect device queries and compare those queries against known stalkerware domains.

There are two ways to do this: run your own resolver on the local network (Pi-hole), or route the device's DNS queries through a filtering resolver that logs and blocks known threats (NextDNS).

## Option one: Pi-hole on your local network

Pi-hole is an open-source DNS resolver that runs on a Raspberry Pi, a spare computer, or in Docker on any machine. It logs all DNS queries from devices on your network and blocks those that match its blocklists. Several blocklists specifically target stalkerware and spyware command-and-control infrastructure.

Install Pi-hole using Docker if you have Docker already available. The Pi-hole documentation at docs.pi-hole.net covers installation in full. The Docker approach runs Pi-hole without modifying the host system:

```
docker run -d \
  --name pihole \
  --restart unless-stopped \
  -e TZ=Europe/London \
  -e WEBPASSWORD=choose-a-strong-password \
  -v pihole-data:/etc/pihole \
  -v dnsmasq-data:/etc/dnsmasq.d \
  -p 53:53/tcp -p 53:53/udp \
  -p 8080:80 \
  pihole/pihole
```

After Pi-hole is running, configure your router to use the Pi-hole's IP address as its primary DNS server. This routes all DNS queries from all devices on the network through Pi-hole. Alternatively, configure the DNS settings on the suspect device individually, pointing it at Pi-hole's IP.

Once configured, the Pi-hole dashboard (at its IP address on port 8080) shows all DNS queries from all devices. You can filter by the suspect device's IP address to see only its queries.

Add a stalkerware-focused blocklist to Pi-hole. The Exodus Privacy blocklist and the ones maintained by the Coalition Against Stalkerware project are good starting points. Add them under Group Management, Adlists in the Pi-hole dashboard, then run gravity update to load them.

Domains that appear in these lists will be blocked and logged. Blocked queries show up in the Pi-hole query log with the device's IP and the domain name. Any device that attempts to contact a known stalkerware domain will appear here.

## Option two: NextDNS

NextDNS is a cloud DNS resolver with a free tier that offers logging, filtering, and threat intelligence without requiring any local infrastructure. You create an account at nextdns.io, configure a profile with the blocklists you want enabled, and then point the suspect device at NextDNS's resolver addresses.

In the NextDNS dashboard, enable the security blocklists under the Security tab. The Threat Intelligence Feeds and Native Tracking Protection options cover a broad range of stalkerware and spyware infrastructure. You can also add custom blocklists if you have specific domains to watch for.

To configure the suspect device to use NextDNS, change its DNS settings to use the addresses provided in your NextDNS configuration page. On Android, go to Settings, Network and internet, Advanced, Private DNS, and enter the NextDNS hostname shown in your account. On iPhone, NextDNS provides a configuration profile to download and install.

The NextDNS logs tab shows every DNS query from the device, the time, whether it was blocked, and which blocklist matched. This gives you the same picture as Pi-hole but without needing to run local infrastructure.

The limitation of NextDNS is that the queries are processed on NextDNS's servers rather than locally. Consider whether this is acceptable for your context.

## What to look for

Once the suspect device is routing its DNS through Pi-hole or NextDNS, let it run normally for an extended period. The patterns worth noting are:

Domains matching known stalkerware blocklists. A direct match is a strong indicator. It does not prove stalkerware is installed, because some commercial products reuse infrastructure across legitimate and illegitimate deployments, but it warrants further investigation.

Regular queries to the same unfamiliar domain at consistent intervals. Stalkerware typically checks in with its server on a schedule. Queries to the same domain every few minutes, or every hour, that occur regardless of whether the device is in active use, suggest a background process rather than user-initiated activity.

Domains that resolve to hosting infrastructure commonly used for data collection, without an obvious connection to any application on the device.

DNS monitoring does not capture the content of communications or confirm what data was transmitted. It shows only that a connection was attempted. For more detailed traffic analysis, see the [PiRogue and Wazuh](pirogue-wazuh.md) or [PCAPdroid](pcapdroid.md) playbooks.

## If you see something concerning

If DNS monitoring surfaces domains matching stalkerware blocklists or suspicious patterns, contact a specialist organisation before taking action on the device itself. The Coalition Against Stalkerware (stopstalkerware.org) can connect you with technical experts. See the [check a device for stalkerware](stalkerware-check.md) playbook for the considerations around next steps, including the factory reset decision.
