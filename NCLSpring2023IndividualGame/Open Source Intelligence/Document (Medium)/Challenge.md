# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: Document (Medium)

### Challenge Description:

This information is encoding someone's document information, can you tell us more about what this is encoding?

```
P<USAFEDDER<<TOM<<<<<<<<<<<<<<<<<<<<<<<<<<<<
9026159592USA9002144M5002146<<<<<<<<<<<<<<02
```

### Challenge Questions:

1. What is the first name of the person?
2. What is the last name of the person?
3. When is the person's date of birth?
4. When is the document's expiration date?
5. What is the person's nationality?

### Solution:

I used the following steps to solve the challenge:

#### Step 1: Identify the format of the document information

To identify the format of the document information, I searched for "document information format" on Google and eventually came across the MRZ (Machine Readable Zone) format. This format is used to encode information on passports and other travel documents.

#### Step 2: Use a decoder to decode the document information

I found a website that defined each section of the MRZ format; I used this to find all the information I needed to answer the challenge questions:

#### Step 3: Provide answers to the challenge questions

Based on the MRZ format, I was able to provide answers to all of the challenge questions:

1. The first name of the person is TOM.
2. The last name of the person is FEDDER.
3. The person's date of birth is 1990-02-14.
4. The document's expiration date is 2050-02-14 00:00.
5. The person's nationality is USA.

## Conclusion:

The Document (Medium) challenge required decoding a document's information using the MRZ format. By completing this challenge, I learned about the MRZ format and how it is used to encode information on travel documents.

## Excerpts from Methodologies and techhniques used from NCL Discord
`I'm glad I'm not the only one who didn't understand the date encoding at first, the document in question is based off the Machine Readable Passport format
https://en.wikipedia.org/wiki/Machine-readable_passport`

`Dates were in the format YYMMDD, and yes the expiry date was much further into the future than you may expect`

`I just dropped the screenshot in image search`