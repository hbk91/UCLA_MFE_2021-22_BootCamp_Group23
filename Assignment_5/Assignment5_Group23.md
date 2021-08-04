---
Assignment - Module 5
04 August 2021
Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu
---

#### Q1.Quant Interview: A quant driven hedge fund wants to interview all the UCLA MFE students for an internship. Say 50% of all students who received their first interview received a second interview. 95% of the people interviewed that got a second interview said they had a good first interview. 75% of the people interviewed that did not get a second interview said they had a good first interview. If you felt you had a good first interview, what is the probability that you will receive a second interview? Alternatively, if you felt you had a bad first interview, what is the probability that you will receive a second interview?<br>

#### Answer 1:

<br>

**Let:**
- The probability of the first interview being felt good be denoted by $P(First_{FG})$
- The probability of the first interview being felt bad be denoted by $P(First_{FB})$
- The probability of receiving a second interview be denoted by $P(Y_{second})$
- The probability of receiving a second interview be denoted by $P(N_{second})$

**Therefore, $P(Y_{second}|First_{FG})$ using Bayes' Theorem is:**

$$P(Y_{second}|First_{FG}) = P(First_{FG}|Y_{second})*\frac{P(Y_{second})}{P(First_{FG})}$$

$$\implies P(Y_{second}|First_{FG}) = 0.95*\frac{0.5}{0.5*0.95+0.5*0.75}$$

$$\implies P(Y_{second}|First_{FG}) = 0.5588$$

<br>

**Similarly, $P(Y_{second}|First_{FB}) is$:**

$$P(Y_{second}|First_{FB}) = P(First_{FB}|Y_{second})*\frac{P(Y_{second})}{P(First_{FB})}$$

$$\implies P(Y_{second}|First_{FB}) = 0.05*\frac{0.5}{0.5*0.05+0.5*0.25}$$

$$\implies P(Y_{second}|First_{FB}) = 0.1667$$

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q2. Hypothesis Testing: There are two biased coins A and B in a bag. Probability of heads for coin A is 0.75 and the probability of heads for coin B is 0.3. You pick a coin randomly and perform 10 tosses (without knowing which coin you picked). Hint: To solve the two problems below, compute the posterior probability P(Hypothesis|Data) and argue that one of the coin has a higher posterior probability. You will have to test and compare the two hypothesis - picking coin A given data and picking coin B given data. Since we are choosing a coin randomly, P(picking coin A) = (picking coin B) = 1/2. Key takeaway is how the data changes your beliefs about which coin you picked.<br>

**i.** You observe that you get 8 heads and 2 tails from your coin tosses. What is the probability that you picked coin A from the bag given the data. Compare this with the posterior probability of picking the other coin.<br>
**ii.** Now, say you observed 8 tails and 2 heads from your coin tosses. What is the probability that you picked coin B given the data. Compare this with the posterior probability of picking the other coin.<br>

#### Answer 2:
<br>

**Let:** 
- The probability for coin A be denoted by $P(A)$
- The probability for coin B be denoted by $P(B)$
 

#### i. 8 heads & 2 tails:
<br>

**Let:** 
- The Probability of 8 heads and 2 tails be denoted by $P(8_H2_T)$ 

**Therefore, $P(A|8_H2_T)$ using Bayes' Theorem is:**

$$P(A|8_H2_T) = P(8_H2_T|A)*\frac{P(A)}{P(8_H2_T)}$$

$$\implies P(A|8_H2_T) =\, ^{10}C_8(0.75)^8(0.25)^2*\frac{0.5}{^{10}C_8(0.75)^8(0.25)^2+ ^{10}C_8(0.3)^8(0.7)^2}$$

$$\implies P(A|8_H2_T) = 0.4974$$

**Therefore, $P(B|8_H2_T)$ is:**

$$P(B|8_H2_T) = P(8_H2_T|B)*\frac{P(B)}{P(8_H2_T)}$$

$$\implies P(B|8_H2_T) =\, ^{10}C_8(0.3)^8(0.7)^2*\frac{0.5}{^{10}C_8(0.75)^8(0.25)^2+ ^{10}C_8(0.3)^8(0.7)^2}$$

$$\implies P(A|8_H2_T) = 0.0026$$
<br>

**Thus, given our observed data, there is much higher probability that coin A was initially picked.**

<br>

#### ii. 2 heads & 8 tails:
<br>

**Let:** 
- The Probability of 8 heads and 2 tails be denoted by $P(8_H2_T)$ 


**Therefore, $P(B|2_H8_T)$ using Bayes' Theorem is:**

$$P(B|2_H8_T) = P(2_H8_T|B)*\frac{P(B)}{P(2_H8_T)}$$

$$\implies P(B|2_H8_T) =\, ^{10}C_2(0.3)^2(0.7)^8*\frac{0.5}{^{10}C_2(0.75)^2(0.25)^8+ ^{10}C_2(0.3)^2(0.7)^8}$$

$$\implies P(B|2_H8_T) = 0.4492$$

**Similarly, $P(A|2_H8_T)$ is:**

$$P(A|2_H8_T) = P(2_H8_T|A)*\frac{P(A)}{P(2_H8_T)}$$

$$\implies P(A|2_H8_T) =\, ^{10}C_2(0.75)^2(0.25)^8*\frac{0.5}{^{10}C_2(0.75)^2(0.25)^8+ ^{10}C_2(0.3)^2(0.7)^8}$$

$$\implies P(A|2_H8_T) = 0.0008$$

<br>

**Thus, given our observed data, there is much higher probability that coin B was initially picked.**

<br>

---
## The End.
---