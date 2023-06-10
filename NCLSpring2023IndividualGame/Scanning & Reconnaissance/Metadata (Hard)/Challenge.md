# CTF Writeup: NCL Spring 2023 Individual Game

## Challenge Name: AES (Hard) ! Unsolved

### Challenge Description:

We have found what appears to be a server on metadata.services.cityinthe.cloud:1338 displaying metadata about something. Can you find out more information?

Note: your scope is limited to the provided port number on this host.


### Challenge Questions:

1. What availability zone is this instance hosted in?
2. What is the security credentials role named?
3. What is the instance type being used?
4. What major OS version is being used?
5. What is the flag?


### Solution:



#### Step 1: Identify the format of the document information



#### Step 2: Use a decoder to decode the document information



#### Step 3: Provide answers to the challenge questions

#### Final Answer

1. us-west-2a
2. liber8-role
3. c6g.16xlarge
4. Ubuntu Server 16.04 LTS
5. SKY-AWSM-1570

## Conclusion:

## Excerpts from Methodologies and techhniques used from NCL Discord
```import requests

def recursive_scrape(url, level, to_print):
  print("\t"*level + to_print)
  resp = requests.get(url)
  if resp.status_code != 200:
    return
  lines = resp.text.splitlines()
  for l in lines:
    recursive_scrape(url+"/"+l,level+1,l)

recursive_scrape("http://metadata.services.cityinthe.cloud:1338", 0, "/")
```
`I dropped the AMI number into https://cloud-images.ubuntu.com/locator/ec2/`