# Browser fingerprinting

Cookies can be cleared. IP addresses can be hidden behind a VPN. But the browser itself is a kind of signature. A fingerprinting script, running silently when a page loads, assembles a profile from the properties of the browser and device: the screen dimensions, the installed fonts, the GPU and its driver, the time zone, whether cookies are enabled, the exact version of the rendering engine. Each value is unremarkable on its own. Together they form a combination that is statistically unique for the vast majority of browsers in the world.

## How it works

The script runs in the browser as ordinary JavaScript. No permissions are requested. No download occurs. The browser discloses these properties as a normal part of rendering web content, and the script simply collects and combines them.

```
collect from browser environment:
    user-agent string         → browser name, version, OS
    screen resolution         → width × height in pixels
    colour depth              → bits per pixel
    time zone offset          → inferred location
    hardware thread count     → number of CPU cores
    cookie and JS settings    → privacy configuration
    installed fonts:
        for each font in candidate list:
            render a string using that font
            measure the pixel width of the rendered output
            if width differs from default → font is installed
    GPU fingerprint:
        draw a specific shape using WebGL
        read back the pixel values
        hash the result → reflects GPU vendor and driver version

combine all collected values
hash the combination → fingerprint string
```

The font detection step exploits the fact that each installed font renders text at a slightly different width. By measuring rendered widths for a list of candidate fonts, the script can determine which fonts are installed without directly querying the font list. The WebGL step draws something on the graphics hardware; because different GPUs and drivers produce slightly different results even for identical instructions, the output is a signature of the hardware configuration.

The complete fingerprint is sent to the tracking service and stored. On a return visit, from any site using the same service, the same fingerprint is generated and matched. The user has not logged in, has not accepted cookies, and may be behind a different IP address. They are still recognised.

## What this reveals

Browser fingerprinting is widely used in advertising, fraud detection, and analytics. Its value lies precisely in its persistence: it survives the privacy measures most users take. A person who clears their cookies, uses private browsing, and changes their IP address still presents the same fingerprint if they have not changed their browser, device, or configuration.

Research from the Electronic Frontier Foundation found that over 80% of browsers had a unique fingerprint among their test population. Amiunique.org allows anyone to check their own browser's uniqueness in the current distribution.

## Defences

The Tor Browser and Firefox with `privacy.resistFingerprinting` enabled return randomised or normalised values for many of the measurements fingerprinting relies on, making each session appear to be a different browser. Using a common browser on a common operating system, without unusual fonts or extensions, reduces uniqueness because more people share the same configuration. Browser extensions such as uBlock Origin block many fingerprinting scripts from running at all. The most complete defence is the Tor Browser, which is specifically designed to make all users appear identical to outside observers.
