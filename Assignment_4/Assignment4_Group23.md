<h2><p style="text-align:center;"> Assignment - Module 4 </p></h2>
<h3><p style="text-align:center;"> 01 August 2021 </p></h3>
<h3><p style="text-align:center;"> Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu </p></h3>
<br>

#### Q1.There are 10 people. What are the number of ways in which you can split them into a team of 6 and a team of 4? Additionally, what are the number of ways in which you can split them into two teams of 5 each?<br>

#### Answer 1:

- Number of ways to split the 10 people in teams of 6 and 4 are:
    
$$^{10}C_6\,=\,^{10}C_4 = 210$$

- Number of ways to split the 10 people in teams of 5 and 5 are:
  
$$\frac{^{10}C_5}{2} = 126$$
  
This is because the two groups have identical count of people. Hence, the division by two.

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q2.  Prove $P(A \cup B) = P(A) + P(B) - P(A \cap B)$. Hint: The goal is to prove this mathematically (not using Venn diagrams). Try writing $A \cup B$ as union of three disjoint sets and then apply axiom 3 that we discussed in class.<br>

#### Answer 2:

- The third axiom of probability states that, For every finite sequence of n disjoint events $A_1,.....,A_n$, the probability of the union of the events is equal to the summation of their individual properties

- The union of two events, $A\cup B$, can be partitioned into three disjoint sets:

    - Elements of $A$ that are not in $B$
    - Elements of $B$ that are not in $A$
    - Elements that are both in $A$ and $B$

- Thus, $$P(A\cup B) = P(AB^c) + P(A^cB) + P(AB) \qquad (1)$$
  
- Also because $AB^c$ and $AB$ are disjoint, thus,  $$P(A) = P(AB^c) + P(AB) \qquad (2)$$

- Similarly, $$P(B) = P(BA^c) + P(AB) \qquad (3)$$

 - Adding $(2)$ & $(3)$, we get

$$P(A) + P(B) = P(AB^c) + P(A^cB) +2*P(AB) \qquad(4)$$

- Comparing $(1)$ and $(4)$, we get $$P(A \cup B) = P(A) + P(B) - P(A \cap B) \qquad (5)$$

Q.E.D.

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q3. Two people take turns trying to sink a basketball into a net. Person 1 succeeds with probability 1/3 and person 2 succeeds with probability 1/4. What is the probability that person 2 succeeds before person 1. Additionally, compute the probability that person 1 succeeds before person 2.<br>

#### Answer 3:

- Let the probability of Person 1 succeeding should Person 1 take the first turn, be denoted by `x`. <br>
- Let the probability of Person 2 succeeding should Person 2 take the first turn, be denoted by `y`. <br>

Thus,

$$x = \frac{1}{3} + \frac{2}{3}(1-y) \qquad (1)$$
$$y = \frac{1}{4} + \frac{3}{4}(1-x) \qquad (2)$$

- Thus for each person the probability of winning is the sum of the following two components viz.
    - Component A: Probability of the person winning on the first turn. For instance, $\frac{1}{3}$ in case of Person 1.
    - Component B: It is the product of the following two probabilities:
      -  Probability of the person losing on the first turn. For instance, $\frac{2}{3}$ in case of Person 1.
      -  Probability of the person winning if the person had started second which is equal to 1 - the probability of the other person winning if the other person took the turn first. For instance, $1-y$ in case of Person 1.

- Thus, on solving $(1)$ and $(2)$ above, we get $x = \frac{2}{3}$ and $y = \frac{1}{2}$ 

**Thus, Probability of Person 2 succeeding first is $\frac{1}{2}$.<br>
Probability of Person 1 succeeding first is $\frac{2}{3}$.**

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q4. Suppose we toss a fair coin until we get exactly two heads. Describe the sample space S. What is the probability that exactly k tosses are required?<br>

#### Answer 4: 

$$S = \{X_1, X_2, X_3, ...., X_n\}$$
Where,
  - $n \ge 2$
  - $X_n = \text{head}$
  - $X_h = \text{head for exactly one h from the set}\{1,2,3,....n-1\}$
  - $X_t = \text{tail for all, except one from the set}\{1,2,3,....n-1\}$<br>

Probability that exactly k tosses are required is the product of the following:

- Probability of head on the final $k^{th}$ toss
- Probability of one head and rest all tails in $k-1$ tosses and the all possible combinations of such occurrences.

$$P =\,^{k-1}C_{k-2}*{\left(\frac{1}{2}\right)}^{k-2}*\frac{1}{2}*\frac{1}{2}$$
$$\implies P = \frac{k-1}{2^k}$$

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q5. Birth Month Problem - This is a variation of the birthday problem. How many people are needed in a room to make it possible that atleast two people have the same birth month with a probability of 50%. There are 12 months in a year and probability of being born in any month is the same. Hint: Try expressing the probability of atleast 2 people having the same birth month as a complementary event.<br>

#### Answer 5:

- Event $A$: At least two people have the same birthday month
- Event $\bar{A}$: No two people have the same birthday month

- Thus, $$P(\bar{A}) = \frac{12}{12}*\frac{11}{12}*\text{.....}*\frac{12-n+1}{12} \qquad (1)$$

- This is because the first person can have the birthday in any of the 12 months. The next person in rest of the 11 months and so on and so forth.

- Thus, $$P(A) = 1- \frac{12}{12}*\frac{11}{12}*\text{.....}*\frac{12-n+1}{12} \qquad (2)$$

- Our answer would be the lowest value of n (number of people in the room) for which the probability in $(2)$ becomes greater than 0.5 <br>

- n turns out to be 5. Thus, there should be atleast 5 people in the room to make it possible that atleast two people have the same birth month with a probability of 50%.

<hr style="height:1.5px;color:black;background-color:black"><br>
<h2><p style="text-align:center;">The End.</p></h2>
<hr style="height:1.5px;color:black;background-color:black"><br>



























