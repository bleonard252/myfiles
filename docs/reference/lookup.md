---
title: Lookup
---
This is the order/methodology of lookups. The first working copy found should be used. If all checks fail, then consider the Myfile does not exist.

## HTTPS/DNS-based Myfile lookups
1. Check the address directly. Consider it not working if the result is a 4xx class error or a 200 OK where the contents do not appear to be a Myfile.
2. Check `/.well-known/myfiles/<username>.json` (or, in the case of a "site" Myfile, `/.well-known/index.myfile.json`) and apply the same conditions to determine if it is working.
3. Check `/<username>.json` and apply the same checks.

If a 5xx class error results, try the same check again, perhaps with a timeout. If it persists, continue to another check. Then, if all checks fail with the same 5xx class error, show the user that error and explain it, as a Web browser would.

**Important!** All Myfile lookups should be done in HTTPS, unless you are using localhost or 127.0.0.1, in which case HTTP should be tried first.

## IPFS Myfile lookups
Myfiles that are formatted similar to `ipfs!Qm...//username` or `ipns!Qm...//username` (preferred) should be looked up using the following methodology:

1. Check `/<username>.json`. Fail if any IPFS error occurs or if the Myfile is invalid.
2. Check `/.well-known/myfiles/<username>.json` (or, in the case of a "site" Myfile, `/.well-known/index.myfile.json`) and apply the same checks.