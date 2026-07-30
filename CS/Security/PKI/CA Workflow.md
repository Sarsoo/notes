---
date: 2026-04-04
title: CA Workflow
tags:
  - security/pki
---
# Root Private Key
```bash
openssl genrsa \
	-out rootCA1.key.pem \
	-aes256 \ # encryption on the output
	-passout pass:ca1passwd # password for the encrypted output
	
# view
openssl rsa \
	-in rootCA1.key.pem \
	-passin pass:ca1passwd \
	-text -noout
```

# Self-Sign Root
```bash
mydn="/C=US/ST=Florida/L=Anytown/O=Acme Software Inc./OU=Database CA/"
mydn=${mydn}"CN=Database CA Root1/emailAddress=dba_ca1@acme.info"

openssl req \
	-new \
	-x509 \
	-key rootCA1.key.pem \
	-passin pass:ca1passwd \
	-subj "${mydn}" \
	-days 365 \
	-out rootCA1.cert.pem
```