---
jupyter:
  interpreter:
    hash: b3ba2566441a7c06988d0923437866b63cedc61552a5af99d1f4fb67d367b25f
  kernelspec:
    display_name: Python 3.8.8 64-bit (conda)
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.8.8
  nbformat: 4
  nbformat_minor: 2
  orig_nbformat: 4
---

<div class="cell markdown">

<h2><p align=center> Assignment - Module 4 </p></h2>
<h3><p align=center> 31 July 2021 </p></h3>
<h3><p align=center> Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu </p></h3>

<br>

</div>

<div class="cell markdown">

#### Q1.There are 10 people. What are the number of ways in which you can split them into a team of 6 and a team of 4? Additionally, what are the number of ways in which you can split them into two teams of 5 each?

</div>

<div class="cell markdown">

#### Answer 1:

-   Number of ways to split the 10 people in teams of 6 and 4 are
    <sup>10</sup>*C*<sub>6</sub>  =  <sup>10</sup>*C*<sub>4</sub>
-   Number of ways to split the 10 people in teams of 5 and 5 are
    <sup>10</sup>*C*<sub>5</sub>/2. This is because the two groups are
    identical in number. Thus, division by 2.

</div>

<div class="cell markdown">

<hr style="height:1.5px;color:black;background-color:black">

</div>

<div class="cell markdown">

#### Q2. Prove P(A ∪ B) = P(A) + P(B) − P(A ∩ B). Hint: The goal is to prove this mathematically (not using Venn diagrams). Try writing A ∪ B as union of three disjoint sets and then apply axiom 3 that we discussed in class.

</div>

<div class="cell markdown">

#### Answer 2:

-   Partitioning a Set: For every two sets *A* and *B*, *B* and
    *A* ∩ *B*<sup>*c*</sup> are disjoint, Thus,
    *A* ∪ *B* = *B* ∪ (*A*∩*B*<sup>*c*</sup>)

</div>

<div class="cell code">

``` python
```

</div>