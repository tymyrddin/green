# Cross-app & cross-device tracking

***Your phone is not just listening. It's gossiping — across the whole digital garden.***

When you tap “Accept” on an app’s privacy policy (or, more likely, don’t), you’re handing over more than just 
permissions. You're effectively inviting a swarm of third-party trackers to set up shop in your digital greenhouse. 
And they’re not content with just watching your tomatoes grow — they’re following you through the whole garden, 
shed to compost heap.

Modern tracking doesn’t stop at a single app, or even a single device. Using techniques like Mobile Ad IDs (MAIDs) 
and device fingerprinting, advertisers and data brokers link your activity across apps and across devices — phone, 
laptop, smart fridge, smartwatch, smart speaker, smart kettle (probably).

Here’s how it works:

* Your phone, tablet, and laptop each give off a unique scent trail — called a “fingerprint” — based on screen size, language, browser plugins, battery level, font list, and more.
* This fingerprint can identify you even if you switch accounts, turn off cookies, or don a digital wig and sunglasses.
* Your MAID is basically your ad surname. It’s meant to be “resettable,” but resetting it is buried deeper than a cat’s shame. Apps trade it like Pokémon cards.

A 2025 study found that 73% of mobile apps share data with five or more third parties. Not just ad platforms — but 
location brokers, behavioural profilers, hedge funds, and anyone else willing to pay. If you're using a free weather 
app, there's a good chance it knows more about your habits than your GP.

And it doesn’t stop with apps.

## Enter the IoT circus

Your smart TV wants to know what you watch. Your fitness tracker knows when you sleep (and when you don’t). 
Your voice assistant hears you ask about how to boil an egg and records your emotional state while doing so.

These IoT devices quietly leak behavioural metadata — things like:

* When you’re home and active (smart lights)
* What you’re doing (smart speakers)
* How you’re feeling (sleep patterns, voice stress)
* Where you’ve been (location-sharing wearables)

They ping this data to servers run by manufacturers, “partners,” or whichever ad ecosystem has the biggest watering can. 
Even your doorbell might be making notes.

***You’re not just being tracked on the internet — you are the internet now.***

This interlinked tracking ecosystem builds a unified timeline of your life — app usage, web history, streaming 
habits, physical location, emotional state — and sells it on to anyone with cash and curiosity.

## Protections

* [Reset advertising IDs weekly](../pii/adids.md).
* [Segment IoT devices on a separate network](../pii/vlan.md).