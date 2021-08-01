<h2><p style="text-align:center;"> Assignment - Module 4 </p></h2>
<h3><p style="text-align:center;"> 01 August 2021 </p></h3>
<h3><p style="text-align:center;"> Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu </p></h3>
<br>

#### Q1.There are 10 people. What are the number of ways in which you can split them into a team of 6 and a team of 4? Additionally, what are the number of ways in which you can split them into two teams of 5 each?

#### Answer 1:

- Number of ways to split the 10 people in teams of 6 and 4 are:
    
$$^{10}C_6\,=\,^{10}C_4$$

- Number of ways to split the 10 people in teams of 5 and 5 are:
  
$$\frac{^{10}C_5}{2}$$
  
This is because the two groups have identical count of people. Hence, the division by two.

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q2.  Prove $P(A \cup B) = P(A) + P(B) - P(A \cap B)$. Hint: The goal is to prove this mathematically (not using Venn diagrams). Try writing $A \cup B$ as union of three disjoint sets and then apply axiom 3 that we discussed in class.

#### Answer 2:

- Partitioning a Set: For any two sets $A$ and $B$, $B$ and $A \cap B^c$ are disjoint. Thus,
  
$$A \cup B = B \cup (A \cap B^c) \qquad (1)$$

- For every finite sequence of n disjoint events $A_1,.....,A_n$, the probability of the union of the events is equal to the summation of their individual properties. Thus,

$$Pr(A \cup B) = Pr(B) \cup Pr(A \cap B^c) \qquad (2)$$

- For any two events A and B, the events $A \cap B^c$ and $A \cap B$ are disjoint. Thus,

$$A = (A \cap B) \cup (A \cap B^c) \qquad (3)$$

$$\implies Pr(A) = Pr(A \cap B) + Pr(A \cap B^c) \qquad (4)$$

$$\implies Pr(A \cap B^c) = Pr(A) - Pr(A \cap B) \qquad (5)$$

- Hence, from $(1)$ and $(5)$, we get,

$$Pr(A \cup B) = Pr(A) + Pr(B) - Pr(A \cap B) \qquad (6)$$

Q.E.D.

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q3. Two people take turns trying to sink a basketball into a net. Person 1 succeeds with probability 1/3 and person 2 succeeds with probability 1/4. What is the probability that person 2 succeeds before person 1. Additionally, compute the probability that person 1 succeeds before person 2.

#### Answer 3:

- Let the probability of Person 1 succeeding, should the Person 1 go first, be denoted by `x`. <br>
- Let the probability of Person 2 succeeding, should the Person 2 go first, be denoted by `y`. <br>

Thus,

$$x = \frac{1}{3} + \frac{2}{3}(1-y) \qquad (1)$$
$$y = \frac{1}{4} + \frac{3}{4}(1-x) \qquad (2)$$

- Thus for each person the probability of winning is the sum of the following two components viz.
    - Component A: Probability of the person winning on the first turn. For instance, $\frac{1}{3}$ in case of Person 1.
    - Component B: It is the product of the following two probabilities:
      -  Probability of the person losing on the first turn. For instance, $\frac{2}{3}$ in case of Person 1.
      -  Probability of the person winning if he had started second which is equal to 1 - the probability of the other person winning if the other person took the turn first. For instance, $1-y$ in case of Person 1.

- Thus, on solving $(1)$ and $(2)$ above, we get $x = \frac{2}{3}$ and $y = \frac{1}{2}$ 

**Thus, Probability of Person 2 succeeding first is $\frac{1}{2}$.<br>
Probability of Person 1 succeeding first is $\frac{2}{3}$.**

<hr style="height:1.5px;color:black;background-color:black"><br>

#### Q4. Suppose we toss a fair coin until we get exactly two heads. Describe the sample space S. What is the probability that exactly k tosses are required? 

#### Answer 4: 



























