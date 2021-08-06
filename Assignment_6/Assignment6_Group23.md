---
Assignment - Module 6
06 August 2021
Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu
---

#### Q1.Show that sum of two independent binomial distributions is also binomial, i.e. X ∼ Bin(n, p), Y ∼ Bin(m, p) then X + Y ∼ Bin(n + m, p). Hint: You might want to use the Vandermonde’s identity.<br>

#### Answer 1:

#### For, any value $a$ for random variables $X$ and $Y$, such that, $0\le{a}\le{n+m}$, we have:
$$P(X+Y = a) = \sum_{i=0}^{a} {P(X = i, Y = a-i)} \qquad \text{where,} \,\, 0\le{a}\le{n+m}$$ <br>

#### As the Binomial experiments are independent, we have:

$$\therefore P(X+Y = a) = \sum_{i=0}^{a} {P(X = i) P(Y = a-i)}$$ <br>

$$\implies P(X+Y = a) = \sum_{i=0}^{a} {[^nC_ip^i(1-p)^{n-i}}]\,[^mC_{a-i}p^{a-i}(1-p)^{m-a+i}]$$ <br>

$$\implies P(X+Y = a) = \sum_{i=0}^{a} {^nC_{i}\,^mC_{a-i}\,p^a(1-p)^{n+m-a}}$$ <br>

#### As the Binomial experiments are independent, we have:

$$\implies P(X+Y = a) = p^a(1-p)^{n+m-a}\sum_{i=0}^{a} {^nC_{i}\,^mC_{a-i}\,}$$ <br>

#### Now, Vandermonde's identity states that: $\quad^{m+n}C_{r} = \sum_{k=0}^{r} {^mC_{k}\,^nC_{r-k}\,}$ <br>

$$\therefore P(X+Y = a) =\,^{m+n}C_{a}\, p^a(1-p)^{n+m-a}$$ <br>

$$\implies X+Y \sim Bin(n+m, p)  $$ <br>

#### Q.E.D.

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q2. Say X ∼ Pois(3) and Y ∼ Pois(2) are two independent poisson distributions. Compute the probability that X + Y = 5. Additionally, compute the probability that X = 4, Y = 1 given X + Y = 5. Hint: Sum of two poisson distributions is also a poisson distribution. For the second part, independence assumption is key! <br>

#### Answer 2:

#### i. Probability that $X + Y = 5$

#### For a poisson distribution, if $X_i \sim Pois(\lambda_i) \quad \text{for}\, i= 1,2,....,n \;$; then:

$$\sum_{i=1}^n X_i \sim Pois\left(\sum_{i=1}^{n}\right)\lambda_{i}$$ <br>

#### Thus, $$X+Y \sim Pois(5)$$ 

#### Therefore,

$$P(X+Y = 5) = \frac{\lambda^{k}e^{-\lambda}}{k!}, \quad \text{where} \; \lambda=5,\: k = 5; $$ <br>

$$P(X+Y = 5) = 0.1755 $$ <br>

#### ii. Probability that $X = 4, Y = 1, \; given \; X + Y = 5$

#### $X + Y = 5,$ can result from the following $(X,Y)$ combinations $(0,5), (1,4), (2,3), (3,2), (4,1), and\; (5,0).$

- Thus Probability that $X = 4, Y = 1, \; given \; X + Y = 5$ would be the probability of the pair $(4, 1)$ divided by the sum of the probabilities of all the $(X,Y)$ pairs that result in $X + Y = 5$ <br>

- The sum of all the $(X,Y)$ pairs that result in $X + Y = 5$ is same the probability calculated in part (i) above.

#### Therefore, Probability that $X = 4, Y = 1, \; given \; X + Y = 5$ is:

$$P(X=4, Y=1 | X+Y = 5) = \frac{P(X=4)*P(Y=1)}{P (X+Y=5)}$$ <br>

- Note: X & Y are independent

