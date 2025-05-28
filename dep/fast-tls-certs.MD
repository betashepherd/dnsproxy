## fast gen self-signed tls certs

```bash
openssl genpkey -algorithm RSA -out private.key -pkeyopt rsa_keygen_bits:2048\n
openssl req -new -key private.key -out certificate.csr\n
openssl x509 -req -days 3650 -in certificate.csr -signkey private.key -out certificate.crt
```
