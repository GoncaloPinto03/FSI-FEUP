# Work from Week 10 - Secret-Key Encryption

## Task 1: Frequency Analysis
First, we analyzed the file that contained the frequencies, _freq.py_

![Fig 1](./imgs/LOGBOOK10/freq1.png)

![Fig 2](./imgs/LOGBOOK10/freq2.png)


Then we analyzed the most common trigrams in the English language, using the link provided in the sheet itself

Comparing the two pieces of information, we were able to map the first two trigrams

| Subtituition |
| ---------- |
| ytn => the |
| vup => and |

After that, we made the modifications below:

|Subtituition|
|----|
|x => o|
|mq => is|
|hr => rg|
|ibz => lfu|
|sdacg => kycmb|
|l => w|
|efok => pvjx|
|q => j|

In the end we had this text

![Fig 3](./imgs/LOGBOOK10/text1.png)

![Fig 4](./imgs/LOGBOOK10/text2.png)


## Task 2: Encryption using Different Ciphers and Modes

First, we create an file with this message:

![Fig 5](./imgs/LOGBOOK10/text.png)


The result of our messenger encryption was:

|Cipher|Encrypted|
|----|----|
|-aes-128-cbc|![Fig 7](./imgs/LOGBOOK10/c1.png)|
|-bf-cbc|![Fig 8](./imgs/LOGBOOK10/c2.png)|
|-aes-128-cfb|![Fig 9](./imgs/LOGBOOK10/c3.png)|

## Task 3: Encryption Mode – ECB vs. CBC

![Fig 10](./imgs/LOGBOOK10/header.png)

### ECB

1) ![Fig 11](./imgs/LOGBOOK10/ecb1.png)
2) ![Fig 12](./imgs/LOGBOOK10/ecb_body.png)
3) ![Fig 13](./imgs/LOGBOOK10/ecb_final.png)

|original|final|
|----|----|
|![Fig 14](./imgs/LOGBOOK10/original.png)|![Fig 7](./imgs/LOGBOOK10/ecb.png)|


### CBC

1) ![Fig 11](./imgs/LOGBOOK10/cbc1.png)
2) ![Fig 12](./imgs/LOGBOOK10/cbc_body.png)
3) ![Fig 13](./imgs/LOGBOOK10/cbc_final.png)

|original|final|
|----|----|
|![Fig 14](./imgs/LOGBOOK10/original.png)|![Fig 7](./imgs/LOGBOOK10/cbc.png)|
