---
title: References
---
For Myfiles, references are used to indicate a relationship between a Myfile or its owner and an outside entity or identifier. The following are the standard reference fields. They go alongside the fields listed in the [Fields](fields.md) page. **All fields are optional** and are **strings** unless otherwise noted.

(Formatted as **`fieldname`: Source or relationship type**)

=== "Social"

    `ap:actor`: ActivityPub
    : The URL to an ActivityPub actor. This is what you append "/outbox" to, for example, to get posts. This allows software to look up an actor via the address here, allowing users of that software to use a Myfile address as a mention. This is also used to look up posts for a user.

    `ap:announcement`: ActivityPub
    : The URL to an ActivityPub post (say, a root post of a thread or latest announcement). This tells viewers what post to prioritize loading and showing above any others. The post does not have to be on the `ap:actor` account.

=== "Contact"

    `email`: E-mail
    : An email address corresponding to the Myfile.

    `phone`: Telephony
    : The Myfile's phone number. You can use this to call the user, etc.

    `fax`: Telephony
    : The Myfile's fax number. You can use this to fax the user, etc.

=== "Internet"

    `ip4`: Internet
    : The Myfile's IPv4 address. You can use this to access a server, etc. This is not recommended for use as it does reveal the location of the Myfile correspondent in a way that may not be intended.

    `ip6`: Internet
    : The Myfile's IPv6 address.

    `website`: Internet
    : This is the closest thing to a Link that is still a Reference. It refers to the Myfile owner's website.

    `io.keybase.acct`: Keybase
    : This corresponds to a Keybase username. You can input a verification in another field.

=== "Location"

    `location:latlong`: Physical location
    : This corresponds to a location indicated by latitude and longitude. They are separated by a space.

    `location:pluscode`: Physical location
    : This corresponds to a location indicated by a Pluscode.

    !!! info inline end ""
        
        `location:what3words` and `location:whatthreewords` are also accepted in place of `location:w3w`.
    
    `location:w3w`: Physical location
    : This corresponds to a location indicated by a What3Words address.

    `org.openstreetmap.id`: Physical location via OpenStreetMap
    : This corresponds to an OpenStreetMap item accessible from openstreetmap.org. This can then be used to get a location.
