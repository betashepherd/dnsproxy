## why do this 

if you are puzzled by dns leak, do is just 1 minue you will have a self-host dot server and you are free now.

## fast gen self-signed tls certs

```bash
openssl genpkey -algorithm RSA -out private.key -pkeyopt rsa_keygen_bits:2048
openssl req -new -key private.key -out certificate.csr
openssl x509 -req -days 3650 -in certificate.csr -signkey private.key -out certificate.crt
```
