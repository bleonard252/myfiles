---
title: References
---
Myfiles reference other things. We call these "references," to differentiate them from "links," which is for hyperlinks. References are quite similar in functionality to hyperlinks. They both reference a target. However, references use addresses relative to a particular service, usually internal ones. References, like links, are strings. Some of these are listed below.

(Formatted as **`fieldname`: Source or relationship type**)

`ap:actor`: ActivityPub
: The URL to an ActivityPub actor. Append /outbox, for example, to get posts. This allows software to look up an actor via the address here, allowing users of that software to use a Myfile address as a mention.

`ap:announcement`: ActivityPub
: The URL to an ActivityPub post (root post of a thread or latest announcement).

`email`: E-mail
: An email address corresponding to the Myfile.

`phone`: Telephony
: The Myfile's phone number. You can use this to call the user, etc.

`fax`: Telephony
: The Myfile's fax number. You can use this to fax the user, etc.

`ip4`: Internet
: The Myfile's IPv4 address. You can use this to access a server, etc. This is not recommended for use as it does reveal the location of the Myfile correspondent in a way that may not be intended.

`ip6`: Internet
: The Myfile's IPv6 address.

`website`: Internet
: This is the closest thing to a Link that is still a Reference. It refers to the Myfile owner's website.

`io.keybase.acct`: Keybase
: This corresponds to a Keybase username. You can input a verification in another field.

`location:latlong`: Physical location
: This corresponds to a location indicated by latitude and longitude. They are separated by a space.

`location:pluscode`: Physical location
: This corresponds to a location indicated by a Pluscode.

`org.openstreetmap.id`: Physical location/OpenStreetMap
: This corresponds to an OpenStreetMap item accessible from openstreetmap.org. This can then be used to get a location.
