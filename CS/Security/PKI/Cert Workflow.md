---
date: 2026-04-04
title: Cert Workflow
---
# Generate RSA Private Key
```bash
# generate private key
openssl genpkey \
	-algorithm RSA \
	-pkeyopt rsa_keygen_bits:2048 \
	-pkeyopt rsa_keygen_pubexp:3 \
	-out privkey-A.pem
```
- ~~`openssl genrsa -out yourdomain.key 2048`~~

```bash
# view content
openssl pkey \
	-in privkey-A.pem \
	-text \
	-noout
```
- ~~`openssl rsa -text -in yourdomain.key -noout`~~

```bash
# extract pub key
openssl pkey \
	-in privkey-A.pem \
	-pubout -out pubkey-A.pem
# view
openssl pkey \
	-pubin -in pubkey-A.pem \
	-text \
	-noout
```
- ~~`openssl rsa -in yourdomain.key -pubout -out yourdomain_public.key`~~

# Generate CSR
```bash
openssl req \
	-new \
	-key yourdomain.key \
	-out yourdomain.csr
```
- With inline details
```bash
openssl req -new -key yourdomain.key -out yourdomain.csr \ -subj "/C=US/ST=Utah/L=Lehi/O=Your Company, Inc./OU=IT/CN=yourdomain.com"
```

# Private Key + CSR
```bash
openssl req -new \ -newkey rsa:2048 -nodes -keyout yourdomain.key \ -out yourdomain.csr \ -subj "/C=US/ST=Utah/L=Lehi/O=Your Company, Inc./OU=IT/CN=yourdomain.com"
```

# View Cert as Text
```bash
openssl x509 \
	-in Alice.crt \
	-text \
	-noout
```

# Verify
```bash
openssl verify \
	-CAfile root.crt \
	Bob.crt
```
