# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: AES (Hard) ! Unsolved

### Challenge Description:

We have found a seemingly corrupted file. Can you recover the original image?

### Challenge Questions:

1. What is the original file type of the file inside the tarball?
2. What is the flag?

### Solution:



#### Step 1: Identify the format of the document information



#### Step 2: Use a decoder to decode the document information



#### Step 3: Provide answers to the challenge questions

#### Final Answer




## Conclusion:

## Excerpts from Methodologies and techhniques used from NCL Discord
`The file in this challenge was a .tar file based on the extension, but if you open it in a hex editor you'll notice a lot of weird bytes (For example a lot of 0x0B's, where I expected 0x00's)

I may have done this a difficult way but I went through and compared against another tar archive I made, and figured out what each byte translated to. The trick was every lower bit was changed, like how every lower 0 became a B above. I used a python script to take every bit and translate it to the correct hex value

After doing that the tar file becomes valid, revealing a png file inside. This png file also didn't open, that was missing it's header bytes. Transplanting the magic bytes into the beginning of the png file revealed the flag`

`for me i was able to just compare the headers between a real tar and this
saw the obvious xor
from there it was trivial`

`Basically this. It was a png with magic bytes cut off, then put in a tarball. The tarball was then XOR'd with 0x0b`

`literally the hint was headless. 1cebp for cyberseed told me to get a hex editor on my mac. decided to show the file. and then see multiple same file. tried copying from a random tar.. didnt work.. played with xor (took me an hr to set up with python) And voila playable tar file... png came out which is not working.. hex editor'd it again voila PNG hex not there put it there from CHRIS.PNG... THANKS FOR Crypto challenge`

