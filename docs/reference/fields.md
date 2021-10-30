---
title: Fields
---
All fields are optional. These are base fields. The fields in [References](references) also apply. 

(Formatted as **`fieldname`: Value type**)

`name`: string (display name)
: This is the name the user should see upon visiting the Myfile's page. If this is not present, it falls back on the username.

`description`: string
: This is the *bio* section of the Myfile's profile. This explains the purpose of the Myfile or describes what it represents.

`picture`: Address as string
: This is a an address (data: URIs recommended) to a profile picture. The address needs to be a URL beginning with the scheme (including the signature `://`) or a Multiformats address beginning with a `/`. Since Multiformats isn't very well adopted, they may be ignored.

`type`: Type as string
: The current types are: `["person", "event", "organization", "place", "website"]`. If a valid type is not set, it is assumed to be "`person`."

`links`: Array of string
: Each link can be in Markdown format, i.e. `[Label](URL)`, or can be the URL itself. Due to the way browsers handle links, it is not recommended to use Multiformats addresses here.

`publickey`: string (JSON-escaped armored public key string)
: The **PUBLIC KEY** that represents/belongs to the (person represented by the) Myfile. <font color="red">**NEVER use a private key in a Myfile!**</font> This is used to verify the `owner` of most non-`"person"` Myfiles, such as websites.

`owner`: MyfileAddress as string
: The Myfile address to a party responsible for this Myfile or what it represents. If the owner has a `"publickey"` set, then the property (the Myfile this field is on) must have a `"verification"` field.

`cards`: Array of Card
: See [Cards](cards).

`verification`: string
: See [Verification](verification).

`sshkey`: string
: The Myfile user's SSH **PUBLIC KEY.** <font color="red">**NEVER use a private key in a Myfile!**</font> Servers can use this to allow users to authenticate to their servers.