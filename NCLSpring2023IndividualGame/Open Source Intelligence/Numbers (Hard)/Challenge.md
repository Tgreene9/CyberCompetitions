# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: Numbers (Hard)

### Challenge Description:

We have found a list of numbers that seem to be targeting entities in New Zealand. Can you find what organizations are being targeted?

### Challenge Questions:

1. 1743309846
2. 3389847817
3. 1952048332

### Solution:

I used the following steps to solve the challenge:

#### Step 1: Identify the format of the numbers

The numbers are binary representations of the IP addresses of the organizations being targeted. I used the following website to convert the binary numbers to IP addresses: https://www.binaryhexconverter.com/binary-to-ip-address-converter

#### Step 2: Use a decoder to decode the document information

I found a website that defined each section of the MRZ format; I used this to find all the information I needed to answer the challenge questions:

#### Step 3: Provide answers to the challenge questions

Based on the MRZ format, I was able to provide answers to all of the challenge questions:

1. Payment Express
2. New Zealand Post
3. One New Zealand Group Limited

## Conclusion:

The Document (Medium) challenge required decoding a document's information using the MRZ format. By completing this challenge, I learned about the MRZ format and how it is used to encode information on travel documents.

## Excerpts from Methodologies and techhniques used from NCL Discord
`https://www.xmyip.com/ip/`
`Use google search " operator with new zealand`
`Decimal to IP, whois on IPs`