$$P(X=4, Y=1 | X+Y = 5) = 0.2592$$ <br>

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q3. The arrival of buses at the bus stop can be modeled as a poisson process. Say buses arrive at a rate of 5 per hour (λ = 5). You just arrived at the bus stop. What is the probability that the next bus will arrive at the stop in the next 10 minutes. Additionally, find the probability that there will be a bus arriving in the next 5 minutes if there was no bus in the last 10 minutes.<br>

#### Answer 3:

#### i. Probability of the next bus arriving in next 10 minutes

- The probability of the next bus arriving in next 10 minutes is equal to $1 - \text{the probability of no bus arriving in next 10 minutes}$ 

- The average number of buses per 10 minutes is $5/6$

#### Therefore, 

$$P(Bus_{\ge0,\,10\,mins}) = 1 - P(Bus_{0,\,10\,mins})$$ <br>

$$\implies P(Bus_{\ge0,\,10\,mins}) = 1 - \frac{\lambda^{k}e^{-\lambda}}{k!}, \quad \text{where} \; \lambda=5/6,\: k = 0;$$ <br>

$$\implies P(Bus_{\ge0,\,10\,mins}) = 0.5654$$ <br>

#### ii. Probability of a bus arriving in the next 5 minutes if there was no bus in the last 10 minutes.

- The distribution of the waiting times in the Poisson process is memoryless i.e., 

$$P(T>t+s|T>s)=P(T>t)$$ <br>

- Therefore, in our case what has happened in the previous 10 minutes is immaterial. The answer would be similar to the answer in part (i) above, with the only difference that the probability is required for next 5 minutes instead of next 10 minutes.

#### Therefore, 

$$P(Bus_{\ge0,\,5\,mins}) = 1 - P(Bus_{0,\,5\,mins})$$ <br>

$$\implies P(Bus_{\ge0,\,5\,mins}) = 1 - \frac{\lambda^{k}e^{-\lambda}}{k!}, \quad \text{where} \; \lambda=5/12,\: k = 0;$$ <br>

$$\implies P(Bus_{\ge0,\,5\,mins}) = 0.3408$$ <br>

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q4. Suppose you are given the PMF function of a random variable X such that P (X = −2) = P (X = 2) = 1/8, P (X = −1) = P (X = 1) = 1/8, P (X = 0) = 1/2. Lets define $Y = X^2$. Compute the PMF and the CDF of the random variable Y.<br>

#### Answer 4:

$$
\mathrm{P}_X(k) = \begin{cases}
    1/8 & \text{if\quad} k = -2,2 \\ % & is your "\tab"-like command (it's a tab alignment character)
    1/8 & \text{if \quad} k = -1,1 \\
    1/2 & \text{if \quad} k = 0 \\
    0 & \text{otherwise}
\end{cases}
$$ <br>

- Thus, $X \in \{-2, -1, 0, 1, 2\}$  and the sum the PMF of X is 1
- Thus, for $Y = X^2$, $Y \in \{0, 1, 4\}$

$$\therefore \{Y=4\} = \{X=2\} \cup \{X=-2\}$$ <br>

- In the above equation the two events on the RHS are disjoint
  
  $$\therefore P(Y=4) = P(X=2) + P(X=-2) = 1/4$$

#### Thus, solving similarly for $Y = 0, 1$; we get the PMF of Y as:

$${P}_Y(k) = \begin{cases}
    1/2 & \text{if \quad} k = 0 \\
    1/4 & \text{if \quad} k = 1 \\
    1/4 & \text{if \quad} k = 4 \\
    0 & \text{otherwise}
\end{cases}$$ <br>

#### CDF of Y is:

$${P}_{Y\le k}(k) = \begin{cases}
    1/2 & \text{if \quad}  0\le k \lt 1 \\ 
    3/4 & \text{if \quad}  1\le k \lt 4 \\
    1 & \text{if \quad}  k \ge 4 \\
    0 & \text{otherwise}
\end{cases}$$ <br>

<br>

---
## The End.
---


