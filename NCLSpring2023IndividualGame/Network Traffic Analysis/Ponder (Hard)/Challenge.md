# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: AES (Hard) ! Unsolved

### Challenge Description:

Can you figure out what data was exfiltrated?


### Challenge Questions:

1. What protocol is being used to exfiltrate data?
2. What is the flag?
3. What is the md5 of the extracted file?

### Solution:



#### Step 1: Identify the format of the document information



#### Step 2: Use a decoder to decode the document information



#### Step 3: Provide answers to the challenge questions

#### Final Answer

1. dns
2. SKY-DNSX-8452
3. 184E5B00BF82D36B67DBC01590B2AC67

## Conclusion:

## Excerpts from Methodologies and techhniques used from NCL Discord
`the flag was inside the zip file that you reconstruct from the base64 in the dnsq md5 the zip`
`so what i did was create a file called flag.txt
store flag there
and then md5sum that`
`Change the underscores to /'s
Forward slashes are valid base64 (as a seperator?), replacing the underscores that were invalid`
`the file was a pkzip
unzip it, theres the flag
like the base64 encoded data was a zip file
cyberchef should (?) have told you that though via autodetect
if you guys arent using it already, its the most useful tool in all of these challenges`