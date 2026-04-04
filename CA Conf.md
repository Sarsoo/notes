---
date: 2026-04-04
title: Untitled
---
[OpenSSL CA tutorial – A full-featured openssl PKI](https://grimoire.carcano.ch/blog/openssl-ca-tutorial-a-full-featured-openssl-pki/)

# Root
```ini
oid_section     = custom_oids

[ ca ]
default_ca = CA_default

[ CA_default ]
dir               = ##PKI_LIB_PATH##/##CA_LABEL##
certs             = ##PKI_CONF_PATH##/##CA_LABEL##/certs
private_key       = ##PKI_CONF_PATH##/##CA_LABEL##/keys/ca.key
certificate       = ##PKI_CONF_PATH##/##CA_LABEL##/certs/ca.crt
new_certs_dir     = $dir/certs
database          = $dir/db/index.txt
serial            = $dir/db/serial
default_md        = sha256
unique_subject    = no
policy            = policy_short
preserveDN        = no
email_in_dn       = no

[ custom_oids ]
CPS           = 1.3.6.1.4.1.##ENTERPRISE_OID##.1.1
CA-Cert       = 1.3.6.1.4.1.##ENTERPRISE_OID##.1.2
EV-Cert       = 2.23.140.1.1

[ policy_short ]
countryName             = match
organizationName        = match
organizationalUnitName  = optional
commonName              = supplied

[ req ]
distinguished_name = req_distinguished_name

[ req_distinguished_name ]

[ root_ca ]
subjectKeyIdentifier = hash
##AUTHORITY_KEY_IDENTIFIER##
keyUsage = critical,keyCertSign
basicConstraints = critical,CA:TRUE

[ crl_issuer ]
subjectKeyIdentifier = hash
authorityKeyIdentifier = keyid:always
keyUsage = critical,cRLSign,nonRepudiation,digitalSignature,keyEncipherment
basicConstraints = critical,CA:FALSE
extendedKeyUsage = OCSPSigning

[ aia ]
OCSP;URI.1=##OCSP_URI##
caIssuers;URI.2=##CAISSUERS_URI##

[ intermediate_ca ]
subjectKeyIdentifier = hash
##AUTHORITY_KEY_IDENTIFIER##
basicConstraints = critical,CA:TRUE
keyUsage = critical, keyCertSign, cRLSign
crlDistributionPoints = crl_dp
authorityInfoAccess = @aia
certificatePolicies = ia5org,@CPS,@CA_policy,@EV_policy

[ crl_dp ]
fullname = URI:##CRL_URI##
CRLissuer = dirName:crl_issuer_dn

[ crl_issuer_dn ]
C=##COUNTRY##
O=##ORGANIZATION##
CN=##CA_NAME##

[ CPS ]
policyIdentifier = CPS
CPS.1            = "##CPS_URL##"
userNotice.1     = @CPS_Notice

[ CPS_Notice ]
explicitText  = "##CA_NAME## Certification Practice Statement"

[ CA_policy ]
policyIdentifier = CA-Cert
userNotice.2     = @CA_Notice

[ CA_Notice ]
explicitText  = "CA Certificate Policy"

[ EV_policy ]
policyIdentifier = EV-Cert
userNotice.6     = @EV_Notice

[ EV_Notice ]
explicitText  = "Certificate issued in compliance with the Extended Validation Guidelines"
```

[llekn](https://github.com/llekn) / **[openssl-ca](https://github.com/llekn/openssl-ca)**
```ini
# This config file is meant to provide sane values to OpenSSL
# to create a CA and sign certificates for typical webu usage
# (i.e. webserver, database connections, etc)
# It is possible to tweak verious configurations like
# extendedKeyUsage params.

HOME = .


[ ca ]
default_ca = CA_default


[ CA_default ]
dir              = .
serial           = $dir/serial
database         = $dir/index.txt
new_certs_dir    = $dir/newcerts
certificate      = $dir/CA/ca.crt
private_key      = $dir/CA/private/ca.key
default_days     = 730
default_md       = sha512
preserve         = no                     # whether keep DN ordering
email_in_dn      = no
nameopt          = default_ca
certopt          = default_ca
policy           = policy_match

crlnumber        = $dir/crlnumber         # the current crl number
crl              = $dir/crl/crl.pem       # The current CRL
default_crl_days = 30                     # how long before next CRL

RANDFILE         = $dir/CA/private/.rand  # private random number file
copy_extensions  = copy                   # Honor extensions requested of us


[ req ]
default_bits       = 2048                 # Size of keys
default_keyfile    = key.pem              # name of generated keys
default_md         = sha256               # message digest algorithm
string_mask        = utf8only             # permitted characters
distinguished_name = req_distinguished_name
req_extensions     = v3_req


[ req_distinguished_name ]
0.organizationName      = Organization Name (company)
#organizationalUnitName = Organizational Unit Name (department, division)
#emailAddress           = Email Address
#emailAddress_max       = 40
localityName            = Locality Name (city, district)
stateOrProvinceName     = State or Province Name (full name)
countryName             = Country Name (2 letter code)
countryName_min         = 2
countryName_max         = 2
commonName              = Common Name (hostname, IP, or your name)
commonName_max          = 64

# Defaults:
#0.organizationName_default     = Default ON
#organizationalUnitName_default = Default UN
#localityName_default           = Default LN
#stateOrProvinceName_default    = Default PN
#countryName_default            = Default CN
#emailAddress_default           = Default EA
commonName_default              = ${ENV::SUBJECT_ALT_NAME}


[ v3_req ]
basicConstraints     = critical,CA:FALSE
subjectKeyIdentifier = hash
keyUsage             = nonRepudiation, digitalSignature, keyEncipherment, dataEncipherment
extendedKeyUsage     = critical,serverAuth, clientAuth
subjectAltName       = critical,DNS:${ENV::SUBJECT_ALT_NAME},DNS:www.${ENV::SUBJECT_ALT_NAME},email:move


[ v3_ca ]
basicConstraints       = critical,CA:TRUE
subjectKeyIdentifier   = hash
authorityKeyIdentifier = keyid:always,issuer:always
keyUsage               = cRLSign, keyCertSign
issuerAltName          = issuer:copy
subjectAltName         = critical,DNS:${ENV::SUBJECT_ALT_NAME},email:move


[ policy_match ]
countryName            = match
stateOrProvinceName    = match
organizationName       = match
organizationalUnitName = optional
commonName             = supplied
emailAddress           = optional


[ crl_ext ]    # CRL extensions.
issuerAltName          = issuer:copy
authorityKeyIdentifier = keyid:always,issuer:always
```

# Intermediate
```ini
oid_section     = custom_oids

[ ca ]
default_ca = CA_default

[ CA_default ]
dir               = ##PKI_LIB_PATH##/##CA_LABEL##
certs             = ##PKI_CONF_PATH##/##CA_LABEL##/certs
private_key       = ##PKI_CONF_PATH##/##CA_LABEL##/keys/ca.key
certificate       = ##PKI_CONF_PATH##/##CA_LABEL##/certs/ca.crt
new_certs_dir     = $dir/certs
database          = $dir/db/index.txt
serial            = $dir/db/serial
default_md        = sha256
unique_subject    = no
policy            = policy_short
preserveDN        = no
email_in_dn       = no

[ custom_oids ]
CPS           = 1.3.6.1.4.1.##ENTERPRISE_OID##.1.1
CA-Cert       = 1.3.6.1.4.1.##ENTERPRISE_OID##.1.2
DV-Cert       = 2.23.140.1.2.1
OV-Cert       = 2.23.140.1.2.2
IV-Cert       = 2.23.140.1.2.3
EV-Cert       = 2.23.140.1.1

[ policy_short ]
countryName             = match
organizationName        = match
organizationalUnitName  = optional
commonName              = supplied

[ req ]
distinguished_name = req_distinguished_name

[ req_distinguished_name ]

[ crl_issuer ]
subjectKeyIdentifier = hash
authorityKeyIdentifier = keyid:always
keyUsage = critical,cRLSign,nonRepudiation,digitalSignature,keyEncipherment
basicConstraints = critical,CA:FALSE
extendedKeyUsage = OCSPSigning

[ aia ]
OCSP;URI.1=##OCSP_URI##
caIssuers;URI.2=##CAISSUERS_URI##

[ intermediate_ca ]
subjectKeyIdentifier = hash
##AUTHORITY_KEY_IDENTIFIER##
basicConstraints = critical,CA:TRUE
keyUsage = critical, keyCertSign, cRLSign
crlDistributionPoints = crl_dp
authorityInfoAccess = @aia
certificatePolicies = ia5org,@CPS,@CA_policy,@EV_policy

[ dv ]
subjectKeyIdentifier = hash
##AUTHORITY_KEY_IDENTIFIER##
basicConstraints = critical,CA:FALSE
keyUsage = critical, digitalSignature, keyEncipherment
extendedKeyUsage = critical, serverAuth
crlDistributionPoints = crl_dp
authorityInfoAccess = @aia
certificatePolicies = ia5org,@CPS,@DV_policy

[ iv ]
subjectKeyIdentifier = hash
##AUTHORITY_KEY_IDENTIFIER##
basicConstraints = critical,CA:FALSE
keyUsage = critical, digitalSignature, keyEncipherment
extendedKeyUsage = critical, serverAuth
crlDistributionPoints = crl_dp
authorityInfoAccess = @aia
certificatePolicies = ia5org,@CPS,@IV_policy

[ ov ]
subjectKeyIdentifier = hash
##AUTHORITY_KEY_IDENTIFIER##
basicConstraints = critical,CA:FALSE
keyUsage = critical, digitalSignature, keyEncipherment
extendedKeyUsage = critical, serverAuth
crlDistributionPoints = crl_dp
authorityInfoAccess = @aia
certificatePolicies = ia5org,@CPS,@OV_policy

[ ev ]
subjectKeyIdentifier = hash
##AUTHORITY_KEY_IDENTIFIER##
basicConstraints = critical,CA:FALSE
keyUsage = critical, digitalSignature, keyEncipherment
extendedKeyUsage = critical, serverAuth
crlDistributionPoints = crl_dp
authorityInfoAccess = @aia
certificatePolicies = ia5org,@CPS,@EV_policy

[ crl_dp ]
fullname = URI:##CRL_URI##
CRLissuer = dirName:crl_issuer_dn

[ crl_issuer_dn ]
C=##COUNTRY##
O=##ORGANIZATION##
CN=##CA_NAME##

[ CPS ]
policyIdentifier = CPS
CPS.1            = "##CPS_URL##"
userNotice.1     = @CPS_Notice

[ CPS_Notice ]
explicitText  = "##CA_NAME## Certification Practice Statement"

[ CA_policy ]
policyIdentifier = CA-Cert
userNotice.2     = @CA_Notice

[ CA_Notice ]
explicitText  = "CA Certificate Policy"

[ DV_policy ]
policyIdentifier = DV-Cert
userNotice.3     = @DV_Notice

[ DV_Notice ]
explicitText  = "Compliant with Baseline Requirements – No entity identity asserted"

[ IV_policy ]
policyIdentifier = IV-Cert
userNotice.4     = @IV_Notice

[ IV_Notice ]
explicitText  = "Compliant with Baseline Requirements – Individual identity asserted"

[ OV_policy ]
policyIdentifier = OV-Cert
userNotice.5     = @OV_Notice

[ OV_Notice ]
explicitText  = "Compliant with Baseline Requirements – Individual identity asserted"

[ EV_policy ]
policyIdentifier = EV-Cert
userNotice.6     = @EV_Notice

[ EV_Notice ]
explicitText  = "Certificate issued in compliance with the Extended Validation Guidelines"
```
