# Disable Chrome's Topics API

Google's Topics API is a feature in Chrome that tracks your browsing habits to show "relevant" ads. Instead of
tracking you across websites with cookies, it assigns you interest categories (like "Fitness" or "Travel") based on
what you visit.

## Turn off Topics in Chrome

Open Chrome and type in the address bar `chrome://settings/privacy`

Scroll down to "Ad privacy" (or search for it) and disable all three options:

* "Ad Topics" (stops interest-based tracking)
* "Site-suggested ads" (blocks sites from recommending ads)
* "Ad measurement" (prevents tracking ad clicks)

Note: Google may still collect some data, but this reduces how much is used for ads.

## Why disabling Topics API is not enough

Even with these settings off, Chrome still:

* Tracks your IP address
* Keeps browser fingerprinting active
* Shares data with Google for "analytics"

For stronger privacy, consider [switching to a privacy-focused browser](../playbooks/chrome.md).
