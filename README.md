# Generating Private Key, Self-Signed Certificate and MD5 Hash using OpenSSL
OpenSSL is an open-source command line tool that is commonly used to generate private keys, create CSRs, install your SSL/TLS certificate, and identify certificate information.

Installation of OpenSSL on Linux:
```
sudo apt install openssl
```
To verify the installation and check the version of openssl:

```
openssl version
```
![version-openssl](https://github.com/malvika-thakur/OpenSSL/assets/60217652/46d515a7-9315-4878-b3de-68db1fd01239)

To generate a private key:

```
openssl genpkey -algorithm RSA -out private.key
```
![val-openssl1 (xca)](https://github.com/malvika-thakur/OpenSSL/assets/60217652/5dbf13e8-729f-47c1-b425-2df8ef6ba652)


To generate a self-signed certificate:
```
openssl req -x509 -new -key private.key -out certificate.crt
```
![val-openssl2 (xca)](https://github.com/malvika-thakur/OpenSSL/assets/60217652/edcbb555-1aef-4bce-a5b5-31e5a5fa4b2e)

To verify and view the generated private.key:
```
cat private.key
```
![val-openssl3 (xca)](https://github.com/malvika-thakur/OpenSSL/assets/60217652/8bc36964-4404-44fd-ad6d-5dc2f54df527)

To verify and view the generated certificate.crt:
```
cat certificate.crt
```
![val-openssl4 (xca)](https://github.com/malvika-thakur/OpenSSL/assets/60217652/9cebe283-eda2-47a5-a5e5-f7b8350cbf58)

To generate MD5 Hash for X.509 Certificate Modulus:
```
openssl x509 -noout -modulus -in certificate1.crt | openssl md5
```
To generate MD5 Hash for RSA Private Key Modulus:
```
openssl rsa -noout -modulus -in private.key | openssl md5
```
![val-openssl5 (xca)](https://github.com/malvika-thakur/OpenSSL/assets/60217652/bb74bfe7-9252-4168-abdb-2614293b252e)

