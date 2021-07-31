<div class="cell markdown" markdown="1">

<h2><p align=center> Assignment - Module 4 </p></h2>
<h3><p align=center> 31 July 2021 </p></h3>
<h3><p align=center> Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu </p></h3>

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q1.There are 10 people. What are the number of ways in which you can split them into a team of 6 and a team of 4? Additionally, what are the number of ways in which you can split them into two teams of 5 each? {#q1there-are-10-people-what-are-the-number-of-ways-in-which-you-can-split-them-into-a-team-of-6-and-a-team-of-4-additionally-what-are-the-number-of-ways-in-which-you-can-split-them-into-two-teams-of-5-each}

</div>

<div class="cell markdown" markdown="1">

#### Answer 1: {#answer-1}

-   Number of ways to split the 10 people in teams of 6 and 4 are
    <sup>10</sup>*C*<sub>6</sub>  =  <sup>10</sup>*C*<sub>4</sub>
-   Number of ways to split the 10 people in teams of 5 and 5 are
    <sup>10</sup>*C*<sub>5</sub>/2. This is because the two groups are
    identical in number. Thus, division by 2.

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="height:1.5px;color:black;background-color:black">

</div>

<div class="cell markdown" markdown="1">

#### Q2. Prove P(A ∪ B) = P(A) + P(B) − P(A ∩ B). Hint: The goal is to prove this mathematically (not using Venn diagrams). Try writing A ∪ B as union of three disjoint sets and then apply axiom 3 that we discussed in class. {#q2-prove-pa--b--pa--pb--pa--b-hint-the-goal-is-to-prove-this-mathematically-not-using-venn-diagrams-try-writing-a--b-as-union-of-three-disjoint-sets-and-then-apply-axiom-3-that-we-discussed-in-class}

</div>

<div class="cell markdown" markdown="1">

#### Answer 2: {#answer-2}

-   Partitioning a Set: For every two sets *A* and *B*, *B* and
    *A* ∩ *B*<sup>*c*</sup> are disjoint, Thus,
    *A* ∪ *B* = *B* ∪ (*A*∩*B*<sup>*c*</sup>)

</div>

<div class="cell code" markdown="1">

~~~ python
~~~

</div>
