---
title: Namespaces
---
Myfiles have several types of field namespacing:

* **URL-based namespacing.** This is mostly for compatibility with older systems. A URL can be the key.
* **Domain or family namespacing.** This is used for shared namespaces based on well-known names, standards, or protocols, such as ActivityPub or cryptography (`"ap:..."` and `"crypto:..."`).
* **Subnaming or reverse domain naming.** This is used for proprietary or other names, standards, protocols, websites, etc. For example, for a Google Play signing key, you might see a key like this: `"com.google.play.signing"` This format looks familiar if you're an Android developer or power user. (Technically, `com.google.play` is the namespace and `signing` is the name.)

Similarly, there are several types of field naming under namespaces or transcending them:

* **Unique naming.** This type of naming is completely unique because it uses a UUID to uniquely identify the field. This is not recommended as its function is not obvious.
* **Distinct naming.** This type of naming should be used in almost all scenarios. The purpose of the key is obvious and known.
