---
layout: post
title: Best practices for cryptography
---


# General

1. Don't create your own cryptography solutions. Use libraries.
2. Keys are very important. Lose your key, lose your confidentiality.

# SSL/TLS


You specify cipher suites on your web server, and those suites are a mix of older ones that have not yet been broken, and newer ones that provide more protection.

It's complicated and changes often. The best resources I've found are here:

Test your implementation here: [SSL Labs Site Test](https://www.ssllabs.com/ssltest/index.html)

* [SSL Labs Docs](https://www.ssllabs.com/projects/best-practices/index.html)
* [SSL Labs PDF](https://www.ssllabs.com/downloads/SSL_TLS_Deployment_Best_Practices.pdf)


# Hash

When choosing a hashing function, the current recommendation is using SHA-256 or greater.

There is a secret about hashing algorithms - they can't prove they aren't reversible. But we haven't heard they are breakable at the specified levels.

## Storing passwords in databases.

Salt your hash when you're storing information, like passwords, that are vulnerable to rainbow tables. See [crack station](https://crackstation.net/) for more practical information on storing passwords in databases.

Remember that this concept might apply to other hashed information as well.

# HMAC

Closely related to hash is hmac. Go with the same recommendation as for hash.

The key should be as big as the bit-length. If you use hmac with sha-256, use a 256-bit key.

# Private/Public Cyphers and Keys

Use 2048-bit RSA or 256-bit ECDSA private keys for all your needs.

# Symmetric Cyphers

Use AES-CBC-256 for all your needs. Make sure the key is 256bits of random entropy.

# GPG

Use 4096-bit keys for your communication. See [EFF: PGP for Mac](https://ssd.eff.org/en/module/how-use-pgp-mac-os-x) and [EFF: PGP for Windows](https://ssd.eff.org/en/module/how-use-pgp-windows-pc) for details on using GPG/PGP and best practices.

Follow [Google's project](http://googleonlinesecurity.blogspot.com/2014/06/making-end-to-end-encryption-easier-to.html) to bring GPG to the web and gmail. This hasn't been done yet because HTML didn't support encryption through javascript. There are a lot of sites that explain why you can't trust encryption implemented in javascript. But it's [coming](https://dvcs.w3.org/hg/webcrypto-api/raw-file/tip/spec/Overview.html). With these new functions, we can finally look forward to GPG support on yahoo and gmail. Follow the project on github: [End-To-End](https://github.com/google/end-to-end).


