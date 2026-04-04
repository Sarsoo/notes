---
date: 2026-04-04
title: Encryption Workflow
---
[OpenSSL Tutorial](https://www.cs.toronto.edu/~arnold/427/19s/427_19S/tool/ssl/notes.pdf)
# Encrypt with opposing Pub
- 🚨 won't work 🚨
	- Too big, use symmetric
```bash
openssl pkeyutl \
	-encrypt \
	-in largefile.txt \
	-pubin -inkey pubkey-B.pem \
	-out ciphertext.bin
```

# 1. Symmetric Key Delivery
## Generate symmetric key
```bash
openssl rand \
	-base64 32 \
	-out symkey.pem
```

## Encrypt symmetric key
```bash
openssl pkeyutl \
	-encrypt \
	-in symkey.pem \
	-pubin -inkey pubkey-B.pem \
	-out symkey.enc
```

## Hash and Sign
```bash
openssl dgst \
	-sha1 \
	-sign privkey-A.pem \
	-out signature.bin \
	symkey.pem
```

# 2. Encryption
## Decrypt symmetric key
```bash
openssl pkeyutl \
	-decrypt \
	-in symkey.enc \
	-inkey privkey-B.pem \
	-out symkey.pem
```

## Verify hashed signature
```bash
openssl dgst \
	-sha1 \
	-verify pubkey-A.pem \
	-signature signature.bin \
	symkey.pem
```

## Encrypt symmetrically
```bash
openssl enc \
	-aes-256-cbc \
	-pass file:symkey.pem \
	-p \
	-md sha256 \
	-in largefile.txt \
	-out ciphertext.bin
```

# 3. Decryption
```bash
openssl enc \
	-aes-256-cbc \
	-d \
	-pass file:symkey.pem \
	-p \
	-md sha256 \
	-in ciphertext.bin \
	-out largefile.txt
```
