# Cross-app and cross-device tracking

The identity a person uses on one app and the identity they use on another may feel entirely separate. They rarely are. Three distinct mechanisms allow tracking to follow a person across applications and devices without their awareness, and without requiring any single system to have complete information.

## Shared identifiers

When a user logs into an app with their email address, the app may hash that address and report it to a shared analytics service along with the user's behaviour. A second app, appearing unrelated, can do the same. The same hash arrives at the same endpoint from two different sources, and the connection is made silently in the backend.

```
# App A: user logs in, reports behaviour
user_hash = sha256(user_email)
send_to_tracker(user_hash, source="app_A", event="opened_app")

# App B: unrelated in appearance, same analytics partner
send_to_tracker(user_hash, source="app_B", event="clicked_ad")

# Tracker backend:
profile[user_hash] = merge(app_A_events, app_B_events)
```

The user never sees this connection. From their perspective, the two apps have nothing to do with each other. From the tracker's perspective, both streams of behaviour belong to the same person.

## Logged-in session correlation

If a user signs into the same account on a phone and a laptop, the service observes both devices as belonging to one identity. Behaviour on the phone and purchases on the laptop are combined into a single record.

```
sessions_for_user = ["device_phone", "device_laptop"]

activity = {
    "device_phone":  ["browsed travel sites", "searched for flights"],
    "device_laptop": ["visited airline site", "completed purchase"]
}

combined_profile = merge all activity across sessions_for_user
→ infer: user researched and then booked a flight
```

The cross-device picture is considerably more revealing than either device's record alone. The sequence of actions across devices shows decision-making, research patterns, and purchases in a way that single-device tracking cannot.

## Behavioural fingerprinting without any identifier

The third mechanism requires no shared login and no common identifier. A fingerprinting script running on different websites generates the same fingerprint from the same device regardless of which site is visited or which session is active. The behaviour is linked to a consistent device identity derived entirely from observable browser properties.

```
# Same device visits site_X and site_Y, both using the same fingerprinting service
fingerprint = generate(screen_resolution, fonts, GPU, browser_version, ...)

# site_X visit
tracker_database[fingerprint].append(site_X_behaviour)

# site_Y visit, different session, no cookies
tracker_database[fingerprint].append(site_Y_behaviour)

# Result: linked profile with no login required
```

## What this reveals

The combination of these three mechanisms means that the assumption of compartmentalisation, that using separate apps or clearing cookies separates one's identities, is largely false. A person using two apps owned by different brands but the same parent company, or two websites using the same analytics provider, will be tracked as one person. Their behaviour across those surfaces is combined, sold, and used for targeting without their knowledge.

## Defences

Separate browsers for separate contexts reduce fingerprint correlation across activities. Avoiding cross-platform login, particularly using a major platform account to log into third-party services, eliminates the shared-identifier mechanism. Reviewing which apps have access to email addresses in the device's privacy settings removes a common source of hashed identifier sharing. Blocking fingerprinting scripts through a browser extension addresses the third mechanism, though it requires regular maintenance as scripts adapt.
