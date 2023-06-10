# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: AES (Hard) ! Unsolved

### Challenge Description:

Hackers have encrypted a sensitive flag. We know they used AES 128-bit CBC mode encryption and that they used the UNIX timestamp as their encryption password. We believe they encrypted this file some time on 2023-01-01. Analyze the encrypted data and break their encryption and retrieve the flag.

### Challenge Questions:

1. When was the file encrypted?
2. What is the flag?


### Solution:



#### Step 1: Identify the format of the document information



#### Step 2: Use a decoder to decode the document information



#### Step 3: Provide answers to the challenge questions

#### Final Answer




## Conclusion:


## Excerpts from Methodologies and techhniques used from NCL Discord
```
for i in {1672531200..1672617600}; do  openssl aes-128-cbc -nosalt -d -k $i  -in ciphertext  -out /dev/stdout 2>/dev/null > out$i.txt && echo $i ; done
```
`1 liner and grep for SKY`
`Also the time stamp in UTC is key. I'm sure that screwed up many folks`
`bruteforce-salted-openssl and openssl. Make sure the encryption scheme is right and -nosalt`
`-pass "pass:$TIMESTAMP" is the most important part. openssl has a variety of options for encrypting, when given only a password instead of a key, it should be a hint that you're not putting in a key`



