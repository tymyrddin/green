# Disabling Chrome's Topics API

Chrome's Topics API tracks browsing habits to show "relevant" ads. Rather than following a user across sites with cookies, it assigns interest categories (such as "Fitness" or "Travel") based on the sites visited.

## Turn Topics off

Open Chrome and enter `chrome://settings/privacy` in the address bar.

Scroll to "Ad privacy" (or search for it) and disable all three options:

* Ad Topics, which stops interest-based categorisation
* Site-suggested ads, which blocks sites from recommending ads
* Ad measurement, which prevents tracking of ad clicks

Google may still collect some data, but this reduces how much is used for ads.

## Why it is not enough

Even with these off, Chrome still tracks the IP address, keeps browser fingerprinting active, and shares data with Google for "analytics". For stronger privacy, consider [switching to a privacy-focused browser](../playbooks/chrome.md).
