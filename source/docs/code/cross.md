# Cross-app & cross-device tracking

## Context

Cross-app and cross-device tracking involves correlating a user’s identity across multiple apps and devices, often 
without their explicit consent. Techniques may involve:

* Shared identifiers (e.g. device ID, email hash)
* Behavioural fingerprinting
* Cloud-synchronised identifiers
* First-party tracking embedded across ecosystems

## Cross-app tracking via shared identifiers (hashed email)

Apps may collect login identifiers like email addresses, hash them, and share across apps or services owned by the 
same entity. ***Even if the apps appear unrelated to the user, the backend can correlate their behaviours using 
the hash.***

```
// App A
const userEmail = "user@example.com";
const hashedEmail = sha256(userEmail); // Use a proper cryptographic hash

// Send to analytics endpoint
fetch("https://tracker.example.com/collect", {
  method: "POST",
  body: JSON.stringify({
    id: hashedEmail,
    app: "com.example.appA",
    behaviour: "opened_app"
  }),
  headers: { "Content-Type": "application/json" }
});
```

Then, in App B:

```
// App B - same hash, different behaviour
fetch("https://tracker.example.com/collect", {
  method: "POST",
  body: JSON.stringify({
    id: hashedEmail,
    app: "com.example.appB",
    behaviour: "clicked_ad"
  }),
  headers: { "Content-Type": "application/json" }
});
```

## Cross-device tracking using logged-in sessions

If a user logs into the same account on multiple devices, tracking firms can synchronise their behaviour across 
devices. Profiling happens server-side using consistent logins.

```python
# Backend pseudocode (e.g. Python Flask)

user_sessions = {
    "user123": ["device_iphone", "device_macbook"]
}

activity_log = {
    "device_iphone": ["opened app", "browsed travel site"],
    "device_macbook": ["booked flight"]
}

# Stitching together a full behavioural profile
combined_behaviour = []
for device in user_sessions["user123"]:
    combined_behaviour.extend(activity_log[device])
```

## Behavioural fingerprinting (No shared ID needed)

Fingerprinting gathers subtle traits (device size, installed fonts, GPU, etc.) to identify users even across apps 
or websites. This kind of fingerprint can be used to recognise the same user across apps or sites, even when no 
explicit login is used.

```
// Simplified fingerprinting using canvas & device properties
function getFingerprint() {
  const canvas = document.createElement("canvas");
  const ctx = canvas.getContext("2d");
  ctx.textBaseline = "top";
  ctx.font = "14px Arial";
  ctx.fillText("fingerprint me", 2, 2);

  const canvasData = canvas.toDataURL();
  const fingerprint = sha256(
    navigator.userAgent + screen.width + screen.height + canvasData
  );

  return fingerprint;
}

const userID = getFingerprint();
console.log("Unique fingerprint:", userID);
```

## Cross-device tracking via household IP or Wi-Fi

Tracking systems can link devices used on the same IP address to a "household" profile. This is commonly used for 
attribution and ad delivery, even if identities differ per device.

```python
# Backend pseudo-matching logic
user1 = {"ip": "123.45.67.89", "device": "iPad", "behaviour": "watched ad"}
user2 = {"ip": "123.45.67.89", "device": "Smart TV", "behaviour": "bought product"}

if user1["ip"] == user2["ip"]:
    print("Likely same household — possible attribution")
```

## Summary

| Technique	                     | Identifier Used	       | Privacy Risk |
|--------------------------------|------------------------|--------------|
| Hashed email or login ID	      | Pseudonymous ID	       | High         |
| Login sessions across devices	 | Account correlation	   | High         |
| Fingerprinting	                | Device/browser traits	 | Very High    |
| IP-based tracking	             | Network identifiers	   | Medium       |

