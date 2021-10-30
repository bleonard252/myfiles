---
title: Overview
---
Myfile is a profile in a file that is easily referred to by the notation `host//user`. For example, my Myfile address might be `blogold.xyz//blake`. You can navigate to that in a browser to go to my profile page, composed from the data you see if you fetch it with `Accept: application/json` (or sometimes `?type=json`).

## Why Myfile?
1. Webfinger isn't very useful for profiles or the like.
2. Myfile is a universal and user-readable profile serialization.
3. You can use fields nothing else is supposed to use and (if it keeps with the naming schemes) it's completely valid.
4. Myfiles are read like regular HTTP files.

## Myfile implementation trivia
* Looking up a Myfile is a simple HTTP request. If you want to keep Myfile pages at their normal location, you must implement, i.e. an Express middleware or a PHP handler.
* The best practice is to present your Myfile as minified JSON. Myfiles rely upon the ubiquity of JSON; it's a required filetype to present it as. You can use YAML, TOML, XML, HTML, or really whatever you want to present the Myfile as long as the JSON version is accessible by `?type=json` and/or the `Accept` header.
* Since Myfile usernames can include `.`, you cannot use ".json" or any file extension of that sort for the server to present the Myfile as JSON or whatever format. You must use the Accept header or the "type" query string.
* You need to set up CORS to accept all hosts. CORS is a pain in the butt for this type of thing.