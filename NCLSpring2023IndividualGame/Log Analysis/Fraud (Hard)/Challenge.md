# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: AES (Hard) ! Unsolved

### Challenge Description:

We think that one of the customers at metro bank has made a fraudulent purchase recently, can you figure out who?

### Challenge Questions:

1. What account was used to make a fraudulent purchase?
2. At what time was it made? (Round to the nearest minute)


### Solution:



#### Step 1: Identify the format of the document information



#### Step 2: Use a decoder to decode the document information



#### Step 3: Provide answers to the challenge questions

#### Final Answer

1. Dawson_Kautzer18
2. 2023-04-02 01:13


## Conclusion:

## Excerpts from Methodologies and techhniques used from NCL Discord
`I put the logs from this one into a spreadsheet and made a pivot table. Made it pretty easy to spot that way, I thought.`
`This required a more behavioral approach. Imported in csv and sorted by name. each person had 3-4 routine purchases. 1 person had a purchase unlike that persons typical purchases.`
`awk '{print $2, $3}' logfile.txt | sort | uniq -c`
`cat fraud.log | awk '{print $3" "$2}' | sort | uniq -c | sort -n | head`