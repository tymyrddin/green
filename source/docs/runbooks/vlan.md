# Isolating IoT devices on a guest network

Most home routers (ASUS, TP-Link, Netgear and others) support this.

1. Log into the router:
   * Enter the router's IP in a browser (usually 192.168.1.1 or 192.168.0.1).
   * The default login is often admin and a password printed on the router's sticker.
2. Enable the guest network:
   * Find Wireless Settings, Guest Network (ASUS, TP-Link) or Advanced, Guest Access (Netgear).
   * Name it something memorable.
   * Enable "Isolate devices", which stops the gadgets talking to each other.
3. Block internet access (optional):
   * Some routers can restrict a guest network to local-only, with no web access.
   * Look for "Client Isolation" or "AP Isolation" in the settings.
4. Connect the IoT devices to the guest network:
   * In each smart device's Wi-Fi settings, join the guest network instead of the main one.

The smart bulbs and cameras can then reach the internet, where allowed, but not the laptop or phone on the main network.

Last reviewed: 2026-07-08.
