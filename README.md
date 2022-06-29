# cryptoscan

cryptoscan is a bash script to check system binaries (like executables or
shared libraries) for embedded statically linked crypto implementations.

Currently it can detect AES, ChaCha20, Curve25519, DES, MD5, and SHA by
searching for well-known constants used within the respective algorithms.

## Usage

```
$ ./cryptoscan /bin
File                                              	Primitives
====                                               	==========
/bin/golang-shadow                                	SHA256 
/bin/golang-netrcauth                             	MD5 SHA1 SHA256 SHA512 
/bin/mkisofs                                      	MD5 SHA1 
/bin/dirmngr                                      	AES 
/bin/systemd                                      	MD5 SHA1 
/bin/golang-gitauth                               	AES ChaCha20 MD5 SHA1 SHA256 SHA512 
...
```
