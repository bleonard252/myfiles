---
title: Verification
---
To verify ownership of a Myfile:

1. Using the fingerprint of the owner's key (try `gpg --fingerprint`, it's the part with the 4 character chunks) and the Myfile addresses of the owner and property, match this example in a file:
```
566F 3272 E816 387F C202  ECD1 9311 427A DFCA 5407
blogold.xyz//blake
blogold.xyz//blogold.xyz
```
2. Sign that file. It should be armored but not cleartext, i.e. `gpg -sa <file>`.
3. Copy or export, then JSON-escape the response. That becomes the `verification` value, which ends up like this:
```yaml
"verification": "-----BEGIN PGP MESSAGE-----\n\nowGbwMvMwMU4WdCp6v6pEHbGNWlJjGVxXn8vmZqZuSkYG5kbKbhaGJopGFuYuyk4\nGxkYKSi4OrsYKlgaGxoqmBiZOyq4uDk7KpiaGJhzJeXkp+fnpOhVVFbp6yflJGan\nogvBOVydjJtZGBi5GGTFFFnC8o2KXohZ1B9ienMR5hBWJpAjGLg4BWAimZ+5/yc2\nm0qcN85QY81pdTE8dnPFdM1c1ZvTns6Mcig8+iq7qpol2d20lLH1Za77roadBU0X\nl9R+lblrlsHW9NBwzkv1gJ1FLj3rVwv/i5cKtmrmun04Mj3H+pOnVBjbxuqcZCkt\nPpHJwhPvcM04u1L+T7vhBMYHrL2FzPxxni+PtyXwsnoxX/5k3rbpcdJZtftiXjzn\nj0iKLZB6vG/GmlgzgSORdqE/qjMu6D2VDja6plR9fnP15uurGY97zpjClVQ9/cAV\nwfVdj+ZK+E5Zv/vaodCcR05PK1sCYzxSLpReWZ/lkuN/XTD+ptETYbl3gddUfj7a\nu9PsMMeLR79jc5RPXe5fIfS/J7U+I/DkxVe1/+O+CZYdz7JsbdJUXPt9WZSS7bst\nK8+dvuzb1/fhw/Mj4hnuUaJqP57fjF12XIVdWujFIcEj6xqWCjzcH3M/vNjt7vHj\nqoWmsdPkTiupFbBtYZ/zm1OpPP7mhKmtdbwHYn4H3Srdtfrku1Krx/99X6+OiXeI\n9bI++m/BGl1Dz2cSkdevGuUIAwA=\n=pj2g\n-----END PGP MESSAGE-----"
```
This value is then to be checked against the owner's key, and the addresses in the message have to match the owner and property addresses.