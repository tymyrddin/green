# Monitor device traffic with a spare Android phone

This playbook describes using a spare Android phone as a WiFi hotspot and running PCAPdroid on it to capture and analyse all traffic from a suspect device. It requires no specialised hardware beyond a second Android phone, and no modifications to the device being checked.

The phone acting as the monitor runs PCAPdroid. The suspect device connects to the hotspot that phone creates, and PCAPdroid captures all the traffic passing through it. You can then inspect that traffic, or export it for analysis elsewhere.

Before checking anyone else's device, confirm you have their informed consent and that they understand what the process involves. The person whose device is being checked should be present and in control of the decision.

## What you need

A spare Android phone running Android 7 or later. It does not need to be fast or have much storage; it is only acting as a hotspot and capture point. PCAPdroid is free and available on the Play Store and on F-Droid.

The suspect device can be any phone, tablet, or laptop that can connect to a WiFi hotspot. You do not need to install anything on it.

## Set up the hotspot

On the spare Android phone, go to Settings, then Network and internet, then Hotspot and tethering, then Wi-Fi hotspot. Give the hotspot a neutral name that will not raise suspicion if the person whose device you are checking notices it. Enable the hotspot.

## Install and configure PCAPdroid

Install PCAPdroid on the spare phone from the Play Store or F-Droid. Open it. On the main screen, set the capture mode to Root or, if the phone is not rooted, VPN mode. VPN mode does not require root and works for most purposes, though it captures the spare phone's own traffic rather than traffic from connected devices.

For capturing traffic from connected devices on an unrooted phone, you need a different approach: PCAPdroid can capture traffic that passes through it only when it acts as a VPN on the same device. To capture a connected device's traffic without root, see the note below on traffic mirroring.

On a rooted spare phone, PCAPdroid can run in traffic capture mode that intercepts all packets on the hotspot interface. This gives you a full view of everything the suspect device sends and receives.

If the spare phone is not rooted and you do not want to root it, the most practical path is to use the spare phone as a VPN endpoint and connect the suspect device through it, or to use the PCAPdroid remote capture feature if your setup supports it. The PCAPdroid documentation at emanuele-f.github.io/PCAPdroid covers these options in detail for the version you have installed.

## Running a capture

With PCAPdroid running and the suspect device connected to the hotspot, press the start button on PCAPdroid's main screen. Let the suspect device run normally for ten to twenty minutes: open the apps that are suspected of behaving badly, send and receive messages, and allow background processes to run.

PCAPdroid logs each connection in real time. The main view shows the remote host, the application on the monitored device that opened the connection (where this can be determined), and the data volume. You can tap any connection to see more detail.

Look for connections to hosts you do not recognise, particularly if they occur in the background without any visible activity on the suspect device. Regular periodic connections to the same external host, especially outside the times when an application would normally need to communicate, suggest a check-in or heartbeat from monitoring software.

PCAPdroid checks destinations against a blocklist of known malicious hosts. Connections that match appear flagged in the interface.

## Reviewing and exporting the capture

At the end of the session, PCAPdroid can export the capture as a PCAP file. This is a standard format readable by Wireshark and other analysis tools. If you want to inspect the traffic in more detail, or share it with a technical specialist, export the PCAP from the PCAPdroid menu and transfer it to a computer.

Wireshark can filter the PCAP by destination address, protocol, or time window to look at specific patterns. The PCAPdroid interface is sufficient for initial triage; Wireshark is useful for deeper investigation.

## What this does and does not tell you

PCAPdroid sees the network traffic at the IP level. It cannot decrypt traffic that is encrypted end-to-end, which most modern traffic is. What it can tell you is which remote hosts the device contacted, how often, and how much data was transferred.

A device contacting a known stalkerware server is a strong indicator. A device sending regular small packets to an unfamiliar host may indicate a heartbeat. Large data transfers at unexpected times may indicate exfiltration. None of these are conclusive alone, but patterns across a monitoring session build a picture.

If the assessment produces concerning results, contact a specialist organisation before taking action on the device itself. The Coalition Against Stalkerware (stopstalkerware.org) can connect you with technical experts. See the [check a device for stalkerware](stalkerware-check.md) playbook for the considerations around next steps.
