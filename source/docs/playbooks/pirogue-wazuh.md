# Detect stalkerware using PiRogue and Wazuh

This playbook describes setting up a low-cost network monitoring station that can detect patterns consistent with stalkerware and spyware on a suspect device. It uses two open-source tools: the PiRogue Tool Suite on a Raspberry Pi, which creates an instrumented WiFi access point and analyses all traffic passing through it, and Wazuh on an old PC, which collects, stores, and correlates the alerts PiRogue produces over time.

This setup is intended for support workers, technically capable individuals helping a survivor check a device, or small organisations that handle sensitive device assessments. It requires some comfort with Linux and a willingness to follow documentation carefully. It is not a point-and-click solution.

Before checking anyone else's device, confirm you have their informed consent and that they understand what the process involves. The person whose device is being checked should be present and in control of the decision.

## What you need

The old PC runs Wazuh, which stores and analyses logs. It needs to meet the following minimum requirements or the indexer will perform poorly enough to be frustrating:

64-bit processor, at least four CPU cores, 8 GB of RAM (16 GB is considerably more comfortable), 50 GB of free disk space on an SSD (a spinning disk works but makes the indexer slow), and a network interface. Wazuh's all-in-one installer runs on Ubuntu 22.04 LTS or Debian 12. If the PC cannot run Ubuntu 22.04, it is probably too old for this purpose.

The Raspberry Pi runs PiRogue Tool Suite and acts as the WiFi hotspot through which the suspect device's traffic is routed. A Raspberry Pi 4 with at least 2 GB of RAM is required; 4 GB is recommended. You need a microSD card of at least 32 GB (Class 10 or A1 speed rating), a USB-C power supply rated at 5V/3A, and an ethernet cable to connect the Pi to your router. The Pi's built-in WiFi becomes the access point.

Both devices need to be on the same local network.

## Set up PiRogue

PiRogue Tool Suite is maintained by the Defensive Lab Agency and documented at pts-project.org. The installation process uses a setup script that runs on a fresh installation of Raspberry Pi OS Lite (64-bit).

Flash Raspberry Pi OS Lite (64-bit) to the microSD card using the Raspberry Pi Imager. Before writing, use the imager's settings to enable SSH and set a hostname and password. Connect the Pi to your router via ethernet, insert the card, and power it on.

SSH into the Pi and run the PiRogue installation script following the current instructions at pts-project.org/docs/. The script configures the WiFi interface as a hotspot, installs Suricata for network intrusion detection, sets up traffic capture and analysis, and starts a local dashboard accessible via the Pi's ethernet IP address on port 3000 (Grafana).

Once installation is complete, the Pi broadcasts a WiFi network. Connecting a device to this network routes all its traffic through PiRogue's analysis pipeline.

## Set up Wazuh

Wazuh provides an all-in-one installation script for single-node deployments that installs the indexer, manager, and dashboard together. The current script and instructions are at documentation.wazuh.com under the quickstart guide.

On the PC, install Ubuntu 22.04 LTS. Download the Wazuh installation assistant script and run it. The process takes fifteen to thirty minutes depending on the hardware. When it completes, the Wazuh dashboard is accessible via the browser at the PC's IP address on port 443. The installer prints the initial admin credentials.

## Connect PiRogue to Wazuh

Install a Wazuh agent on the Raspberry Pi. From the Wazuh dashboard, go to Agents, Deploy new agent, select Debian/Ubuntu as the OS, and follow the instructions to generate and run the agent installation command on the Pi. The agent registers itself with the Wazuh manager and begins forwarding system logs.

PiRogue generates alerts in its own log files, typically under `/var/log/pirogue/`. Configure the Wazuh agent on the Pi to monitor these files by adding them to the agent's `ossec.conf` under the `<localfile>` section. Wazuh will then ingest PiRogue's alerts alongside system logs and make them searchable and correlatable in the dashboard.

The PiRogue documentation includes specific guidance on log locations and formats for the current release. Check pts-project.org for the version you installed.

## Running an assessment

Connect the suspect device to PiRogue's WiFi network. Use the device normally for ten to twenty minutes, opening the applications that are suspected of behaving badly, checking email, using messaging apps, and generally allowing background processes to run.

Watch the PiRogue dashboard (the Pi's ethernet IP on port 3000) for outbound connections. PiRogue checks destinations against threat intelligence feeds that include known stalkerware command-and-control servers, data exfiltration endpoints, and tracking infrastructure. Connections to these flagged destinations appear as alerts.

In the Wazuh dashboard on the PC, the same alerts appear in the agent's event stream alongside any other indicators. Wazuh allows you to search across a time window, correlate events, and build a picture of what the device communicated with and when.

Patterns worth noting include regular periodic connections to the same external host (suggesting a heartbeat or check-in from monitoring software), connections to domains associated with commercial stalkerware products, unexpected connections during periods when the device appeared idle, and large outbound data transfers that are not accounted for by visible app activity.

## What this does and does not tell you

A positive match against a known stalkerware domain is a strong indicator but not conclusive proof of installation: 
some commercial products reuse infrastructure across legitimate and illegitimate deployments. An absence of matches 
does not confirm the device is clean: novel or custom stalkerware may not yet appear in threat intelligence feeds.

The value of PiRogue is in surfacing behavioural patterns, not just matching against a known list. Unexplained 
regular connections, unusual data volumes, and contact with unfamiliar infrastructure are all worth investigating 
further even when no threat intelligence match fires.

If the assessment produces concerning results, contact a specialist organisation before taking action on the device 
itself. The Coalition Against Stalkerware (stopstalkerware.org) can connect you with technical experts. The decision 
about whether to remove detected software, preserve evidence, or reset the device depends on the individual's safety 
and legal situation. See the [check a device for stalkerware](stalkerware-check.md) playbook for the considerations around that decision.
