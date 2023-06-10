# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: AES (Hard) ! Unsolved

### Challenge Description:

We have obtained password dumps storing hacker passwords. They appear to be default passwords to IoT devices. We know these default passwords follow a pattern: a noun + a major US city + 2 digits and have found a list of nouns used. Can you figure the passwords out?

```
recommendation
role
meaning
intention
idea
reflection
homework
environment
customer
depth
oven
understanding
sympathy
football
session
dinner
mixture
buyer
phone
sample
chapter
elevator
midnight
description
difference
imagination
actor
solution
emphasis
chocolate
responsibility
pollution
opportunity
replacement
extent
entry
salad
camera
hat
insect
analyst
situation
meat
breath
potato
flight
clothes
moment
resolution
country
addition
chest
thought
restaurant
energy
error
requirement
membership
bird
singer
obligation
preference
interaction
championship
audience
failure
charity
organization
truth
shopping
distribution
photo
estate
office
newspaper
feedback
agency
```

### Challenge Questions:

1. d0323eaf9441cffeaaf08e2ff2e9f290
2. 3800e9a3b59adef33661198b873abf14
3. 12fa89e0328d8f6df047c337a3d73d5b


### Solution:



#### Step 1: Identify the format of the document information



#### Step 2: Use a decoder to decode the document information



#### Step 3: Provide answers to the challenge questions

#### Final Answer

1. dinnerwashington22
2. entryneworleans22
3. championshipfortworth99




## Conclusion:

## Excerpts from Methodologies and techhniques used from NCL Discord
`I found a JSON list of top US cities on GitHub and converted that to a plaintext word list, then I used the hashcat combinator tool to combine them with the plain words, removed all whitespace/uppercase, then used rules to add the digits`
`pulled cities from wiki, python script to merge the lists and add numbers for each entry.`