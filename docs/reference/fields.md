---
title: Basic Fields
---
**All fields are optional.** These are some of the fundamental fields that all viewers should recognize and display. The fields in [References](references) also apply.

(Formatted as **`fieldname`: Value type**)

`name`: string
: This is the name the user should see upon visiting the Myfile's page. If this is not present, it falls back on the username.

`nickname`: string
: A name that the user prefers to go by, displayed prominently in place of the `name` if set. Some viewers may show the `name` beneath this, such as myfv, which displays the real name next to the pronouns when a `nickname` is set.

`description`: string
: This is the *bio* section of the Myfile's profile. This explains the purpose of the Myfile or describes what it represents.

`image`: Address as string
: This is a an address (data: URIs recommended) to a profile picture. The address needs to be a URL beginning with the scheme (including the signature `://`) or a Multiformats address beginning with a `/`. Since Multiformats isn't very well adopted, they may be ignored.
: **NOTE:** `picture` is still accepted, however clients and servers alike should start using `image` instead.

`banner`: Address as string
: This address should go to an image that may be used by viewer software in a way similar to Twitter banners. This is distinct from a background image or wallpaper, which displays behind the entire profile.

`pronouns`: Pronouns as string
: This is a standard, run-of-the-mill pronoun indicator. No specific format is required, but it is recommended to use a format such as "he/him" or all forms, such as "she/her/her/hers/herself" to convey what you feel needs conveying.

`type`: Type as string
: The current types are: `["person", "event", "organization", "place", "website"]`. If a valid type is not set, it is assumed to be "`person`." This may affect how a Myfile is rendered. For example, organization Myfiles may show or prioritize a member list, and a website Myfile may prioritize links.
: This option may be deprecated in the future in favor of display options.

`links`: Array of string
: Each link can be in Markdown format, i.e. `[Label](URL)`, or can be the URL itself. Due to the way browsers handle links, it is not recommended to use Multiformats addresses here.

`publickey`: string (JSON-escaped armored public key string)
: The **PUBLIC KEY** that represents/belongs to the (person represented by the) Myfile. **NEVER use a private key in a Myfile!**{: style="color:#ffc107"} This is used to verify the `owner` of most non-`"person"` Myfiles, such as websites.

`owner`: Myfile Address as string
: The Myfile address to a party responsible for this Myfile or what it represents. If the owner has a `"publickey"` set, then the property (the Myfile this field is on) must have a `"verification"` field.

`cards`: Array of Card
: See [Cards](cards).

`verification`: string
: See [Verification](verification).

`sshkey`: string
: The Myfile user's SSH **PUBLIC KEY.** **NEVER use a private key in a Myfile!**{: style="color:#ffc107"} Servers can use this to allow users to authenticate to their servers.