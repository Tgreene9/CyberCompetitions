# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: PGP (Medium)

### Challenge Description:
We're sending you a secure communication, please decrypt the message. Please then respond to the encrypted message using the same encryption protocol here. We'll decrypt your message and read its contents.

Note: Please use a reputable tool that supports Modification Detection Code (MDC) as that is the best practice to correctly craft your response.

```
-----BEGIN PGP MESSAGE-----
Version: OpenPGP.js v4.10.10
Comment: https://openpgpjs.org

wYwDCGklPwNpJTUBA/9wmlmogYnxxNHf9EsFu0a0n/eLUVgMlfF/bioThZ6O
b1YgD5aTbez87MHDcFnytbYVGy83Yv0POEmeGP7Bdgu7tRha+rbq9zFeteQB
8Sb/A57keINHOCZbusLh+rr/W2ggHFXsKRYk6o+9bn1t8KYmYnEe2Z6ILivT
mj0wFfj2adLABwHp+zpM5HHwqmZ/ORVpeeCX1V2hIv0FCgjjACRwS1Qbw1pD
KSCiX/ynh8Jb15+8PHaEmn+mt0q4WV2GYci8FtxajQizRXxnViX6Mxe8pwCU
htw4E8WZm2ltxeCsuG5THI7PKv69C6XHcNtqLO2W03KT2jPFVP479HqdeJin
zCm10gKTvNm39W9tbFoIA5cZnJ3PSzcLdrq2WY4pdVpm3jD95KRNKHGeWwiS
c9Ow1oiaZAGb+QOpD1O/xGea5MxFGocbA1HZN/8=
=mUV8
-----END PGP MESSAGE-----
```

### Challenge Questions:

1. Please then respond to the encrypted message using the same encryption protocol here. We'll decrypt your message and read its contents.


### Solution:



#### Step 1: Identify the format of the document information



#### Step 2: Use a decoder to decode the document information



#### Step 3: Provide answers to the challenge questions

#### Final Answer

```
-----BEGIN PGP MESSAGE-----

hIwDP788M89ptnwBBACaiJrkNnMPypKZovrcyBn1N80wj+YfdCyoavwKzRmPG33j
wbaGbue58PquBV91rt+HaSP/QAPW0Ll0lod5NybmyvDwVo/v7+A7wgWBoLHxPPDL
j4q33QG0nHTNG07YxC0AWWaWnuN6k0KiFIeVDRBPTs6Pt2dHQb4K3p+p7dzNg9Jb
AV+bDU6xw921vCRz7I7RQKJeSnDTe0HbYhoZwBnt0YsTwN7d5yfHZWgdUEdKzrU8
dr7GEMZdCWP6nxXdPviA1W/quqWQh11hhDNduT0yrFDpWSPqYSYpOtFuTA==
=nAty
-----END PGP MESSAGE-----
```

## Conclusion:

## Excerpts from Methodologies and techhniques used from NCL Discord
`https://www.openpgp.org/software/kleopatra/ Downloaded keys and imported it into this app, and then it decrypted the message for me. As well as encrypted my message to send as an answer`

```
import gnupg

gpg = gnupg.GPG()



# Encrypt the message using the recipient's key
message = "the flag is SKY-PGPM-1104"
recipient = "C07CAEB88258B57D700C3E4E6F7FBEA07649C196"
encrypted = str(gpg.encrypt(message, recipient, always_trust=True, symmetric=False, armor=True, sign=False, passphrase=None))

# Print the encrypted message
print(encrypted)
```
