<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

##  {#section}

Assignment - Module 3

###  {#section-1}

30 July 2021

###  {#section-2}

Group 23: Aman Jindal \| Yuhang Jiang \| Daniel Gabriel Tan \| Qining
Liu

  
  

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs"
markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[1\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Importing Libraries

    import pandas as pd
    import numpy as np
    from pprint import pprint
    from functools import reduce
    import dateparser
    import matplotlib.pyplot as plt
    plt.style.use('seaborn')

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q1. List Comprehension: First generate a list using the range(20) function. Next, create a second list that calculates $0.5 \\cdot n \\cdot (n+1)$ for each item $n$ in the first list. Solve this using a while loop and also the list comprehension method. Check if the outputs match for the two methods.[¶](#Q1.-List-Comprehension:-First-generate-a-list-using-the-range(20)-function.-Next,-create-a-second-list-that-calculates-$0.5-\cdot-n-\cdot-(n+1)$-for-each-item-$n$-in-the-first-list.-Solve-this-using-a-while-loop-and-also-the-list-comprehension-method.-Check-if-the-outputs-match-for-the-two-methods.){.anchor-link} {#Q1.-List-Comprehension:-First-generate-a-list-using-the-range(20)-function.-Next,-create-a-second-list-that-calculates-$0.5-\\cdot-n-\\cdot-(n+1)$-for-each-item-$n$-in-the-first-list.-Solve-this-using-a-while-loop-and-also-the-list-comprehension-method.-Check-if-the-outputs-match-for-the-two-methods.}

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Answer 1[¶](#Answer-1){.anchor-link} {#Answer-1}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[2\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # While Loop Method

    input_list = range(20)
    ans_q1_whileLoop = []
    i = 0
    while i<len(input_list):
        ans_q1_whileLoop.append(0.5*input_list[i]*(input_list[i]+1))
        i = i+1

    print('The Answer:\n\n {}'.format(ans_q1_whileLoop))
    print('\nThe Length of the list is: {}'.format(len(ans_q1_whileLoop)))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    The Answer:

     [0.0, 1.0, 3.0, 6.0, 10.0, 15.0, 21.0, 28.0, 36.0, 45.0, 55.0, 66.0, 78.0, 91.0, 105.0, 120.0, 136.0, 153.0, 171.0, 190.0]

    The Length of the list is: 20

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[3\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # List Comprehension Method

    input_list = range(20)
    ans_q1_lc = [0.5*n*(n+1) for n in input_list]

    print('The Answer:\n\n {}'.format(ans_q1_lc))
    print('\nThe Length of the list is: {}'.format(len(ans_q1_lc)))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    The Answer:

     [0.0, 1.0, 3.0, 6.0, 10.0, 15.0, 21.0, 28.0, 36.0, 45.0, 55.0, 66.0, 78.0, 91.0, 105.0, 120.0, 136.0, 153.0, 171.0, 190.0]

    The Length of the list is: 20

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[4\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Check if the two lists are equal

    print('Check if the lists are equal: {}'.format(ans_q1_whileLoop == ans_q1_lc))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    Check if the lists are equal:True

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q2. Lambda function: Create a numpy array of integers from 1 to 50. Use the lambda function to compute $x^3+x^2+x+1$ for each element $x$ of the array. Compare your output using the list comprehension method.[¶](#Q2.-Lambda-function:-Create-a-numpy-array-of-integers-from-1-to-50.-Use-the-lambda-function-to-compute-$x%5E3+x%5E2+x+1$-for-each-element-$x$-of-the-array.-Compare-your-output-using-the-list-comprehension-method.){.anchor-link} {#Q2.-Lambda-function:-Create-a-numpy-array-of-integers-from-1-to-50.-Use-the-lambda-function-to-compute-$x^3+x^2+x+1$-for-each-element-$x$-of-the-array.-Compare-your-output-using-the-list-comprehension-method.}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs"
markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[5\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # A General Purpose Function for calculating sum of a geometric power series where a = 1 & r = pow 

    def sum_geom_pow(elem, pow): return sum([elem**p for p in range(pow+1)])

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[6\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Lambda Function Method

    input_arr = np.arange(50)+1
    max_pow = 3

    cubic_func = lambda x: sum_geom_pow(x, max_pow)
    ans_q2_lambda = cubic_func(input_arr)
    print('The Answer is:\n')
    pprint(ans_q2_lambda)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    The Answer is:

    array([     4,     15,     40,     85,    156,    259,    400,    585,
              820,   1111,   1464,   1885,   2380,   2955,   3616,   4369,
             5220,   6175,   7240,   8421,   9724,  11155,  12720,  14425,
            16276,  18279,  20440,  22765,  25260,  27931,  30784,  33825,
            37060,  40495,  44136,  47989,  52060,  56355,  60880,  65641,
            70644,  75895,  81400,  87165,  93196,  99499, 106080, 112945,
           120100, 127551], dtype=int32)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[7\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # List Comprehension Method

    input_arr = np.arange(50)+1
    max_pow = 3

    ans_q2_lc = np.array([sum_geom_pow(x, max_pow) for x in input_arr])
    print('The Answer is:\n')
    pprint(ans_q2_lc)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    The Answer is:

    array([     4,     15,     40,     85,    156,    259,    400,    585,
              820,   1111,   1464,   1885,   2380,   2955,   3616,   4369,
             5220,   6175,   7240,   8421,   9724,  11155,  12720,  14425,
            16276,  18279,  20440,  22765,  25260,  27931,  30784,  33825,
            37060,  40495,  44136,  47989,  52060,  56355,  60880,  65641,
            70644,  75895,  81400,  87165,  93196,  99499, 106080, 112945,
           120100, 127551])

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[8\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Check if the two outputs are same

    print('Check if the arrays are equal: {}'.format((ans_q2_lambda == ans_q2_lc).all()))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    Check if the arrays are equal: True

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q3. For Loop: Create a list with range(50). Return $x^3+x^2+x+1$ for every element $x$ in the list with an exception that for the last 5 elements return $x^4+x^3+x^2+x+1$. Use a for loop to do this operation. Hint: You might want to read up on "enumerate" and how that can be used with a for loop.[¶](#Q3.-For-Loop:-Create-a-list-with-range(50).-Return-$x%5E3+x%5E2+x+1$-for-every-element-$x$-in-the-list-with-an-exception-that-for-the-last-5-elements-return-$x%5E4+x%5E3+x%5E2+x+1$.-Use-a-for-loop-to-do-this-operation.-Hint:-You-might-want-to-read-up-on-%22enumerate%22-and-how-that-can-be-used-with-a-for-loop.){.anchor-link} {#Q3.-For-Loop:-Create-a-list-with-range(50).-Return-$x^3+x^2+x+1$-for-every-element-$x$-in-the-list-with-an-exception-that-for-the-last-5-elements-return-$x^4+x^3+x^2+x+1$.-Use-a-for-loop-to-do-this-operation.-Hint:-You-might-want-to-read-up-on-\"enumerate\"-and-how-that-can-be-used-with-a-for-loop.}

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Answer 3[¶](#Answer-3){.anchor-link} {#Answer-3}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[9\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # For Loop Method

    input_list = range(50)
    last_elem_count = 5
    max_pow_start45 = 3
    max_pow_last5 = 4
    ans_q3_forLoop = []

    for i, x in enumerate(input_list):
        if i >= len(input_list)-last_elem_count:
            ans_q3_forLoop.append(sum_geom_pow(x, max_pow_last5))
        else:
            ans_q3_forLoop.append(sum_geom_pow(x, max_pow_start45))

    print('The Answer: \n\n{}'.format(ans_q3_forLoop))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    The Answer: 

    [1, 4, 15, 40, 85, 156, 259, 400, 585, 820, 1111, 1464, 1885, 2380, 2955, 3616, 4369, 5220, 6175, 7240, 8421, 9724, 11155, 12720, 14425, 16276, 18279, 20440, 22765, 25260, 27931, 30784, 33825, 37060, 40495, 44136, 47989, 52060, 56355, 60880, 65641, 70644, 75895, 81400, 87165, 4193821, 4576955, 4985761, 5421361, 5884901]

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[10\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # List Comprehension Method

    input_list = range(50)
    last_elem_count = 5
    max_pow_start45 = 3
    max_pow_last5 = 4

    ans_q3_lc = [sum_geom_pow(x, max_pow_last5) 
                 if i >= len(input_list)-last_elem_count
                 else sum_geom_pow(x, max_pow_start45)  
                 for i, x in enumerate(input_list)]

    print('The Answer: \n\n{}'.format(ans_q3_lc))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    The Answer: 

    [1, 4, 15, 40, 85, 156, 259, 400, 585, 820, 1111, 1464, 1885, 2380, 2955, 3616, 4369, 5220, 6175, 7240, 8421, 9724, 11155, 12720, 14425, 16276, 18279, 20440, 22765, 25260, 27931, 30784, 33825, 37060, 40495, 44136, 47989, 52060, 56355, 60880, 65641, 70644, 75895, 81400, 87165, 4193821, 4576955, 4985761, 5421361, 5884901]

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[11\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    print(ans_q3_forLoop == ans_q3_lc)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    True

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q4. List comprehension with logical statements: First generate a list using the range(30) function. Next, create a second list that creates elements based on the logic below. Hint: You can do this by including an if statement inside your list comprehension.[¶](#Q4.-List-comprehension-with-logical-statements:-First-generate-a-list-using-the-range(30)-function.-Next,-create-a-second-list-that-creates-elements-based-on-the-logic-below.-Hint:-You-can-do-this-by-including-an-if-statement-inside-your-list-comprehension.){.anchor-link} {#Q4.-List-comprehension-with-logical-statements:-First-generate-a-list-using-the-range(30)-function.-Next,-create-a-second-list-that-creates-elements-based-on-the-logic-below.-Hint:-You-can-do-this-by-including-an-if-statement-inside-your-list-comprehension.}

$$ f(x)=\\begin{cases} x^2;\\quad \\text{if x is even}\\\\ x^3;\\quad
\\text{if x is odd} \\end{cases} $$

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

### Answer 4:[¶](#Answer-4:){.anchor-link} {#Answer-4:}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[12\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    input_list = range(30)

    ans_q4 = [x**2 if x % 2 == 0 else x**3 for x in input_list]

    print('The Answer: \n\n{}'.format(ans_q4))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    The Answer: 

    [0, 1, 4, 27, 16, 125, 36, 343, 64, 729, 100, 1331, 144, 2197, 196, 3375, 256, 4913, 324, 6859, 400, 9261, 484, 12167, 576, 15625, 676, 19683, 784, 24389]

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q5. Fibonacci sequence: Construct a function "fibonacci" that takes in the required variable integer "$n$" and returns the $n\_{th}$ term in a Fibonacci sequence (1,1,2,3,5,...). For example, if your call your function and pass in the argument n = 6, i.e fibonacci(n=6) it should return the value 8. You can use a for or a while loop inside your function. Print the function output for n=30, 50, and 100.[¶](#Q5.-Fibonacci-sequence:-Construct-a-function-%22fibonacci%22-that-takes-in-the-required-variable-integer-%22$n$%22-and-returns-the-$n_%7Bth%7D$-term-in-a-Fibonacci-sequence-(1,1,2,3,5,...).-For-example,-if-your-call-your-function-and-pass-in-the-argument-n-=-6,-i.e-fibonacci(n=6)-it-should-return-the-value-8.-You-can-use-a-for-or-a-while-loop-inside-your-function.-Print-the-function-output-for-n=30,-50,-and-100.){.anchor-link} {#Q5.-Fibonacci-sequence:-Construct-a-function-\"fibonacci\"-that-takes-in-the-required-variable-integer-\"$n$\"-and-returns-the-$n_{th}$-term-in-a-Fibonacci-sequence-(1,1,2,3,5,...).-For-example,-if-your-call-your-function-and-pass-in-the-argument-n-=-6,-i.e-fibonacci(n=6)-it-should-return-the-value-8.-You-can-use-a-for-or-a-while-loop-inside-your-function.-Print-the-function-output-for-n=30,-50,-and-100.}

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Answer 5[¶](#Answer-5){.anchor-link} {#Answer-5}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[13\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Method 1 of generating the nth element of the Fibonacci series

    pos_list = [6, 30, 50, 100]

    def get_fib_nth_elem_m1(elem_pos=0):
        if isinstance(elem_pos, int) and elem_pos >= 0:
            return reduce(lambda x, _:(x[1],x[0]+x[1]), range(elem_pos), (0,1))[0]
        else:
            raise TypeError('Element Position entered is not an integer greater than or equal to 0')

    for pos in pos_list:
       print('Fibonacci Series Value at position {}: {:,}\n'.format(pos, get_fib_nth_elem_m1(pos)))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    Fibonacci Series Value at position 6: 8

    Fibonacci Series Value at position 30: 832,040

    Fibonacci Series Value at position 50: 12,586,269,025

    Fibonacci Series Value at position 100: 354,224,848,179,261,915,075

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[14\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Method 2 of generating the nth element of the Fibonacci series

    pos_list = [6, 30, 50, 100]

    def get_fib_nth_elem_m2(elem_pos=0):
        
        if isinstance(elem_pos, int) and elem_pos >= 0:
            a, b = 0, 1
            for i in range(elem_pos):
                a, b = b, a+b
            return a
        else:
            raise TypeError('Element Position entered is not an integer greater than or equal to 0')

    for pos in pos_list:
     print('Fibonacci Series Value at position {}: {:,}\n'.format(pos, get_fib_nth_elem_m2(pos)))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    Fibonacci Series Value at position 6: 8

    Fibonacci Series Value at position 30: 832,040

    Fibonacci Series Value at position 50: 12,586,269,025

    Fibonacci Series Value at position 100: 354,224,848,179,261,915,075

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[15\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Method 3 of generating the nth element of the Fibonacci series

    from functools import lru_cache
    pos_list = [6, 30, 50, 100]

    @lru_cache(maxsize=1000)
    def get_fib_nth_elem_m3(n):
        """Function takes input integer 'n' and returns the n-th sequence of the fibonacci series (no loops & no memoization)"""
        if n <= 2 : return 1
        else : return get_fib_nth_elem_m3(n-1) + get_fib_nth_elem_m3(n-2)

    for pos in pos_list:
       print('Fibonacci Series Value at position {}: {:,}\n'.format(pos, get_fib_nth_elem_m3(pos)))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    Fibonacci Series Value at position 6: 8

    Fibonacci Series Value at position 30: 832,040

    Fibonacci Series Value at position 50: 12,586,269,025

    Fibonacci Series Value at position 100: 354,224,848,179,261,915,075

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q6. Net Present Value: Code up a function that computes the net present value of a stream of cash-flows and call this function NPV. The function will take three inputs - cash-flows, dates, and interest rate (constant). We will use the formula specified below to compute the NPV of a stream of cash-flows on specific dates. The time periods $t_1,t_2,..,t_N$ are computed as differences from first date. Make sure you annualize the difference in days (convert them to years). Check out this wikipedia link if you want to read up some more (<https://en.wikipedia.org/wiki/Net_present_value>).[¶](#Q6.-Net-Present-Value:-Code-up-a-function-that-computes-the-net-present-value-of-a-stream-of-cash-flows-and-call-this-function-NPV.-The-function-will-take-three-inputs---cash-flows,-dates,-and-interest-rate-(constant).-We-will-use-the-formula-specified-below-to-compute-the-NPV-of-a-stream-of-cash-flows-on-specific-dates.-The-time-periods-$t_1,t_2,..,t_N$-are-computed-as-differences-from-first-date.-Make-sure-you-annualize-the-difference-in-days-(convert-them-to-years).-Check-out-this-wikipedia-link-if-you-want-to-read-up-some-more-(https://en.wikipedia.org/wiki/Net_present_value).){.anchor-link} {#Q6.-Net-Present-Value:-Code-up-a-function-that-computes-the-net-present-value-of-a-stream-of-cash-flows-and-call-this-function-NPV.-The-function-will-take-three-inputs---cash-flows,-dates,-and-interest-rate-(constant).-We-will-use-the-formula-specified-below-to-compute-the-NPV-of-a-stream-of-cash-flows-on-specific-dates.-The-time-periods-$t_1,t_2,..,t_N$-are-computed-as-differences-from-first-date.-Make-sure-you-annualize-the-difference-in-days-(convert-them-to-years).-Check-out-this-wikipedia-link-if-you-want-to-read-up-some-more-(https://en.wikipedia.org/wiki/Net_present_value).}

$$NPV(CF) = CF_0 + \\frac{CF_1}{(1+r)^{t_1}} + \\frac{CF_2}{(1+r)^{t_2}}
+ ... \\frac{CF_N}{(1+r)^{t_N}}$$

**Run this function for the following input:**

$$\\text{Compute : } \\text{NPV}(\\text{CF} =
\\text{\[-100,50,40,30\]},\\text{date} =
\[\\text{01-Jan-2020,31-Mar-2021,30-Jun-2021,31-Dec-2024}\],r=0.05)$$

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Answer 6:  {#answer-6}

#### Notes on Parsing Dates:[¶](#Notes-on-Parsing-Dates:){.anchor-link} {#Notes-on-Parsing-Dates:}

-   Date Formats are available
    [here](https://docs.python.org/2/library/datetime.html#strftime-and-strptime-behavior)
    for parsing string as dates
-   [dateparser library](https://dateparser.readthedocs.io/en/latest/).
    It can even parse dates even without providing a date format
-   More date formats can be supplied as additional list elements in
    `date_formats` argument of `dateparser.parse`

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs"
markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[16\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    def NPV(cash_flows, cf_dates, interest_rate):
        '''
        Computes the NPV of a series of cash flows. First date in the `dates`list assumed to be the date of calculation of NPV

        Args:
        cash_flows (list of int/float): The list of cash flows
        cf_dates (list of str): List of cash flow dates in the str format 'DD-MMM-YYYY' (e.g.: 01-Jan-2021)
        interest_rate (int/float): Yearly Interest Rate for discounting (absolute value)

        Returns:
        npv (float): Net Present Value of the cash flows
        ''' 

        
        date_formats = ['%d-%b-%Y']             # More date formats can be supplied as additional list element
        days_a_year = 365                       # Actual/365 day-count convetion is chosen

        cf_dates_parsed = [dateparser.parse(date_string=date_string, date_formats=date_formats).date()
                           for date_string in cf_dates]  
        
        cf_time_deltas =  [(cf_date - cf_dates_parsed[0]).days/days_a_year for cf_date in cf_dates_parsed]

        pv_cash_flows = [cash_flow/(1+interest_rate)**time_to_maturity 
                         for cash_flow, time_to_maturity in zip(cash_flows, cf_time_deltas)]

        npv = sum(pv_cash_flows)
        return npv

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[17\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    cash_flows = [-100, 50, 40, 30]
    cash_flow_dates = ['01-Jan-2020', '31-Mar-2021', '30-Jun-2021', '31-Dec-2024']
    interest_rate = 0.05

    print('NPV of the cash flows: {:,.2f}'.format(NPV(cash_flows, cash_flow_dates, interest_rate)))

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

    NPV of the cash flows: 7.74

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q7. Pandas .rolling() is a very useful function to know (check out the doc string of pandas.Series.rolling for a better understanding of what the function does). In this problem, we will calculate the 1-year rolling sum of returns for the data in stock_data.csv file. Clean the data (remove strings and drop NaN values). Use the pandas rolling function (window=12) to calculate the sum of 1-year returns. Add this column to the original dataframe.[¶](#Q7.-Pandas-.rolling()-is-a-very-useful-function-to-know-(check-out-the-doc-string-of-pandas.Series.rolling-for-a-better-understanding-of-what-the-function-does).-In-this-problem,-we-will-calculate-the-1-year-rolling-sum-of-returns-for-the-data-in-stock_data.csv-file.-Clean-the-data-(remove-strings-and-drop-NaN-values).-Use-the-pandas-rolling-function-(window=12)-to-calculate-the-sum-of-1-year-returns.-Add-this-column-to-the-original-dataframe.){.anchor-link} {#Q7.-Pandas-.rolling()-is-a-very-useful-function-to-know-(check-out-the-doc-string-of-pandas.Series.rolling-for-a-better-understanding-of-what-the-function-does).-In-this-problem,-we-will-calculate-the-1-year-rolling-sum-of-returns-for-the-data-in-stock_data.csv-file.-Clean-the-data-(remove-strings-and-drop-NaN-values).-Use-the-pandas-rolling-function-(window=12)-to-calculate-the-sum-of-1-year-returns.-Add-this-column-to-the-original-dataframe.}

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Answer 7[¶](#Answer-7){.anchor-link} {#Answer-7}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs"
markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[18\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Setting the Input File Path

    input_file_folder = 'Data'          # Folder Name within current directory where the file is stored
    input_file_name = 'stock_data.csv'  # Name of the File
    cwd = os.getcwd() 
    input_file_path = os.path.join(cwd, input_file_folder, input_file_name)

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

-   More details on dtpyes & converters used below while reading data is
    available [here](https://pbpython.com/pandas_dtypes.html)
-   In the above link, specifying dtypes vs. specifying converters while
    reading data is quite useful

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[19\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Reading & Cleaning the Data

    def numeric_converter(x): return pd.to_numeric(x, errors='coerce')  

    # Specifying dtype converters for specific columns
    converters = {'total_returns': numeric_converter,                      
                  'price': numeric_converter,
                  'date': lambda x: pd.to_datetime(x, errors='coerce')}

    df = pd.read_csv(filepath_or_buffer=input_file_path, sep=',', header=0, 
                     converters=converters).dropna(axis=0, how='any').reset_index(drop=True)

    df.drop_duplicates(subset=['permno', 'date'], keep='first', inplace=True, ignore_index=True)
    df.sort_values(by = ['permno', 'date'], ascending=[True, True], inplace=True, ignore_index=True)
    df.shape

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

Out\[19\]:

</div>

<div
class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult"
markdown="1" mime-type="text/plain">

    (2913, 6)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[20\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Calculating 12 months Rolling Returns & Adding them to the DataFrame 

    def calc_roll_returns(df, months=12):
        
        # Offset is 1 month less as the addition of returns is inclusive of both start & end months
        # Additional 10 days are added while comparing 11 month previous days to allow for misaligned months such as Feb

        offset = months - 1
        df.reset_index(inplace=True, drop=True)
        return [np.nan if index < offset else np.nan if 
                df.loc[index-offset, 'date'] < (df.loc[index, 'date'] 
                - pd.DateOffset(months=offset, days=10)) else
                sum([df_group.loc[i, 'total_returns'] for i in range(index-offset, index+1)])
                for index in df_group.index]

    months = 12                     # Rolling returns required for 12 months
    roll_returns = []
    for _, df_group in df.groupby('permno'):
        roll_returns.extend(calc_roll_returns(df_group, 12))

    df['roll_returns_'+str(months)+'months'] = roll_returns
    print(df.tail())

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

          permno          company_name       date  total_returns  price  \
    2908   10137  ALLEGHENY ENERGY INC 2010-07-31       0.102514  22.80   
    2909   10137  ALLEGHENY ENERGY INC 2010-08-31      -0.010965  22.55   
    2910   10137  ALLEGHENY ENERGY INC 2010-09-30       0.094013  24.52   
    2911   10137  ALLEGHENY ENERGY INC 2010-10-31      -0.053834  23.20   
    2912   10137  ALLEGHENY ENERGY INC 2011-01-31       0.063531  25.78   

          share_outstanding  roll_returns_12months  
    2908             169579              -0.041395  
    2909             169615              -0.099960  
    2910             169615              -0.015792  
    2911             169615               0.069891  
    2912             169939                    NaN  

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

  

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q8. Combining Pandas apply and lambda functions: Load and clean the stock_data.csv file. Compute the market cap by multiplying the price and outstanding shares. You need to segregate PERMNOs into large-cap, mid-cap, and small-cap stocks. First, you have to write a function that takes in a value $x$ (market cap) as an input. For segregating use the following criteria mentioned below. Use the pandas apply along with lambda function, to pass the function pass you have just coded up.[¶](#Q8.-Combining-Pandas-apply-and-lambda-functions:-Load-and-clean-the-stock_data.csv-file.-Compute-the-market-cap-by-multiplying-the-price-and-outstanding-shares.-You-need-to-segregate-PERMNOs-into-large-cap,-mid-cap,-and-small-cap-stocks.-First,-you-have-to-write-a-function-that-takes-in-a-value-$x$-(market-cap)-as-an-input.-For-segregating-use-the-following-criteria-mentioned-below.-Use-the-pandas-apply-along-with-lambda-function,-to-pass-the-function-pass-you-have-just-coded-up.){.anchor-link} {#Q8.-Combining-Pandas-apply-and-lambda-functions:-Load-and-clean-the-stock_data.csv-file.-Compute-the-market-cap-by-multiplying-the-price-and-outstanding-shares.-You-need-to-segregate-PERMNOs-into-large-cap,-mid-cap,-and-small-cap-stocks.-First,-you-have-to-write-a-function-that-takes-in-a-value-$x$-(market-cap)-as-an-input.-For-segregating-use-the-following-criteria-mentioned-below.-Use-the-pandas-apply-along-with-lambda-function,-to-pass-the-function-pass-you-have-just-coded-up.}

$$ f(x)=\\begin{cases} \\text{small cap} ,\\quad \\text{if x} &lt;
100000\\\\ \\text{mid cap} ,\\quad 100000 \\le \\text{if x} &lt;
1000000\\\\ \\text{large cap} ,\\quad \\text{if x} \\ge 1000000
\\end{cases} $$

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Answer 8[¶](#Answer-8){.anchor-link} {#Answer-8}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[21\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # For each permno, average market cap has been used yo determine market cap size

    pd.options.display.float_format = '{:,.2f}'.format         # Setrting Display Options for Market Cap

    df['market_cap'] = df['price']*df['share_outstanding']
    mcap_determiner = lambda x: np.select(condlist=
                                [x['market_cap']<10**5, x['market_cap']>10**6],
                                choicelist=['small_cap', 'large_cap'],
                                          default='mid_cap') 

    ans_q8 = df.groupby('permno')['market_cap'].mean().reset_index()\
               .assign(m_cap_size = lambda x: mcap_determiner(x)) 
    print(ans_q8)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedText jp-OutputArea-output" markdown="1"
mime-type="text/plain">

        permno     market_cap m_cap_size
    0    10001      93,580.90  small_cap
    1    10006     310,702.33    mid_cap
    2    10014      14,424.92  small_cap
    3    10028      22,384.82  small_cap
    4    10029      16,272.76  small_cap
    5    10042      39,216.34  small_cap
    6    10048     212,748.54    mid_cap
    7    10051     353,276.30    mid_cap
    8    10057      77,620.70  small_cap
    9    10064     306,181.12    mid_cap
    10   10066      25,052.92  small_cap
    11   10071     663,672.97    mid_cap
    12   10085     863,383.78    mid_cap
    13   10092     196,100.03    mid_cap
    14   10097      15,511.71  small_cap
    15   10102     318,587.27    mid_cap
    16   10104 178,854,090.59  large_cap
    17   10108   5,892,340.14  large_cap
    18   10116      32,546.23  small_cap
    19   10119   1,298,080.17  large_cap
    20   10120     286,089.80    mid_cap
    21   10123     219,657.30    mid_cap
    22   10125      35,624.19  small_cap
    23   10126   1,106,541.70  large_cap
    24   10137   2,702,880.54  large_cap

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Q9.Plot and Subplots: For the 4 PERMNOs - (10137, 10051, 10057, 10028), calculate the cumulative sum of returns and plot them in a 4-by-4 sub plot. Also, plot all their cumulative sum of returns in one plot. Hint: To compute the cumulative sum, you can use the .cumsum() function of pandas. You can also use the .plot() function of pandas dataframe instead of using matplotlib's plt function.[¶](#Q9.Plot-and-Subplots:-For-the-4-PERMNOs---(10137,-10051,-10057,-10028),-calculate-the-cumulative-sum-of-returns-and-plot-them-in-a-4-by-4-sub-plot.-Also,-plot-all-their-cumulative-sum-of-returns-in-one-plot.-Hint:-To-compute-the-cumulative-sum,-you-can-use-the-.cumsum()-function-of-pandas.-You-can-also-use-the-.plot()-function-of-pandas-dataframe-instead-of-using-matplotlib's-plt-function.){.anchor-link} {#Q9.Plot-and-Subplots:-For-the-4-PERMNOs---(10137,-10051,-10057,-10028),-calculate-the-cumulative-sum-of-returns-and-plot-them-in-a-4-by-4-sub-plot.-Also,-plot-all-their-cumulative-sum-of-returns-in-one-plot.-Hint:-To-compute-the-cumulative-sum,-you-can-use-the-.cumsum()-function-of-pandas.-You-can-also-use-the-.plot()-function-of-pandas-dataframe-instead-of-using-matplotlib's-plt-function.}

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

#### Answer 9[¶](#Answer-9){.anchor-link} {#Answer-9}

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[24\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Plotting a 4-by-4 subplot

    fig, ((ax1,ax2),(ax3,ax4)) = plt.subplots(2,2,sharex=False, sharey=False, 
                                              squeeze=True, figsize=(12,8))

    axs_permno = {ax1: 10137,ax2: 10051,ax3: 10057,ax4: 10028} 
    dfs_to_plot = {}
    for ax, permno in axs_permno.items(): 
        dfs_to_plot[permno] = df.loc[df['permno'] == permno, ['date','total_returns']].set_index('date').cumsum()
        ax.plot(dfs_to_plot[permno], label='permno: {}'.format(permno))
        ax.tick_params(labelsize=10)
        ax.legend(fontsize=12,frameon=True)

    fig.text(0.5, 0.04, 'Date', ha='center', fontsize=12)
    fig.text(0.08, 0.5, 'Cumulative Returns (Absolute)', va='center', rotation='vertical', fontsize=12)
    fig.suptitle("Cumulative Returns over Time for different permnos", ha='center', fontsize=16)
    fig.tight_layout()
    fig.subplots_adjust(left = 0.14,top=0.92, bottom = 0.14)
    plt.show();

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedSVG jp-OutputArea-output" markdown="1"
mime-type="image/svg+xml">

![](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjU1OC4yMjVwdCIgdmVyc2lvbj0iMS4xIiB2aWV3Ym94PSIwIDAgNzk4LjQ4IDU1OC4yMjUiIHdpZHRoPSI3OTguNDhwdCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayI+CiA8bWV0YWRhdGE+CiAgPHJkZiB4bWxuczpjYz0iaHR0cDovL2NyZWF0aXZlY29tbW9ucy5vcmcvbnMjIiB4bWxuczpkYz0iaHR0cDovL3B1cmwub3JnL2RjL2VsZW1lbnRzLzEuMS8iIHhtbG5zOnJkZj0iaHR0cDovL3d3dy53My5vcmcvMTk5OS8wMi8yMi1yZGYtc3ludGF4LW5zIyI+CiAgIDx3b3JrPgogICAgPHR5cGUgcmRmOnJlc291cmNlPSJodHRwOi8vcHVybC5vcmcvZGMvZGNtaXR5cGUvU3RpbGxJbWFnZSI+PC90eXBlPgogICAgPGRhdGU+MjAyMS0wNy0zMFQxMDoxNTozMC4yNTg5MDA8L2RhdGU+CiAgICA8Zm9ybWF0PmltYWdlL3N2Zyt4bWw8L2Zvcm1hdD4KICAgIDxjcmVhdG9yPgogICAgIDxhZ2VudD4KICAgICAgPHRpdGxlPk1hdHBsb3RsaWIgdjMuMy40LCBodHRwczovL21hdHBsb3RsaWIub3JnLzwvdGl0bGU+CiAgICAgPC9hZ2VudD4KICAgIDwvY3JlYXRvcj4KICAgPC93b3JrPgogIDwvcmRmPgogPC9tZXRhZGF0YT4KIDxkZWZzPgogIDxzdHlsZSB0eXBlPSJ0ZXh0L2NzcyI+KntzdHJva2UtbGluZWNhcDpidXR0O3N0cm9rZS1saW5lam9pbjpyb3VuZDt9PC9zdHlsZT4KIDwvZGVmcz4KIDxnIGlkPSJmaWd1cmVfMSI+CiAgPGcgaWQ9InBhdGNoXzEiPgogICA8cGF0aCBkPSJNIDAgNTU4LjIyNSAKTCA3OTguNDggNTU4LjIyNSAKTCA3OTguNDggMCAKTCAwIDAgCnoKIiBzdHlsZT0iZmlsbDojZmZmZmZmOyI+PC9wYXRoPgogIDwvZz4KICA8ZyBpZD0iYXhlc18xIj4KICAgPGcgaWQ9InBhdGNoXzIiPgogICAgPHBhdGggZD0iTSA1OS4wNCAyNTQuNTkzOTU1IApMIDQxMi44NTQyODcgMjU0LjU5Mzk1NSAKTCA0MTIuODU0Mjg3IDQxLjc2IApMIDU5LjA0IDQxLjc2IAp6CiIgc3R5bGU9ImZpbGw6I2VhZWFmMjsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0ibWF0cGxvdGxpYi5heGlzXzEiPgogICAgPGcgaWQ9Inh0aWNrXzEiPgogICAgIDxnIGlkPSJsaW5lMmRfMSI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwNGUyOGFiNmU3NikiIGQ9Ik0gODMuMzE3MiAyNTQuNTkzOTU1IApMIDgzLjMxNzIgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8yIj48L2c+CiAgICAgPGcgaWQ9InRleHRfMSI+CiAgICAgIDwhLS0gMTk3NiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDcyLjE5NTMyNSAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8ZGVmcz4KICAgICAgICA8cGF0aCBkPSJNIDM3LjI1IDAgCkwgMjguNDY4NzUgMCAKTCAyOC40Njg3NSA1NiAKUSAyNS4yOTY4NzUgNTIuOTg0Mzc1IDIwLjE0MDYyNSA0OS45NTMxMjUgClEgMTQuOTg0Mzc1IDQ2LjkyMTg3NSAxMC44OTA2MjUgNDUuNDA2MjUgCkwgMTAuODkwNjI1IDUzLjkwNjI1IApRIDE4LjI2NTYyNSA1Ny4zNzUgMjMuNzgxMjUgNjIuMjk2ODc1IApRIDI5LjI5Njg3NSA2Ny4yMzQzNzUgMzEuNTkzNzUgNzEuODc1IApMIDM3LjI1IDcxLjg3NSAKegoiIGlkPSJBcmlhbE1ULTQ5Ij48L3BhdGg+CiAgICAgICAgPHBhdGggZD0iTSA1LjQ2ODc1IDE2LjU0Njg3NSAKTCAxMy45MjE4NzUgMTcuMzI4MTI1IApRIDE0Ljk4NDM3NSAxMS4zNzUgMTguMDE1NjI1IDguNjg3NSAKUSAyMS4wNDY4NzUgNiAyNS43ODEyNSA2IApRIDI5LjgyODEyNSA2IDMyLjg3NSA3Ljg1OTM3NSAKUSAzNS45Mzc1IDkuNzE4NzUgMzcuODkwNjI1IDEyLjgxMjUgClEgMzkuODQzNzUgMTUuOTIxODc1IDQxLjE1NjI1IDIxLjE4NzUgClEgNDIuNDg0Mzc1IDI2LjQ2ODc1IDQyLjQ4NDM3NSAzMS45Mzc1IApRIDQyLjQ4NDM3NSAzMi41MTU2MjUgNDIuNDM3NSAzMy42ODc1IApRIDM5Ljc5Njg3NSAyOS41IDM1LjIzNDM3NSAyNi44NzUgClEgMzAuNjcxODc1IDI0LjI2NTYyNSAyNS4zNDM3NSAyNC4yNjU2MjUgClEgMTYuNDUzMTI1IDI0LjI2NTYyNSAxMC4yOTY4NzUgMzAuNzAzMTI1IApRIDQuMTU2MjUgMzcuMTU2MjUgNC4xNTYyNSA0Ny43MDMxMjUgClEgNC4xNTYyNSA1OC41OTM3NSAxMC41NzgxMjUgNjUuMjM0Mzc1IApRIDE3IDcxLjg3NSAyNi42NTYyNSA3MS44NzUgClEgMzMuNjQwNjI1IDcxLjg3NSAzOS40MjE4NzUgNjguMTA5Mzc1IApRIDQ1LjIxODc1IDY0LjM1OTM3NSA0OC4yMTg3NSA1Ny4zOTA2MjUgClEgNTEuMjE4NzUgNTAuNDM3NSA1MS4yMTg3NSAzNy4yNSAKUSA1MS4yMTg3NSAyMy41MzEyNSA0OC4yMzQzNzUgMTUuNDA2MjUgClEgNDUuMjY1NjI1IDcuMjgxMjUgMzkuMzc1IDMuMDMxMjUgClEgMzMuNSAtMS4yMTg3NSAyNS41OTM3NSAtMS4yMTg3NSAKUSAxNy4xODc1IC0xLjIxODc1IDExLjg1OTM3NSAzLjQzNzUgClEgNi41NDY4NzUgOC4xMDkzNzUgNS40Njg3NSAxNi41NDY4NzUgCnoKTSA0MS40NTMxMjUgNDguMTQwNjI1IApRIDQxLjQ1MzEyNSA1NS43MTg3NSAzNy40MjE4NzUgNjAuMTU2MjUgClEgMzMuNDA2MjUgNjQuNTkzNzUgMjcuNzM0Mzc1IDY0LjU5Mzc1IApRIDIxLjg3NSA2NC41OTM3NSAxNy41MzEyNSA1OS44MTI1IApRIDEzLjE4NzUgNTUuMDMxMjUgMTMuMTg3NSA0Ny40MDYyNSAKUSAxMy4xODc1IDQwLjU3ODEyNSAxNy4zMTI1IDM2LjI5Njg3NSAKUSAyMS40Mzc1IDMyLjAzMTI1IDI3LjQ4NDM3NSAzMi4wMzEyNSAKUSAzMy41OTM3NSAzMi4wMzEyNSAzNy41MTU2MjUgMzYuMjk2ODc1IApRIDQxLjQ1MzEyNSA0MC41NzgxMjUgNDEuNDUzMTI1IDQ4LjE0MDYyNSAKegoiIGlkPSJBcmlhbE1ULTU3Ij48L3BhdGg+CiAgICAgICAgPHBhdGggZD0iTSA0LjczNDM3NSA2Mi4yMDMxMjUgCkwgNC43MzQzNzUgNzAuNjU2MjUgCkwgNTEuMDc4MTI1IDcwLjY1NjI1IApMIDUxLjA3ODEyNSA2My44MTI1IApRIDQ0LjIzNDM3NSA1Ni41NDY4NzUgMzcuNTE1NjI1IDQ0LjQ4NDM3NSAKUSAzMC44MTI1IDMyLjQyMTg3NSAyNy4xNTYyNSAxOS42NzE4NzUgClEgMjQuNTE1NjI1IDEwLjY4NzUgMjMuNzgxMjUgMCAKTCAxNC43NSAwIApRIDE0Ljg5MDYyNSA4LjQ1MzEyNSAxOC4wNjI1IDIwLjQwNjI1IApRIDIxLjIzNDM3NSAzMi4zNzUgMjcuMTcxODc1IDQzLjQ4NDM3NSAKUSAzMy4xMDkzNzUgNTQuNTkzNzUgMzkuNzk2ODc1IDYyLjIwMzEyNSAKegoiIGlkPSJBcmlhbE1ULTU1Ij48L3BhdGg+CiAgICAgICAgPHBhdGggZD0iTSA0OS43NSA1NC4wNDY4NzUgCkwgNDEuMDE1NjI1IDUzLjM3NSAKUSAzOS44NDM3NSA1OC41NDY4NzUgMzcuNzAzMTI1IDYwLjg5MDYyNSAKUSAzNC4xMjUgNjQuNjU2MjUgMjguOTA2MjUgNjQuNjU2MjUgClEgMjQuNzAzMTI1IDY0LjY1NjI1IDIxLjUzMTI1IDYyLjMxMjUgClEgMTcuMzkwNjI1IDU5LjI4MTI1IDE0Ljk4NDM3NSA1My40Njg3NSAKUSAxMi41OTM3NSA0Ny42NTYyNSAxMi41IDM2LjkyMTg3NSAKUSAxNS42NzE4NzUgNDEuNzUgMjAuMjY1NjI1IDQ0LjA5Mzc1IApRIDI0Ljg1OTM3NSA0Ni40Mzc1IDI5Ljg5MDYyNSA0Ni40Mzc1IApRIDM4LjY3MTg3NSA0Ni40Mzc1IDQ0Ljg0Mzc1IDM5Ljk2ODc1IApRIDUxLjAzMTI1IDMzLjUgNTEuMDMxMjUgMjMuMjUgClEgNTEuMDMxMjUgMTYuNSA0OC4xMjUgMTAuNzE4NzUgClEgNDUuMjE4NzUgNC45Mzc1IDQwLjE0MDYyNSAxLjg1OTM3NSAKUSAzNS4wNjI1IC0xLjIxODc1IDI4LjYwOTM3NSAtMS4yMTg3NSAKUSAxNy42MjUgLTEuMjE4NzUgMTAuNjg3NSA2Ljg1OTM3NSAKUSAzLjc2NTYyNSAxNC45Mzc1IDMuNzY1NjI1IDMzLjUgClEgMy43NjU2MjUgNTQuMjUgMTEuNDIxODc1IDYzLjY3MTg3NSAKUSAxOC4xMDkzNzUgNzEuODc1IDI5LjQzNzUgNzEuODc1IApRIDM3Ljg5MDYyNSA3MS44NzUgNDMuMjgxMjUgNjcuMTQwNjI1IApRIDQ4LjY4NzUgNjIuNDA2MjUgNDkuNzUgNTQuMDQ2ODc1IAp6Ck0gMTMuODc1IDIzLjE4NzUgClEgMTMuODc1IDE4LjY1NjI1IDE1Ljc5Njg3NSAxNC41IApRIDE3LjcxODc1IDEwLjM1OTM3NSAyMS4xODc1IDguMTcxODc1IApRIDI0LjY1NjI1IDYgMjguNDY4NzUgNiAKUSAzNC4wMzEyNSA2IDM4LjAzMTI1IDEwLjQ4NDM3NSAKUSA0Mi4wNDY4NzUgMTQuOTg0Mzc1IDQyLjA0Njg3NSAyMi43MDMxMjUgClEgNDIuMDQ2ODc1IDMwLjEyNSAzOC4wNzgxMjUgMzQuMzkwNjI1IApRIDM0LjEyNSAzOC42NzE4NzUgMjguMTI1IDM4LjY3MTg3NSAKUSAyMi4xNzE4NzUgMzguNjcxODc1IDE4LjAxNTYyNSAzNC4zOTA2MjUgClEgMTMuODc1IDMwLjEyNSAxMy44NzUgMjMuMTg3NSAKegoiIGlkPSJBcmlhbE1ULTU0Ij48L3BhdGg+CiAgICAgICA8L2RlZnM+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU1Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTQiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzIiPgogICAgIDxnIGlkPSJsaW5lMmRfMyI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwNGUyOGFiNmU3NikiIGQ9Ik0gMTE5LjA1NjAxNyAyNTQuNTkzOTU1IApMIDExOS4wNTYwMTcgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF80Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMiI+CiAgICAgIDwhLS0gMTk4MCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwNy45MzQxNDIgMjY4Ljc1MTc2OClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPGRlZnM+CiAgICAgICAgPHBhdGggZD0iTSAxNy42NzE4NzUgMzguODEyNSAKUSAxMi4yMDMxMjUgNDAuODI4MTI1IDkuNTYyNSA0NC41MzEyNSAKUSA2LjkzNzUgNDguMjUgNi45Mzc1IDUzLjQyMTg3NSAKUSA2LjkzNzUgNjEuMjM0Mzc1IDEyLjU0Njg3NSA2Ni41NDY4NzUgClEgMTguMTcxODc1IDcxLjg3NSAyNy40ODQzNzUgNzEuODc1IApRIDM2Ljg1OTM3NSA3MS44NzUgNDIuNTc4MTI1IDY2LjQyMTg3NSAKUSA0OC4yOTY4NzUgNjAuOTg0Mzc1IDQ4LjI5Njg3NSA1My4xNzE4NzUgClEgNDguMjk2ODc1IDQ4LjE4NzUgNDUuNjcxODc1IDQ0LjUgClEgNDMuMDYyNSA0MC44MjgxMjUgMzcuNzUgMzguODEyNSAKUSA0NC4zNDM3NSAzNi42NzE4NzUgNDcuNzgxMjUgMzEuODc1IApRIDUxLjIxODc1IDI3LjA5Mzc1IDUxLjIxODc1IDIwLjQ1MzEyNSAKUSA1MS4yMTg3NSAxMS4yODEyNSA0NC43MTg3NSA1LjAzMTI1IApRIDM4LjIzNDM3NSAtMS4yMTg3NSAyNy42NDA2MjUgLTEuMjE4NzUgClEgMTcuMDQ2ODc1IC0xLjIxODc1IDEwLjU0Njg3NSA1LjA0Njg3NSAKUSA0LjA0Njg3NSAxMS4zMjgxMjUgNC4wNDY4NzUgMjAuNzAzMTI1IApRIDQuMDQ2ODc1IDI3LjY4NzUgNy41OTM3NSAzMi4zOTA2MjUgClEgMTEuMTQwNjI1IDM3LjEwOTM3NSAxNy42NzE4NzUgMzguODEyNSAKegpNIDE1LjkyMTg3NSA1My43MTg3NSAKUSAxNS45MjE4NzUgNDguNjQwNjI1IDE5LjE4NzUgNDUuNDA2MjUgClEgMjIuNDY4NzUgNDIuMTg3NSAyNy42ODc1IDQyLjE4NzUgClEgMzIuNzY1NjI1IDQyLjE4NzUgMzYuMDE1NjI1IDQ1LjM3NSAKUSAzOS4yNjU2MjUgNDguNTc4MTI1IDM5LjI2NTYyNSA1My4yMTg3NSAKUSAzOS4yNjU2MjUgNTguMDYyNSAzNS45MDYyNSA2MS4zNTkzNzUgClEgMzIuNTYyNSA2NC42NTYyNSAyNy41OTM3NSA2NC42NTYyNSAKUSAyMi41NjI1IDY0LjY1NjI1IDE5LjIzNDM3NSA2MS40MjE4NzUgClEgMTUuOTIxODc1IDU4LjIwMzEyNSAxNS45MjE4NzUgNTMuNzE4NzUgCnoKTSAxMy4wOTM3NSAyMC42NTYyNSAKUSAxMy4wOTM3NSAxNi44OTA2MjUgMTQuODc1IDEzLjM3NSAKUSAxNi42NTYyNSA5Ljg1OTM3NSAyMC4xNzE4NzUgNy45MjE4NzUgClEgMjMuNjg3NSA2IDI3LjczNDM3NSA2IApRIDM0LjAzMTI1IDYgMzguMTI1IDEwLjA0Njg3NSAKUSA0Mi4yMzQzNzUgMTQuMTA5Mzc1IDQyLjIzNDM3NSAyMC4zNTkzNzUgClEgNDIuMjM0Mzc1IDI2LjcwMzEyNSAzOC4wMTU2MjUgMzAuODU5Mzc1IApRIDMzLjc5Njg3NSAzNS4wMTU2MjUgMjcuNDM3NSAzNS4wMTU2MjUgClEgMjEuMjM0Mzc1IDM1LjAxNTYyNSAxNy4xNTYyNSAzMC45MDYyNSAKUSAxMy4wOTM3NSAyNi44MTI1IDEzLjA5Mzc1IDIwLjY1NjI1IAp6CiIgaWQ9IkFyaWFsTVQtNTYiPjwvcGF0aD4KICAgICAgICA8cGF0aCBkPSJNIDQuMTU2MjUgMzUuMjk2ODc1IApRIDQuMTU2MjUgNDggNi43NjU2MjUgNTUuNzM0Mzc1IApRIDkuMzc1IDYzLjQ4NDM3NSAxNC41MTU2MjUgNjcuNjcxODc1IApRIDE5LjY3MTg3NSA3MS44NzUgMjcuNDg0Mzc1IDcxLjg3NSAKUSAzMy4yNSA3MS44NzUgMzcuNTkzNzUgNjkuNTQ2ODc1IApRIDQxLjkzNzUgNjcuMjM0Mzc1IDQ0Ljc2NTYyNSA2Mi44NTkzNzUgClEgNDcuNjA5Mzc1IDU4LjUgNDkuMjE4NzUgNTIuMjE4NzUgClEgNTAuODI4MTI1IDQ1Ljk1MzEyNSA1MC44MjgxMjUgMzUuMjk2ODc1IApRIDUwLjgyODEyNSAyMi43MDMxMjUgNDguMjM0Mzc1IDE0Ljk2ODc1IApRIDQ1LjY1NjI1IDcuMjM0Mzc1IDQwLjUgMyAKUSAzNS4zNTkzNzUgLTEuMjE4NzUgMjcuNDg0Mzc1IC0xLjIxODc1IApRIDE3LjE0MDYyNSAtMS4yMTg3NSAxMS4yMzQzNzUgNi4yMDMxMjUgClEgNC4xNTYyNSAxNS4xNDA2MjUgNC4xNTYyNSAzNS4yOTY4NzUgCnoKTSAxMy4xODc1IDM1LjI5Njg3NSAKUSAxMy4xODc1IDE3LjY3MTg3NSAxNy4zMTI1IDExLjgyODEyNSAKUSAyMS40Mzc1IDYgMjcuNDg0Mzc1IDYgClEgMzMuNTQ2ODc1IDYgMzcuNjcxODc1IDExLjg1OTM3NSAKUSA0MS43OTY4NzUgMTcuNzE4NzUgNDEuNzk2ODc1IDM1LjI5Njg3NSAKUSA0MS43OTY4NzUgNTIuOTg0Mzc1IDM3LjY3MTg3NSA1OC43ODEyNSAKUSAzMy41NDY4NzUgNjQuNTkzNzUgMjcuMzkwNjI1IDY0LjU5Mzc1IApRIDIxLjM0Mzc1IDY0LjU5Mzc1IDE3LjcxODc1IDU5LjQ2ODc1IApRIDEzLjE4NzUgNTIuOTM3NSAxMy4xODc1IDM1LjI5Njg3NSAKegoiIGlkPSJBcmlhbE1ULTQ4Ij48L3BhdGg+CiAgICAgICA8L2RlZnM+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU2Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzMiPgogICAgIDxnIGlkPSJsaW5lMmRfNSI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwNGUyOGFiNmU3NikiIGQ9Ik0gMTU0Ljc5NDgzMyAyNTQuNTkzOTU1IApMIDE1NC43OTQ4MzMgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF82Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMyI+CiAgICAgIDwhLS0gMTk4NCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE0My42NzI5NTggMjY4Ljc1MTc2OClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPGRlZnM+CiAgICAgICAgPHBhdGggZD0iTSAzMi4zMjgxMjUgMCAKTCAzMi4zMjgxMjUgMTcuMTQwNjI1IApMIDEuMjY1NjI1IDE3LjE0MDYyNSAKTCAxLjI2NTYyNSAyNS4yMDMxMjUgCkwgMzMuOTM3NSA3MS41NzgxMjUgCkwgNDEuMTA5Mzc1IDcxLjU3ODEyNSAKTCA0MS4xMDkzNzUgMjUuMjAzMTI1IApMIDUwLjc4MTI1IDI1LjIwMzEyNSAKTCA1MC43ODEyNSAxNy4xNDA2MjUgCkwgNDEuMTA5Mzc1IDE3LjE0MDYyNSAKTCA0MS4xMDkzNzUgMCAKegpNIDMyLjMyODEyNSAyNS4yMDMxMjUgCkwgMzIuMzI4MTI1IDU3LjQ2ODc1IApMIDkuOTA2MjUgMjUuMjAzMTI1IAp6CiIgaWQ9IkFyaWFsTVQtNTIiPjwvcGF0aD4KICAgICAgIDwvZGVmcz4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTYiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC01MiI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfNCI+CiAgICAgPGcgaWQ9ImxpbmUyZF83Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A0ZTI4YWI2ZTc2KSIgZD0iTSAxOTAuNTMzNjUgMjU0LjU5Mzk1NSAKTCAxOTAuNTMzNjUgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF84Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfNCI+CiAgICAgIDwhLS0gMTk4OCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE3OS40MTE3NzUgMjY4Ljc1MTc2OClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTciPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC01NiI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU2Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja181Ij4KICAgICA8ZyBpZD0ibGluZTJkXzkiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDIyNi4yNzI0NjcgMjU0LjU5Mzk1NSAKTCAyMjYuMjcyNDY3IDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTAiPjwvZz4KICAgICA8ZyBpZD0idGV4dF81Ij4KICAgICAgPCEtLSAxOTkyIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMjE1LjE1MDU5MiAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8ZGVmcz4KICAgICAgICA8cGF0aCBkPSJNIDUwLjM0Mzc1IDguNDUzMTI1IApMIDUwLjM0Mzc1IDAgCkwgMy4wMzEyNSAwIApRIDIuOTM3NSAzLjE3MTg3NSA0LjA0Njg3NSA2LjEwOTM3NSAKUSA1Ljg1OTM3NSAxMC45Mzc1IDkuODI4MTI1IDE1LjYyNSAKUSAxMy44MTI1IDIwLjMxMjUgMjEuMzQzNzUgMjYuNDY4NzUgClEgMzMuMDE1NjI1IDM2LjAzMTI1IDM3LjEwOTM3NSA0MS42MjUgClEgNDEuMjE4NzUgNDcuMjE4NzUgNDEuMjE4NzUgNTIuMjAzMTI1IApRIDQxLjIxODc1IDU3LjQyMTg3NSAzNy40Njg3NSA2MSAKUSAzMy43MzQzNzUgNjQuNTkzNzUgMjcuNzM0Mzc1IDY0LjU5Mzc1IApRIDIxLjM5MDYyNSA2NC41OTM3NSAxNy41NzgxMjUgNjAuNzgxMjUgClEgMTMuNzY1NjI1IDU2Ljk4NDM3NSAxMy43MTg3NSA1MC4yNSAKTCA0LjY4NzUgNTEuMTcxODc1IApRIDUuNjA5Mzc1IDYxLjI4MTI1IDExLjY1NjI1IDY2LjU3ODEyNSAKUSAxNy43MTg3NSA3MS44NzUgMjcuOTM3NSA3MS44NzUgClEgMzguMjM0Mzc1IDcxLjg3NSA0NC4yMzQzNzUgNjYuMTU2MjUgClEgNTAuMjUgNjAuNDUzMTI1IDUwLjI1IDUyIApRIDUwLjI1IDQ3LjcwMzEyNSA0OC40ODQzNzUgNDMuNTQ2ODc1IApRIDQ2LjczNDM3NSAzOS40MDYyNSA0Mi42NTYyNSAzNC44MTI1IApRIDM4LjU3ODEyNSAzMC4yMTg3NSAyOS4xMDkzNzUgMjIuMjE4NzUgClEgMjEuMTg3NSAxNS41NzgxMjUgMTguOTM3NSAxMy4yMDMxMjUgClEgMTYuNzAzMTI1IDEwLjg0Mzc1IDE1LjIzNDM3NSA4LjQ1MzEyNSAKegoiIGlkPSJBcmlhbE1ULTUwIj48L3BhdGg+CiAgICAgICA8L2RlZnM+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzYiPgogICAgIDxnIGlkPSJsaW5lMmRfMTEiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDI2Mi4wMTEyODQgMjU0LjU5Mzk1NSAKTCAyNjIuMDExMjg0IDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTIiPjwvZz4KICAgICA8ZyBpZD0idGV4dF82Ij4KICAgICAgPCEtLSAxOTk2IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMjUwLjg4OTQwOSAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTQiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzciPgogICAgIDxnIGlkPSJsaW5lMmRfMTMiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDI5Ny43NTAxMDEgMjU0LjU5Mzk1NSAKTCAyOTcuNzUwMTAxIDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTQiPjwvZz4KICAgICA8ZyBpZD0idGV4dF83Ij4KICAgICAgPCEtLSAyMDAwIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMjg2LjYyODIyNiAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzgiPgogICAgIDxnIGlkPSJsaW5lMmRfMTUiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDMzMy40ODg5MTggMjU0LjU5Mzk1NSAKTCAzMzMuNDg4OTE4IDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTYiPjwvZz4KICAgICA8ZyBpZD0idGV4dF84Ij4KICAgICAgPCEtLSAyMDA0IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzIyLjM2NzA0MyAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTIiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzkiPgogICAgIDxnIGlkPSJsaW5lMmRfMTciPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDM2OS4yMjc3MzUgMjU0LjU5Mzk1NSAKTCAzNjkuMjI3NzM1IDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTgiPjwvZz4KICAgICA8ZyBpZD0idGV4dF85Ij4KICAgICAgPCEtLSAyMDA4IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzU4LjEwNTg2IDI2OC43NTE3Njgpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC01NiI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMTAiPgogICAgIDxnIGlkPSJsaW5lMmRfMTkiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDQwNC45NjY1NTEgMjU0LjU5Mzk1NSAKTCA0MDQuOTY2NTUxIDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMjAiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xMCI+CiAgICAgIDwhLS0gMjAxMiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDM5My44NDQ2NzYgMjY4Ljc1MTc2OClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgPC9nPgogICA8ZyBpZD0ibWF0cGxvdGxpYi5heGlzXzIiPgogICAgPGcgaWQ9Inl0aWNrXzEiPgogICAgIDxnIGlkPSJsaW5lMmRfMjEiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDU5LjA0IDI1Mi41NjM5MjggCkwgNDEyLjg1NDI4NyAyNTIuNTYzOTI4IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMjIiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xMSI+CiAgICAgIDwhLS0gMCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ2LjQ3OTA2MyAyNTYuMTQyODM0KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja18yIj4KICAgICA8ZyBpZD0ibGluZTJkXzIzIj4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A0ZTI4YWI2ZTc2KSIgZD0iTSA1OS4wNCAyMTcuNTk0MzU3IApMIDQxMi44NTQyODcgMjE3LjU5NDM1NyAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzI0Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMTIiPgogICAgICA8IS0tIDEgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0Ni40NzkwNjMgMjIxLjE3MzI2MylzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfMyI+CiAgICAgPGcgaWQ9ImxpbmUyZF8yNSI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwNGUyOGFiNmU3NikiIGQ9Ik0gNTkuMDQgMTgyLjYyNDc4NSAKTCA0MTIuODU0Mjg3IDE4Mi42MjQ3ODUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8yNiI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzEzIj4KICAgICAgPCEtLSAyIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDYuNDc5MDYzIDE4Ni4yMDM2OTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inl0aWNrXzQiPgogICAgIDxnIGlkPSJsaW5lMmRfMjciPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDRlMjhhYjZlNzYpIiBkPSJNIDU5LjA0IDE0Ny42NTUyMTQgCkwgNDEyLjg1NDI4NyAxNDcuNjU1MjE0IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMjgiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xNCI+CiAgICAgIDwhLS0gMyAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ2LjQ3OTA2MyAxNTEuMjM0MTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDxkZWZzPgogICAgICAgIDxwYXRoIGQ9Ik0gNC4yMDMxMjUgMTguODkwNjI1IApMIDEyLjk4NDM3NSAyMC4wNjI1IApRIDE0LjUgMTIuNTkzNzUgMTguMTQwNjI1IDkuMjk2ODc1IApRIDIxLjc4MTI1IDYgMjcgNiAKUSAzMy4yMDMxMjUgNiAzNy40Njg3NSAxMC4yOTY4NzUgClEgNDEuNzUgMTQuNTkzNzUgNDEuNzUgMjAuOTUzMTI1IApRIDQxLjc1IDI3IDM3Ljc5Njg3NSAzMC45MjE4NzUgClEgMzMuODQzNzUgMzQuODU5Mzc1IDI3LjczNDM3NSAzNC44NTkzNzUgClEgMjUuMjUgMzQuODU5Mzc1IDIxLjUzMTI1IDMzLjg5MDYyNSAKTCAyMi41MTU2MjUgNDEuNjA5Mzc1IApRIDIzLjM5MDYyNSA0MS41IDIzLjkyMTg3NSA0MS41IApRIDI5LjU0Njg3NSA0MS41IDM0LjAzMTI1IDQ0LjQyMTg3NSAKUSAzOC41MzEyNSA0Ny4zNTkzNzUgMzguNTMxMjUgNTMuNDY4NzUgClEgMzguNTMxMjUgNTguMjk2ODc1IDM1LjI1IDYxLjQ2ODc1IApRIDMxLjk4NDM3NSA2NC42NTYyNSAyNi44MTI1IDY0LjY1NjI1IApRIDIxLjY4NzUgNjQuNjU2MjUgMTguMjY1NjI1IDYxLjQyMTg3NSAKUSAxNC44NDM3NSA1OC4yMDMxMjUgMTMuODc1IDUxLjc2NTYyNSAKTCA1LjA3ODEyNSA1My4zMjgxMjUgClEgNi42ODc1IDYyLjE1NjI1IDEyLjM5MDYyNSA2Ny4wMTU2MjUgClEgMTguMTA5Mzc1IDcxLjg3NSAyNi42MDkzNzUgNzEuODc1IApRIDMyLjQ2ODc1IDcxLjg3NSAzNy4zOTA2MjUgNjkuMzU5Mzc1IApRIDQyLjMyODEyNSA2Ni44NDM3NSA0NC45Mzc1IDYyLjUgClEgNDcuNTYyNSA1OC4xNTYyNSA0Ny41NjI1IDUzLjI2NTYyNSAKUSA0Ny41NjI1IDQ4LjY0MDYyNSA0NS4wNjI1IDQ0LjgyODEyNSAKUSA0Mi41NzgxMjUgNDEuMDE1NjI1IDM3LjcwMzEyNSAzOC43NjU2MjUgClEgNDQuMDQ2ODc1IDM3LjMxMjUgNDcuNTYyNSAzMi42ODc1IApRIDUxLjA3ODEyNSAyOC4wNzgxMjUgNTEuMDc4MTI1IDIxLjE0MDYyNSAKUSA1MS4wNzgxMjUgMTEuNzY1NjI1IDQ0LjIzNDM3NSA1LjI1IApRIDM3LjQwNjI1IC0xLjI2NTYyNSAyNi45NTMxMjUgLTEuMjY1NjI1IApRIDE3LjUzMTI1IC0xLjI2NTYyNSAxMS4yOTY4NzUgNC4zNDM3NSAKUSA1LjA3ODEyNSA5Ljk2ODc1IDQuMjAzMTI1IDE4Ljg5MDYyNSAKegoiIGlkPSJBcmlhbE1ULTUxIj48L3BhdGg+CiAgICAgICA8L2RlZnM+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUxIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja181Ij4KICAgICA8ZyBpZD0ibGluZTJkXzI5Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A0ZTI4YWI2ZTc2KSIgZD0iTSA1OS4wNCAxMTIuNjg1NjQzIApMIDQxMi44NTQyODcgMTEyLjY4NTY0MyAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzMwIj48L2c+CiAgICAgPGcgaWQ9InRleHRfMTUiPgogICAgICA8IS0tIDQgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0Ni40NzkwNjMgMTE2LjI2NDU0OSlzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MiI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfNiI+CiAgICAgPGcgaWQ9ImxpbmUyZF8zMSI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwNGUyOGFiNmU3NikiIGQ9Ik0gNTkuMDQgNzcuNzE2MDcyIApMIDQxMi44NTQyODcgNzcuNzE2MDcyIAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMzIiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xNiI+CiAgICAgIDwhLS0gNSAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ2LjQ3OTA2MyA4MS4yOTQ5Nzgpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDxkZWZzPgogICAgICAgIDxwYXRoIGQ9Ik0gNC4xNTYyNSAxOC43NSAKTCAxMy4zNzUgMTkuNTMxMjUgClEgMTQuNDA2MjUgMTIuNzk2ODc1IDE4LjE0MDYyNSA5LjM5MDYyNSAKUSAyMS44NzUgNiAyNy4xNTYyNSA2IApRIDMzLjUgNiAzNy44OTA2MjUgMTAuNzgxMjUgClEgNDIuMjgxMjUgMTUuNTc4MTI1IDQyLjI4MTI1IDIzLjQ4NDM3NSAKUSA0Mi4yODEyNSAzMSAzOC4wNjI1IDM1LjM0Mzc1IApRIDMzLjg0Mzc1IDM5LjcwMzEyNSAyNyAzOS43MDMxMjUgClEgMjIuNzUgMzkuNzAzMTI1IDE5LjMyODEyNSAzNy43NjU2MjUgClEgMTUuOTIxODc1IDM1Ljg0Mzc1IDEzLjk2ODc1IDMyLjc2NTYyNSAKTCA1LjcxODc1IDMzLjg0Mzc1IApMIDEyLjY0MDYyNSA3MC42MDkzNzUgCkwgNDguMjUgNzAuNjA5Mzc1IApMIDQ4LjI1IDYyLjIwMzEyNSAKTCAxOS42NzE4NzUgNjIuMjAzMTI1IApMIDE1LjgyODEyNSA0Mi45Njg3NSAKUSAyMi4yNjU2MjUgNDcuNDY4NzUgMjkuMzQzNzUgNDcuNDY4NzUgClEgMzguNzE4NzUgNDcuNDY4NzUgNDUuMTU2MjUgNDAuOTY4NzUgClEgNTEuNjA5Mzc1IDM0LjQ2ODc1IDUxLjYwOTM3NSAyNC4yNjU2MjUgClEgNTEuNjA5Mzc1IDE0LjU0Njg3NSA0NS45NTMxMjUgNy40Njg3NSAKUSAzOS4wNjI1IC0xLjIxODc1IDI3LjE1NjI1IC0xLjIxODc1IApRIDE3LjM5MDYyNSAtMS4yMTg3NSAxMS4yMDMxMjUgNC4yNSAKUSA1LjAzMTI1IDkuNzE4NzUgNC4xNTYyNSAxOC43NSAKegoiIGlkPSJBcmlhbE1ULTUzIj48L3BhdGg+CiAgICAgICA8L2RlZnM+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUzIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja183Ij4KICAgICA8ZyBpZD0ibGluZTJkXzMzIj4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A0ZTI4YWI2ZTc2KSIgZD0iTSA1OS4wNCA0Mi43NDY1IApMIDQxMi44NTQyODcgNDIuNzQ2NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzM0Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMTciPgogICAgICA8IS0tIDYgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0Ni40NzkwNjMgNDYuMzI1NDA3KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU0Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgPC9nPgogICA8ZyBpZD0ibGluZTJkXzM1Ij4KICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwNGUyOGFiNmU3NikiIGQ9Ik0gNzUuMTIyNDY4IDI0MC45MDc0MTYgCkwgNzUuODA3NCAyNDIuOTY0NDY2IApMIDc2LjU2NTcxOSAyNDMuNzczMTM3IApMIDc3LjI5OTU3NiAyNDQuOTE5Njg1IApMIDc4LjA1Nzg5NCAyMzcuMjE0NTI0IApMIDc4Ljc5MTc1MSAyMzYuOTYxOTc0IApMIDc5LjU1MDA2OSAyMzkuMTc4MzQ1IApMIDgwLjMwODM4OCAyMzguOTE1NDA5IApMIDgxLjA0MjI0NCAyMzguOTA0OTUzIApMIDgxLjgwMDU2MyAyMzYuNzY5Mzk3IApMIDgyLjUzNDQxOSAyMzIuOTQ1MzY5IApMIDgzLjI5MjczOCAyMzMuNjQwMTQ1IApMIDg0LjA1MTA1NiAyMzEuOTg2MTg5IApMIDg0Ljc2MDQ1MSAyMzQuNDY3OTA5IApMIDg1LjUxODc3IDIzNC40MTkzMzcgCkwgODYuMjUyNjI2IDIzNC4xNzEzMzIgCkwgODcuMDEwOTQ1IDIzMy42Nzg3ODYgCkwgODcuNzQ0ODAxIDIzMy4zODczODQgCkwgODguNTAzMTIgMjMyLjE1NjA3MSAKTCA4OS45OTUyOTUgMjI2LjYxODE4NSAKTCA5MC43NTM2MTMgMjI4LjI4MzQwMSAKTCA5MS40ODc0NyAyMjUuNjYwNjgzIApMIDkyLjI0NTc4OCAyMjMuNzU3Njc0IApMIDkzLjY4OTA0IDIyNS4xNDY0MiAKTCA5NC40NDczNTggMjI2LjcwODc5MSAKTCA5NS4xODEyMTUgMjI1LjgzNDU1MiAKTCA5NS45Mzk1MzMgMjI0LjEyODczNiAKTCA5Ny40MzE3MDkgMjIyLjgzNTY2NiAKTCA5OC4xOTAwMjcgMjIzLjYzNDk2NiAKTCA5OC45MjM4ODQgMjIzLjM1Njg1MyAKTCA5OS42ODIyMDIgMjI0LjU5ODM3NyAKTCAxMDAuNDE2MDU5IDIyMy4wOTY2MDkgCkwgMTAxLjkzMjY5NiAyMjQuODk4MDY2IApMIDEwMi42MTc2MjkgMjI2LjY2ODY4MSAKTCAxMDMuMzc1OTQ3IDIyNi4wOTk4MzEgCkwgMTA0LjEwOTgwNCAyMjcuNTA3OTg1IApMIDEwNC44NjgxMjIgMjI2LjUyOTgxNyAKTCAxMDUuNjAxOTc5IDIyNi40MjUxNTMgCkwgMTA2LjM2MDI5NyAyMjUuNjk2NjMyIApMIDEwNy4xMTg2MTYgMjI1LjIyMDg3MSAKTCAxMDcuODUyNDcyIDIyNS41ODcwMDIgCkwgMTA4LjYxMDc5MSAyMjcuNzcyNiAKTCAxMDkuMzQ0NjQ3IDIyNi45OTU1MDYgCkwgMTEwLjEwMjk2NiAyMjkuNjcxNDQ4IApMIDExMC44NjEyODQgMjI2LjAwNTI3MyAKTCAxMTEuNTQ2MjE3IDIyNy41MzY4IApMIDExMi4zMDQ1MzYgMjI2LjM1MTU3NyAKTCAxMTMuMDM4MzkyIDIyNi42MTY1MDYgCkwgMTEzLjc5NjcxMSAyMjQuNzQ3OTA3IApMIDExNC41MzA1NjcgMjI0LjM2Mjc1MiAKTCAxMTUuMjg4ODg2IDIyMi41NjI4MzMgCkwgMTE2LjA0NzIwNCAyMjMuMjk2NDYgCkwgMTE2Ljc4MTA2MSAyMjUuNjY0MzkgCkwgMTE3LjUzOTM4IDIyNy41OTE4NDIgCkwgMTE4LjI3MzIzNiAyMjMuNTEyMDQ3IApMIDExOS4wMzE1NTUgMjI1LjE4MjIyOSAKTCAxMTkuNzg5ODczIDIyNi4zMTAyNzggCkwgMTIwLjQ5OTI2OCAyMjguNjQxNTk0IApMIDEyMS4yNTc1ODYgMjI5LjA3ODcxNCAKTCAxMjEuOTkxNDQzIDIyNC41MDMyNiAKTCAxMjIuNzQ5NzYyIDIyMS45MDIyMjMgCkwgMTIzLjQ4MzYxOCAyMTkuODU3ODMyIApMIDEyNS4wMDAyNTUgMjIzLjYxMjA2IApMIDEyNS43MzQxMTIgMjIzLjcyODYxNCAKTCAxMjYuNDkyNDMgMjI1LjIzNTkwNyAKTCAxMjcuMjI2Mjg3IDIyMy45NzU3NDQgCkwgMTI3Ljk4NDYwNSAyMjQuNDAxNDY0IApMIDEyOC43NDI5MjQgMjI0LjA4MzU1NSAKTCAxMzAuMTg2MTc1IDIyMi44NTkzMDUgCkwgMTMwLjkyMDAzMiAyMjEuOTE0MTgzIApMIDEzMS42NzgzNSAyMjAuMDczNjY0IApMIDEzMi40MTIyMDcgMjE5LjgwNTU1MyAKTCAxMzMuMTcwNTI1IDIxNy43MTMzNTggCkwgMTMzLjkyODg0NCAyMTcuNzEzMzU4IApMIDEzNC42NjI3IDIxOS40Mjc5ODYgCkwgMTM1LjQyMTAxOSAyMTcuODk0MjIxIApMIDEzNi4xNTQ4NzYgMjEzLjE5MjQyMiAKTCAxMzYuOTEzMTk0IDIxMy42Mjc1ODMgCkwgMTM3LjY3MTUxMyAyMTEuMTg3ODYxIApMIDEzOC4zNTY0NDUgMjA5LjY2NzQ1NCAKTCAxMzkuMTE0NzY0IDIwOC4zNzU1MzggCkwgMTM5Ljg0ODYyMSAyMDYuMjA1MDEyIApMIDE0MC42MDY5MzkgMjA3LjExMzMxMiAKTCAxNDEuMzQwNzk2IDIwNi4xMDYxODggCkwgMTQyLjA5OTExNCAyMDYuMzM5MzMgCkwgMTQyLjg1NzQzMyAyMDAuNDcxOTYxIApMIDE0My41OTEyODkgMTk5LjkwOTIzIApMIDE0NC4zNDk2MDggMTk5LjA5NTk3OCAKTCAxNDUuMDgzNDY0IDE5Ny41MDY0MzYgCkwgMTQ1Ljg0MTc4MyAxOTUuNDUzODYyIApMIDE0Ni42MDAxMDEgMTk1LjYzNzkwNyAKTCAxNDcuMjg1MDM0IDE5NC4zNDI3MzkgCkwgMTQ4LjA0MzM1MyAxOTUuNjI3MzQ2IApMIDE0OC43NzcyMDkgMTkzLjkxNjg4IApMIDE0OS41MzU1MjggMTkyLjgyOTc0NiAKTCAxNTAuMjY5Mzg0IDE5NS4zMjUwNjkgCkwgMTUxLjAyNzcwMyAxOTMuMTg4MDQ0IApMIDE1MS43ODYwMjEgMTkyLjI3MjYxIApMIDE1Mi41MTk4NzggMTg5LjczOTEgCkwgMTU0LjAxMjA1MyAxODYuNDA2NzggCkwgMTU0Ljc3MDM3MiAxODcuMzA4MjI1IApMIDE1NS41Mjg2OSAxODcuNjM1MDUxIApMIDE1Ni4yMzgwODUgMTg2Ljk3NTI0NSAKTCAxNTYuOTk2NDAzIDE4OC4yMzgwMzEgCkwgMTU3LjczMDI2IDE4Ny44OTM1MTEgCkwgMTU4LjQ4ODU3OCAxODcuMzgxNzY2IApMIDE1OS4yMjI0MzUgMTg4LjE4ODc1OSAKTCAxNjAuNzM5MDcyIDE4My43MzgyNTIgCkwgMTYxLjQ3MjkyOSAxODMuNTUwOTIgCkwgMTYyLjIzMTI0NyAxODEuODAyNDQxIApMIDE2Mi45NjUxMDQgMTgxLjE5NjkwOCAKTCAxNjMuNzIzNDIyIDE4MS4xMzczOSAKTCAxNjQuNDgxNzQxIDE4MC42ODEyODIgCkwgMTY1LjE2NjY3NCAxNzkuNjMwNjkxIApMIDE2NS45MjQ5OTIgMTc3LjY3ODIzNSAKTCAxNjYuNjU4ODQ5IDE3Ni45NzMyMTMgCkwgMTY3LjQxNzE2NyAxNzUuMzE0NTcxIApMIDE2OC4xNTEwMjQgMTc0LjczMzkzNyAKTCAxNjguOTA5MzQyIDE3Ny45MTI5ODUgCkwgMTY5LjY2NzY2MSAxNzcuMDM4NzQ2IApMIDE3MC40MDE1MTcgMTc4LjQwMzM5OSAKTCAxNzEuMTU5ODM2IDE3NS4zNzU3MzMgCkwgMTcxLjg5MzY5MiAxNzMuNTY0NTU0IApMIDE3Mi42NTIwMTEgMTcyLjcxNjgyMiAKTCAxNzMuNDEwMzI5IDE3MC43Mzc0MDQgCkwgMTc0LjA5NTI2MiAxNjcuNjE1MTExIApMIDE3NC44NTM1ODEgMTY2LjE3MDQ4MyAKTCAxNzUuNTg3NDM3IDE2Ni4yODI1NjEgCkwgMTc2LjM0NTc1NiAxNjQuNTk1OTA4IApMIDE3Ny4wNzk2MTIgMTYwLjk5MTY5OSAKTCAxNzguNTk2MjQ5IDE1NS44NDY2MjYgCkwgMTc5LjMzMDEwNiAxNTkuMDMxNTg1IApMIDE4MC4wODg0MjUgMTU3Ljc4NjEwOSAKTCAxODAuODIyMjgxIDE1Ny42MDEwODUgCkwgMTgxLjU4MDYgMTU5LjQ1NjMyNSAKTCAxODIuMzM4OTE4IDE1Ni40OTI3OTQgCkwgMTgzLjc4MjE3IDE1OS43NzA1NjIgCkwgMTg0LjUxNjAyNiAxNjEuNTAzNzU5IApMIDE4NS4yNzQzNDUgMTYyLjQ2OTE2NCAKTCAxODYuMDA4MjAxIDE2MS4zODM2NzMgCkwgMTg2Ljc2NjUyIDE2NC44Njk3MiAKTCAxODcuNTI0ODM4IDE2Mi4yMDc2NjEgCkwgMTg4LjI1ODY5NSAxNjMuMTI1MTkzIApMIDE4OS4wMTcwMTMgMTYzLjAwNzQ1IApMIDE4OS43NTA4NyAxNjQuMDYzNTY2IApMIDE5MC41MDkxODggMTYyLjM2OTUzNiAKTCAxOTEuMjY3NTA3IDE1OS4xOTA0ODcgCkwgMTkxLjk3NjkwMiAxNjAuNDg1NjU1IApMIDE5Mi43MzUyMiAxNjAuOTM0IApMIDE5My40NjkwNzcgMTYyLjIwNzczMSAKTCAxOTQuMjI3Mzk1IDE1OS41NjM5OTcgCkwgMTk0Ljk2MTI1MiAxNjAuMzQ2MDU2IApMIDE5NS43MTk1NyAxNjAuMjI5NTAzIApMIDE5Ni40Nzc4ODkgMTYwLjIyOTUwMyAKTCAxOTcuMjExNzQ1IDE1OC44MzUzNzEgCkwgMTk3Ljk3MDA2NCAxNTguODM1MzcxIApMIDE5OC43MDM5MjEgMTU5LjE3NzA5MyAKTCAxOTkuNDYyMjM5IDE1OS4wNDM2NSAKTCAyMDAuMjIwNTU4IDE1OS4xNjA1ODggCkwgMjAwLjkwNTQ5IDE1OS4wNDMyMyAKTCAyMDEuNjYzODA5IDE1OS43MjYyNTYgCkwgMjAyLjM5NzY2NSAxNTkuMjM4ODg1IApMIDIwMy4xNTU5ODQgMTU3LjkxNyAKTCAyMDMuODg5ODQxIDE1Ny4wODc5MDYgCkwgMjA0LjY0ODE1OSAxNTQuMzE4MDM3IApMIDIwNS40MDY0NzggMTU1LjM4NzQ0MSAKTCAyMDYuMTQwMzM0IDE1NC43MDc5MTIgCkwgMjA2Ljg5ODY1MyAxNTQuOTI4NTM1IApMIDIwNy42MzI1MDkgMTUzLjE1MjI5MSAKTCAyMDguMzkwODI4IDE1Mi4wNjIwMSAKTCAyMDkuMTQ5MTQ2IDE1My41MjM0MjMgCkwgMjEwLjU5MjM5OCAxNTMuNzA2NjY0IApMIDIxMS4zMjYyNTQgMTU1LjYwNTk2NiAKTCAyMTIuMDg0NTczIDE1My44MzM4NDggCkwgMjEyLjgxODQyOSAxNTMuNDYwNTQ4IApMIDIxMy41NzY3NDggMTU0LjE0MTc5IApMIDIxNC4zMzUwNjYgMTU1Ljc2MjkwOSAKTCAyMTUuMDY4OTIzIDE1Ni4zMzExNjUgCkwgMjE1LjgyNzI0MSAxNTQuMzExMjUyIApMIDIxNi41NjEwOTggMTUzLjU5NTE0NiAKTCAyMTguMDc3NzM1IDE1My4wODY3MjMgCkwgMjE4Ljc2MjY2OCAxNTEuMzIwNTg1IApMIDIxOS41MjA5ODYgMTUwLjM4ODA1MSAKTCAyMjAuMjU0ODQzIDE1MC40OTk0MjkgCkwgMjIxLjAxMzE2MSAxNTAuMDUyNTE4IApMIDIyMS43NDcwMTggMTUwLjIzNzg1NyAKTCAyMjIuNTA1MzM3IDE0OC44Nzk4MTQgCkwgMjIzLjI2MzY1NSAxNDguMDA4MzAyIApMIDIyMy45OTc1MTIgMTQ1LjIxMDczNiAKTCAyMjQuNzU1ODMgMTQ1LjQxMTE0NyAKTCAyMjUuNDg5Njg3IDE0NC4zMDI2MTEgCkwgMjI2LjI0ODAwNSAxNDMuODcyOCAKTCAyMjcuMDA2MzI0IDE0NS4xNDk3ODQgCkwgMjI3LjcxNTcxOCAxNDQuNzQxOTY5IApMIDIyOC40NzQwMzcgMTQ1LjQwNzA5IApMIDIyOS4yMDc4OTQgMTQ0Ljc3ODg5NyAKTCAyMjkuOTY2MjEyIDE0Mi44MjQ3MjcgCkwgMjMwLjcwMDA2OSAxNDIuODgzMTYyIApMIDIzMS40NTgzODcgMTQwLjY5NzU2MyAKTCAyMzIuMjE2NzA2IDEzOS41NzU1MyAKTCAyMzMuNzA4ODgxIDE0MC4yNzM2NjIgCkwgMjM0LjQ0MjczNyAxMzkuNjE1NjQgCkwgMjM1LjIwMTA1NiAxMzguNjQ4NjYxIApMIDIzNS45NTkzNzQgMTM4LjAwOTUyMiAKTCAyMzYuNjQ0MzA3IDEzNi4xMjY1NTEgCkwgMjM3LjQwMjYyNiAxMzUuNzQ1MzgzIApMIDIzOC4xMzY0ODIgMTM1LjE0Njg3OCAKTCAyMzguODk0ODAxIDEzNC44OTQ2NzggCkwgMjQwLjM4Njk3NiAxMzIuOTQ4MDI3IApMIDI0MS4xNDUyOTQgMTMyLjYyNzIxNiAKTCAyNDEuODc5MTUxIDEzMS42MjkwMDkgCkwgMjQyLjYzNzQ3IDEzMi4wMjEwNTMgCkwgMjQzLjM3MTMyNiAxMzMuODQ0ODU2IApMIDI0NC4xMjk2NDUgMTMyLjc5NDA5MSAKTCAyNDQuODg3OTYzIDEzNC43NzM1MDggCkwgMjQ2LjMzMTIxNCAxMzcuMzk2MjI2IApMIDI0Ny4wNjUwNzEgMTM2LjA1MTIyNiAKTCAyNDcuODIzMzkgMTM5LjU2NjY4MiAKTCAyNDguNTU3MjQ2IDEzOS4zMDMzOTcgCkwgMjQ5LjMxNTU2NSAxMzguMjYyNjMyIApMIDI1MC4wNzM4ODMgMTM2Ljg0NzY5MyAKTCAyNTAuODA3NzQgMTM5LjkwMTY5MSAKTCAyNTEuNTY2MDU4IDEzOC44MTU2NzYgCkwgMjUyLjI5OTkxNSAxMzcuMTMwMzg3IApMIDI1My4wNTgyMzMgMTM2LjQ3MTE3NiAKTCAyNTMuODE2NTUyIDEzMi44NTM2NDQgCkwgMjU1LjI1OTgwMyAxMzQuMjc0MTA4IApMIDI1NS45OTM2NiAxMzIuOTIxNjk1IApMIDI1Ni43NTE5NzggMTMwLjg3NTU5IApMIDI1Ny40ODU4MzUgMTMyLjIzMjIgCkwgMjU4LjI0NDE1MyAxMzEuNDg4MTUyIApMIDI1OS4wMDI0NzIgMTMwLjk0MTc1MiAKTCAyNTkuNzM2MzI5IDEyOC43Mzk1NzkgCkwgMjYwLjQ5NDY0NyAxMjcuNTM5NjMzIApMIDI2Mi43NDUxNDEgMTIyLjA5OTQ1MSAKTCAyNjMuNDU0NTM1IDEyMy4zOTk5NyAKTCAyNjQuMjEyODU0IDEyMS4zOTQ4NSAKTCAyNjQuOTQ2NzEgMTIyLjY5MDAxOCAKTCAyNjUuNzA1MDI5IDEyMi41NDA1NTggCkwgMjY2LjQzODg4NiAxMjAuMjU0ODc3IApMIDI2Ny4xOTcyMDQgMTIyLjA5NTM5NSAKTCAyNjcuOTU1NTIzIDEyMS42NDcwNSAKTCAyNjguNjg5Mzc5IDEyMS44ODkwNCAKTCAyNjkuNDQ3Njk4IDEyMC44MzM5MzggCkwgMjcwLjkzOTg3MyAxMTkuNzUzNjU4IApMIDI3MS42OTgxOTEgMTE5LjQ2NTg1OCAKTCAyNzIuMzgzMTI0IDExOS40NjU4NTggCkwgMjczLjE0MTQ0MyAxMjAuMTE2NzEyIApMIDI3My44NzUyOTkgMTI0LjEwMDU4NSAKTCAyNzQuNjMzNjE4IDEyNC4yNjcxMSAKTCAyNzUuMzY3NDc0IDEyMi45Mzg2MTYgCkwgMjc2LjEyNTc5MyAxMTkuNDk4OTc0IApMIDI3Ni44ODQxMTEgMTE5Ljc5NzIzIApMIDI3Ny42MTc5NjggMTE3Ljg1MDk2MyAKTCAyNzguMzc2Mjg2IDEyMC4xNjMwMTEgCkwgMjc5Ljg2ODQ2MiAxMTQuNTkwMjYxIApMIDI4MC42MjY3OCAxMTYuNjA3NzI1IApMIDI4MS4zMTE3MTMgMTE2LjY3OTA5OCAKTCAyODIuMDcwMDMxIDExMi43NTQ0OTggCkwgMjgzLjU2MjIwNiAxMTguNzQxMTQ5IApMIDI4NC4yOTYwNjMgMTE1LjYzNTE1MSAKTCAyODUuMDU0MzgyIDExOC45NzI1MDcgCkwgMjg1LjgxMjcgMTE5Ljc3NDU2OSAKTCAyODYuNTQ2NTU3IDExMi43MjQ4NDQgCkwgMjg3LjMwNDg3NSAxMTMuNjI1MDY1IApMIDI4OC4wMzg3MzIgMTEwLjE0MjM0MSAKTCAyODguNzk3MDUgMTA4Ljk4NjU5NyAKTCAyODkuNTU1MzY5IDExMS45MDA3MTYgCkwgMjkwLjI0MDMwMiAxMTQuMDQzMTI3IApMIDI5MC45OTg2MiAxMTMuNzU3NDk1IApMIDI5MS43MzI0NzcgMTA4LjM0OTA2NiAKTCAyOTIuNDkwNzk1IDEwNy41MTQ5MzcgCkwgMjkzLjIyNDY1MiAxMDkuOTAzODgzIApMIDI5My45ODI5NyAxMDguMDYzMzY1IApMIDI5NC43NDEyODkgMTA4LjA2MzM2NSAKTCAyOTUuNDc1MTQ1IDEwOS41NjA1ODcgCkwgMjk2LjIzMzQ2NCAxMDkuNjI5MTYyIApMIDI5Ni45NjczMjEgMTEyLjcyMDc4NyAKTCAyOTcuNzI1NjM5IDExNC42ODkzMjkgCkwgMjk4LjQ4Mzk1NyAxMTQuMDQwMjU5IApMIDI5OS4xOTMzNTIgMTE1Ljg3MjM4NSAKTCAyOTkuOTUxNjcxIDExMy4wMjQzOTMgCkwgMzAwLjY4NTUyNyAxMDkuNjMwMDcyIApMIDMwMS40NDM4NDYgMTA4LjgzODU3IApMIDMwMi4xNzc3MDIgMTEyLjUwNTc5NCAKTCAzMDMuNjk0MzM5IDEwMi4zODA1MyAKTCAzMDUuMTg2NTE1IDk3LjE4ODk4MiAKTCAzMDUuOTIwMzcxIDk2LjQ5NDk0MSAKTCAzMDYuNjc4NjkgOTAuNzQyNzYxIApMIDMwNy40MzcwMDggOTIuNTk4NzM2IApMIDMwOC4xMjE5NDEgOTEuMjAzOTQgCkwgMzA4Ljg4MDI1OSA5MS43NjQwNDggCkwgMzA5LjYxNDExNiA4OC4wNTk5NjYgCkwgMzEwLjM3MjQzNSA4Ni42NjU1NTQgCkwgMzExLjEwNjI5MSA4OS42MzY2MzkgCkwgMzExLjg2NDYxIDkzLjM1NDYzOSAKTCAzMTIuNjIyOTI4IDkyLjU3NjA3NiAKTCAzMTMuMzU2Nzg1IDk4LjA4OTY1OSAKTCAzMTQuMTE1MTAzIDk4LjIzMjU3OSAKTCAzMTQuODQ4OTYgOTkuODU5MDg0IApMIDMxNS42MDcyNzggOTguMDUyOTA2IApMIDMxNi4zNjU1OTcgMTAxLjI0ODYzNSAKTCAzMTcuMDUwNTMgOTkuNDg0NzM1IApMIDMxNy44MDg4NDggOTIuMTkxNDExIApMIDMxOC41NDI3MDUgOTEuNzA5MzU1IApMIDMxOS4zMDEwMjMgOTYuNzA2MTkyIApMIDMyMC4wMzQ4OCAxMDYuMTk1NTcgCkwgMzIwLjc5MzE5OCAxMTIuNTc4MzU2IApMIDMyMS41NTE1MTcgMTEzLjI0Mjg0OCAKTCAzMjIuMjg1Mzc0IDEyNS4zMDAxNDYgCkwgMzIzLjA0MzY5MiAxNDUuMDUzOTMzIApMIDMyMy43Nzc1NDkgMTM3Ljc1MzI2NSAKTCAzMjUuMjk0MTg2IDEzMC40NjcyNSAKTCAzMjUuOTc5MTE4IDE0MC41MDAxOTUgCkwgMzI2LjczNzQzNyAxMzkuMjE1ODMzIApMIDMyNy40NzEyOTQgMTI3LjQ0NjY4NCAKTCAzMjguMjI5NjEyIDEyNS44MDM1MzMgCkwgMzI4Ljk2MzQ2OSAxMjYuNzY5MzIzIApMIDMyOS43MjE3ODcgMTI3LjUxNDI0NSAKTCAzMzAuNDgwMTA2IDEyMy4yODU3NTkgCkwgMzMxLjIxMzk2MiAxMjMuNzc2MTcyIApMIDMzMS45NzIyODEgMTE4LjI2Njc1MiAKTCAzMzIuNzA2MTM3IDExNy43MDQ4NiAKTCAzMzMuNDY0NDU2IDExMS4xNjYzNTUgCkwgMzM0LjIyMjc3NCAxMTEuNTUwMDQxIApMIDMzNC45MzIxNjkgMTA5Ljk3MDYwNSAKTCAzMzUuNjkwNDg4IDEwOC41OTE5NjUgCkwgMzM2LjQyNDM0NCAxMDguNDEzNDEgCkwgMzM3LjE4MjY2MyAxMDcuMjIwNzAzIApMIDMzNy45MTY1MTkgMTA0LjM3NDA0IApMIDMzOC42NzQ4MzggMTA1LjY2NzUzIApMIDMzOS40MzMxNTYgMTA2LjAyMTAwMiAKTCAzNDAuMTY3MDEzIDEwMi45OTc3NzggCkwgMzQwLjkyNTMzMSA5Ny44NDg3NTMgCkwgMzQxLjY1OTE4OCA5Ni4yNjM1ODMgCkwgMzQyLjQxNzUwNiA5NS4yMjIxNTQgCkwgMzQzLjE3NTgyNSA5NS44Nzg2MDMgCkwgMzQzLjg2MDc1OCA5Ni42MTk5NTcgCkwgMzQ0LjYxOTA3NiA5My40MjQxMjMgCkwgMzQ1LjM1MjkzMyA4Ny4wMjYwMjEgCkwgMzQ2LjExMTI1MSA4Ny4zOTgwMjcgCkwgMzQ2Ljg0NTEwOCA4NS44OTM5NTEgCkwgMzQ3LjYwMzQyNyA4MS4zNDU5NDggCkwgMzQ4LjM2MTc0NSA3OS4zMDkxMSAKTCAzNDkuMDk1NjAyIDc4LjY1OTc5NSAKTCAzNDkuODUzOTIgODEuNDYwMDg5IApMIDM1MC41ODc3NzcgODEuOTkyMTg2IApMIDM1MS4zNDYwOTUgNzcuMTkyMTkyIApMIDM1Mi4xMDQ0MTQgNzMuNzIyODYxIApMIDM1Mi43ODkzNDcgNzIuNzQ3ODc1IApMIDM1My41NDc2NjUgNzQuNjE1NjY5IApMIDM1NC4yODE1MjIgNzIuNzc2Nzk1IApMIDM1NS4wMzk4NCA3MS45NTIzNTIgCkwgMzU1Ljc3MzY5NyA3MS4zNzcwMzMgCkwgMzU2LjUzMjAxNSA2Ny42MjI1NTkgCkwgMzU3LjI5MDMzNCA2Ny4wMzQ3NTYgCkwgMzU4LjAyNDE5IDY4LjM1MDEwMSAKTCAzNTguNzgyNTA5IDY1Ljg2MDM3MyAKTCAzNjAuMjc0Njg0IDYzLjU1NzYyNyAKTCAzNjEuNzE3OTM1IDYyLjYwNDM5MSAKTCAzNjIuNDc2MjU0IDYxLjE0MzkyMiAKTCAzNjMuMjEwMTEgNTguMDY5Njc3IApMIDM2My45Njg0MjkgNTguMTE1NDUyIApMIDM2NC43MDIyODYgNTkuMTk2MTg3IApMIDM2NS40NjA2MDQgNTguODY1MDI1IApMIDM2Ni4yMTg5MjMgNTkuMjgwMTQ5IApMIDM2Ni45NTI3NzkgNTguODM5NzQyIApMIDM2Ny43MTEwOTggNTMuMjE4OTA4IApMIDM2OC40NDQ5NTQgNTMuMDgwNTY4IApMIDM2OS4yMDMyNzMgNTEuNDM0MjcxIApMIDM2OS45NjE1OTEgNTYuMjk0MDYyIApMIDM3MC42NzA5ODYgNTguOTExODQ5IApMIDM3MS40MjkzMDQgNTguOTI1NjYyIApMIDM3Mi4xNjMxNjEgNTYuNjQwNTA2IApMIDM3Mi45MjE0OCA1Ni4wMjMwMTMgCkwgMzczLjY1NTMzNiA1OC44OTA4MzIgCkwgMzc0LjQxMzY1NSA2MC4wODQxNjkgCkwgMzc1LjE3MTk3MyA2Mi4zMDIyODkgCkwgMzc2LjY2NDE0OCA3NS4wODU5NzUgCkwgMzc3LjM5ODAwNSA2OS4xNzA3MzIgCkwgMzc4LjE1NjMyMyA3MC40MDA4NTcgCkwgMzc4LjkxNDY0MiA3MS4wNDExODUgCkwgMzc5LjU5OTU3NSA4MS4xNDA3MTIgCkwgMzgwLjM1Nzg5MyA4MS42MTQwNiAKTCAzODEuMDkxNzUgNzcuNDYzNTkxIApMIDM4MS44NTAwNjggNzguNzA0ODAxIApMIDM4Mi41ODM5MjUgNzcuNTg1Nzc1IApMIDM4My4zNDIyNDMgNzguMTg1NjQzIApMIDM4NC4xMDA1NjIgNzYuNTIxMDkxIApMIDM4NC44MzQ0MTggNzYuMTc2ODE2IApMIDM4NS41OTI3MzcgODEuMDU1NjY2IApMIDM4Ni4zMjY1OTQgODIuMzQyODk2IApMIDM4Ny4wODQ5MTIgNzkuNzE3OCAKTCAzODcuODQzMjMxIDgzLjQ4NTgwNiAKTCAzODguNTI4MTYzIDgwLjY0ODE2NSAKTCAzODkuMjg2NDgyIDc5Ljg3NjIxMiAKTCAzOTAuNzc4NjU3IDgzLjg1MDQ2OSAKTCAzOTEuNTEyNTE0IDgzLjIxODA3OSAKTCAzOTIuMjcwODMyIDc5LjYzMzIwOCAKTCAzOTMuMDI5MTUxIDgwLjAxNjY1IApMIDM5My43NjMwMDcgNzYuNzI5MDU1IApMIDM5NC41MjEzMjYgNzguNjExNjA3IApMIDM5Ni43NzE4MTkgNzYuMzg5OTU2IApMIDM5Ni43NzE4MTkgNzYuMzg5OTU2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiM0YzcyYjA7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7c3Ryb2tlLXdpZHRoOjEuNzU7Ij48L3BhdGg+CiAgIDwvZz4KICAgPGcgaWQ9InBhdGNoXzMiPgogICAgPHBhdGggZD0iTSA1OS4wNCAyNTQuNTkzOTU1IApMIDU5LjA0IDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7Ij48L3BhdGg+CiAgIDwvZz4KICAgPGcgaWQ9InBhdGNoXzQiPgogICAgPHBhdGggZD0iTSA0MTIuODU0Mjg3IDI1NC41OTM5NTUgCkwgNDEyLjg1NDI4NyA0MS43NiAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF81Ij4KICAgIDxwYXRoIGQ9Ik0gNTkuMDQgMjU0LjU5Mzk1NSAKTCA0MTIuODU0Mjg3IDI1NC41OTM5NTUgCiIgc3R5bGU9ImZpbGw6bm9uZTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0icGF0Y2hfNiI+CiAgICA8cGF0aCBkPSJNIDU5LjA0IDQxLjc2IApMIDQxMi44NTQyODcgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0ibGVnZW5kXzEiPgogICAgPGcgaWQ9InBhdGNoXzciPgogICAgIDxwYXRoIGQ9Ik0gNjcuNDQgNjguMzcgCkwgMTg2LjU1Njg3NSA2OC4zNyAKUSAxODguOTU2ODc1IDY4LjM3IDE4OC45NTY4NzUgNjUuOTcgCkwgMTg4Ljk1Njg3NSA1MC4xNiAKUSAxODguOTU2ODc1IDQ3Ljc2IDE4Ni41NTY4NzUgNDcuNzYgCkwgNjcuNDQgNDcuNzYgClEgNjUuMDQgNDcuNzYgNjUuMDQgNTAuMTYgCkwgNjUuMDQgNjUuOTcgClEgNjUuMDQgNjguMzcgNjcuNDQgNjguMzcgCnoKIiBzdHlsZT0iZmlsbDojZWFlYWYyO29wYWNpdHk6MC44O3N0cm9rZTojY2NjY2NjO3N0cm9rZS1saW5lam9pbjptaXRlcjtzdHJva2Utd2lkdGg6MC4zOyI+PC9wYXRoPgogICAgPC9nPgogICAgPGcgaWQ9ImxpbmUyZF8zNiI+CiAgICAgPHBhdGggZD0iTSA2OS44NCA1Ni45ODUgCkwgOTMuODQgNTYuOTg1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiM0YzcyYjA7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7c3Ryb2tlLXdpZHRoOjEuNzU7Ij48L3BhdGg+CiAgICA8L2c+CiAgICA8ZyBpZD0ibGluZTJkXzM3Ij48L2c+CiAgICA8ZyBpZD0idGV4dF8xOCI+CiAgICAgPCEtLSBwZXJtbm86IDEwMTM3IC0tPgogICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMDMuNDQgNjEuMTg1KXNjYWxlKDAuMTIgLTAuMTIpIj4KICAgICAgPGRlZnM+CiAgICAgICA8cGF0aCBkPSJNIDYuNTkzNzUgLTE5Ljg3NSAKTCA2LjU5Mzc1IDUxLjg1OTM3NSAKTCAxNC41OTM3NSA1MS44NTkzNzUgCkwgMTQuNTkzNzUgNDUuMTI1IApRIDE3LjQzNzUgNDkuMDc4MTI1IDIxIDUxLjA0Njg3NSAKUSAyNC41NjI1IDUzLjAzMTI1IDI5LjY0MDYyNSA1My4wMzEyNSAKUSAzNi4yODEyNSA1My4wMzEyNSA0MS4zNTkzNzUgNDkuNjA5Mzc1IApRIDQ2LjQzNzUgNDYuMTg3NSA0OS4wMTU2MjUgMzkuOTUzMTI1IApRIDUxLjYwOTM3NSAzMy43MzQzNzUgNTEuNjA5Mzc1IDI2LjMxMjUgClEgNTEuNjA5Mzc1IDE4LjM1OTM3NSA0OC43NSAxMS45ODQzNzUgClEgNDUuOTA2MjUgNS42MDkzNzUgNDAuNDUzMTI1IDIuMjE4NzUgClEgMzUuMDE1NjI1IC0xLjE3MTg3NSAyOSAtMS4xNzE4NzUgClEgMjQuNjA5Mzc1IC0xLjE3MTg3NSAyMS4xMDkzNzUgMC42ODc1IApRIDE3LjYyNSAyLjU0Njg3NSAxNS4zNzUgNS4zNzUgCkwgMTUuMzc1IC0xOS44NzUgCnoKTSAxNC41NDY4NzUgMjUuNjQwNjI1IApRIDE0LjU0Njg3NSAxNS42MjUgMTguNTkzNzUgMTAuODQzNzUgClEgMjIuNjU2MjUgNi4wNjI1IDI4LjQyMTg3NSA2LjA2MjUgClEgMzQuMjgxMjUgNi4wNjI1IDM4LjQ1MzEyNSAxMS4wMTU2MjUgClEgNDIuNjI1IDE1Ljk2ODc1IDQyLjYyNSAyNi4zNzUgClEgNDIuNjI1IDM2LjI4MTI1IDM4LjU0Njg3NSA0MS4yMDMxMjUgClEgMzQuNDY4NzUgNDYuMTQwNjI1IDI4LjgxMjUgNDYuMTQwNjI1IApRIDIzLjE4NzUgNDYuMTQwNjI1IDE4Ljg1OTM3NSA0MC44OTA2MjUgClEgMTQuNTQ2ODc1IDM1LjY0MDYyNSAxNC41NDY4NzUgMjUuNjQwNjI1IAp6CiIgaWQ9IkFyaWFsTVQtMTEyIj48L3BhdGg+CiAgICAgICA8cGF0aCBkPSJNIDQyLjA5Mzc1IDE2LjcwMzEyNSAKTCA1MS4xNzE4NzUgMTUuNTc4MTI1IApRIDQ5LjAzMTI1IDcuNjI1IDQzLjIxODc1IDMuMjE4NzUgClEgMzcuNDA2MjUgLTEuMTcxODc1IDI4LjM3NSAtMS4xNzE4NzUgClEgMTcgLTEuMTcxODc1IDEwLjMyODEyNSA1LjgyODEyNSAKUSAzLjY1NjI1IDEyLjg0Mzc1IDMuNjU2MjUgMjUuNDg0Mzc1IApRIDMuNjU2MjUgMzguNTc4MTI1IDEwLjM5MDYyNSA0NS43OTY4NzUgClEgMTcuMTQwNjI1IDUzLjAzMTI1IDI3Ljg3NSA1My4wMzEyNSAKUSAzOC4yODEyNSA1My4wMzEyNSA0NC44NzUgNDUuOTUzMTI1IApRIDUxLjQ2ODc1IDM4Ljg3NSA1MS40Njg3NSAyNi4wMzEyNSAKUSA1MS40Njg3NSAyNS4yNSA1MS40MjE4NzUgMjMuNjg3NSAKTCAxMi43NSAyMy42ODc1IApRIDEzLjIzNDM3NSAxNS4xNDA2MjUgMTcuNTc4MTI1IDEwLjU5Mzc1IApRIDIxLjkyMTg3NSA2LjA2MjUgMjguNDIxODc1IDYuMDYyNSAKUSAzMy4yNSA2LjA2MjUgMzYuNjcxODc1IDguNTkzNzUgClEgNDAuMDkzNzUgMTEuMTQwNjI1IDQyLjA5Mzc1IDE2LjcwMzEyNSAKegpNIDEzLjIzNDM3NSAzMC45MDYyNSAKTCA0Mi4xODc1IDMwLjkwNjI1IApRIDQxLjYwOTM3NSAzNy40NTMxMjUgMzguODc1IDQwLjcxODc1IApRIDM0LjY3MTg3NSA0NS43OTY4NzUgMjcuOTg0Mzc1IDQ1Ljc5Njg3NSAKUSAyMS45MjE4NzUgNDUuNzk2ODc1IDE3Ljc5Njg3NSA0MS43NSAKUSAxMy42NzE4NzUgMzcuNzAzMTI1IDEzLjIzNDM3NSAzMC45MDYyNSAKegoiIGlkPSJBcmlhbE1ULTEwMSI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSA2LjUgMCAKTCA2LjUgNTEuODU5Mzc1IApMIDE0LjQwNjI1IDUxLjg1OTM3NSAKTCAxNC40MDYyNSA0NCAKUSAxNy40Mzc1IDQ5LjUxNTYyNSAyMCA1MS4yNjU2MjUgClEgMjIuNTYyNSA1My4wMzEyNSAyNS42NDA2MjUgNTMuMDMxMjUgClEgMzAuMDc4MTI1IDUzLjAzMTI1IDM0LjY3MTg3NSA1MC4yMDMxMjUgCkwgMzEuNjQwNjI1IDQyLjA0Njg3NSAKUSAyOC40MjE4NzUgNDMuOTUzMTI1IDI1LjIwMzEyNSA0My45NTMxMjUgClEgMjIuMzEyNSA0My45NTMxMjUgMjAuMDE1NjI1IDQyLjIxODc1IApRIDE3LjcxODc1IDQwLjQ4NDM3NSAxNi43NSAzNy40MDYyNSAKUSAxNS4yODEyNSAzMi43MTg3NSAxNS4yODEyNSAyNy4xNTYyNSAKTCAxNS4yODEyNSAwIAp6CiIgaWQ9IkFyaWFsTVQtMTE0Ij48L3BhdGg+CiAgICAgICA8cGF0aCBkPSJNIDYuNTkzNzUgMCAKTCA2LjU5Mzc1IDUxLjg1OTM3NSAKTCAxNC40NTMxMjUgNTEuODU5Mzc1IApMIDE0LjQ1MzEyNSA0NC41NzgxMjUgClEgMTYuODkwNjI1IDQ4LjM5MDYyNSAyMC45Mzc1IDUwLjcwMzEyNSAKUSAyNSA1My4wMzEyNSAzMC4xNzE4NzUgNTMuMDMxMjUgClEgMzUuOTM3NSA1My4wMzEyNSAzOS42MjUgNTAuNjQwNjI1IApRIDQzLjMxMjUgNDguMjUgNDQuODI4MTI1IDQzLjk1MzEyNSAKUSA1MC45ODQzNzUgNTMuMDMxMjUgNjAuODQzNzUgNTMuMDMxMjUgClEgNjguNTYyNSA1My4wMzEyNSA3Mi43MDMxMjUgNDguNzUgClEgNzYuODU5Mzc1IDQ0LjQ4NDM3NSA3Ni44NTkzNzUgMzUuNTkzNzUgCkwgNzYuODU5Mzc1IDAgCkwgNjguMTA5Mzc1IDAgCkwgNjguMTA5Mzc1IDMyLjY3MTg3NSAKUSA2OC4xMDkzNzUgMzcuOTM3NSA2Ny4yNSA0MC4yNSAKUSA2Ni40MDYyNSA0Mi41NzgxMjUgNjQuMTU2MjUgNDMuOTg0Mzc1IApRIDYxLjkyMTg3NSA0NS40MDYyNSA1OC44OTA2MjUgNDUuNDA2MjUgClEgNTMuNDIxODc1IDQ1LjQwNjI1IDQ5Ljc5Njg3NSA0MS43NjU2MjUgClEgNDYuMTg3NSAzOC4xNDA2MjUgNDYuMTg3NSAzMC4xMjUgCkwgNDYuMTg3NSAwIApMIDM3LjQwNjI1IDAgCkwgMzcuNDA2MjUgMzMuNjg3NSAKUSAzNy40MDYyNSAzOS41NDY4NzUgMzUuMjUgNDIuNDY4NzUgClEgMzMuMTA5Mzc1IDQ1LjQwNjI1IDI4LjIxODc1IDQ1LjQwNjI1IApRIDI0LjUxNTYyNSA0NS40MDYyNSAyMS4zNTkzNzUgNDMuNDUzMTI1IApRIDE4LjIxODc1IDQxLjUgMTYuNzk2ODc1IDM3LjczNDM3NSAKUSAxNS4zNzUgMzMuOTg0Mzc1IDE1LjM3NSAyNi45MDYyNSAKTCAxNS4zNzUgMCAKegoiIGlkPSJBcmlhbE1ULTEwOSI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSA2LjU5Mzc1IDAgCkwgNi41OTM3NSA1MS44NTkzNzUgCkwgMTQuNSA1MS44NTkzNzUgCkwgMTQuNSA0NC40ODQzNzUgClEgMjAuMjE4NzUgNTMuMDMxMjUgMzEgNTMuMDMxMjUgClEgMzUuNjg3NSA1My4wMzEyNSAzOS42MjUgNTEuMzQzNzUgClEgNDMuNTYyNSA0OS42NTYyNSA0NS41MTU2MjUgNDYuOTIxODc1IApRIDQ3LjQ2ODc1IDQ0LjE4NzUgNDguMjUgNDAuNDM3NSAKUSA0OC43MzQzNzUgMzcuOTg0Mzc1IDQ4LjczNDM3NSAzMS44OTA2MjUgCkwgNDguNzM0Mzc1IDAgCkwgMzkuOTM3NSAwIApMIDM5LjkzNzUgMzEuNTQ2ODc1IApRIDM5LjkzNzUgMzYuOTIxODc1IDM4LjkwNjI1IDM5LjU3ODEyNSAKUSAzNy44OTA2MjUgNDIuMjM0Mzc1IDM1LjI4MTI1IDQzLjgxMjUgClEgMzIuNjcxODc1IDQ1LjQwNjI1IDI5LjE1NjI1IDQ1LjQwNjI1IApRIDIzLjUzMTI1IDQ1LjQwNjI1IDE5LjQ1MzEyNSA0MS44NDM3NSAKUSAxNS4zNzUgMzguMjgxMjUgMTUuMzc1IDI4LjMyODEyNSAKTCAxNS4zNzUgMCAKegoiIGlkPSJBcmlhbE1ULTExMCI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSAzLjMyODEyNSAyNS45MjE4NzUgClEgMy4zMjgxMjUgNDAuMzI4MTI1IDExLjMyODEyNSA0Ny4yNjU2MjUgClEgMTguMDE1NjI1IDUzLjAzMTI1IDI3LjY0MDYyNSA1My4wMzEyNSAKUSAzOC4zMjgxMjUgNTMuMDMxMjUgNDUuMTA5Mzc1IDQ2LjAxNTYyNSAKUSA1MS45MDYyNSAzOS4wMTU2MjUgNTEuOTA2MjUgMjYuNjU2MjUgClEgNTEuOTA2MjUgMTYuNjU2MjUgNDguOTA2MjUgMTAuOTA2MjUgClEgNDUuOTA2MjUgNS4xNzE4NzUgNDAuMTU2MjUgMiAKUSAzNC40MjE4NzUgLTEuMTcxODc1IDI3LjY0MDYyNSAtMS4xNzE4NzUgClEgMTYuNzUgLTEuMTcxODc1IDEwLjAzMTI1IDUuODEyNSAKUSAzLjMyODEyNSAxMi43OTY4NzUgMy4zMjgxMjUgMjUuOTIxODc1IAp6Ck0gMTIuMzU5Mzc1IDI1LjkyMTg3NSAKUSAxMi4zNTkzNzUgMTUuOTY4NzUgMTYuNzAzMTI1IDExLjAxNTYyNSAKUSAyMS4wNDY4NzUgNi4wNjI1IDI3LjY0MDYyNSA2LjA2MjUgClEgMzQuMTg3NSA2LjA2MjUgMzguNTMxMjUgMTEuMDMxMjUgClEgNDIuODc1IDE2LjAxNTYyNSA0Mi44NzUgMjYuMjE4NzUgClEgNDIuODc1IDM1Ljg0Mzc1IDM4LjUgNDAuNzk2ODc1IApRIDM0LjEyNSA0NS43NSAyNy42NDA2MjUgNDUuNzUgClEgMjEuMDQ2ODc1IDQ1Ljc1IDE2LjcwMzEyNSA0MC44MTI1IApRIDEyLjM1OTM3NSAzNS44OTA2MjUgMTIuMzU5Mzc1IDI1LjkyMTg3NSAKegoiIGlkPSJBcmlhbE1ULTExMSI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSA5LjAzMTI1IDQxLjg0Mzc1IApMIDkuMDMxMjUgNTEuODU5Mzc1IApMIDE5LjA0Njg3NSA1MS44NTkzNzUgCkwgMTkuMDQ2ODc1IDQxLjg0Mzc1IAp6Ck0gOS4wMzEyNSAwIApMIDkuMDMxMjUgMTAuMDE1NjI1IApMIDE5LjA0Njg3NSAxMC4wMTU2MjUgCkwgMTkuMDQ2ODc1IDAgCnoKIiBpZD0iQXJpYWxNVC01OCI+PC9wYXRoPgogICAgICAgPHBhdGggaWQ9IkFyaWFsTVQtMzIiPjwvcGF0aD4KICAgICAgPC9kZWZzPgogICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMiI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTQ0LjUzMTI1IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDkiPjwvdXNlPgogICAgICA8dXNlIHg9IjIyNy44MzIwMzEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjgzLjQ0NzI2NiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTExIj48L3VzZT4KICAgICAgPHVzZSB4PSIzMzkuMDYyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTgiPjwvdXNlPgogICAgICA8dXNlIHg9IjM2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgICAgPHVzZSB4PSIzOTQuNjI4OTA2IiB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgIDx1c2UgeD0iNDUwLjI0NDE0MSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8dXNlIHg9IjUwNS44NTkzNzUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPHVzZSB4PSI1NjEuNDc0NjA5IiB4bGluazpocmVmPSIjQXJpYWxNVC01MSI+PC91c2U+CiAgICAgIDx1c2UgeD0iNjE3LjA4OTg0NCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTUiPjwvdXNlPgogICAgIDwvZz4KICAgIDwvZz4KICAgPC9nPgogIDwvZz4KICA8ZyBpZD0iYXhlc18yIj4KICAgPGcgaWQ9InBhdGNoXzgiPgogICAgPHBhdGggZD0iTSA0MzcuNDY1NzEzIDI1NC41OTM5NTUgCkwgNzkxLjI4IDI1NC41OTM5NTUgCkwgNzkxLjI4IDQxLjc2IApMIDQzNy40NjU3MTMgNDEuNzYgCnoKIiBzdHlsZT0iZmlsbDojZWFlYWYyOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJtYXRwbG90bGliLmF4aXNfMyI+CiAgICA8ZyBpZD0ieHRpY2tfMTEiPgogICAgIDxnIGlkPSJsaW5lMmRfMzgiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGYyNmYwOTU0YzgpIiBkPSJNIDQ2MC4xNzE1NTEgMjU0LjU5Mzk1NSAKTCA0NjAuMTcxNTUxIDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMzkiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xOSI+CiAgICAgIDwhLS0gMTk5MiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ0OS4wNDk2NzYgMjY4Ljc1MTc2OClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTciPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja18xMiI+CiAgICAgPGcgaWQ9ImxpbmUyZF80MCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwZjI2ZjA5NTRjOCkiIGQ9Ik0gNTA1LjE3OTY2NCAyNTQuNTkzOTU1IApMIDUwNS4xNzk2NjQgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF80MSI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzIwIj4KICAgICAgPCEtLSAxOTk2IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDk0LjA1Nzc4OSAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTQiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzEzIj4KICAgICA8ZyBpZD0ibGluZTJkXzQyIj4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BmMjZmMDk1NGM4KSIgZD0iTSA1NTAuMTg3Nzc2IDI1NC41OTM5NTUgCkwgNTUwLjE4Nzc3NiA0MS43NiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzQzIj48L2c+CiAgICAgPGcgaWQ9InRleHRfMjEiPgogICAgICA8IS0tIDIwMDAgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg1MzkuMDY1OTAxIDI2OC43NTE3Njgpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMTQiPgogICAgIDxnIGlkPSJsaW5lMmRfNDQiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGYyNmYwOTU0YzgpIiBkPSJNIDU5NS4xOTU4ODkgMjU0LjU5Mzk1NSAKTCA1OTUuMTk1ODg5IDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfNDUiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8yMiI+CiAgICAgIDwhLS0gMjAwNCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDU4NC4wNzQwMTQgMjY4Ljc1MTc2OClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUyIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja18xNSI+CiAgICAgPGcgaWQ9ImxpbmUyZF80NiI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwZjI2ZjA5NTRjOCkiIGQ9Ik0gNjQwLjIwNDAwMSAyNTQuNTkzOTU1IApMIDY0MC4yMDQwMDEgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF80NyI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzIzIj4KICAgICAgPCEtLSAyMDA4IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNjI5LjA4MjEyNiAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTYiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzE2Ij4KICAgICA8ZyBpZD0ibGluZTJkXzQ4Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BmMjZmMDk1NGM4KSIgZD0iTSA2ODUuMjEyMTE0IDI1NC41OTM5NTUgCkwgNjg1LjIxMjExNCA0MS43NiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzQ5Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMjQiPgogICAgICA8IS0tIDIwMTIgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2NzQuMDkwMjM5IDI2OC43NTE3Njgpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMTciPgogICAgIDxnIGlkPSJsaW5lMmRfNTAiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGYyNmYwOTU0YzgpIiBkPSJNIDczMC4yMjAyMjYgMjU0LjU5Mzk1NSAKTCA3MzAuMjIwMjI2IDQxLjc2IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfNTEiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8yNSI+CiAgICAgIDwhLS0gMjAxNiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDcxOS4wOTgzNTEgMjY4Ljc1MTc2OClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU0Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja18xOCI+CiAgICAgPGcgaWQ9ImxpbmUyZF81MiI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwZjI2ZjA5NTRjOCkiIGQ9Ik0gNzc1LjIyODMzOSAyNTQuNTkzOTU1IApMIDc3NS4yMjgzMzkgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF81MyI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzI2Ij4KICAgICAgPCEtLSAyMDIwIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNzY0LjEwNjQ2NCAyNjguNzUxNzY4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgIDxnIGlkPSJtYXRwbG90bGliLmF4aXNfNCI+CiAgICA8ZyBpZD0ieXRpY2tfOCI+CiAgICAgPGcgaWQ9ImxpbmUyZF81NCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwZjI2ZjA5NTRjOCkiIGQ9Ik0gNDM3LjQ2NTcxMyAyMzcuNzc0NyAKTCA3OTEuMjggMjM3Ljc3NDcgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF81NSI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzI3Ij4KICAgICAgPCEtLSAwIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDI0LjkwNDc3NiAyNDEuMzUzNjA2KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja185Ij4KICAgICA8ZyBpZD0ibGluZTJkXzU2Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BmMjZmMDk1NGM4KSIgZD0iTSA0MzcuNDY1NzEzIDIwNC4yNDc5NTcgCkwgNzkxLjI4IDIwNC4yNDc5NTcgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF81NyI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzI4Ij4KICAgICAgPCEtLSAxIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDI0LjkwNDc3NiAyMDcuODI2ODYzKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja18xMCI+CiAgICAgPGcgaWQ9ImxpbmUyZF81OCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwZjI2ZjA5NTRjOCkiIGQ9Ik0gNDM3LjQ2NTcxMyAxNzAuNzIxMjE0IApMIDc5MS4yOCAxNzAuNzIxMjE0IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfNTkiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8yOSI+CiAgICAgIDwhLS0gMiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQyNC45MDQ3NzYgMTc0LjMwMDEyMSlzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfMTEiPgogICAgIDxnIGlkPSJsaW5lMmRfNjAiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGYyNmYwOTU0YzgpIiBkPSJNIDQzNy40NjU3MTMgMTM3LjE5NDQ3MiAKTCA3OTEuMjggMTM3LjE5NDQ3MiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzYxIj48L2c+CiAgICAgPGcgaWQ9InRleHRfMzAiPgogICAgICA8IS0tIDMgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0MjQuOTA0Nzc2IDE0MC43NzMzNzgpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTEiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inl0aWNrXzEyIj4KICAgICA8ZyBpZD0ibGluZTJkXzYyIj4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BmMjZmMDk1NGM4KSIgZD0iTSA0MzcuNDY1NzEzIDEwMy42Njc3MjkgCkwgNzkxLjI4IDEwMy42Njc3MjkgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF82MyI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzMxIj4KICAgICAgPCEtLSA0IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDI0LjkwNDc3NiAxMDcuMjQ2NjM1KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUyIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja18xMyI+CiAgICAgPGcgaWQ9ImxpbmUyZF82NCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwZjI2ZjA5NTRjOCkiIGQ9Ik0gNDM3LjQ2NTcxMyA3MC4xNDA5ODYgCkwgNzkxLjI4IDcwLjE0MDk4NiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzY1Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMzIiPgogICAgICA8IS0tIDUgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0MjQuOTA0Nzc2IDczLjcxOTg5MilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MyI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgIDwvZz4KICAgPGcgaWQ9ImxpbmUyZF82NiI+CiAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGYyNmYwOTU0YzgpIiBkPSJNIDQ1My41NDgxODEgMjM2Ljg5MjQxIApMIDQ1NC40NzIzNzIgMjQxLjE5MDcwNiAKTCA0NTUuNDI3MzY5IDI0My4xNjI4ODMgCkwgNDU2LjM4MjM2NyAyMzQuNzgxMTk4IApMIDQ1Ny4zMDY1NTggMjIyLjIwODY2OSAKTCA0NTguMjYxNTU2IDIxMy42NzQ2MDQgCkwgNDU5LjE4NTc0NyAyMTcuMDc1ODU5IApMIDQ2MC4xNDA3NDUgMjA2LjI2MDc2OSAKTCA0NjEuMDk1NzQyIDIwMC45NDU1MzkgCkwgNDYxLjk4OTEyNyAyMDAuMjM5NzAxIApMIDQ2Mi45NDQxMjUgMjA3LjE1MjQ0NiAKTCA0NjMuODY4MzE2IDIwOS4zMjk1MDUgCkwgNDY1Ljc0NzUwNSAyMTguODUyNzc2IApMIDQ2Ny42NTc1IDIxMi4yMjE1ODkgCkwgNDY4LjU4MTY5MSAyMTEuMTczODc4IApMIDQ2OS41MzY2ODkgMjExLjE3Mzg3OCAKTCA0NzAuNDYwODggMjExLjY4MTg3NSAKTCA0NzEuNDE1ODc4IDIxMS4xNjYwNjYgCkwgNDcyLjM3MDg3NSAyMTIuNjkwMDI1IApMIDQ3My4yMzM0NTQgMjIwLjE0MDQwNCAKTCA0NzQuMTg4NDUxIDIxOC43NzE5NzcgCkwgNDc1LjExMjY0MyAyMTYuMTQyNDQxIApMIDQ3Ni4wNjc2NCAyMTEuMjY1ODA4IApMIDQ3Ni45OTE4MzEgMjE0Ljk5MDk5OCAKTCA0NzcuOTQ2ODI5IDIxNi43ODcwNiAKTCA0ODAuNzgxMDE1IDIxOC43MjE3ODcgCkwgNDgxLjcwNTIwNyAyMTYuMDM5NjQ4IApMIDQ4Mi42NjAyMDQgMjE4LjUyMzEwOCAKTCA0ODQuNDc3NzggMjE4LjUyMzEwOCAKTCA0ODUuNDMyNzc4IDIxOS44NjQxNzggCkwgNDg2LjM1Njk2OSAyMjEuOTU5NTk5IApMIDQ4Ny4zMTE5NjcgMjI5LjQwOTk3OSAKTCA0ODguMjM2MTU4IDIyOC40NTIwODYgCkwgNDg5LjE5MTE1NSAyMzMuMTA4NTgyIApMIDQ5MC4xNDYxNTMgMjMyLjAyNzA3NiAKTCA0OTEuMDcwMzQ0IDIzMy41OTg2NDIgCkwgNDkyLjAyNTM0MiAyMzMuMDQ5MDM4IApMIDQ5Mi45NDk1MzMgMjQwLjYxOTU3OCAKTCA0OTMuOTA0NTMxIDI0MC42MTk1NzggCkwgNDk0Ljg1OTUyOCAyNDMuNDEzNDYyIApMIDQ5NS43MjIxMDcgMjQ0LjE3NTQyNCAKTCA0OTYuNjc3MTA0IDI0My4zOTU3MjcgCkwgNDk3LjYwMTI5NiAyNDQuOTE5Njg1IApMIDQ5OC41NTYyOTMgMjM2LjkzNzEzNSAKTCA0OTkuNDgwNDg0IDIzOC4yMjY2NCAKTCA1MDAuNDM1NDgyIDIzOC4yMjY2NCAKTCA1MDEuMzkwNDggMjQxLjU3OTMxNSAKTCA1MDIuMzE0NjcxIDIzMy4zODM5MDQgCkwgNTAzLjI2OTY2OCAyMzUuNzc4Njg1IApMIDUwNC4xOTM4NiAyNDAuOTM2NjQxIApMIDUwNS4xNDg4NTcgMjQwLjkzNjY0MSAKTCA1MDYuOTk3MjQgMjM1LjA5NDg3NCAKTCA1MDcuOTUyMjM3IDIyMC45MTA0OCAKTCA1MDguODc2NDI5IDIyMy42Mjg4NjIgCkwgNTA5LjgzMTQyNiAyMTguMjA1NDA4IApMIDUxMC43NTU2MTcgMjEwLjE0MjAyNiAKTCA1MTIuNjY1NjEzIDIxMi4yMjcwODcgCkwgNTEzLjU4OTgwNCAyMDYuMDMxOTE1IApMIDUxNS40Njg5OTMgMjEwLjE1NzE4IApMIDUxNi40MjM5OSAyMDcuMzYzMjk2IApMIDUxNy4zNzg5ODggMjA5LjI5NzUyIApMIDUxOC4yNDE1NjYgMjEwLjY2NTk0OCAKTCA1MTkuMTk2NTY0IDIwNy44MTI2MjEgCkwgNTIwLjEyMDc1NSAyMDUuODQwNDQ0IApMIDUyMS4wNzU3NTMgMTk0Ljk3NTI5OCAKTCA1MjEuOTk5OTQ0IDE5Ni4xNDc1NjEgCkwgNTIyLjk1NDk0MSAxODEuMDg0ODM0IApMIDUyMy45MDk5MzkgMTgyLjA5MDYzNiAKTCA1MjQuODM0MTMgMTc0LjMxMzgwNiAKTCA1MjUuNzg5MTI4IDE3OC42NjI0NTkgCkwgNTI2LjcxMzMxOSAxODAuMjc0MzI1IApMIDUyNy42NjgzMTcgMTc4LjkxOTcxIApMIDUyOC42MjMzMTQgMTc2LjMxNTY4OCAKTCA1MjkuNDg1ODkzIDE3Ny4yMjE4MTUgCkwgNTMwLjQ0MDg5IDE2OC45OTUzNTggCkwgNTMxLjM2NTA4MiAxNjUuMjU2MzIyIApMIDUzMi4zMjAwNzkgMTY0LjAyMjkwNiAKTCA1MzMuMjQ0MjcgMTYyLjI5MjQ5MSAKTCA1MzQuMTk5MjY4IDE2Ny44NDU5OTQgCkwgNTM1LjE1NDI2NiAxNzEuOTEzNTkzIApMIDUzNi4wNzg0NTcgMTYzLjYzNzExNCAKTCA1MzcuMDMzNDU0IDE2MS42MTE5OTggCkwgNTM3Ljk1NzY0NiAxNTQuMzk3Mzc5IApMIDUzOC45MTI2NDMgMTU2LjQ5MjggCkwgNTM5Ljg2NzY0MSAxNTIuNzY3NjEgCkwgNTQwLjczMDIxOSAxNjUuOTI2ODU3IApMIDU0MS42ODUyMTcgMTY5LjY1MjA0NyAKTCA1NDIuNjA5NDA4IDE2Ni44NTgxNjMgCkwgNTQzLjU2NDQwNiAxNjIuODQ2NDIgCkwgNTQ0LjQ4ODU5NyAxNjcuMzI1MTkgCkwgNTQ1LjQ0MzU5NSAxNzMuMDg1Mjg2IApMIDU0Ni4zOTg1OTIgMTY3LjM3ODU5OCAKTCA1NDcuMzIyNzgzIDE2NS41NDk4ODIgCkwgNTQ4LjI3Nzc4MSAxNzAuNjA3NzkzIApMIDU0OS4yMDE5NzIgMTc2LjIyMzk1OSAKTCA1NTAuMTU2OTcgMTc3LjA0MTY3NiAKTCA1NTEuMTExOTY3IDE5NS40ODEzODQgCkwgNTUyLjAwNTM1MiAxOTMuNjE4NzczIApMIDU1Mi45NjAzNSAxOTAuMDg5NjQ3IApMIDU1My44ODQ1NDEgMTkxLjY4NjE1NyAKTCA1NTQuODM5NTM5IDE5Mi45NDM0MSAKTCA1NTUuNzYzNzMgMTkyLjA3MjU4NiAKTCA1NTYuNzE4NzI3IDE5OC4wMTQwMjggCkwgNTU3LjY3MzcyNSAyMDIuNjU2MjA4IApMIDU1OC41OTc5MTYgMjAwLjI2MTQyNiAKTCA1NTkuNTUyOTE0IDIwNC43MzE2NDcgCkwgNTYxLjQzMjEwMyAyMjkuMTU2MTE0IApMIDU2Mi4zODcxIDIyOS4yMTk5ODMgCkwgNTYzLjI0OTY3OSAyMzYuNjQxOTMyIApMIDU2NC4yMDQ2NzYgMjIxLjE5MzM0NSAKTCA1NjUuMTI4ODY4IDIyOS41MTg3NzMgCkwgNTY2LjA4Mzg2NSAyMTMuOTUyNzc2IApMIDU2Ny4wMDgwNTYgMTk1LjM0OTUyNCAKTCA1NjcuOTYzMDU0IDE4NS40ODg3MDUgCkwgNTY4LjkxODA1MiAxODIuNDQwODIzIApMIDU2OS44NDIyNDMgMTgxLjUwOTUxNyAKTCA1NzAuNzk3MjQgMTU4LjQwMzI1NCAKTCA1NzEuNzIxNDMyIDE1OS4yMDc4OTYgCkwgNTcyLjY3NjQyOSAxNTkuNzU3NSAKTCA1NzMuNjMxNDI3IDE0OC4wMjMxNCAKTCA1NzQuNDk0MDA1IDE0My4yNjMxODEgCkwgNTc1LjQ0OTAwMyAxMzkuMjc2MjE0IApMIDU3Ni4zNzMxOTQgMTI2LjY0MjkzNSAKTCA1NzcuMzI4MTkyIDEyNS4xMTM2NDYgCkwgNTc4LjI1MjM4MyAxMjQuNDYxMTE1IApMIDU3OS4yMDczODEgMTMxLjcyMjY3MyAKTCA1ODAuMTYyMzc4IDExNi41MDg4NzQgCkwgNTgxLjA4NjU2OSAxMTkuMjIyMDI1IApMIDU4Mi4wNDE1NjcgMTIyLjgwNjYzOCAKTCA1ODIuOTY1NzU4IDEyNS42Mzk4ODIgCkwgNTgzLjkyMDc1NiAxMjUuMjUzMDUxIApMIDU4NC44NzU3NTMgMTIzLjIxMzM4NCAKTCA1ODUuNzM4MzMyIDEzMS42NzMxODcgCkwgNTg2LjY5MzMyOSAxMjguNDU4NzQ0IApMIDU4Ny42MTc1MjEgMTMxLjc0Mzk2MiAKTCA1ODguNTcyNTE4IDEyOC43NTIyMzcgCkwgNTg5LjQ5NjcwOSAxMjguMDk1NDQ4IApMIDU5MC40NTE3MDcgMTIwLjk4MDE2OCAKTCA1OTEuNDA2NzA1IDEyMC44MTEwOTIgCkwgNTkzLjI4NTg5MyAxMTMuNzMzMzYyIApMIDU5NC4yMTAwODUgMTE0LjAyODMzMSAKTCA1OTUuMTY1MDgyIDExNi42NjY4MTggCkwgNTk2LjEyMDA4IDEwOS44MTkzNSAKTCA1OTcuMDEzNDY1IDExNC4zNzg5ODcgCkwgNTk3Ljk2ODQ2MiAxMTAuNTUwMzMzIApMIDU5OC44OTI2NTQgMTEzLjY3MDgzNSAKTCA1OTkuODQ3NjUxIDExMy40MDQ1OTkgCkwgNjAwLjc3MTg0MiAxMjMuMTE3MTk2IApMIDYwMS43MjY4NCAxMjcuNzUxNDMgCkwgNjAyLjY4MTgzOCAxNDMuMTg3MDA4IApMIDYwMy42MDYwMjkgMTQ1Ljg5Mzc1NiAKTCA2MDQuNTYxMDI2IDEzNi4yNTczMzIgCkwgNjA1LjQ4NTIxOCAxMjkuMjQwMTE4IApMIDYwNi40NDAyMTUgMTI3Ljk1MDYxMiAKTCA2MDcuMzk1MjEzIDEzMS42NzU4MDIgCkwgNjA4LjI1Nzc5MSAxMzYuODkxMDg4IApMIDYxMC4xMzY5OCAxMzguMjI3NzY2IApMIDYxMS4wOTE5NzggMTQyLjQ3NjAwNyAKTCA2MTIuMDE2MTY5IDE0Mi44NzA0NDkgCkwgNjEyLjk3MTE2NyAxMjQuNTc3MDg0IApMIDYxMy45MjYxNjQgMTIzLjYzMDI1NiAKTCA2MTQuODUwMzU1IDEyNC45Mjc4MDggCkwgNjE1LjgwNTM1MyAxMzEuNzIwMjI1IApMIDYxNi43Mjk1NDQgMTMwLjY4Mjc0IApMIDYxNy42ODQ1NDIgMTMzLjk2NjU1IApMIDYxOC42Mzk1MzkgMTI3LjY4Mzk0MSAKTCA2MTkuNTAyMTE4IDEzMS4wOTU5NTcgCkwgNjIwLjQ1NzExNSAxMjYuMzYxNDc4IApMIDYyMS4zODEzMDcgMTI3LjUxOTIyNCAKTCA2MjIuMzM2MzA0IDEyMS45MjMxMDcgCkwgNjIzLjI2MDQ5NSAxMTkuNjUzNzQ5IApMIDYyNC4yMTU0OTMgMTI0LjA2NTE2NSAKTCA2MjUuMTcwNDkxIDEyNC4zODg0MjkgCkwgNjI2LjA5NDY4MiAxMjcuMjMyODM4IApMIDYyNy4wNDk2NzkgMTIxLjIyMDQ1NCAKTCA2MjcuOTczODcxIDEyNC41MDM5OTYgCkwgNjI4LjkyODg2OCAxMjEuOTY1NTUyIApMIDYyOS44ODM4NjYgMTE1LjY0MzExMyAKTCA2MzAuNzQ2NDQ0IDEwNS40NTM5NjcgCkwgNjMxLjcwMTQ0MiAxMDUuNDUzOTY3IApMIDYzMi42MjU2MzMgMTA0LjczNTc1NyAKTCA2MzMuNTgwNjMxIDEwNi4wODU4MTIgCkwgNjM0LjUwNDgyMiAxMDcuOTYxNDMyIApMIDYzNS40NTk4MiAxMDguMTc4NzUyIApMIDYzNi40MTQ4MTcgMTA4LjgwMzY1NyAKTCA2MzcuMzM5MDA4IDEwNi4yNTY1MyAKTCA2MzguMjk0MDA2IDEwMi45NDIzMTEgCkwgNjM5LjIxODE5NyAxMDguMzAxMTkyIApMIDY0MC4xNzMxOTUgMTA2LjUzODMyMiAKTCA2NDEuMTI4MTkyIDExMS4yODg2OTMgCkwgNjQyLjAyMTU3NyAxMDMuNjk2Mzk0IApMIDY0Mi45NzY1NzUgMTA2LjAzOTUxMSAKTCA2NDQuODU1NzY0IDk5LjQ1NzcwOSAKTCA2NDUuNzc5OTU1IDkwLjQ1NzA1MiAKTCA2NDYuNzM0OTUzIDg5LjMxODQ4NCAKTCA2NDcuNjg5OTUgODkuNTU0NDQ1IApMIDY0OC42MTQxNDEgODguNTI0NjcyIApMIDY0OS41NjkxMzkgOTAuMDQyNDk0IApMIDY1MC40OTMzMyA5MS4yNzAwNzYgCkwgNjUxLjQ0ODMyOCA5NC40ODY5NjcgCkwgNjUyLjQwMzMyNSA5Ni40NzQwOTcgCkwgNjUzLjI2NTkwNCA5Ny4zMzM3NTYgCkwgNjU0LjIyMDkwMSA5Ny40NTk3ODMgCkwgNjU2LjEwMDA5IDkzLjg4NTY2NSAKTCA2NTcuMDI0MjgxIDk2LjQxNzI2OSAKTCA2NTcuOTc5Mjc5IDk2LjA5NjU1MiAKTCA2NTguOTM0Mjc3IDk1LjM4Nzg5NyAKTCA2NTkuODU4NDY4IDk1LjcyMjkzIApMIDY2MC44MTM0NjUgOTUuNzk1NDQ5IApMIDY2MS43Mzc2NTcgOTcuMDA2NjY5IApMIDY2Mi42OTI2NTQgOTUuNzc1MTY1IApMIDY2NC41MTAyMyA4NC45NTYzODcgCkwgNjY1LjQ2NTIyOCA4NS44MDEyOTQgCkwgNjY2LjM4OTQxOSA4NC45NTMwMDEgCkwgNjY3LjM0NDQxNyA4Ny44MTI4MzIgCkwgNjY4LjI2ODYwOCA4Ni4wMjM0NDIgCkwgNjY5LjIyMzYwNiA4Ny41MzU0OTggCkwgNjcwLjE3ODYwMyA5NS41NTA2MzYgCkwgNjcxLjEwMjc5NCA5MS43MjI2ODcgCkwgNjcyLjA1Nzc5MiA4Mi4wODQzMTggCkwgNjcyLjk4MTk4MyA4MS4yNjA0NjYgCkwgNjczLjkzNjk4MSA3Ny43NDY5NjQgCkwgNjc0Ljg5MTk3OCA3OC43NTk1NzIgCkwgNjc1Ljc1NDU1NyA2OC4zOTk3NDEgCkwgNjc2LjcwOTU1NCA2OS40ODQwNjMgCkwgNjc3LjYzMzc0NiA2OC4wMTU3MjYgCkwgNjc4LjU4ODc0MyA3MC41MDgzMzkgCkwgNjc5LjUxMjkzNSA3MS40MTQ4MzUgCkwgNjgwLjQ2NzkzMiA3Ni4xNTU0NDkgCkwgNjgxLjQyMjkzIDc5LjcxMzk3OCAKTCA2ODIuMzQ3MTIxIDc5LjUxNzYxMSAKTCA2ODQuMjI2MzEgODQuODU5Njk2IApMIDY4NS4xODEzMDcgNzkuMjIzMDEyIApMIDY4Ni4xMzYzMDUgNzcuNjA4NTY1IApMIDY4Ny45ODQ2ODcgNzMuODMwMTAxIApMIDY4OC45MDg4NzkgNzEuMjM4MTQ5IApMIDY4OS44NjM4NzYgNzQuMDU2OTQzIApMIDY5MC43ODgwNjcgNjcuNzMwODQ5IApMIDY5MS43NDMwNjUgNjcuNTYwODY5IApMIDY5Mi42OTgwNjMgNjMuODY2MDIgCkwgNjkzLjYyMjI1NCA2My45NTk3NjEgCkwgNjk0LjU3NzI1MSA2Ny42OTY3MTkgCkwgNjk1LjUwMTQ0MyA2Ni42OTE1ODcgCkwgNjk3LjQxMTQzOCA2My40MDc3NDMgCkwgNjk4LjI3NDAxNiA2Mi4zMjI0ODMgCkwgNjk5LjIyOTAxNCA2MC4yMDg2ODkgCkwgNzAwLjE1MzIwNSA2MS40MjA4ODIgCkwgNzAxLjEwODIwMyA1OS43NDQwMDggCkwgNzAyLjAzMjM5NCA2MC4wMzgyMDUgCkwgNzAyLjk4NzM5MiA1NC40MzA5OTIgCkwgNzAzLjk0MjM4OSA2MC4wNzAyNTcgCkwgNzA0Ljg2NjU4IDU2Ljc0MDUxNSAKTCA3MDUuODIxNTc4IDUzLjgyMDgzOCAKTCA3MDYuNzQ1NzY5IDUxLjg2NTg2IApMIDcwNy43MDA3NjcgNTEuNDM0MjcxIApMIDcwOC42NTU3NjQgNTYuMTQ3MDkxIApMIDcwOS41MTgzNDMgNTQuNTIwODQzIApMIDcxMC40NzMzNCA1Ni4xOTQ4IApMIDcxMS4zOTc1MzIgNTUuMjA5MzE1IApMIDcxMi4zNTI1MjkgNTkuMzU3ODQ3IApMIDcxMy4yNzY3MjEgNTguMTc3MDAyIApMIDcxNC4yMzE3MTggNTcuOTYzODA1IApMIDcxNS4xODY3MTYgNjcuNzYyMjk3IApMIDcxNi4xMTA5MDcgNzAuNTc2MTYzIApMIDcxNy4wNjU5MDUgNjUuMDA0NzIzIApMIDcxNy45OTAwOTYgNjguNDc5MyAKTCA3MTguOTQ1MDkzIDY3Ljc3NTk0MyAKTCA3MTkuOTAwMDkxIDY4LjI2NTgzNSAKTCA3MjAuNzYyNjY5IDYxLjU2OTgwNyAKTCA3MjEuNzE3NjY3IDY1LjcxMzcxMyAKTCA3MjIuNjQxODU4IDY2LjIzMDg2MyAKTCA3MjMuNTk2ODU2IDY1LjI1NTM2OSAKTCA3MjQuNTIxMDQ3IDY0LjU5OTExNiAKTCA3MjUuNDc2MDQ1IDY3LjE3MzcwMiAKTCA3MjYuNDMxMDQyIDcyLjkyMTU5NCAKTCA3MjcuMzU1MjMzIDgwLjk0MzMzNiAKTCA3MjguMzEwMjMxIDc5LjAyNjEwOSAKTCA3MjkuMjM0NDIyIDc2LjM1MjM1MiAKTCA3MzAuMTg5NDIgNzQuNDU3NDU0IApMIDczMS4xNDQ0MTcgODAuNDkwMjIyIApMIDc2Mi4wNzQwMTcgODMuOTgyOTM4IApMIDc2Mi45OTgyMDggODEuNTIxNDM4IApMIDc2My45NTMyMDYgODMuMzI5MTY2IApMIDc2NC45MDgyMDMgNzkuNzM3NjQ4IApMIDc2NS43NzA3ODIgODAuOTUyMTU0IApMIDc2Ni43MjU3OCA4Mi44OTIxNDUgCkwgNzY3LjY0OTk3MSA4MS40NDg5ODcgCkwgNzY4LjYwNDk2OCA4My40OTA2MzEgCkwgNzY5LjUyOTE2IDgyLjYxMDI1MiAKTCA3NzAuNDg0MTU3IDg1LjkzNjY3NSAKTCA3NzEuNDM5MTU1IDgyLjc2ODYzMyAKTCA3NzIuMzYzMzQ2IDgwLjEwNDk2NiAKTCA3NzMuMzE4MzQ0IDc2LjQzNjQzNyAKTCA3NzQuMjQyNTM1IDcxLjExMzA5NCAKTCA3NzUuMTk3NTMyIDY5LjMwODc4NSAKTCA3NzUuMTk3NTMyIDY5LjMwODc4NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojNGM3MmIwO3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF85Ij4KICAgIDxwYXRoIGQ9Ik0gNDM3LjQ2NTcxMyAyNTQuNTkzOTU1IApMIDQzNy40NjU3MTMgNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0icGF0Y2hfMTAiPgogICAgPHBhdGggZD0iTSA3OTEuMjggMjU0LjU5Mzk1NSAKTCA3OTEuMjggNDEuNzYgCiIgc3R5bGU9ImZpbGw6bm9uZTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0icGF0Y2hfMTEiPgogICAgPHBhdGggZD0iTSA0MzcuNDY1NzEzIDI1NC41OTM5NTUgCkwgNzkxLjI4IDI1NC41OTM5NTUgCiIgc3R5bGU9ImZpbGw6bm9uZTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0icGF0Y2hfMTIiPgogICAgPHBhdGggZD0iTSA0MzcuNDY1NzEzIDQxLjc2IApMIDc5MS4yOCA0MS43NiAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJsZWdlbmRfMiI+CiAgICA8ZyBpZD0icGF0Y2hfMTMiPgogICAgIDxwYXRoIGQ9Ik0gNDQ1Ljg2NTcxMyA2OC4zNyAKTCA1NjQuOTgyNTg4IDY4LjM3IApRIDU2Ny4zODI1ODggNjguMzcgNTY3LjM4MjU4OCA2NS45NyAKTCA1NjcuMzgyNTg4IDUwLjE2IApRIDU2Ny4zODI1ODggNDcuNzYgNTY0Ljk4MjU4OCA0Ny43NiAKTCA0NDUuODY1NzEzIDQ3Ljc2IApRIDQ0My40NjU3MTMgNDcuNzYgNDQzLjQ2NTcxMyA1MC4xNiAKTCA0NDMuNDY1NzEzIDY1Ljk3IApRIDQ0My40NjU3MTMgNjguMzcgNDQ1Ljg2NTcxMyA2OC4zNyAKegoiIHN0eWxlPSJmaWxsOiNlYWVhZjI7b3BhY2l0eTowLjg7c3Ryb2tlOiNjY2NjY2M7c3Ryb2tlLWxpbmVqb2luOm1pdGVyO3N0cm9rZS13aWR0aDowLjM7Ij48L3BhdGg+CiAgICA8L2c+CiAgICA8ZyBpZD0ibGluZTJkXzY3Ij4KICAgICA8cGF0aCBkPSJNIDQ0OC4yNjU3MTMgNTYuOTg1IApMIDQ3Mi4yNjU3MTMgNTYuOTg1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiM0YzcyYjA7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7c3Ryb2tlLXdpZHRoOjEuNzU7Ij48L3BhdGg+CiAgICA8L2c+CiAgICA8ZyBpZD0ibGluZTJkXzY4Ij48L2c+CiAgICA8ZyBpZD0idGV4dF8zMyI+CiAgICAgPCEtLSBwZXJtbm86IDEwMDUxIC0tPgogICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0ODEuODY1NzEzIDYxLjE4NSlzY2FsZSgwLjEyIC0wLjEyKSI+CiAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEyIj48L3VzZT4KICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxNDQuNTMxMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjI3LjgzMjAzMSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEwIj48L3VzZT4KICAgICAgPHVzZSB4PSIyODMuNDQ3MjY2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTEiPjwvdXNlPgogICAgICA8dXNlIHg9IjMzOS4wNjI1IiB4bGluazpocmVmPSIjQXJpYWxNVC01OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMzY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgICA8dXNlIHg9IjM5NC42Mjg5MDYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPHVzZSB4PSI0NTAuMjQ0MTQxIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTA1Ljg1OTM3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8dXNlIHg9IjU2MS40NzQ2MDkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUzIj48L3VzZT4KICAgICAgPHVzZSB4PSI2MTcuMDg5ODQ0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgPC9nPgogIDxnIGlkPSJheGVzXzMiPgogICA8ZyBpZD0icGF0Y2hfMTQiPgogICAgPHBhdGggZD0iTSA1OS4wNCA0OTEuMDQgCkwgNDEyLjg1NDI4NyA0OTEuMDQgCkwgNDEyLjg1NDI4NyAyNzguMjA2MDQ1IApMIDU5LjA0IDI3OC4yMDYwNDUgCnoKIiBzdHlsZT0iZmlsbDojZWFlYWYyOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJtYXRwbG90bGliLmF4aXNfNSI+CiAgICA8ZyBpZD0ieHRpY2tfMTkiPgogICAgIDxnIGlkPSJsaW5lMmRfNjkiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGFjODAyNmM1MmYpIiBkPSJNIDg4Ljg5OTgwMiA0OTEuMDQgCkwgODguODk5ODAyIDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF83MCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzM0Ij4KICAgICAgPCEtLSAxOTc2IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNzcuNzc3OTI3IDUwNS4xOTc4MTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTUiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC01NCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMjAiPgogICAgIDxnIGlkPSJsaW5lMmRfNzEiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGFjODAyNmM1MmYpIiBkPSJNIDE0OC45ODU0MzEgNDkxLjA0IApMIDE0OC45ODU0MzEgMjc4LjIwNjA0NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzcyIj48L2c+CiAgICAgPGcgaWQ9InRleHRfMzUiPgogICAgICA8IS0tIDE5ODAgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMzcuODYzNTU2IDUwNS4xOTc4MTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTYiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMjEiPgogICAgIDxnIGlkPSJsaW5lMmRfNzMiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGFjODAyNmM1MmYpIiBkPSJNIDIwOS4wNzEwNiA0OTEuMDQgCkwgMjA5LjA3MTA2IDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF83NCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzM2Ij4KICAgICAgPCEtLSAxOTg0IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTk3Ljk0OTE4NSA1MDUuMTk3ODEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU2Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTIiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzIyIj4KICAgICA8ZyBpZD0ibGluZTJkXzc1Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BhYzgwMjZjNTJmKSIgZD0iTSAyNjkuMTU2Njg4IDQ5MS4wNCAKTCAyNjkuMTU2Njg4IDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF83NiI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzM3Ij4KICAgICAgPCEtLSAxOTg4IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMjU4LjAzNDgxMyA1MDUuMTk3ODEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU2Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTYiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzIzIj4KICAgICA8ZyBpZD0ibGluZTJkXzc3Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BhYzgwMjZjNTJmKSIgZD0iTSAzMjkuMjQyMzE3IDQ5MS4wNCAKTCAzMjkuMjQyMzE3IDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF83OCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzM4Ij4KICAgICAgPCEtLSAxOTkyIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzE4LjEyMDQ0MiA1MDUuMTk3ODEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzI0Ij4KICAgICA8ZyBpZD0ibGluZTJkXzc5Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BhYzgwMjZjNTJmKSIgZD0iTSAzODkuMzI3OTQ2IDQ5MS4wNCAKTCAzODkuMzI3OTQ2IDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF84MCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzM5Ij4KICAgICAgPCEtLSAxOTk2IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzc4LjIwNjA3MSA1MDUuMTk3ODEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTQiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgIDxnIGlkPSJtYXRwbG90bGliLmF4aXNfNiI+CiAgICA8ZyBpZD0ieXRpY2tfMTQiPgogICAgIDxnIGlkPSJsaW5lMmRfODEiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGFjODAyNmM1MmYpIiBkPSJNIDU5LjA0IDQ4NS44Mjk2MTIgCkwgNDEyLjg1NDI4NyA0ODUuODI5NjEyIAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfODIiPjwvZz4KICAgICA8ZyBpZD0idGV4dF80MCI+CiAgICAgIDwhLS0gMCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ2LjQ3OTA2MyA0ODkuNDA4NTE4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja18xNSI+CiAgICAgPGcgaWQ9ImxpbmUyZF84MyI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwYWM4MDI2YzUyZikiIGQ9Ik0gNTkuMDQgNDM5LjAwODQ0OSAKTCA0MTIuODU0Mjg3IDQzOS4wMDg0NDkgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF84NCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzQxIj4KICAgICAgPCEtLSAxIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDYuNDc5MDYzIDQ0Mi41ODczNTUpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inl0aWNrXzE2Ij4KICAgICA8ZyBpZD0ibGluZTJkXzg1Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BhYzgwMjZjNTJmKSIgZD0iTSA1OS4wNCAzOTIuMTg3Mjg2IApMIDQxMi44NTQyODcgMzkyLjE4NzI4NiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzg2Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfNDIiPgogICAgICA8IS0tIDIgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0Ni40NzkwNjMgMzk1Ljc2NjE5MilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfMTciPgogICAgIDxnIGlkPSJsaW5lMmRfODciPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcGFjODAyNmM1MmYpIiBkPSJNIDU5LjA0IDM0NS4zNjYxMjIgCkwgNDEyLjg1NDI4NyAzNDUuMzY2MTIyIAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfODgiPjwvZz4KICAgICA8ZyBpZD0idGV4dF80MyI+CiAgICAgIDwhLS0gMyAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ2LjQ3OTA2MyAzNDguOTQ1MDI5KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUxIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja18xOCI+CiAgICAgPGcgaWQ9ImxpbmUyZF84OSI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwYWM4MDI2YzUyZikiIGQ9Ik0gNTkuMDQgMjk4LjU0NDk1OSAKTCA0MTIuODU0Mjg3IDI5OC41NDQ5NTkgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF85MCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzQ0Ij4KICAgICAgPCEtLSA0IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDYuNDc5MDYzIDMwMi4xMjM4NjUpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTIiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgIDxnIGlkPSJsaW5lMmRfOTEiPgogICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3BhYzgwMjZjNTJmKSIgZD0iTSA3NS4xMjI0NjggNDc1LjUxMzA4NCAKTCA3Ni4yNzQwMDYgNDgxLjM2NTcyOSAKTCA3OC43ODI3MTUgNDc2Ljk3NTE2OCAKTCA4MC4wNTc2MzIgNDcyLjg0MzkwMyAKTCA4MS4yOTE0MjMgNDcwLjMxMzAzMiAKTCA4Mi41NjYzNDEgNDcyLjc0NTI5OCAKTCA4My44NDEyNTggNDc3LjIzNDk3OSAKTCA4Ni4zNDk5NjcgNDgwLjE0MDE4NSAKTCA4Ny41ODM3NTggNDc0Ljc2NzI3IApMIDg4Ljg1ODY3NiA0NzcuNTIxNDc4IApMIDkwLjEzMzU5MyA0NjkuMzQ2MzYyIApMIDkxLjMyNjI1OCA0NjguMDgwOTI3IApMIDkyLjYwMTE3NSA0NjUuNjE2NjM1IApMIDkzLjgzNDk2NyA0NjguNTc5OTkzIApMIDk1LjEwOTg4NCA0NjguNTc5OTkzIApMIDk2LjM0MzY3NSA0NjkuMjEyNzM1IApMIDk3LjYxODU5MyA0NzAuNTEzMzMzIApMIDk4Ljg5MzUxIDQ2OS4xNzU2MDUgCkwgMTAwLjEyNzMwMSA0NzAuNDk0NTExIApMIDEwMS40MDIyMTkgNDYzLjcwODgxMyAKTCAxMDIuNjM2MDEgNDY5LjA0Mjg2NyAKTCAxMDMuOTEwOTI4IDQ2NC4zNjA3NTEgCkwgMTA1LjE4NTg0NSA0NTMuMjcxNTMzIApMIDEwNi4zMzczODQgNDU1LjI2MzkxNCAKTCAxMDcuNjEyMzAxIDQ1MS42MjIyNTggCkwgMTA4Ljg0NjA5MiA0NTIuMTA5OTk0IApMIDExMC4xMjEwMSA0NTEuNjE3MTU0IApMIDExMS4zNTQ4MDEgNDUxLjYxNzE1NCAKTCAxMTIuNjI5NzE4IDQ0Ny42NzQyOTcgCkwgMTEzLjkwNDYzNiA0NDguMDM3OTU3IApMIDExNS4xMzg0MjcgNDQ4Ljk2NTExIApMIDExNi40MTMzNDUgNDUzLjY5NDUxNSAKTCAxMTcuNjQ3MTM2IDQ0NC4xMTk4NjggCkwgMTE4LjkyMjA1MyA0NDYuMzI4NDIzIApMIDEyMC4xOTY5NzEgNDQ1Ljg2NDg0NiAKTCAxMjEuMzQ4NTA5IDQ0Mi4xOTI2MTYgCkwgMTIyLjYyMzQyNyA0MzUuMTI2ODgxIApMIDEyMy44NTcyMTggNDMxLjc1NTc1NyAKTCAxMjUuMTMyMTM1IDQyNC40MTgxMzIgCkwgMTI2LjM2NTkyNyA0MjcuMjU3NjAxIApMIDEyOC45MTU3NjIgNDE1LjYyNDU1NSAKTCAxMzAuMTQ5NTUzIDQxNi42NjUwMTUgCkwgMTMxLjQyNDQ3IDQyNS45NzYwNTkgCkwgMTMyLjY1ODI2MSA0MjcuNjM2Mzg0IApMIDEzMy45MzMxNzkgNDIyLjA0NTc5NyAKTCAxMzUuMjA4MDk2IDQxOC4zMDAxMDQgCkwgMTM2LjM1OTYzNSA0MjMuOTY0OTAzIApMIDEzNy42MzQ1NTIgNDIxLjI4OTQwMSAKTCAxMzguODY4MzQzIDQxNi40MTc0NzIgCkwgMTQwLjE0MzI2MSA0MjAuMTk4MDQ3IApMIDE0MS4zNzcwNTIgNDE0LjUwMzU2MyAKTCAxNDIuNjUxOTcgNDE2LjQ3Nzk2NSAKTCAxNDMuOTI2ODg3IDQwOC40MDk0MTQgCkwgMTQ1LjE2MDY3OCA0MDkuNDI3MjU5IApMIDE0Ni40MzU1OTYgNDEyLjI4ODU0NyAKTCAxNDcuNjY5Mzg3IDQwOS4xMzAxNzkgCkwgMTQ4Ljk0NDMwNCA0MDAuOTc1OTQ2IApMIDE1MC4yMTkyMjIgMzg3Ljc1ODQ3MiAKTCAxNTEuNDExODg3IDM5Ni4zNTM5OTUgCkwgMTUyLjY4NjgwNCA0MDEuNTU2MzQxIApMIDE1My45MjA1OTUgNDA4LjE4OTM1NSAKTCAxNTUuMTk1NTEzIDM5OS41MTg3NzcgCkwgMTU2LjQyOTMwNCAzOTkuMDMxMDQxIApMIDE1Ny43MDQyMjIgMzkzLjcyMTQyOCAKTCAxNTguOTc5MTM5IDM4OS42NDYyNTQgCkwgMTYwLjIxMjkzIDM4OC44MzkwMTEgCkwgMTYxLjQ4Nzg0OCAzOTUuNDI1NzE4IApMIDE2Mi43MjE2MzkgMzk0LjAyMTA4MyAKTCAxNjUuMjcxNDc0IDM5NC45MzQ3MDUgCkwgMTY2LjQyMzAxMiAzOTUuMjEyODY5IApMIDE2Ny42OTc5MyAzOTQuMjY2OTg4IApMIDE2OC45MzE3MjEgMzg5LjY3NzU3OCAKTCAxNzAuMjA2NjM5IDM4Ni4yNTY4NyAKTCAxNzIuNzE1MzQ3IDM5NC4yMDQyOTQgCkwgMTczLjk5MDI2NSAzOTguNTQ4NTQ5IApMIDE3NS4yMjQwNTYgNDA0LjEzNTE1NyAKTCAxNzYuNDk4OTczIDQwNC43OTk3MzYgCkwgMTc5LjAwNzY4MiAzOTkuMDQ1NzQzIApMIDE4MC4yODI2IDM5NC44OTAwMzcgCkwgMTgxLjQzNDEzOCAzOTYuMjEzMjUgCkwgMTgyLjcwOTA1NiAzOTcuMjc3MzU1IApMIDE4My45NDI4NDcgMzk1LjE1NDA2MiAKTCAxODUuMjE3NzY0IDM5OS45MTU1NCAKTCAxODYuNDUxNTU1IDQwNS4yMTYwNyAKTCAxODcuNzI2NDczIDQwNC44ODQwMTUgCkwgMTg5LjAwMTM5IDM5Ni43MDY3OTIgCkwgMTkwLjIzNTE4MiA0MDAuNDE4MjEyIApMIDE5MS41MTAwOTkgNDAwLjE3MDE1MyAKTCAxOTIuNzQzODkgNDAyLjM2OTgxMiAKTCAxOTQuMDE4ODA4IDQwMS4zODA2MjEgCkwgMTk1LjI5MzcyNSAzOTkuNzY2MDg3IApMIDE5Ni40NDUyNjQgMzk5LjgyODQ5OSAKTCAxOTcuNzIwMTgxIDM5Ni45NjE5MjEgCkwgMTk4Ljk1Mzk3MiAzOTUuMTYxMDg1IApMIDIwMS40NjI2ODEgMzgzLjQ4ODg1IApMIDIwMi43Mzc1OTggMzg5LjQ1NjI1NCAKTCAyMDQuMDEyNTE2IDM4Ni4wODkzNDQgCkwgMjA1LjI0NjMwNyAzODguMDYwNzQ5IApMIDIwNi41MjEyMjUgMzg4LjM2OTQ0MSAKTCAyMDcuNzU1MDE2IDM4MC4zMDU4MDcgCkwgMjA5LjAyOTkzMyAzODIuMzAyOTE3IApMIDIxMC4zMDQ4NTEgMzgyLjk5ODI1OCAKTCAyMTEuNDk3NTE2IDM4Ny4wNDUxMDUgCkwgMjEyLjc3MjQzMyAzOTAuNDA3OTQxIApMIDIxNC4wMDYyMjQgMzkwLjE4NDk3OSAKTCAyMTUuMjgxMTQyIDM5NS43NTg5NDQgCkwgMjE2LjUxNDkzMyAzOTguNjA2MTg2IApMIDIxNy43ODk4NSA0MDguNzExNDU3IApMIDIxOS4wNjQ3NjggNDA0LjUwMTg2IApMIDIyMC4yOTg1NTkgNDA0LjEwNTA1MSAKTCAyMjEuNTczNDc3IDQwMS4wMzYxMTEgCkwgMjIyLjgwNzI2OCA0MDUuNDk1MjY1IApMIDIyNC4wODIxODUgNDA5LjYwMjM3IApMIDIyNS4zNTcxMDMgMzg4Ljk4MzAzMiAKTCAyMjYuNTA4NjQxIDM4OS42MTE1MTMgCkwgMjI3Ljc4MzU1OSAzOTYuOTM3MjkzIApMIDIyOS4wMTczNSAzOTkuNjU1OTYzIApMIDIzMC4yOTIyNjcgNDAwLjA1OTYwOSAKTCAyMzEuNTI2MDU5IDM5MS45MTY4IApMIDIzMi44MDA5NzYgMzk0Ljc2MDc2NCAKTCAyMzQuMDc1ODk0IDM5OS41OTE1MzggCkwgMjM2LjU4NDYwMiA0MDcuNDYyNTUgCkwgMjM3LjgxODM5MyA0MDEuNDg1MzYgCkwgMjM5LjA5MzMxMSA0MDQuMTM1NjI1IApMIDI0MC4zNjgyMjggMzk5LjU0NzE1MSAKTCAyNDEuNTE5NzY3IDQwNC4yNzIyMDIgCkwgMjQyLjc5NDY4NCAzOTcuNTgzNDcxIApMIDI0NS4zMDMzOTMgNDAyLjg1MDg1MiAKTCAyNDYuNTM3MTg0IDQwNC43NDI2MTUgCkwgMjQ3LjgxMjEwMiA0MTIuNzI2ODQgCkwgMjQ5LjA4NzAxOSA0MDcuMzI0MzggCkwgMjUwLjMyMDgxIDQxMS42Mjk3NzQgCkwgMjUxLjU5NTcyOCA0MDcuNTk5NTk1IApMIDI1NC4xMDQ0MzYgNDA4LjcwNzg1MiAKTCAyNTUuMzc5MzU0IDQwMy43NDM2ODUgCkwgMjU2LjUzMDg5MiAzOTYuMDI1OTE5IApMIDI1Ny44MDU4MSAzOTkuNTU5NjA2IApMIDI1OS4wMzk2MDEgMzk1LjgzMzAxNSAKTCAyNjAuMzE0NTE5IDM5Ni43MjQ4NjUgCkwgMjYxLjU0ODMxIDM5Ny4xNzk0NTIgCkwgMjYyLjgyMzIyNyAzODMuNTAwMzIxIApMIDI2NC4wOTgxNDUgMzg1LjI4NzM5MSAKTCAyNjUuMzMxOTM2IDM4OC42MzE3OCAKTCAyNjYuNjA2ODUzIDM5OS45MTY4OTggCkwgMjY3Ljg0MDY0NSA0MDYuMzAxNjE5IApMIDI2OS4xMTU1NjIgMzkzLjM2NDE4MiAKTCAyNzAuMzkwNDggMzk0LjgxMjI2NyAKTCAyNzEuNTgzMTQ0IDM5Ny45MDA0NTEgCkwgMjcyLjg1ODA2MiAzODYuMDYwNTk2IApMIDI3NC4wOTE4NTMgMzkwLjQ0MjAyNyAKTCAyNzUuMzY2NzcxIDM5NS42OTc0NjggCkwgMjc2LjYwMDU2MiAzOTMuNTQ0NzcyIApMIDI3Ny44NzU0NzkgMzk2LjExNzM2IApMIDI3OS4xNTAzOTcgNDAwLjU4MTcxMSAKTCAyODAuMzg0MTg4IDQwMy42MjIwNDQgCkwgMjgxLjY1OTEwNSA0MDQuNDAyNDEyIApMIDI4Mi44OTI4OTcgNDA5LjA4NDUyOCAKTCAyODQuMTY3ODE0IDM5OS40MjMwMjggCkwgMjg1LjQ0MjczMiAzOTYuNDY1ODk3IApMIDI4Ni41OTQyNyAzOTQuNzEwMTA0IApMIDI4Ny44NjkxODggMzk0LjE0NjAwMiAKTCAyODkuMTAyOTc5IDM5NS4yNjA4MTQgCkwgMjkwLjM3Nzg5NiAzOTMuMDkxMDc1IApMIDI5MS42MTE2ODcgMzg4LjEzMzU1NiAKTCAyOTIuODg2NjA1IDM4OC4xMzM1NTYgCkwgMjk0LjE2MTUyMiAzOTAuNzIzNjU2IApMIDI5NS4zOTUzMTQgMzkyLjMxOTgzNiAKTCAyOTYuNjcwMjMxIDM5NC42MzMzNjQgCkwgMjk3LjkwNDAyMiAzOTYuMzg5MTU3IApMIDI5OS4xNzg5NCAzOTAuMzA4NDkzIApMIDMwMC40NTM4NTcgMzkyLjU2ODgzMSAKTCAzMDEuNjA1Mzk2IDM5My4xMzk4MTUgCkwgMzAyLjg4MDMxMyAzOTUuNDUxOTg1IApMIDMwNC4xMTQxMDQgMzk3LjM5Nzc3OSAKTCAzMDUuMzg5MDIyIDM5OC4wMzkxODIgCkwgMzA2LjYyMjgxMyA0MDIuNTkxMjI5IApMIDMwNy44OTc3MyA0MDIuNzM1Mjk4IApMIDMwOS4xNzI2NDggNDEyLjI0NTg0NyAKTCAzMTAuNDA2NDM5IDQxOC42NzIyODUgCkwgMzExLjY4MTM1NyA0MTguODg1MDg3IApMIDMxMi45MTUxNDggNDE3Ljc5NjIxNSAKTCAzMTQuMTkwMDY1IDQyNC4xODA5MzYgCkwgMzE1LjQ2NDk4MyA0MTcuMDM0NTI4IApMIDMxNi42MTY1MjEgNDA2LjE0NTg5MiAKTCAzMTcuODkxNDM5IDQwNi4xNDU4OTIgCkwgMzE5LjEyNTIzIDQwNi4zMjI1OTUgCkwgMzIwLjQwMDE0NyA0MDYuMzIyNTk1IApMIDMyMS42MzM5MzkgNDA5LjkyNDIxOSAKTCAzMjIuOTA4ODU2IDQwMi4zMTU3OCAKTCAzMjQuMTgzNzc0IDQwNC4wMTgzODUgCkwgMzI1LjQxNzU2NSA0MDYuNjY4NjUgCkwgMzI2LjY5MjQ4MiA0MDQuOTgzMDg4IApMIDMyNy45MjYyNzMgNDA0Ljk4MzA4OCAKTCAzMjkuMjAxMTkxIDM5OC41NTY2NDkgCkwgMzMwLjQ3NjEwOCAzODMuMjE4NjkyIApMIDMzMS42Njg3NzMgMzgyLjEyNDE1MyAKTCAzMzIuOTQzNjkxIDM3OS43MjMwNzEgCkwgMzM0LjE3NzQ4MiAzODguOTczMTA2IApMIDMzNS40NTIzOTkgMzk3LjYxNjk5NSAKTCAzMzYuNjg2MTkxIDQwMS4xNTA2ODIgCkwgMzM3Ljk2MTEwOCAzOTQuNDYxOTUxIApMIDMzOS4yMzYwMjYgMzk1LjQ2NTI4MiAKTCAzNDAuNDY5ODE3IDM5NS40NjUyODIgCkwgMzQxLjc0NDczNCAzOTAuMjYyOTM2IApMIDM0Mi45Nzg1MjUgMzc4LjcxMzcgCkwgMzQ0LjI1MzQ0MyAzODMuNzc1NDQyIApMIDM0NS41MjgzNiAzODAuOTM3Nzk5IApMIDM0Ni42Nzk4OTkgMzgzLjc0NzA2OSAKTCAzNDcuOTU0ODE2IDM4My43NDcwNjkgCkwgMzQ5LjE4ODYwNyAzNzcuOTg0NDYgCkwgMzUwLjQ2MzUyNSAzNjkuMTMzMzQxIApMIDM1MS42OTczMTYgMzY2Ljk1NTU5NSAKTCAzNTIuOTcyMjM0IDM2Ny45OTYwNTUgCkwgMzU0LjI0NzE1MSAzNzQuOTc2NjY5IApMIDM1NS40ODA5NDIgMzczLjcxMTIzMyAKTCAzNTYuNzU1ODYgMzY5LjM5ODc3IApMIDM1Ny45ODk2NTEgMzcyLjg1MTEyOCAKTCAzNTkuMjY0NTY4IDM3Mi44NTExMjggCkwgMzYwLjUzOTQ4NiAzNjcuOTIyNTkyIApMIDM2MS42OTEwMjQgMzcyLjQ0ODY1NCAKTCAzNjIuOTY1OTQyIDM3Mi40NDg2NTQgCkwgMzY0LjE5OTczMyAzNDMuMTA3Mzc2IApMIDM2NS40NzQ2NTEgMzU2LjIwMTk0NCAKTCAzNjYuNzA4NDQyIDM1OC4zNTQ2NDEgCkwgMzY3Ljk4MzM1OSAzNTMuODQxNzM2IApMIDM2OS4yNTgyNzcgMzQ4Ljc1ODMxNiAKTCAzNzAuNDkyMDY4IDM0My4xMzk3NzYgCkwgMzcxLjc2Njk4NSAzNDQuNDQ0MDczIApMIDM3My4wMDA3NzcgMzUzLjU0ODE2NyAKTCAzNzQuMjc1Njk0IDM1NS4xNjI3MDIgCkwgMzc1LjU1MDYxMiAzMzEuNzc0NDA3IApMIDM3Ni43MDIxNSAzMzUuMTQ1NTMxIApMIDM3Ny45NzcwNjggMzMwLjMwMTk3NSAKTCAzNzkuMjEwODU5IDMxNi40MDE5NDIgCkwgMzgwLjQ4NTc3NiAzMTAuMjA4MDE3IApMIDM4MS43MTk1NjcgMzA5LjcwNzI2NSAKTCAzODIuOTk0NDg1IDMwNC4wMDk0NTcgCkwgMzg0LjI2OTQwMiAzMDYuODg5MzggCkwgMzg1LjUwMzE5NCAzMDMuMTA1ODU1IApMIDM4Ni43NzgxMTEgMzExLjYzODY4NSAKTCAzODguMDExOTAyIDMwOS41MDg5NzcgCkwgMzg5LjI4NjgyIDMxNy43NDEyNjEgCkwgMzkwLjU2MTczNyAzMTguMDUzNDE4IApMIDM5MS43NTQ0MDIgMzE2LjE1NTQyOSAKTCAzOTMuMDI5MzIgMjg3Ljg4MDMxNSAKTCAzOTQuMjYzMTExIDI4OS4wMTc2NDggCkwgMzk1LjUzODAyOCAyODkuNTkyNzA2IApMIDM5Ni43NzE4MTkgMjg5LjAwMDA0MyAKTCAzOTYuNzcxODE5IDI4OS4wMDAwNDMgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6IzRjNzJiMDtzdHJva2UtbGluZWNhcDpyb3VuZDtzdHJva2Utd2lkdGg6MS43NTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0icGF0Y2hfMTUiPgogICAgPHBhdGggZD0iTSA1OS4wNCA0OTEuMDQgCkwgNTkuMDQgMjc4LjIwNjA0NSAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF8xNiI+CiAgICA8cGF0aCBkPSJNIDQxMi44NTQyODcgNDkxLjA0IApMIDQxMi44NTQyODcgMjc4LjIwNjA0NSAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF8xNyI+CiAgICA8cGF0aCBkPSJNIDU5LjA0IDQ5MS4wNCAKTCA0MTIuODU0Mjg3IDQ5MS4wNCAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF8xOCI+CiAgICA8cGF0aCBkPSJNIDU5LjA0IDI3OC4yMDYwNDUgCkwgNDEyLjg1NDI4NyAyNzguMjA2MDQ1IAoiIHN0eWxlPSJmaWxsOm5vbmU7Ij48L3BhdGg+CiAgIDwvZz4KICAgPGcgaWQ9ImxlZ2VuZF8zIj4KICAgIDxnIGlkPSJwYXRjaF8xOSI+CiAgICAgPHBhdGggZD0iTSA2Ny40NCAzMDQuODE2MDQ1IApMIDE4Ni41NTY4NzUgMzA0LjgxNjA0NSAKUSAxODguOTU2ODc1IDMwNC44MTYwNDUgMTg4Ljk1Njg3NSAzMDIuNDE2MDQ1IApMIDE4OC45NTY4NzUgMjg2LjYwNjA0NSAKUSAxODguOTU2ODc1IDI4NC4yMDYwNDUgMTg2LjU1Njg3NSAyODQuMjA2MDQ1IApMIDY3LjQ0IDI4NC4yMDYwNDUgClEgNjUuMDQgMjg0LjIwNjA0NSA2NS4wNCAyODYuNjA2MDQ1IApMIDY1LjA0IDMwMi40MTYwNDUgClEgNjUuMDQgMzA0LjgxNjA0NSA2Ny40NCAzMDQuODE2MDQ1IAp6CiIgc3R5bGU9ImZpbGw6I2VhZWFmMjtvcGFjaXR5OjAuODtzdHJva2U6I2NjY2NjYztzdHJva2UtbGluZWpvaW46bWl0ZXI7c3Ryb2tlLXdpZHRoOjAuMzsiPjwvcGF0aD4KICAgIDwvZz4KICAgIDxnIGlkPSJsaW5lMmRfOTIiPgogICAgIDxwYXRoIGQ9Ik0gNjkuODQgMjkzLjQzMTA0NSAKTCA5My44NCAyOTMuNDMxMDQ1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiM0YzcyYjA7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7c3Ryb2tlLXdpZHRoOjEuNzU7Ij48L3BhdGg+CiAgICA8L2c+CiAgICA8ZyBpZD0ibGluZTJkXzkzIj48L2c+CiAgICA8ZyBpZD0idGV4dF80NSI+CiAgICAgPCEtLSBwZXJtbm86IDEwMDU3IC0tPgogICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMDMuNDQgMjk3LjYzMTA0NSlzY2FsZSgwLjEyIC0wLjEyKSI+CiAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEyIj48L3VzZT4KICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxNDQuNTMxMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjI3LjgzMjAzMSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEwIj48L3VzZT4KICAgICAgPHVzZSB4PSIyODMuNDQ3MjY2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTEiPjwvdXNlPgogICAgICA8dXNlIHg9IjMzOS4wNjI1IiB4bGluazpocmVmPSIjQXJpYWxNVC01OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMzY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgICA8dXNlIHg9IjM5NC42Mjg5MDYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPHVzZSB4PSI0NTAuMjQ0MTQxIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTA1Ljg1OTM3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8dXNlIHg9IjU2MS40NzQ2MDkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUzIj48L3VzZT4KICAgICAgPHVzZSB4PSI2MTcuMDg5ODQ0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NSI+PC91c2U+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgPC9nPgogIDxnIGlkPSJheGVzXzQiPgogICA8ZyBpZD0icGF0Y2hfMjAiPgogICAgPHBhdGggZD0iTSA0MzcuNDY1NzEzIDQ5MS4wNCAKTCA3OTEuMjggNDkxLjA0IApMIDc5MS4yOCAyNzguMjA2MDQ1IApMIDQzNy40NjU3MTMgMjc4LjIwNjA0NSAKegoiIHN0eWxlPSJmaWxsOiNlYWVhZjI7Ij48L3BhdGg+CiAgIDwvZz4KICAgPGcgaWQ9Im1hdHBsb3RsaWIuYXhpc183Ij4KICAgIDxnIGlkPSJ4dGlja18yNSI+CiAgICAgPGcgaWQ9ImxpbmUyZF85NCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwMjQ5MTk2MDdmMCkiIGQ9Ik0gNDUwLjY5MjE3OCA0OTEuMDQgCkwgNDUwLjY5MjE3OCAyNzguMjA2MDQ1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfOTUiPjwvZz4KICAgICA8ZyBpZD0idGV4dF80NiI+CiAgICAgIDwhLS0gMTk5MiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQzOS41NzAzMDMgNTA1LjE5NzgxMilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTciPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja18yNiI+CiAgICAgPGcgaWQ9ImxpbmUyZF85NiI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwMjQ5MTk2MDdmMCkiIGQ9Ik0gNDk3LjA1NDYxOSA0OTEuMDQgCkwgNDk3LjA1NDYxOSAyNzguMjA2MDQ1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfOTciPjwvZz4KICAgICA8ZyBpZD0idGV4dF80NyI+CiAgICAgIDwhLS0gMTk5NiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4NS45MzI3NDQgNTA1LjE5NzgxMilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTciPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU0Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja18yNyI+CiAgICAgPGcgaWQ9ImxpbmUyZF85OCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwMjQ5MTk2MDdmMCkiIGQ9Ik0gNTQzLjQxNzA2IDQ5MS4wNCAKTCA1NDMuNDE3MDYgMjc4LjIwNjA0NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzk5Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfNDgiPgogICAgICA8IS0tIDIwMDAgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg1MzIuMjk1MTg1IDUwNS4xOTc4MTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMjgiPgogICAgIDxnIGlkPSJsaW5lMmRfMTAwIj4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3AyNDkxOTYwN2YwKSIgZD0iTSA1ODkuNzc5NTAxIDQ5MS4wNCAKTCA1ODkuNzc5NTAxIDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8xMDEiPjwvZz4KICAgICA8ZyBpZD0idGV4dF80OSI+CiAgICAgIDwhLS0gMjAwNCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDU3OC42NTc2MjYgNTA1LjE5NzgxMilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUyIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja18yOSI+CiAgICAgPGcgaWQ9ImxpbmUyZF8xMDIiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDI0OTE5NjA3ZjApIiBkPSJNIDYzNi4xNDE5NDIgNDkxLjA0IApMIDYzNi4xNDE5NDIgMjc4LjIwNjA0NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzEwMyI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzUwIj4KICAgICAgPCEtLSAyMDA4IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNjI1LjAyMDA2NyA1MDUuMTk3ODEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTYiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzMwIj4KICAgICA8ZyBpZD0ibGluZTJkXzEwNCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwMjQ5MTk2MDdmMCkiIGQ9Ik0gNjgyLjUwNDM4NCA0OTEuMDQgCkwgNjgyLjUwNDM4NCAyNzguMjA2MDQ1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTA1Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfNTEiPgogICAgICA8IS0tIDIwMTIgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2NzEuMzgyNTA5IDUwNS4xOTc4MTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMzEiPgogICAgIDxnIGlkPSJsaW5lMmRfMTA2Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3AyNDkxOTYwN2YwKSIgZD0iTSA3MjguODY2ODI1IDQ5MS4wNCAKTCA3MjguODY2ODI1IDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8xMDciPjwvZz4KICAgICA8ZyBpZD0idGV4dF81MiI+CiAgICAgIDwhLS0gMjAxNiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDcxNy43NDQ5NSA1MDUuMTk3ODEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTQiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzMyIj4KICAgICA8ZyBpZD0ibGluZTJkXzEwOCI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwMjQ5MTk2MDdmMCkiIGQ9Ik0gNzc1LjIyOTI2NiA0OTEuMDQgCkwgNzc1LjIyOTI2NiAyNzguMjA2MDQ1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTA5Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfNTMiPgogICAgICA8IS0tIDIwMjAgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg3NjQuMTA3MzkxIDUwNS4xOTc4MTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgIDwvZz4KICAgPGcgaWQ9Im1hdHBsb3RsaWIuYXhpc184Ij4KICAgIDxnIGlkPSJ5dGlja18xOSI+CiAgICAgPGcgaWQ9ImxpbmUyZF8xMTAiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDI0OTE5NjA3ZjApIiBkPSJNIDQzNy40NjU3MTMgNDY1LjcxODkwMiAKTCA3OTEuMjggNDY1LjcxODkwMiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzExMSI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzU0Ij4KICAgICAgPCEtLSAwIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDI0LjkwNDc3NiA0NjkuMjk3ODA4KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja18yMCI+CiAgICAgPGcgaWQ9ImxpbmUyZF8xMTIiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDI0OTE5NjA3ZjApIiBkPSJNIDQzNy40NjU3MTMgNDIzLjQzNjY5NCAKTCA3OTEuMjggNDIzLjQzNjY5NCAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzExMyI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzU1Ij4KICAgICAgPCEtLSAxIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDI0LjkwNDc3NiA0MjcuMDE1NilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfMjEiPgogICAgIDxnIGlkPSJsaW5lMmRfMTE0Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3AyNDkxOTYwN2YwKSIgZD0iTSA0MzcuNDY1NzEzIDM4MS4xNTQ0ODYgCkwgNzkxLjI4IDM4MS4xNTQ0ODYgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8xMTUiPjwvZz4KICAgICA8ZyBpZD0idGV4dF81NiI+CiAgICAgIDwhLS0gMiAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQyNC45MDQ3NzYgMzg0LjczMzM5MilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfMjIiPgogICAgIDxnIGlkPSJsaW5lMmRfMTE2Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3AyNDkxOTYwN2YwKSIgZD0iTSA0MzcuNDY1NzEzIDMzOC44NzIyNzggCkwgNzkxLjI4IDMzOC44NzIyNzggCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8xMTciPjwvZz4KICAgICA8ZyBpZD0idGV4dF81NyI+CiAgICAgIDwhLS0gMyAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQyNC45MDQ3NzYgMzQyLjQ1MTE4NClzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MSI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfMjMiPgogICAgIDxnIGlkPSJsaW5lMmRfMTE4Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3AyNDkxOTYwN2YwKSIgZD0iTSA0MzcuNDY1NzEzIDI5Ni41OTAwNyAKTCA3OTEuMjggMjk2LjU5MDA3IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTE5Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfNTgiPgogICAgICA8IS0tIDQgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0MjQuOTA0Nzc2IDMwMC4xNjg5NzYpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTIiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgIDxnIGlkPSJsaW5lMmRfMTIwIj4KICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwMjQ5MTk2MDdmMCkiIGQ9Ik0gNDUzLjU0ODE4MSA0NDcuOTg3NjQ3IApMIDQ1NC41MDAxODIgNDU1LjE5NDg2MSAKTCA0NTYuNDM1OTE3IDQ3Mi42MzEwMjggCkwgNDU3LjQxOTY1MSA0NjguMDM1MTIyIApMIDQ1OC40MDMzODUgNDY3LjIwNjA1MiAKTCA0NTkuMzU1Mzg2IDQ2My45NTM1NzggCkwgNDYwLjMzOTEyIDQ2NS40NjM2NDUgCkwgNDYxLjI5MTEyMSA0NzMuMjkzNjc1IApMIDQ2My4yNTg1ODkgNDczLjI5MzY3NSAKTCA0NjUuMTMwODU4IDQ4MS4zNjU3MjkgCkwgNDY2LjA4Mjg1OCA0NjQuOTIyNjQ0IApMIDQ2Ny4wNjY1OTMgNDU2LjQ2NjIwMiAKTCA0NjguMDE4NTkzIDQ2Mi4xMDM4MTYgCkwgNDY5LjAwMjMyOCA0NTMuOTcyNjA5IApMIDQ2OS45ODYwNjIgNDU1LjMzNjU0OCAKTCA0NzAuOTM4MDYzIDQ1OC4xNTUzNzYgCkwgNDcxLjkyMTc5NyA0NDcuNTg0ODI0IApMIDQ3Mi44NzM3OTggNDUzLjYyNTEzNCAKTCA0NzMuODU3NTMyIDQ0MC45NDA0NzEgCkwgNDc0Ljg0MTI2NiA0MzcuNjg3OTk3IApMIDQ3NS43Mjk4IDQzMi42NTQzODUgCkwgNDc2LjcxMzUzNSA0MzkuODUxMzY2IApMIDQ3Ny42NjU1MzUgNDM0LjQzMDU3NiAKTCA0NzguNjQ5MjcgNDQxLjE1NzI5NCAKTCA0NzkuNjAxMjcgNDQyLjMwMDA1NiAKTCA0ODAuNTg1MDA1IDQ0Ni45OTgwNzQgCkwgNDgxLjU2ODczOSA0NDguMzE5MzkzIApMIDQ4Mi41MjA3NCA0NDEuNDk5Njk2IApMIDQ4My41MDQ0NzQgNDQxLjQ5OTY5NiAKTCA0ODQuNDU2NDc1IDQzOS4xNTA2NjUgCkwgNDg1LjQ0MDIwOSA0NDEuMzc2MDYyIApMIDQ4Ni40MjM5NDMgNDUwLjc3MjA5OSAKTCA0ODcuMzEyNDc3IDQ0Ny43NTE5MjQgCkwgNDg4LjI5NjIxMSA0NDQuOTMzMDk2IApMIDQ4OS4yNDgyMTIgNDUyLjg2MTAxIApMIDQ5MC4yMzE5NDcgNDQ2LjM1NjA2MSAKTCA0OTEuMTgzOTQ3IDQ1My40MDMxMSAKTCA0OTIuMTY3NjgyIDQ1OC40NzY5NzUgCkwgNDkzLjE1MTQxNiA0NTguNDc2OTc1IApMIDQ5NC4xMDM0MTcgNDU5LjQzNzkyMiAKTCA0OTUuMDg3MTUxIDQ2NC4zNTQ0NTUgCkwgNDk2LjAzOTE1MiA0NjYuNTc5ODUzIApMIDQ5Ny4wMjI4ODYgNDYxLjg4MTgzNCAKTCA0OTguMDA2NjIgNDYxLjg4MTgzNCAKTCA0OTguOTI2ODg4IDQ1My40MjUzOTIgCkwgNDk5LjkxMDYyMiA0NTYuOTQ4ODk2IApMIDUwMC44NjI2MjMgNDU2Ljk0ODg5NiAKTCA1MDEuODQ2MzU3IDQ0MS41NzM1NjMgCkwgNTAyLjc5ODM1OCA0NTEuNDM5Mzk3IApMIDUwMy43ODIwOTIgNDU1LjExNjEzMSAKTCA1MDQuNzY1ODI2IDQ2Mi4xNjMxOCAKTCA1MDUuNzE3ODI3IDQ1OC41MzkwMDMgCkwgNTA2LjcwMTU2MSA0NjUuMjE1MTUyIApMIDUwNy42NTM1NjIgNDU5LjkyOTg3NiAKTCA1MDguNjM3Mjk2IDQ2Mi4yNzg5MDYgCkwgNTA5LjYyMTAzIDQ0OS44NDI5NDggCkwgNTEwLjUwOTU2NCA0NDkuODQyOTQ4IApMIDUxMi40NDUzIDQ1My43NzgzMjIgCkwgNTEzLjQyOTAzNCA0NDEuMDkzNjYgCkwgNTE0LjM4MTAzNSA0MzcuODQxMTg1IApMIDUxNS4zNjQ3NjkgNDI4Ljc4MDcgCkwgNTE2LjM0ODUwMyA0MzIuNTExNDcxIApMIDUxNy4zMDA1MDQgNDMxLjE0NzUzMSAKTCA1MTguMjg0MjM4IDQyMC41NzY5NzkgCkwgNTE5LjIzNjIzOSA0MjUuODYyMjU1IApMIDUyMC4yMTk5NzMgNDE0Ljk4OTY4MSAKTCA1MjEuMjAzNzA3IDQxNC4wMjg3MzQgCkwgNTIyLjA5MjI0MSA0MTQuOTY4MzI5IApMIDUyMy4wNzU5NzYgNDE4LjgxMjE2MiAKTCA1MjUuMDExNzExIDQxNC42ODQ2MTUgCkwgNTI1Ljk2MzcxMiA0MjAuNDUwMzg2IApMIDUyNi45NDc0NDYgNDE0Ljg4NjkzNiAKTCA1MjcuOTMxMTggNDE0Ljg4NjkzNiAKTCA1MjguODgzMTgxIDQxNy44MzY4MzggCkwgNTI5Ljg2NjkxNSA0MjYuMjkzMjggCkwgNTMwLjgxODkxNiA0MTQuNDAxNDA5IApMIDUzMS44MDI2NSAzOTMuNzc1OTM2IApMIDUzMi43ODYzODQgMzg3LjUzNzU3NyAKTCA1MzMuNjc0OTE4IDQwNS42NTg1MDUgCkwgNTM0LjY1ODY1MyAzODAuMjg5MTgxIApMIDUzNS42MTA2NTMgMzkyLjE4MTA1MiAKTCA1MzYuNTk0Mzg4IDM3NS42MzU4NTQgCkwgNjM0LjE3NDQ3NCAzNDcuNjQ3NCAKTCA2MzUuMTI2NDc1IDM1MS41ODgzMTQgCkwgNjM2LjExMDIwOSAzNTIuMzc4NjUzIApMIDYzNy4wOTM5NDMgMzU2LjgwODIyMSAKTCA2MzguMDE0MjExIDM1MC41MTA4NzggCkwgNjM4Ljk5Nzk0NSAzNTMuMzI5NzA2IApMIDYzOS45NDk5NDYgMzYxLjcxOTA0NiAKTCA2NDAuOTMzNjggMzU4LjgyMDAwOSAKTCA2NDEuODg1NjgxIDM3Mi41MDI3MDEgCkwgNjQyLjg2OTQxNSAzNjUuNTc4MjcgCkwgNjQzLjg1MzE0OSAzNjguNjY2NTIgCkwgNjQ0LjgwNTE1IDM3Ni40NTE4MTYgCkwgNjQ1Ljc4ODg4NCAzOTAuNjAwNzEyIApMIDY0Ni43NDA4ODUgNDAxLjk3NDg3OSAKTCA2NDcuNzI0NjE5IDM4Ni43NTMyODUgCkwgNjQ4LjcwODM1NCAzOTQuODM2NjI4IApMIDY0OS41OTY4ODggNDEwLjk4MDczNiAKTCA2NTAuNTgwNjIyIDQxMC45ODA3MzYgCkwgNjUxLjUzMjYyMyA0MDMuNTE5MTUzIApMIDY1Mi41MTYzNTcgNDA0Ljc4NzYxOSAKTCA2NTMuNDY4MzU4IDM5OS4xMjA5MTUgCkwgNjU0LjQ1MjA5MiA0MDUuMjcxMDc0IApMIDY1NS40MzU4MjYgMzkxLjk1NjY2IApMIDY1Ni4zODc4MjcgMzg1Ljc5OTA2IApMIDY1Ny4zNzE1NjEgMzgzLjI5MDc5NSAKTCA2NTguMzIzNTYyIDM4Ni45NTUyNjcgCkwgNjU5LjMwNzI5NiAzODUuNzIwNzUzIApMIDY2MC4yOTEwMzEgMzg2LjkyMDI1NyAKTCA2NjEuMTc5NTY1IDM3OS4yMDQ1MTUgCkwgNjYyLjE2MzI5OSAzNjIuNzU4ODA4IApMIDY2My4xMTUzIDM1Ni44NDE0NTUgCkwgNjY0LjA5OTAzNCAzNTcuNzQ4MTEzIApMIDY2NS4wNTEwMzUgMzQ2LjYzMDA5MSAKTCA2NjYuMDM0NzY5IDM1MC4yMzEzOTMgCkwgNjY3LjAxODUwMyAzNTMuMTQ3NDI4IApMIDY2Ny45NzA1MDQgMzM3LjMzMDc1MyAKTCA2NjguOTU0MjM4IDMzMy40NTU4NDIgCkwgNjY5LjkwNjIzOSAzMzIuOTMzODI2IApMIDY3MC44ODk5NzMgMzMxLjA3NzUxIApMIDY3MS44NzM3MDggMzI5LjY5NDQ1OSAKTCA2NzIuNzYyMjQyIDMzMi4xMDcwNCAKTCA2NzMuNzQ1OTc2IDMyMi42NDk5MDUgCkwgNjc0LjY5Nzk3NyAzMTYuODQ2NDYxIApMIDY3NS42ODE3MTEgMzE3LjIxMDk3NiAKTCA2NzcuNjE3NDQ2IDI5Ni44MDI2MjIgCkwgNjc4LjYwMTE4IDI5OC4xODY1NjEgCkwgNjc5LjU1MzE4MSAzMDAuNTA1NDAyIApMIDY4MC41MzY5MTUgMjk5LjI1MjU4IApMIDY4MS40ODg5MTYgMzAyLjI0Mzc1MSAKTCA2ODIuNDcyNjUgMzAzLjc3MTM2NCAKTCA2ODMuNDU2Mzg0IDMwNC45MDM0MjggCkwgNjg0LjM3NjY1MiAzMDEuNDcyMDE2IApMIDY4NS4zNjAzODYgMzAzLjUxNjE5MSAKTCA2OTMuMTAzMzI2IDMxMy45Mzk3NyAKTCA2OTQuMDg3MDYxIDMxNS40ODUyMjcgCkwgNjk1LjA3MDc5NSAzMTMuMTQ5MTc4IApMIDY5NS45NTkzMjkgMzEwLjMwMDgzNyAKTCA2OTYuOTQzMDYzIDMxMy43OTkwMTMgCkwgNjk3Ljg5NTA2NCAzMTcuNzE4MjM1IApMIDY5OC44Nzg3OTggMzMxLjkyMzA3IApMIDY5OS44MzA3OTkgMzM3LjE3NzA1NyAKTCA3MDAuODE0NTMzIDM0Ny4zMTkwNzkgCkwgNzAxLjc5ODI2NyAzMzYuMDQzODEgCkwgNzAyLjc1MDI2OCAzMzQuMjYzNTE3IApMIDcwMy43MzQwMDIgMzQxLjA5Njk5OCAKTCA3MDQuNjg2MDAzIDM0Mi40NTU0NDEgCkwgNzA2LjY1MzQ3MiAzNDguNDU3NTcgCkwgNzA3LjU0MjAwNiAzNDEuMTM5NDkyIApMIDcwOC41MjU3NCAzNDYuMTY0ODE3IApMIDcwOS40Nzc3NDEgMzM1LjM0ODQzNiAKTCA3MTEuNDEzNDc2IDM1Ny43MjM2NzMgCkwgNzEyLjM5NzIxIDM1NS4xMTcyMjkgCkwgNzE0LjMzMjk0NSAzNjAuMTc4NzQ4IApMIDcxNS4zMTY2NzkgMzY2Ljk2ODU5NCAKTCA3MTYuMjY4NjggMzU5LjYxNTE2OCAKTCA3MTcuMjUyNDE0IDM2My42ODY3NzYgCkwgNzE4LjIzNjE0OSAzNTMuNjM2MDgzIApMIDcxOS4xMjQ2ODMgMzU2LjcxNjI1OCAKTCA3MjAuMTA4NDE3IDM1My45OTgxMDQgCkwgNzIxLjA2MDQxOCAzNTkuMzg5ODA0IApMIDcyMi4wNDQxNTIgMzg4LjY2MjExNSAKTCA3MjIuOTk2MTUzIDM4My43MjU2NjcgCkwgNzIzLjk3OTg4NyAzOTAuMDM5MTE5IApMIDcyNC45NjM2MjEgNDAyLjY0NTg5OCAKTCA3MjUuOTE1NjIyIDM4OS40Mzk2NDIgCkwgNzI2Ljg5OTM1NiAzODguMjMxNTk3IApMIDcyNy44NTEzNTcgMzg3LjMzODk3OCAKTCA3MjguODM1MDkxIDM5MS42NjM4MTMgCkwgNzI5LjgxODgyNiAzODIuNjk0ODY5IApMIDczMC43MzkwOTMgMzYxLjU1Mzc2NSAKTCA3MzEuNzIyODI3IDM2OS4zMDU0ODkgCkwgNzMyLjY3NDgyOCAzNjQuMzI2NTQ4IApMIDczMy42NTg1NjIgMzY1LjY5Mjk4MiAKTCA3MzQuNjEwNTYzIDM0OS43Mzc0MSAKTCA3MzUuNTk0Mjk3IDM0Mi43ODY4OTEgCkwgNzM2LjU3ODAzMiAzNDIuNzg2ODkxIApMIDczNy41MzAwMzIgMzQzLjI4NDM0MiAKTCA3MzguNTEzNzY3IDMzOC43NTQwOTkgCkwgNzM5LjQ2NTc2NyAzMzcuODQ0ODIgCkwgNzQwLjQ0OTUwMiAzMjQuOTM3NjI2IApMIDc0MS40MzMyMzYgMzI0LjkzNzYyNiAKTCA3NDIuMzIxNzcgMzIwLjE2MzgzOCAKTCA3NDMuMzA1NTA0IDMxNi43OTM1MjMgCkwgNzQ0LjI1NzUwNSAzMTIuNTM2OTMxIApMIDc0NS4yNDEyMzkgMzEyLjI3OTA5NCAKTCA3NDYuMTkzMjQgMzExLjc2NjU5MiAKTCA3NDcuMTc2OTc0IDMxMS41MjEwMTcgCkwgNzQ4LjE2MDcwOCAzMjAuMzIzODM0IApMIDc0OS4xMTI3MDkgMzIwLjAwNTkxNCAKTCA3NTAuMDk2NDQzIDMzMy44ODk2MTYgCkwgNzUxLjA0ODQ0NCAzMjcuMzEyMzY0IApMIDc1Mi4wMzIxNzkgMzMxLjc0Mzg3OCAKTCA3NTMuMDE1OTEzIDMyOC4zODMxMTkgCkwgNzUzLjkwNDQ0NyAzMzEuNTM4NTEzIApMIDc1NC44ODgxODEgMzM2LjA4NDk5MiAKTCA3NTUuODQwMTgyIDMzNS41NzU1NzYgCkwgNzU2LjgyMzkxNiAzMzcuMDg1NjQzIApMIDc1Ny43NzU5MTcgMzQxLjc4MzY2MiAKTCA3NTguNzU5NjUxIDM0Mi4wMDY4MjcgCkwgNzU5Ljc0MzM4NSAzNDQuNzY5NzU4IApMIDc2MC42OTUzODYgMzQ2LjYzMzA5MyAKTCA3NjEuNjc5MTIgMzU0Ljc1Mzg1NiAKTCA3NjIuNjMxMTIxIDM1Ny43MjI2MTYgCkwgNzYzLjYxNDg1NSAzNTkuNTUyMTY4IApMIDc2NC41OTg1OSAzNjMuMDA5MDM0IApMIDc2NS40ODcxMjQgMzYwLjI0NTYzOCAKTCA3NjYuNDcwODU4IDM2Mi4zMDM4MDkgCkwgNzY3LjQyMjg1OSAzNjAuODYxNDc4IApMIDc2OC40MDY1OTMgMzM0LjM2MTA2MiAKTCA3NjkuMzU4NTk0IDMwMC4zMDA0MTggCkwgNzcwLjM0MjMyOCAzMTYuMzAyNTg1IApMIDc3MS4zMjYwNjIgMjkyLjY0OTY2NCAKTCA3NzIuMjc4MDYzIDI5NC42NjMxIApMIDc3My4yNjE3OTcgMjkxLjg0NDI3MiAKTCA3NzQuMjEzNzk4IDI4Ny44ODAzMTUgCkwgNzc1LjE5NzUzMiAyODkuMzkwMzgyIApMIDc3NS4xOTc1MzIgMjg5LjM5MDM4MiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojNGM3MmIwO3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF8yMSI+CiAgICA8cGF0aCBkPSJNIDQzNy40NjU3MTMgNDkxLjA0IApMIDQzNy40NjU3MTMgMjc4LjIwNjA0NSAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF8yMiI+CiAgICA8cGF0aCBkPSJNIDc5MS4yOCA0OTEuMDQgCkwgNzkxLjI4IDI3OC4yMDYwNDUgCiIgc3R5bGU9ImZpbGw6bm9uZTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0icGF0Y2hfMjMiPgogICAgPHBhdGggZD0iTSA0MzcuNDY1NzEzIDQ5MS4wNCAKTCA3OTEuMjggNDkxLjA0IAoiIHN0eWxlPSJmaWxsOm5vbmU7Ij48L3BhdGg+CiAgIDwvZz4KICAgPGcgaWQ9InBhdGNoXzI0Ij4KICAgIDxwYXRoIGQ9Ik0gNDM3LjQ2NTcxMyAyNzguMjA2MDQ1IApMIDc5MS4yOCAyNzguMjA2MDQ1IAoiIHN0eWxlPSJmaWxsOm5vbmU7Ij48L3BhdGg+CiAgIDwvZz4KICAgPGcgaWQ9ImxlZ2VuZF80Ij4KICAgIDxnIGlkPSJwYXRjaF8yNSI+CiAgICAgPHBhdGggZD0iTSA0NDUuODY1NzEzIDMwNC44MTYwNDUgCkwgNTY0Ljk4MjU4OCAzMDQuODE2MDQ1IApRIDU2Ny4zODI1ODggMzA0LjgxNjA0NSA1NjcuMzgyNTg4IDMwMi40MTYwNDUgCkwgNTY3LjM4MjU4OCAyODYuNjA2MDQ1IApRIDU2Ny4zODI1ODggMjg0LjIwNjA0NSA1NjQuOTgyNTg4IDI4NC4yMDYwNDUgCkwgNDQ1Ljg2NTcxMyAyODQuMjA2MDQ1IApRIDQ0My40NjU3MTMgMjg0LjIwNjA0NSA0NDMuNDY1NzEzIDI4Ni42MDYwNDUgCkwgNDQzLjQ2NTcxMyAzMDIuNDE2MDQ1IApRIDQ0My40NjU3MTMgMzA0LjgxNjA0NSA0NDUuODY1NzEzIDMwNC44MTYwNDUgCnoKIiBzdHlsZT0iZmlsbDojZWFlYWYyO29wYWNpdHk6MC44O3N0cm9rZTojY2NjY2NjO3N0cm9rZS1saW5lam9pbjptaXRlcjtzdHJva2Utd2lkdGg6MC4zOyI+PC9wYXRoPgogICAgPC9nPgogICAgPGcgaWQ9ImxpbmUyZF8xMjEiPgogICAgIDxwYXRoIGQ9Ik0gNDQ4LjI2NTcxMyAyOTMuNDMxMDQ1IApMIDQ3Mi4yNjU3MTMgMjkzLjQzMTA0NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojNGM3MmIwO3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICAgPC9nPgogICAgPGcgaWQ9ImxpbmUyZF8xMjIiPjwvZz4KICAgIDxnIGlkPSJ0ZXh0XzU5Ij4KICAgICA8IS0tIHBlcm1ubzogMTAwMjggLS0+CiAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MS44NjU3MTMgMjk3LjYzMTA0NSlzY2FsZSgwLjEyIC0wLjEyKSI+CiAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEyIj48L3VzZT4KICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxNDQuNTMxMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjI3LjgzMjAzMSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEwIj48L3VzZT4KICAgICAgPHVzZSB4PSIyODMuNDQ3MjY2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTEiPjwvdXNlPgogICAgICA8dXNlIHg9IjMzOS4wNjI1IiB4bGluazpocmVmPSIjQXJpYWxNVC01OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMzY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgICA8dXNlIHg9IjM5NC42Mjg5MDYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPHVzZSB4PSI0NTAuMjQ0MTQxIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTA1Ljg1OTM3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8dXNlIHg9IjU2MS40NzQ2MDkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgPHVzZSB4PSI2MTcuMDg5ODQ0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NiI+PC91c2U+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgPC9nPgogIDxnIGlkPSJ0ZXh0XzYwIj4KICAgPCEtLSBEYXRlIC0tPgogICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzU3LjQwNjg3NSA1NDguNjQpc2NhbGUoMC4xMiAtMC4xMikiPgogICAgPGRlZnM+CiAgICAgPHBhdGggZD0iTSA3LjcxODc1IDAgCkwgNy43MTg3NSA3MS41NzgxMjUgCkwgMzIuMzc1IDcxLjU3ODEyNSAKUSA0MC43MTg3NSA3MS41NzgxMjUgNDUuMTI1IDcwLjU2MjUgClEgNTEuMjY1NjI1IDY5LjE0MDYyNSA1NS42MDkzNzUgNjUuNDM3NSAKUSA2MS4yODEyNSA2MC42NDA2MjUgNjQuMDc4MTI1IDUzLjE4NzUgClEgNjYuODkwNjI1IDQ1Ljc1IDY2Ljg5MDYyNSAzNi4xODc1IApRIDY2Ljg5MDYyNSAyOC4wMzEyNSA2NC45ODQzNzUgMjEuNzM0Mzc1IApRIDYzLjA5Mzc1IDE1LjQzNzUgNjAuMTA5Mzc1IDExLjI5Njg3NSAKUSA1Ny4xMjUgNy4xNzE4NzUgNTMuNTc4MTI1IDQuNzk2ODc1IApRIDUwLjA0Njg3NSAyLjQzNzUgNDUuMDQ2ODc1IDEuMjE4NzUgClEgNDAuMDQ2ODc1IDAgMzMuNTQ2ODc1IDAgCnoKTSAxNy4xODc1IDguNDUzMTI1IApMIDMyLjQ2ODc1IDguNDUzMTI1IApRIDM5LjU0Njg3NSA4LjQ1MzEyNSA0My41NzgxMjUgOS43NjU2MjUgClEgNDcuNjA5Mzc1IDExLjA3ODEyNSA1MCAxMy40ODQzNzUgClEgNTMuMzc1IDE2Ljg0Mzc1IDU1LjI1IDIyLjUzMTI1IApRIDU3LjEyNSAyOC4yMTg3NSA1Ny4xMjUgMzYuMzI4MTI1IApRIDU3LjEyNSA0Ny41NjI1IDUzLjQzNzUgNTMuNTkzNzUgClEgNDkuNzUgNTkuNjI1IDQ0LjQ4NDM3NSA2MS42NzE4NzUgClEgNDAuNjcxODc1IDYzLjE0MDYyNSAzMi4yMzQzNzUgNjMuMTQwNjI1IApMIDE3LjE4NzUgNjMuMTQwNjI1IAp6CiIgaWQ9IkFyaWFsTVQtNjgiPjwvcGF0aD4KICAgICA8cGF0aCBkPSJNIDQwLjQzNzUgNi4zOTA2MjUgClEgMzUuNTQ2ODc1IDIuMjUgMzEuMDMxMjUgMC41MzEyNSAKUSAyNi41MTU2MjUgLTEuMTcxODc1IDIxLjM0Mzc1IC0xLjE3MTg3NSAKUSAxMi43OTY4NzUgLTEuMTcxODc1IDguMjAzMTI1IDMgClEgMy42MDkzNzUgNy4xNzE4NzUgMy42MDkzNzUgMTMuNjcxODc1IApRIDMuNjA5Mzc1IDE3LjQ4NDM3NSA1LjM0Mzc1IDIwLjYyNSAKUSA3LjA3ODEyNSAyMy43ODEyNSA5Ljg5MDYyNSAyNS42ODc1IApRIDEyLjcwMzEyNSAyNy41OTM3NSAxNi4yMTg3NSAyOC41NjI1IApRIDE4Ljc5Njg3NSAyOS4yNSAyNC4wMzEyNSAyOS44OTA2MjUgClEgMzQuNjcxODc1IDMxLjE1NjI1IDM5LjcwMzEyNSAzMi45MDYyNSAKUSAzOS43NSAzNC43MTg3NSAzOS43NSAzNS4yMDMxMjUgClEgMzkuNzUgNDAuNTc4MTI1IDM3LjI1IDQyLjc4MTI1IApRIDMzLjg5MDYyNSA0NS43NSAyNy4yNSA0NS43NSAKUSAyMS4wNDY4NzUgNDUuNzUgMTguMDkzNzUgNDMuNTc4MTI1IApRIDE1LjE0MDYyNSA0MS40MDYyNSAxMy43MTg3NSAzNS44OTA2MjUgCkwgNS4xMjUgMzcuMDYyNSAKUSA2LjI5Njg3NSA0Mi41NzgxMjUgOC45ODQzNzUgNDUuOTY4NzUgClEgMTEuNjcxODc1IDQ5LjM1OTM3NSAxNi43NSA1MS4xODc1IApRIDIxLjgyODEyNSA1My4wMzEyNSAyOC41MTU2MjUgNTMuMDMxMjUgClEgMzUuMTU2MjUgNTMuMDMxMjUgMzkuMjk2ODc1IDUxLjQ2ODc1IApRIDQzLjQ1MzEyNSA0OS45MDYyNSA0NS40MDYyNSA0Ny41MzEyNSAKUSA0Ny4zNTkzNzUgNDUuMTcxODc1IDQ4LjE0MDYyNSA0MS41NDY4NzUgClEgNDguNTc4MTI1IDM5LjMxMjUgNDguNTc4MTI1IDMzLjQ1MzEyNSAKTCA0OC41NzgxMjUgMjEuNzM0Mzc1IApRIDQ4LjU3ODEyNSA5LjQ2ODc1IDQ5LjE0MDYyNSA2LjIxODc1IApRIDQ5LjcwMzEyNSAyLjk4NDM3NSA1MS4zNzUgMCAKTCA0Mi4xODc1IDAgClEgNDAuODI4MTI1IDIuNzM0Mzc1IDQwLjQzNzUgNi4zOTA2MjUgCnoKTSAzOS43MDMxMjUgMjYuMDMxMjUgClEgMzQuOTA2MjUgMjQuMDc4MTI1IDI1LjM0Mzc1IDIyLjcwMzEyNSAKUSAxOS45MjE4NzUgMjEuOTIxODc1IDE3LjY3MTg3NSAyMC45Mzc1IApRIDE1LjQzNzUgMTkuOTY4NzUgMTQuMjAzMTI1IDE4LjA5Mzc1IApRIDEyLjk4NDM3NSAxNi4yMTg3NSAxMi45ODQzNzUgMTMuOTIxODc1IApRIDEyLjk4NDM3NSAxMC40MDYyNSAxNS42NDA2MjUgOC4wNjI1IApRIDE4LjMxMjUgNS43MTg3NSAyMy40Mzc1IDUuNzE4NzUgClEgMjguNTE1NjI1IDUuNzE4NzUgMzIuNDY4NzUgNy45Mzc1IApRIDM2LjQyMTg3NSAxMC4xNTYyNSAzOC4yODEyNSAxNC4wMTU2MjUgClEgMzkuNzAzMTI1IDE3IDM5LjcwMzEyNSAyMi43OTY4NzUgCnoKIiBpZD0iQXJpYWxNVC05NyI+PC9wYXRoPgogICAgIDxwYXRoIGQ9Ik0gMjUuNzgxMjUgNy44NTkzNzUgCkwgMjcuMDQ2ODc1IDAuMDkzNzUgClEgMjMuMzQzNzUgLTAuNjg3NSAyMC40MDYyNSAtMC42ODc1IApRIDE1LjYyNSAtMC42ODc1IDEyLjk4NDM3NSAwLjgyODEyNSAKUSAxMC4zNTkzNzUgMi4zNDM3NSA5LjI4MTI1IDQuODEyNSAKUSA4LjIwMzEyNSA3LjI4MTI1IDguMjAzMTI1IDE1LjE4NzUgCkwgOC4yMDMxMjUgNDUuMDE1NjI1IApMIDEuNzY1NjI1IDQ1LjAxNTYyNSAKTCAxLjc2NTYyNSA1MS44NTkzNzUgCkwgOC4yMDMxMjUgNTEuODU5Mzc1IApMIDguMjAzMTI1IDY0LjcwMzEyNSAKTCAxNi45Mzc1IDY5Ljk2ODc1IApMIDE2LjkzNzUgNTEuODU5Mzc1IApMIDI1Ljc4MTI1IDUxLjg1OTM3NSAKTCAyNS43ODEyNSA0NS4wMTU2MjUgCkwgMTYuOTM3NSA0NS4wMTU2MjUgCkwgMTYuOTM3NSAxNC43MDMxMjUgClEgMTYuOTM3NSAxMC45Mzc1IDE3LjQwNjI1IDkuODU5Mzc1IApRIDE3Ljg3NSA4Ljc5Njg3NSAxOC45MjE4NzUgOC4xNTYyNSAKUSAxOS45Njg3NSA3LjUxNTYyNSAyMS45MjE4NzUgNy41MTU2MjUgClEgMjMuMzkwNjI1IDcuNTE1NjI1IDI1Ljc4MTI1IDcuODU5Mzc1IAp6CiIgaWQ9IkFyaWFsTVQtMTE2Ij48L3BhdGg+CiAgICA8L2RlZnM+CiAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTY4Ij48L3VzZT4KICAgIDx1c2UgeD0iNzIuMjE2Nzk3IiB4bGluazpocmVmPSIjQXJpYWxNVC05NyI+PC91c2U+CiAgICA8dXNlIHg9IjEyNy44MzIwMzEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNiI+PC91c2U+CiAgICA8dXNlIHg9IjE1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgIDwvZz4KICA8L2c+CiAgPGcgaWQ9InRleHRfNjEiPgogICA8IS0tIEN1bXVsYXRpdmUgUmV0dXJucyAoQWJzb2x1dGUpIC0tPgogICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTUuOTM1NjI1IDM2NS4zNzU2MjUpcm90YXRlKC05MClzY2FsZSgwLjEyIC0wLjEyKSI+CiAgICA8ZGVmcz4KICAgICA8cGF0aCBkPSJNIDU4Ljc5Njg3NSAyNS4wOTM3NSAKTCA2OC4yNjU2MjUgMjIuNzAzMTI1IApRIDY1LjI4MTI1IDExLjAzMTI1IDU3LjU0Njg3NSA0LjkwNjI1IApRIDQ5LjgxMjUgLTEuMjE4NzUgMzguNjI1IC0xLjIxODc1IApRIDI3LjA0Njg3NSAtMS4yMTg3NSAxOS43OTY4NzUgMy40ODQzNzUgClEgMTIuNTQ2ODc1IDguMjAzMTI1IDguNzY1NjI1IDE3LjE0MDYyNSAKUSA0Ljk4NDM3NSAyNi4wNzgxMjUgNC45ODQzNzUgMzYuMzI4MTI1IApRIDQuOTg0Mzc1IDQ3LjUxNTYyNSA5LjI1IDU1LjgyODEyNSAKUSAxMy41MzEyNSA2NC4xNTYyNSAyMS40MDYyNSA2OC40Njg3NSAKUSAyOS4yOTY4NzUgNzIuNzk2ODc1IDM4Ljc2NTYyNSA3Mi43OTY4NzUgClEgNDkuNTE1NjI1IDcyLjc5Njg3NSA1Ni44MjgxMjUgNjcuMzI4MTI1IApRIDY0LjE1NjI1IDYxLjg1OTM3NSA2Ny4wNDY4NzUgNTEuOTUzMTI1IApMIDU3LjcxODc1IDQ5Ljc1IApRIDU1LjIxODc1IDU3LjU2MjUgNTAuNDg0Mzc1IDYxLjEyNSAKUSA0NS43NSA2NC43MDMxMjUgMzguNTc4MTI1IDY0LjcwMzEyNSAKUSAzMC4zMjgxMjUgNjQuNzAzMTI1IDI0Ljc4MTI1IDYwLjczNDM3NSAKUSAxOS4yMzQzNzUgNTYuNzgxMjUgMTYuOTg0Mzc1IDUwLjEwOTM3NSAKUSAxNC43NSA0My40NTMxMjUgMTQuNzUgMzYuMzc1IApRIDE0Ljc1IDI3LjI1IDE3LjQwNjI1IDIwLjQzNzUgClEgMjAuMDYyNSAxMy42MjUgMjUuNjcxODc1IDEwLjI1IApRIDMxLjI5Njg3NSA2Ljg5MDYyNSAzNy44NDM3NSA2Ljg5MDYyNSAKUSA0NS43OTY4NzUgNi44OTA2MjUgNTEuMzEyNSAxMS40Njg3NSAKUSA1Ni44NDM3NSAxNi4wNjI1IDU4Ljc5Njg3NSAyNS4wOTM3NSAKegoiIGlkPSJBcmlhbE1ULTY3Ij48L3BhdGg+CiAgICAgPHBhdGggZD0iTSA0MC41NzgxMjUgMCAKTCA0MC41NzgxMjUgNy42MjUgClEgMzQuNTE1NjI1IC0xLjE3MTg3NSAyNC4xMjUgLTEuMTcxODc1IApRIDE5LjUzMTI1IC0xLjE3MTg3NSAxNS41NDY4NzUgMC41NzgxMjUgClEgMTEuNTc4MTI1IDIuMzQzNzUgOS42NDA2MjUgNSAKUSA3LjcxODc1IDcuNjcxODc1IDYuOTM3NSAxMS41MzEyNSAKUSA2LjM5MDYyNSAxNC4xMDkzNzUgNi4zOTA2MjUgMTkuNzM0Mzc1IApMIDYuMzkwNjI1IDUxLjg1OTM3NSAKTCAxNS4xODc1IDUxLjg1OTM3NSAKTCAxNS4xODc1IDIzLjA5Mzc1IApRIDE1LjE4NzUgMTYuMjE4NzUgMTUuNzE4NzUgMTMuODEyNSAKUSAxNi41NDY4NzUgMTAuMzU5Mzc1IDE5LjIzNDM3NSA4LjM3NSAKUSAyMS45MjE4NzUgNi4zOTA2MjUgMjUuODc1IDYuMzkwNjI1IApRIDI5LjgyODEyNSA2LjM5MDYyNSAzMy4yOTY4NzUgOC40MjE4NzUgClEgMzYuNzY1NjI1IDEwLjQ1MzEyNSAzOC4yMDMxMjUgMTMuOTM3NSAKUSAzOS42NTYyNSAxNy40Mzc1IDM5LjY1NjI1IDI0LjA3ODEyNSAKTCAzOS42NTYyNSA1MS44NTkzNzUgCkwgNDguNDM3NSA1MS44NTkzNzUgCkwgNDguNDM3NSAwIAp6CiIgaWQ9IkFyaWFsTVQtMTE3Ij48L3BhdGg+CiAgICAgPHBhdGggZD0iTSA2LjM5MDYyNSAwIApMIDYuMzkwNjI1IDcxLjU3ODEyNSAKTCAxNS4xODc1IDcxLjU3ODEyNSAKTCAxNS4xODc1IDAgCnoKIiBpZD0iQXJpYWxNVC0xMDgiPjwvcGF0aD4KICAgICA8cGF0aCBkPSJNIDYuNjQwNjI1IDYxLjQ2ODc1IApMIDYuNjQwNjI1IDcxLjU3ODEyNSAKTCAxNS40Mzc1IDcxLjU3ODEyNSAKTCAxNS40Mzc1IDYxLjQ2ODc1IAp6Ck0gNi42NDA2MjUgMCAKTCA2LjY0MDYyNSA1MS44NTkzNzUgCkwgMTUuNDM3NSA1MS44NTkzNzUgCkwgMTUuNDM3NSAwIAp6CiIgaWQ9IkFyaWFsTVQtMTA1Ij48L3BhdGg+CiAgICAgPHBhdGggZD0iTSAyMSAwIApMIDEuMjY1NjI1IDUxLjg1OTM3NSAKTCAxMC41NDY4NzUgNTEuODU5Mzc1IApMIDIxLjY4NzUgMjAuNzk2ODc1IApRIDIzLjQ4NDM3NSAxNS43NjU2MjUgMjUgMTAuMzU5Mzc1IApRIDI2LjE3MTg3NSAxNC40NTMxMjUgMjguMjY1NjI1IDIwLjIxODc1IApMIDM5Ljc5Njg3NSA1MS44NTkzNzUgCkwgNDguODI4MTI1IDUxLjg1OTM3NSAKTCAyOS4yMDMxMjUgMCAKegoiIGlkPSJBcmlhbE1ULTExOCI+PC9wYXRoPgogICAgIDxwYXRoIGQ9Ik0gNy44NTkzNzUgMCAKTCA3Ljg1OTM3NSA3MS41NzgxMjUgCkwgMzkuNTkzNzUgNzEuNTc4MTI1IApRIDQ5LjE3MTg3NSA3MS41NzgxMjUgNTQuMTQwNjI1IDY5LjY0MDYyNSAKUSA1OS4xMjUgNjcuNzE4NzUgNjIuMTA5Mzc1IDYyLjgyODEyNSAKUSA2NS4wOTM3NSA1Ny45NTMxMjUgNjUuMDkzNzUgNTIuMDQ2ODc1IApRIDY1LjA5Mzc1IDQ0LjQzNzUgNjAuMTU2MjUgMzkuMjAzMTI1IApRIDU1LjIxODc1IDMzLjk4NDM3NSA0NC45MjE4NzUgMzIuNTYyNSAKUSA0OC42ODc1IDMwLjc2NTYyNSA1MC42NDA2MjUgMjkgClEgNTQuNzgxMjUgMjUuMjAzMTI1IDU4LjUgMTkuNDg0Mzc1IApMIDcwLjk1MzEyNSAwIApMIDU5LjAzMTI1IDAgCkwgNDkuNTYyNSAxNC44OTA2MjUgClEgNDUuNDA2MjUgMjEuMzQzNzUgNDIuNzE4NzUgMjQuNzUgClEgNDAuMDQ2ODc1IDI4LjE3MTg3NSAzNy45MjE4NzUgMjkuNTMxMjUgClEgMzUuNzk2ODc1IDMwLjkwNjI1IDMzLjU5Mzc1IDMxLjQ1MzEyNSAKUSAzMS45ODQzNzUgMzEuNzgxMjUgMjguMzI4MTI1IDMxLjc4MTI1IApMIDE3LjMyODEyNSAzMS43ODEyNSAKTCAxNy4zMjgxMjUgMCAKegpNIDE3LjMyODEyNSAzOS45ODQzNzUgCkwgMzcuNzAzMTI1IDM5Ljk4NDM3NSAKUSA0NC4xODc1IDM5Ljk4NDM3NSA0Ny44NDM3NSA0MS4zMjgxMjUgClEgNTEuNTE1NjI1IDQyLjY3MTg3NSA1My40MjE4NzUgNDUuNjI1IApRIDU1LjMyODEyNSA0OC41NzgxMjUgNTUuMzI4MTI1IDUyLjA0Njg3NSAKUSA1NS4zMjgxMjUgNTcuMTI1IDUxLjY0MDYyNSA2MC4zOTA2MjUgClEgNDcuOTUzMTI1IDYzLjY3MTg3NSAzOS45ODQzNzUgNjMuNjcxODc1IApMIDE3LjMyODEyNSA2My42NzE4NzUgCnoKIiBpZD0iQXJpYWxNVC04MiI+PC9wYXRoPgogICAgIDxwYXRoIGQ9Ik0gMy4wNzgxMjUgMTUuNDg0Mzc1IApMIDExLjc2NTYyNSAxNi44NDM3NSAKUSAxMi41IDExLjYyNSAxNS44NDM3NSA4Ljg0Mzc1IApRIDE5LjE4NzUgNi4wNjI1IDI1LjIwMzEyNSA2LjA2MjUgClEgMzEuMjUgNi4wNjI1IDM0LjE3MTg3NSA4LjUxNTYyNSAKUSAzNy4xMDkzNzUgMTAuOTg0Mzc1IDM3LjEwOTM3NSAxNC4zMTI1IApRIDM3LjEwOTM3NSAxNy4yODEyNSAzNC41MTU2MjUgMTkgClEgMzIuNzE4NzUgMjAuMTcxODc1IDI1LjUzMTI1IDIxLjk2ODc1IApRIDE1Ljg3NSAyNC40MjE4NzUgMTIuMTQwNjI1IDI2LjIwMzEyNSAKUSA4LjQwNjI1IDI3Ljk4NDM3NSA2LjQ2ODc1IDMxLjEyNSAKUSA0LjU0Njg3NSAzNC4yODEyNSA0LjU0Njg3NSAzOC4wOTM3NSAKUSA0LjU0Njg3NSA0MS41NDY4NzUgNi4xMjUgNDQuNSAKUSA3LjcxODc1IDQ3LjQ2ODc1IDEwLjQ1MzEyNSA0OS40MjE4NzUgClEgMTIuNSA1MC45MjE4NzUgMTYuMDMxMjUgNTEuOTY4NzUgClEgMTkuNTc4MTI1IDUzLjAzMTI1IDIzLjY0MDYyNSA1My4wMzEyNSAKUSAyOS43MzQzNzUgNTMuMDMxMjUgMzQuMzQzNzUgNTEuMjY1NjI1IApRIDM4Ljk2ODc1IDQ5LjUxNTYyNSA0MS4xNTYyNSA0Ni41IApRIDQzLjM1OTM3NSA0My41IDQ0LjE4NzUgMzguNDg0Mzc1IApMIDM1LjU5Mzc1IDM3LjMxMjUgClEgMzUuMDE1NjI1IDQxLjMxMjUgMzIuMjAzMTI1IDQzLjU0Njg3NSAKUSAyOS4zOTA2MjUgNDUuNzk2ODc1IDI0LjI2NTYyNSA0NS43OTY4NzUgClEgMTguMjE4NzUgNDUuNzk2ODc1IDE1LjYyNSA0My43OTY4NzUgClEgMTMuMDMxMjUgNDEuNzk2ODc1IDEzLjAzMTI1IDM5LjEwOTM3NSAKUSAxMy4wMzEyNSAzNy40MDYyNSAxNC4xMDkzNzUgMzYuMDMxMjUgClEgMTUuMTg3NSAzNC42MjUgMTcuNDg0Mzc1IDMzLjY4NzUgClEgMTguNzk2ODc1IDMzLjIwMzEyNSAyNS4yNSAzMS40NTMxMjUgClEgMzQuNTc4MTI1IDI4Ljk1MzEyNSAzOC4yNSAyNy4zNTkzNzUgClEgNDEuOTM3NSAyNS43ODEyNSA0NC4wMzEyNSAyMi43NSAKUSA0Ni4xNDA2MjUgMTkuNzM0Mzc1IDQ2LjE0MDYyNSAxNS4yMzQzNzUgClEgNDYuMTQwNjI1IDEwLjg0Mzc1IDQzLjU3ODEyNSA2Ljk1MzEyNSAKUSA0MS4wMTU2MjUgMy4wNzgxMjUgMzYuMTcxODc1IDAuOTUzMTI1IApRIDMxLjM0Mzc1IC0xLjE3MTg3NSAyNS4yNSAtMS4xNzE4NzUgClEgMTUuMTQwNjI1IC0xLjE3MTg3NSA5Ljg0Mzc1IDMuMDMxMjUgClEgNC41NDY4NzUgNy4yMzQzNzUgMy4wNzgxMjUgMTUuNDg0Mzc1IAp6CiIgaWQ9IkFyaWFsTVQtMTE1Ij48L3BhdGg+CiAgICAgPHBhdGggZD0iTSAyMy4zOTA2MjUgLTIxLjA0Njg3NSAKUSAxNi4xMDkzNzUgLTExLjg1OTM3NSAxMS4wNzgxMjUgMC40Mzc1IApRIDYuMDYyNSAxMi43NSA2LjA2MjUgMjUuOTIxODc1IApRIDYuMDYyNSAzNy41NDY4NzUgOS44MTI1IDQ4LjE4NzUgClEgMTQuMjAzMTI1IDYwLjU0Njg3NSAyMy4zOTA2MjUgNzIuNzk2ODc1IApMIDI5LjY4NzUgNzIuNzk2ODc1IApRIDIzLjc4MTI1IDYyLjY0MDYyNSAyMS44NzUgNTguMjk2ODc1IApRIDE4Ljg5MDYyNSA1MS41NjI1IDE3LjE4NzUgNDQuMjM0Mzc1IApRIDE1LjA5Mzc1IDM1LjEwOTM3NSAxNS4wOTM3NSAyNS44NzUgClEgMTUuMDkzNzUgMi4zOTA2MjUgMjkuNjg3NSAtMjEuMDQ2ODc1IAp6CiIgaWQ9IkFyaWFsTVQtNDAiPjwvcGF0aD4KICAgICA8cGF0aCBkPSJNIC0wLjE0MDYyNSAwIApMIDI3LjM0Mzc1IDcxLjU3ODEyNSAKTCAzNy41NDY4NzUgNzEuNTc4MTI1IApMIDY2Ljg0Mzc1IDAgCkwgNTYuMDYyNSAwIApMIDQ3LjcwMzEyNSAyMS42ODc1IApMIDE3Ljc4MTI1IDIxLjY4NzUgCkwgOS45MDYyNSAwIAp6Ck0gMjAuNTE1NjI1IDI5LjM5MDYyNSAKTCA0NC43ODEyNSAyOS4zOTA2MjUgCkwgMzcuMzEyNSA0OS4yMTg3NSAKUSAzMy44OTA2MjUgNTguMjUgMzIuMjM0Mzc1IDY0LjA2MjUgClEgMzAuODU5Mzc1IDU3LjE3MTg3NSAyOC4zNzUgNTAuMzkwNjI1IAp6CiIgaWQ9IkFyaWFsTVQtNjUiPjwvcGF0aD4KICAgICA8cGF0aCBkPSJNIDE0LjcwMzEyNSAwIApMIDYuNTQ2ODc1IDAgCkwgNi41NDY4NzUgNzEuNTc4MTI1IApMIDE1LjMyODEyNSA3MS41NzgxMjUgCkwgMTUuMzI4MTI1IDQ2LjA0Njg3NSAKUSAyMC45MDYyNSA1My4wMzEyNSAyOS41NDY4NzUgNTMuMDMxMjUgClEgMzQuMzI4MTI1IDUzLjAzMTI1IDM4LjU5Mzc1IDUxLjA5Mzc1IApRIDQyLjg3NSA0OS4xNzE4NzUgNDUuNjI1IDQ1LjY3MTg3NSAKUSA0OC4zOTA2MjUgNDIuMTg3NSA0OS45NTMxMjUgMzcuMjUgClEgNTEuNTE1NjI1IDMyLjMyODEyNSA1MS41MTU2MjUgMjYuNzAzMTI1IApRIDUxLjUxNTYyNSAxMy4zNzUgNDQuOTIxODc1IDYuMDkzNzUgClEgMzguMzI4MTI1IC0xLjE3MTg3NSAyOS4xMDkzNzUgLTEuMTcxODc1IApRIDE5LjkyMTg3NSAtMS4xNzE4NzUgMTQuNzAzMTI1IDYuNSAKegpNIDE0LjU5Mzc1IDI2LjMxMjUgClEgMTQuNTkzNzUgMTcgMTcuMTQwNjI1IDEyLjg0Mzc1IApRIDIxLjI5Njg3NSA2LjA2MjUgMjguMzc1IDYuMDYyNSAKUSAzNC4xMjUgNi4wNjI1IDM4LjMyODEyNSAxMS4wNjI1IApRIDQyLjUzMTI1IDE2LjA2MjUgNDIuNTMxMjUgMjUuOTg0Mzc1IApRIDQyLjUzMTI1IDM2LjE0MDYyNSAzOC41IDQwLjk2ODc1IApRIDM0LjQ2ODc1IDQ1Ljc5Njg3NSAyOC43NjU2MjUgNDUuNzk2ODc1IApRIDIzIDQ1Ljc5Njg3NSAxOC43OTY4NzUgNDAuNzk2ODc1IApRIDE0LjU5Mzc1IDM1Ljc5Njg3NSAxNC41OTM3NSAyNi4zMTI1IAp6CiIgaWQ9IkFyaWFsTVQtOTgiPjwvcGF0aD4KICAgICA8cGF0aCBkPSJNIDEyLjM1OTM3NSAtMjEuMDQ2ODc1IApMIDYuMDYyNSAtMjEuMDQ2ODc1IApRIDIwLjY1NjI1IDIuMzkwNjI1IDIwLjY1NjI1IDI1Ljg3NSAKUSAyMC42NTYyNSAzNS4wNjI1IDE4LjU2MjUgNDQuMDkzNzUgClEgMTYuODkwNjI1IDUxLjQyMTg3NSAxMy45MjE4NzUgNTguMTU2MjUgClEgMTIuMDE1NjI1IDYyLjU0Njg3NSA2LjA2MjUgNzIuNzk2ODc1IApMIDEyLjM1OTM3NSA3Mi43OTY4NzUgClEgMjEuNTMxMjUgNjAuNTQ2ODc1IDI1LjkyMTg3NSA0OC4xODc1IApRIDI5LjY4NzUgMzcuNTQ2ODc1IDI5LjY4NzUgMjUuOTIxODc1IApRIDI5LjY4NzUgMTIuNzUgMjQuNjI1IDAuNDM3NSAKUSAxOS41NzgxMjUgLTExLjg1OTM3NSAxMi4zNTkzNzUgLTIxLjA0Njg3NSAKegoiIGlkPSJBcmlhbE1ULTQxIj48L3BhdGg+CiAgICA8L2RlZnM+CiAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTY3Ij48L3VzZT4KICAgIDx1c2UgeD0iNzIuMjE2Nzk3IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTciPjwvdXNlPgogICAgPHVzZSB4PSIxMjcuODMyMDMxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDkiPjwvdXNlPgogICAgPHVzZSB4PSIyMTEuMTMyODEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTciPjwvdXNlPgogICAgPHVzZSB4PSIyNjYuNzQ4MDQ3IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDgiPjwvdXNlPgogICAgPHVzZSB4PSIyODguOTY0ODQ0IiB4bGluazpocmVmPSIjQXJpYWxNVC05NyI+PC91c2U+CiAgICA8dXNlIHg9IjM0NC41ODAwNzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNiI+PC91c2U+CiAgICA8dXNlIHg9IjM3Mi4zNjMyODEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwNSI+PC91c2U+CiAgICA8dXNlIHg9IjM5NC41ODAwNzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExOCI+PC91c2U+CiAgICA8dXNlIHg9IjQ0NC41ODAwNzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICA8dXNlIHg9IjUwMC4xOTUzMTIiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgIDx1c2UgeD0iNTI3Ljk3ODUxNiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtODIiPjwvdXNlPgogICAgPHVzZSB4PSI2MDAuMTk1MzEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgPHVzZSB4PSI2NTUuODEwNTQ3IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTYiPjwvdXNlPgogICAgPHVzZSB4PSI2ODMuNTkzNzUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNyI+PC91c2U+CiAgICA8dXNlIHg9IjczOS4yMDg5ODQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNCI+PC91c2U+CiAgICA8dXNlIHg9Ijc3Mi41MDk3NjYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMCI+PC91c2U+CiAgICA8dXNlIHg9IjgyOC4xMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNSI+PC91c2U+CiAgICA8dXNlIHg9Ijg3OC4xMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgIDx1c2UgeD0iOTA1LjkwODIwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDAiPjwvdXNlPgogICAgPHVzZSB4PSI5MzkuMjA4OTg0IiB4bGluazpocmVmPSIjQXJpYWxNVC02NSI+PC91c2U+CiAgICA8dXNlIHg9IjEwMDUuOTA4MjAzIiB4bGluazpocmVmPSIjQXJpYWxNVC05OCI+PC91c2U+CiAgICA8dXNlIHg9IjEwNjEuNTIzNDM4IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTUiPjwvdXNlPgogICAgPHVzZSB4PSIxMTExLjUyMzQzOCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTExIj48L3VzZT4KICAgIDx1c2UgeD0iMTE2Ny4xMzg2NzIiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOCI+PC91c2U+CiAgICA8dXNlIHg9IjExODkuMzU1NDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTciPjwvdXNlPgogICAgPHVzZSB4PSIxMjQ0Ljk3MDcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE2Ij48L3VzZT4KICAgIDx1c2UgeD0iMTI3Mi43NTM5MDYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICA8dXNlIHg9IjEzMjguMzY5MTQxIiB4bGluazpocmVmPSIjQXJpYWxNVC00MSI+PC91c2U+CiAgIDwvZz4KICA8L2c+CiAgPGcgaWQ9InRleHRfNjIiPgogICA8IS0tIEN1bXVsYXRpdmUgUmV0dXJucyBvdmVyIFRpbWUgZm9yIGRpZmZlcmVudCBwZXJtbm9zIC0tPgogICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTg2LjYwMjUgMTguODQ3NSlzY2FsZSgwLjE2IC0wLjE2KSI+CiAgICA8ZGVmcz4KICAgICA8cGF0aCBkPSJNIDI1LjkyMTg3NSAwIApMIDI1LjkyMTg3NSA2My4xNDA2MjUgCkwgMi4zNDM3NSA2My4xNDA2MjUgCkwgMi4zNDM3NSA3MS41NzgxMjUgCkwgNTkuMDc4MTI1IDcxLjU3ODEyNSAKTCA1OS4wNzgxMjUgNjMuMTQwNjI1IApMIDM1LjQwNjI1IDYzLjE0MDYyNSAKTCAzNS40MDYyNSAwIAp6CiIgaWQ9IkFyaWFsTVQtODQiPjwvcGF0aD4KICAgICA8cGF0aCBkPSJNIDguNjg3NSAwIApMIDguNjg3NSA0NS4wMTU2MjUgCkwgMC45MjE4NzUgNDUuMDE1NjI1IApMIDAuOTIxODc1IDUxLjg1OTM3NSAKTCA4LjY4NzUgNTEuODU5Mzc1IApMIDguNjg3NSA1Ny4zNzUgClEgOC42ODc1IDYyLjU5Mzc1IDkuNjI1IDY1LjE0MDYyNSAKUSAxMC44OTA2MjUgNjguNTYyNSAxNC4wNzgxMjUgNzAuNjcxODc1IApRIDE3LjI4MTI1IDcyLjc5Njg3NSAyMy4wNDY4NzUgNzIuNzk2ODc1IApRIDI2Ljc2NTYyNSA3Mi43OTY4NzUgMzEuMjUgNzEuOTIxODc1IApMIDI5LjkzNzUgNjQuMjY1NjI1IApRIDI3LjIwMzEyNSA2NC43NSAyNC43NSA2NC43NSAKUSAyMC43NSA2NC43NSAxOS4wOTM3NSA2My4wMzEyNSAKUSAxNy40Mzc1IDYxLjMyODEyNSAxNy40Mzc1IDU2LjY0MDYyNSAKTCAxNy40Mzc1IDUxLjg1OTM3NSAKTCAyNy41NDY4NzUgNTEuODU5Mzc1IApMIDI3LjU0Njg3NSA0NS4wMTU2MjUgCkwgMTcuNDM3NSA0NS4wMTU2MjUgCkwgMTcuNDM3NSAwIAp6CiIgaWQ9IkFyaWFsTVQtMTAyIj48L3BhdGg+CiAgICAgPHBhdGggZD0iTSA0MC4yMzQzNzUgMCAKTCA0MC4yMzQzNzUgNi41NDY4NzUgClEgMzUuMjk2ODc1IC0xLjE3MTg3NSAyNS43MzQzNzUgLTEuMTcxODc1IApRIDE5LjUzMTI1IC0xLjE3MTg3NSAxNC4zMjgxMjUgMi4yNSAKUSA5LjEyNSA1LjY3MTg3NSA2LjI2NTYyNSAxMS43OTY4NzUgClEgMy40MjE4NzUgMTcuOTIxODc1IDMuNDIxODc1IDI1Ljg3NSAKUSAzLjQyMTg3NSAzMy42NDA2MjUgNiAzOS45Njg3NSAKUSA4LjU5Mzc1IDQ2LjI5Njg3NSAxMy43NjU2MjUgNDkuNjU2MjUgClEgMTguOTUzMTI1IDUzLjAzMTI1IDI1LjM0Mzc1IDUzLjAzMTI1IApRIDMwLjAzMTI1IDUzLjAzMTI1IDMzLjY4NzUgNTEuMDQ2ODc1IApRIDM3LjM1OTM3NSA0OS4wNzgxMjUgMzkuNjU2MjUgNDUuOTA2MjUgCkwgMzkuNjU2MjUgNzEuNTc4MTI1IApMIDQ4LjM5MDYyNSA3MS41NzgxMjUgCkwgNDguMzkwNjI1IDAgCnoKTSAxMi40NTMxMjUgMjUuODc1IApRIDEyLjQ1MzEyNSAxNS45MjE4NzUgMTYuNjQwNjI1IDEwLjk4NDM3NSAKUSAyMC44NDM3NSA2LjA2MjUgMjYuNTYyNSA2LjA2MjUgClEgMzIuMzI4MTI1IDYuMDYyNSAzNi4zNDM3NSAxMC43NjU2MjUgClEgNDAuMzc1IDE1LjQ4NDM3NSA0MC4zNzUgMjUuMTQwNjI1IApRIDQwLjM3NSAzNS43OTY4NzUgMzYuMjY1NjI1IDQwLjc2NTYyNSAKUSAzMi4xNzE4NzUgNDUuNzUgMjYuMTcxODc1IDQ1Ljc1IApRIDIwLjMxMjUgNDUuNzUgMTYuMzc1IDQwLjk2ODc1IApRIDEyLjQ1MzEyNSAzNi4xODc1IDEyLjQ1MzEyNSAyNS44NzUgCnoKIiBpZD0iQXJpYWxNVC0xMDAiPjwvcGF0aD4KICAgIDwvZGVmcz4KICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNjciPjwvdXNlPgogICAgPHVzZSB4PSI3Mi4yMTY3OTciIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNyI+PC91c2U+CiAgICA8dXNlIHg9IjEyNy44MzIwMzEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOSI+PC91c2U+CiAgICA8dXNlIHg9IjIxMS4xMzI4MTIiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNyI+PC91c2U+CiAgICA8dXNlIHg9IjI2Ni43NDgwNDciIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOCI+PC91c2U+CiAgICA8dXNlIHg9IjI4OC45NjQ4NDQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTk3Ij48L3VzZT4KICAgIDx1c2UgeD0iMzQ0LjU4MDA3OCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE2Ij48L3VzZT4KICAgIDx1c2UgeD0iMzcyLjM2MzI4MSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA1Ij48L3VzZT4KICAgIDx1c2UgeD0iMzk0LjU4MDA3OCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE4Ij48L3VzZT4KICAgIDx1c2UgeD0iNDQ0LjU4MDA3OCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAxIj48L3VzZT4KICAgIDx1c2UgeD0iNTAwLjE5NTMxMiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgPHVzZSB4PSI1MjcuOTc4NTE2IiB4bGluazpocmVmPSIjQXJpYWxNVC04MiI+PC91c2U+CiAgICA8dXNlIHg9IjYwMC4xOTUzMTIiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICA8dXNlIHg9IjY1NS44MTA1NDciIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNiI+PC91c2U+CiAgICA8dXNlIHg9IjY4My41OTM3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE3Ij48L3VzZT4KICAgIDx1c2UgeD0iNzM5LjIwODk4NCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgIDx1c2UgeD0iNzcyLjUwOTc2NiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEwIj48L3VzZT4KICAgIDx1c2UgeD0iODI4LjEyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE1Ij48L3VzZT4KICAgIDx1c2UgeD0iODc4LjEyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgPHVzZSB4PSI5MDUuOTA4MjAzIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTEiPjwvdXNlPgogICAgPHVzZSB4PSI5NjEuNTIzNDM4IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTgiPjwvdXNlPgogICAgPHVzZSB4PSIxMDExLjUyMzQzOCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAxIj48L3VzZT4KICAgIDx1c2UgeD0iMTA2Ny4xMzg2NzIiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNCI+PC91c2U+CiAgICA8dXNlIHg9IjExMDAuNDM5NDUzIiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICA8dXNlIHg9IjExMjYuNDcyNjU2IiB4bGluazpocmVmPSIjQXJpYWxNVC04NCI+PC91c2U+CiAgICA8dXNlIHg9IjExODMuODA2NjQxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDUiPjwvdXNlPgogICAgPHVzZSB4PSIxMjA2LjAyMzQzOCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA5Ij48L3VzZT4KICAgIDx1c2UgeD0iMTI4OS4zMjQyMTkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICA8dXNlIHg9IjEzNDQuOTM5NDUzIiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICA8dXNlIHg9IjEzNzIuNzIyNjU2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDIiPjwvdXNlPgogICAgPHVzZSB4PSIxNDAwLjUwNTg1OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTExIj48L3VzZT4KICAgIDx1c2UgeD0iMTQ1Ni4xMjEwOTQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNCI+PC91c2U+CiAgICA8dXNlIHg9IjE0ODkuNDIxODc1IiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICA8dXNlIHg9IjE1MTcuMjA1MDc4IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDAiPjwvdXNlPgogICAgPHVzZSB4PSIxNTcyLjgyMDMxMiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA1Ij48L3VzZT4KICAgIDx1c2UgeD0iMTU5NS4wMzcxMDkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMiI+PC91c2U+CiAgICA8dXNlIHg9IjE2MjEuMDcwMzEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDIiPjwvdXNlPgogICAgPHVzZSB4PSIxNjQ4Ljg1MzUxNiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAxIj48L3VzZT4KICAgIDx1c2UgeD0iMTcwNC40Njg3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgIDx1c2UgeD0iMTczNy43Njk1MzEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICA8dXNlIHg9IjE3OTMuMzg0NzY2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTAiPjwvdXNlPgogICAgPHVzZSB4PSIxODQ5IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTYiPjwvdXNlPgogICAgPHVzZSB4PSIxODc2Ljc4MzIwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgPHVzZSB4PSIxOTA0LjU2NjQwNiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEyIj48L3VzZT4KICAgIDx1c2UgeD0iMTk2MC4xODE2NDEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICA8dXNlIHg9IjIwMTUuNzk2ODc1IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTQiPjwvdXNlPgogICAgPHVzZSB4PSIyMDQ5LjA5NzY1NiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA5Ij48L3VzZT4KICAgIDx1c2UgeD0iMjEzMi4zOTg0MzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMCI+PC91c2U+CiAgICA8dXNlIHg9IjIxODguMDEzNjcyIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTEiPjwvdXNlPgogICAgPHVzZSB4PSIyMjQzLjYyODkwNiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE1Ij48L3VzZT4KICAgPC9nPgogIDwvZz4KIDwvZz4KIDxkZWZzPgogIDxjbGlwcGF0aCBpZD0icDRlMjhhYjZlNzYiPgogICA8cmVjdCBoZWlnaHQ9IjIxMi44MzM5NTUiIHdpZHRoPSIzNTMuODE0Mjg3IiB4PSI1OS4wNCIgeT0iNDEuNzYiPjwvcmVjdD4KICA8L2NsaXBwYXRoPgogIDxjbGlwcGF0aCBpZD0icGYyNmYwOTU0YzgiPgogICA8cmVjdCBoZWlnaHQ9IjIxMi44MzM5NTUiIHdpZHRoPSIzNTMuODE0Mjg3IiB4PSI0MzcuNDY1NzEzIiB5PSI0MS43NiI+PC9yZWN0PgogIDwvY2xpcHBhdGg+CiAgPGNsaXBwYXRoIGlkPSJwYWM4MDI2YzUyZiI+CiAgIDxyZWN0IGhlaWdodD0iMjEyLjgzMzk1NSIgd2lkdGg9IjM1My44MTQyODciIHg9IjU5LjA0IiB5PSIyNzguMjA2MDQ1Ij48L3JlY3Q+CiAgPC9jbGlwcGF0aD4KICA8Y2xpcHBhdGggaWQ9InAyNDkxOTYwN2YwIj4KICAgPHJlY3QgaGVpZ2h0PSIyMTIuODMzOTU1IiB3aWR0aD0iMzUzLjgxNDI4NyIgeD0iNDM3LjQ2NTcxMyIgeT0iMjc4LjIwNjA0NSI+PC9yZWN0PgogIDwvY2xpcHBhdGg+CiA8L2RlZnM+Cjwvc3ZnPg==)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell" markdown="1">

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputArea jp-Cell-inputArea" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

In \[25\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
markdown="1" data-type="inline">

<div class="CodeMirror cm-s-jupyter" markdown="1">

<div class="highlight hl-ipython3" markdown="1">

    # Plotting a cumulative single plot for all the 4 permnos

    fig = plt.figure(figsize=(10, 6))
    for permno, df_to_plot in dfs_to_plot.items():
        plt.plot(df_to_plot, label='permno: {}'.format(permno))

    ax = plt.gca()
    ax.legend(fontsize=12,frameon=True, loc='upper left');
    plt.xlabel('Date', fontsize=12)
    plt.ylabel('Cumulative Returns (Absolute)', fontsize=12)
    plt.title("Cumulative Returns over Time for different permnos", fontsize=16)
    plt.show();

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper" markdown="1">

<div class="jp-OutputArea jp-Cell-outputArea" markdown="1">

<div class="jp-OutputArea-child" markdown="1">

<div class="jp-OutputPrompt jp-OutputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedSVG jp-OutputArea-output" markdown="1"
mime-type="image/svg+xml">

![](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjM4OS4zMjcxODdwdCIgdmVyc2lvbj0iMS4xIiB2aWV3Ym94PSIwIDAgNjAwLjIyMjE4OCAzODkuMzI3MTg3IiB3aWR0aD0iNjAwLjIyMjE4OHB0IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIj4KIDxtZXRhZGF0YT4KICA8cmRmIHhtbG5zOmNjPSJodHRwOi8vY3JlYXRpdmVjb21tb25zLm9yZy9ucyMiIHhtbG5zOmRjPSJodHRwOi8vcHVybC5vcmcvZGMvZWxlbWVudHMvMS4xLyIgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4KICAgPHdvcms+CiAgICA8dHlwZSByZGY6cmVzb3VyY2U9Imh0dHA6Ly9wdXJsLm9yZy9kYy9kY21pdHlwZS9TdGlsbEltYWdlIj48L3R5cGU+CiAgICA8ZGF0ZT4yMDIxLTA3LTMwVDEwOjE1OjQyLjY2MTgzMzwvZGF0ZT4KICAgIDxmb3JtYXQ+aW1hZ2Uvc3ZnK3htbDwvZm9ybWF0PgogICAgPGNyZWF0b3I+CiAgICAgPGFnZW50PgogICAgICA8dGl0bGU+TWF0cGxvdGxpYiB2My4zLjQsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvPC90aXRsZT4KICAgICA8L2FnZW50PgogICAgPC9jcmVhdG9yPgogICA8L3dvcms+CiAgPC9yZGY+CiA8L21ldGFkYXRhPgogPGRlZnM+CiAgPHN0eWxlIHR5cGU9InRleHQvY3NzIj4qe3N0cm9rZS1saW5lY2FwOmJ1dHQ7c3Ryb2tlLWxpbmVqb2luOnJvdW5kO308L3N0eWxlPgogPC9kZWZzPgogPGcgaWQ9ImZpZ3VyZV8xIj4KICA8ZyBpZD0icGF0Y2hfMSI+CiAgIDxwYXRoIGQ9Ik0gLTAgMzg5LjMyNzE4NyAKTCA2MDAuMjIyMTg4IDM4OS4zMjcxODcgCkwgNjAwLjIyMjE4OCAwIApMIC0wIDAgCnoKIiBzdHlsZT0iZmlsbDojZmZmZmZmOyI+PC9wYXRoPgogIDwvZz4KICA8ZyBpZD0iYXhlc18xIj4KICAgPGcgaWQ9InBhdGNoXzIiPgogICAgPHBhdGggZD0iTSAzNS4wMjIxODggMzUxLjAwNzUgCkwgNTkzLjAyMjE4NyAzNTEuMDA3NSAKTCA1OTMuMDIyMTg3IDI0Ljg0NzUgCkwgMzUuMDIyMTg4IDI0Ljg0NzUgCnoKIiBzdHlsZT0iZmlsbDojZWFlYWYyOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJtYXRwbG90bGliLmF4aXNfMSI+CiAgICA8ZyBpZD0ieHRpY2tfMSI+CiAgICAgPGcgaWQ9ImxpbmUyZF8xIj4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A3ZDc3MTIwZTIwKSIgZD0iTSA1OS40NTgxNjkgMzUxLjAwNzUgCkwgNTkuNDU4MTY5IDI0Ljg0NzUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8yIj48L2c+CiAgICAgPGcgaWQ9InRleHRfMSI+CiAgICAgIDwhLS0gMTk3NSAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4LjMzNjI5NCAzNjUuMTY1MzEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8ZGVmcz4KICAgICAgICA8cGF0aCBkPSJNIDM3LjI1IDAgCkwgMjguNDY4NzUgMCAKTCAyOC40Njg3NSA1NiAKUSAyNS4yOTY4NzUgNTIuOTg0Mzc1IDIwLjE0MDYyNSA0OS45NTMxMjUgClEgMTQuOTg0Mzc1IDQ2LjkyMTg3NSAxMC44OTA2MjUgNDUuNDA2MjUgCkwgMTAuODkwNjI1IDUzLjkwNjI1IApRIDE4LjI2NTYyNSA1Ny4zNzUgMjMuNzgxMjUgNjIuMjk2ODc1IApRIDI5LjI5Njg3NSA2Ny4yMzQzNzUgMzEuNTkzNzUgNzEuODc1IApMIDM3LjI1IDcxLjg3NSAKegoiIGlkPSJBcmlhbE1ULTQ5Ij48L3BhdGg+CiAgICAgICAgPHBhdGggZD0iTSA1LjQ2ODc1IDE2LjU0Njg3NSAKTCAxMy45MjE4NzUgMTcuMzI4MTI1IApRIDE0Ljk4NDM3NSAxMS4zNzUgMTguMDE1NjI1IDguNjg3NSAKUSAyMS4wNDY4NzUgNiAyNS43ODEyNSA2IApRIDI5LjgyODEyNSA2IDMyLjg3NSA3Ljg1OTM3NSAKUSAzNS45Mzc1IDkuNzE4NzUgMzcuODkwNjI1IDEyLjgxMjUgClEgMzkuODQzNzUgMTUuOTIxODc1IDQxLjE1NjI1IDIxLjE4NzUgClEgNDIuNDg0Mzc1IDI2LjQ2ODc1IDQyLjQ4NDM3NSAzMS45Mzc1IApRIDQyLjQ4NDM3NSAzMi41MTU2MjUgNDIuNDM3NSAzMy42ODc1IApRIDM5Ljc5Njg3NSAyOS41IDM1LjIzNDM3NSAyNi44NzUgClEgMzAuNjcxODc1IDI0LjI2NTYyNSAyNS4zNDM3NSAyNC4yNjU2MjUgClEgMTYuNDUzMTI1IDI0LjI2NTYyNSAxMC4yOTY4NzUgMzAuNzAzMTI1IApRIDQuMTU2MjUgMzcuMTU2MjUgNC4xNTYyNSA0Ny43MDMxMjUgClEgNC4xNTYyNSA1OC41OTM3NSAxMC41NzgxMjUgNjUuMjM0Mzc1IApRIDE3IDcxLjg3NSAyNi42NTYyNSA3MS44NzUgClEgMzMuNjQwNjI1IDcxLjg3NSAzOS40MjE4NzUgNjguMTA5Mzc1IApRIDQ1LjIxODc1IDY0LjM1OTM3NSA0OC4yMTg3NSA1Ny4zOTA2MjUgClEgNTEuMjE4NzUgNTAuNDM3NSA1MS4yMTg3NSAzNy4yNSAKUSA1MS4yMTg3NSAyMy41MzEyNSA0OC4yMzQzNzUgMTUuNDA2MjUgClEgNDUuMjY1NjI1IDcuMjgxMjUgMzkuMzc1IDMuMDMxMjUgClEgMzMuNSAtMS4yMTg3NSAyNS41OTM3NSAtMS4yMTg3NSAKUSAxNy4xODc1IC0xLjIxODc1IDExLjg1OTM3NSAzLjQzNzUgClEgNi41NDY4NzUgOC4xMDkzNzUgNS40Njg3NSAxNi41NDY4NzUgCnoKTSA0MS40NTMxMjUgNDguMTQwNjI1IApRIDQxLjQ1MzEyNSA1NS43MTg3NSAzNy40MjE4NzUgNjAuMTU2MjUgClEgMzMuNDA2MjUgNjQuNTkzNzUgMjcuNzM0Mzc1IDY0LjU5Mzc1IApRIDIxLjg3NSA2NC41OTM3NSAxNy41MzEyNSA1OS44MTI1IApRIDEzLjE4NzUgNTUuMDMxMjUgMTMuMTg3NSA0Ny40MDYyNSAKUSAxMy4xODc1IDQwLjU3ODEyNSAxNy4zMTI1IDM2LjI5Njg3NSAKUSAyMS40Mzc1IDMyLjAzMTI1IDI3LjQ4NDM3NSAzMi4wMzEyNSAKUSAzMy41OTM3NSAzMi4wMzEyNSAzNy41MTU2MjUgMzYuMjk2ODc1IApRIDQxLjQ1MzEyNSA0MC41NzgxMjUgNDEuNDUzMTI1IDQ4LjE0MDYyNSAKegoiIGlkPSJBcmlhbE1ULTU3Ij48L3BhdGg+CiAgICAgICAgPHBhdGggZD0iTSA0LjczNDM3NSA2Mi4yMDMxMjUgCkwgNC43MzQzNzUgNzAuNjU2MjUgCkwgNTEuMDc4MTI1IDcwLjY1NjI1IApMIDUxLjA3ODEyNSA2My44MTI1IApRIDQ0LjIzNDM3NSA1Ni41NDY4NzUgMzcuNTE1NjI1IDQ0LjQ4NDM3NSAKUSAzMC44MTI1IDMyLjQyMTg3NSAyNy4xNTYyNSAxOS42NzE4NzUgClEgMjQuNTE1NjI1IDEwLjY4NzUgMjMuNzgxMjUgMCAKTCAxNC43NSAwIApRIDE0Ljg5MDYyNSA4LjQ1MzEyNSAxOC4wNjI1IDIwLjQwNjI1IApRIDIxLjIzNDM3NSAzMi4zNzUgMjcuMTcxODc1IDQzLjQ4NDM3NSAKUSAzMy4xMDkzNzUgNTQuNTkzNzUgMzkuNzk2ODc1IDYyLjIwMzEyNSAKegoiIGlkPSJBcmlhbE1ULTU1Ij48L3BhdGg+CiAgICAgICAgPHBhdGggZD0iTSA0LjE1NjI1IDE4Ljc1IApMIDEzLjM3NSAxOS41MzEyNSAKUSAxNC40MDYyNSAxMi43OTY4NzUgMTguMTQwNjI1IDkuMzkwNjI1IApRIDIxLjg3NSA2IDI3LjE1NjI1IDYgClEgMzMuNSA2IDM3Ljg5MDYyNSAxMC43ODEyNSAKUSA0Mi4yODEyNSAxNS41NzgxMjUgNDIuMjgxMjUgMjMuNDg0Mzc1IApRIDQyLjI4MTI1IDMxIDM4LjA2MjUgMzUuMzQzNzUgClEgMzMuODQzNzUgMzkuNzAzMTI1IDI3IDM5LjcwMzEyNSAKUSAyMi43NSAzOS43MDMxMjUgMTkuMzI4MTI1IDM3Ljc2NTYyNSAKUSAxNS45MjE4NzUgMzUuODQzNzUgMTMuOTY4NzUgMzIuNzY1NjI1IApMIDUuNzE4NzUgMzMuODQzNzUgCkwgMTIuNjQwNjI1IDcwLjYwOTM3NSAKTCA0OC4yNSA3MC42MDkzNzUgCkwgNDguMjUgNjIuMjAzMTI1IApMIDE5LjY3MTg3NSA2Mi4yMDMxMjUgCkwgMTUuODI4MTI1IDQyLjk2ODc1IApRIDIyLjI2NTYyNSA0Ny40Njg3NSAyOS4zNDM3NSA0Ny40Njg3NSAKUSAzOC43MTg3NSA0Ny40Njg3NSA0NS4xNTYyNSA0MC45Njg3NSAKUSA1MS42MDkzNzUgMzQuNDY4NzUgNTEuNjA5Mzc1IDI0LjI2NTYyNSAKUSA1MS42MDkzNzUgMTQuNTQ2ODc1IDQ1Ljk1MzEyNSA3LjQ2ODc1IApRIDM5LjA2MjUgLTEuMjE4NzUgMjcuMTU2MjUgLTEuMjE4NzUgClEgMTcuMzkwNjI1IC0xLjIxODc1IDExLjIwMzEyNSA0LjI1IApRIDUuMDMxMjUgOS43MTg3NSA0LjE1NjI1IDE4Ljc1IAp6CiIgaWQ9IkFyaWFsTVQtNTMiPjwvcGF0aD4KICAgICAgIDwvZGVmcz4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTUiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC01MyI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMiI+CiAgICAgPGcgaWQ9ImxpbmUyZF8zIj4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A3ZDc3MTIwZTIwKSIgZD0iTSAxMTUuOTIxNDQyIDM1MS4wMDc1IApMIDExNS45MjE0NDIgMjQuODQ3NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzQiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8yIj4KICAgICAgPCEtLSAxOTgwIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTA0Ljc5OTU2NyAzNjUuMTY1MzEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8ZGVmcz4KICAgICAgICA8cGF0aCBkPSJNIDE3LjY3MTg3NSAzOC44MTI1IApRIDEyLjIwMzEyNSA0MC44MjgxMjUgOS41NjI1IDQ0LjUzMTI1IApRIDYuOTM3NSA0OC4yNSA2LjkzNzUgNTMuNDIxODc1IApRIDYuOTM3NSA2MS4yMzQzNzUgMTIuNTQ2ODc1IDY2LjU0Njg3NSAKUSAxOC4xNzE4NzUgNzEuODc1IDI3LjQ4NDM3NSA3MS44NzUgClEgMzYuODU5Mzc1IDcxLjg3NSA0Mi41NzgxMjUgNjYuNDIxODc1IApRIDQ4LjI5Njg3NSA2MC45ODQzNzUgNDguMjk2ODc1IDUzLjE3MTg3NSAKUSA0OC4yOTY4NzUgNDguMTg3NSA0NS42NzE4NzUgNDQuNSAKUSA0My4wNjI1IDQwLjgyODEyNSAzNy43NSAzOC44MTI1IApRIDQ0LjM0Mzc1IDM2LjY3MTg3NSA0Ny43ODEyNSAzMS44NzUgClEgNTEuMjE4NzUgMjcuMDkzNzUgNTEuMjE4NzUgMjAuNDUzMTI1IApRIDUxLjIxODc1IDExLjI4MTI1IDQ0LjcxODc1IDUuMDMxMjUgClEgMzguMjM0Mzc1IC0xLjIxODc1IDI3LjY0MDYyNSAtMS4yMTg3NSAKUSAxNy4wNDY4NzUgLTEuMjE4NzUgMTAuNTQ2ODc1IDUuMDQ2ODc1IApRIDQuMDQ2ODc1IDExLjMyODEyNSA0LjA0Njg3NSAyMC43MDMxMjUgClEgNC4wNDY4NzUgMjcuNjg3NSA3LjU5Mzc1IDMyLjM5MDYyNSAKUSAxMS4xNDA2MjUgMzcuMTA5Mzc1IDE3LjY3MTg3NSAzOC44MTI1IAp6Ck0gMTUuOTIxODc1IDUzLjcxODc1IApRIDE1LjkyMTg3NSA0OC42NDA2MjUgMTkuMTg3NSA0NS40MDYyNSAKUSAyMi40Njg3NSA0Mi4xODc1IDI3LjY4NzUgNDIuMTg3NSAKUSAzMi43NjU2MjUgNDIuMTg3NSAzNi4wMTU2MjUgNDUuMzc1IApRIDM5LjI2NTYyNSA0OC41NzgxMjUgMzkuMjY1NjI1IDUzLjIxODc1IApRIDM5LjI2NTYyNSA1OC4wNjI1IDM1LjkwNjI1IDYxLjM1OTM3NSAKUSAzMi41NjI1IDY0LjY1NjI1IDI3LjU5Mzc1IDY0LjY1NjI1IApRIDIyLjU2MjUgNjQuNjU2MjUgMTkuMjM0Mzc1IDYxLjQyMTg3NSAKUSAxNS45MjE4NzUgNTguMjAzMTI1IDE1LjkyMTg3NSA1My43MTg3NSAKegpNIDEzLjA5Mzc1IDIwLjY1NjI1IApRIDEzLjA5Mzc1IDE2Ljg5MDYyNSAxNC44NzUgMTMuMzc1IApRIDE2LjY1NjI1IDkuODU5Mzc1IDIwLjE3MTg3NSA3LjkyMTg3NSAKUSAyMy42ODc1IDYgMjcuNzM0Mzc1IDYgClEgMzQuMDMxMjUgNiAzOC4xMjUgMTAuMDQ2ODc1IApRIDQyLjIzNDM3NSAxNC4xMDkzNzUgNDIuMjM0Mzc1IDIwLjM1OTM3NSAKUSA0Mi4yMzQzNzUgMjYuNzAzMTI1IDM4LjAxNTYyNSAzMC44NTkzNzUgClEgMzMuNzk2ODc1IDM1LjAxNTYyNSAyNy40Mzc1IDM1LjAxNTYyNSAKUSAyMS4yMzQzNzUgMzUuMDE1NjI1IDE3LjE1NjI1IDMwLjkwNjI1IApRIDEzLjA5Mzc1IDI2LjgxMjUgMTMuMDkzNzUgMjAuNjU2MjUgCnoKIiBpZD0iQXJpYWxNVC01NiI+PC9wYXRoPgogICAgICAgIDxwYXRoIGQ9Ik0gNC4xNTYyNSAzNS4yOTY4NzUgClEgNC4xNTYyNSA0OCA2Ljc2NTYyNSA1NS43MzQzNzUgClEgOS4zNzUgNjMuNDg0Mzc1IDE0LjUxNTYyNSA2Ny42NzE4NzUgClEgMTkuNjcxODc1IDcxLjg3NSAyNy40ODQzNzUgNzEuODc1IApRIDMzLjI1IDcxLjg3NSAzNy41OTM3NSA2OS41NDY4NzUgClEgNDEuOTM3NSA2Ny4yMzQzNzUgNDQuNzY1NjI1IDYyLjg1OTM3NSAKUSA0Ny42MDkzNzUgNTguNSA0OS4yMTg3NSA1Mi4yMTg3NSAKUSA1MC44MjgxMjUgNDUuOTUzMTI1IDUwLjgyODEyNSAzNS4yOTY4NzUgClEgNTAuODI4MTI1IDIyLjcwMzEyNSA0OC4yMzQzNzUgMTQuOTY4NzUgClEgNDUuNjU2MjUgNy4yMzQzNzUgNDAuNSAzIApRIDM1LjM1OTM3NSAtMS4yMTg3NSAyNy40ODQzNzUgLTEuMjE4NzUgClEgMTcuMTQwNjI1IC0xLjIxODc1IDExLjIzNDM3NSA2LjIwMzEyNSAKUSA0LjE1NjI1IDE1LjE0MDYyNSA0LjE1NjI1IDM1LjI5Njg3NSAKegpNIDEzLjE4NzUgMzUuMjk2ODc1IApRIDEzLjE4NzUgMTcuNjcxODc1IDE3LjMxMjUgMTEuODI4MTI1IApRIDIxLjQzNzUgNiAyNy40ODQzNzUgNiAKUSAzMy41NDY4NzUgNiAzNy42NzE4NzUgMTEuODU5Mzc1IApRIDQxLjc5Njg3NSAxNy43MTg3NSA0MS43OTY4NzUgMzUuMjk2ODc1IApRIDQxLjc5Njg3NSA1Mi45ODQzNzUgMzcuNjcxODc1IDU4Ljc4MTI1IApRIDMzLjU0Njg3NSA2NC41OTM3NSAyNy4zOTA2MjUgNjQuNTkzNzUgClEgMjEuMzQzNzUgNjQuNTkzNzUgMTcuNzE4NzUgNTkuNDY4NzUgClEgMTMuMTg3NSA1Mi45Mzc1IDEzLjE4NzUgMzUuMjk2ODc1IAp6CiIgaWQ9IkFyaWFsTVQtNDgiPjwvcGF0aD4KICAgICAgIDwvZGVmcz4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTYiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMyI+CiAgICAgPGcgaWQ9ImxpbmUyZF81Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A3ZDc3MTIwZTIwKSIgZD0iTSAxNzIuNDE1NjM3IDM1MS4wMDc1IApMIDE3Mi40MTU2MzcgMjQuODQ3NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzYiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8zIj4KICAgICAgPCEtLSAxOTg1IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTYxLjI5Mzc2MiAzNjUuMTY1MzEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU2Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTMiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzQiPgogICAgIDxnIGlkPSJsaW5lMmRfNyI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwN2Q3NzEyMGUyMCkiIGQ9Ik0gMjI4Ljg3ODkxMSAzNTEuMDA3NSAKTCAyMjguODc4OTExIDI0Ljg0NzUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF84Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfNCI+CiAgICAgIDwhLS0gMTk5MCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIxNy43NTcwMzYgMzY1LjE2NTMxMilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTciPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ4dGlja181Ij4KICAgICA8ZyBpZD0ibGluZTJkXzkiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDI4NS4zNDIxODQgMzUxLjAwNzUgCkwgMjg1LjM0MjE4NCAyNC44NDc1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTAiPjwvZz4KICAgICA8ZyBpZD0idGV4dF81Ij4KICAgICAgPCEtLSAxOTk1IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMjc0LjIyMDMwOSAzNjUuMTY1MzEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NyI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU3Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTMiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzYiPgogICAgIDxnIGlkPSJsaW5lMmRfMTEiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDM0MS44MDU0NTggMzUxLjAwNzUgCkwgMzQxLjgwNTQ1OCAyNC44NDc1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTIiPjwvZz4KICAgICA8ZyBpZD0idGV4dF82Ij4KICAgICAgPCEtLSAyMDAwIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzMwLjY4MzU4MyAzNjUuMTY1MzEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8ZGVmcz4KICAgICAgICA8cGF0aCBkPSJNIDUwLjM0Mzc1IDguNDUzMTI1IApMIDUwLjM0Mzc1IDAgCkwgMy4wMzEyNSAwIApRIDIuOTM3NSAzLjE3MTg3NSA0LjA0Njg3NSA2LjEwOTM3NSAKUSA1Ljg1OTM3NSAxMC45Mzc1IDkuODI4MTI1IDE1LjYyNSAKUSAxMy44MTI1IDIwLjMxMjUgMjEuMzQzNzUgMjYuNDY4NzUgClEgMzMuMDE1NjI1IDM2LjAzMTI1IDM3LjEwOTM3NSA0MS42MjUgClEgNDEuMjE4NzUgNDcuMjE4NzUgNDEuMjE4NzUgNTIuMjAzMTI1IApRIDQxLjIxODc1IDU3LjQyMTg3NSAzNy40Njg3NSA2MSAKUSAzMy43MzQzNzUgNjQuNTkzNzUgMjcuNzM0Mzc1IDY0LjU5Mzc1IApRIDIxLjM5MDYyNSA2NC41OTM3NSAxNy41NzgxMjUgNjAuNzgxMjUgClEgMTMuNzY1NjI1IDU2Ljk4NDM3NSAxMy43MTg3NSA1MC4yNSAKTCA0LjY4NzUgNTEuMTcxODc1IApRIDUuNjA5Mzc1IDYxLjI4MTI1IDExLjY1NjI1IDY2LjU3ODEyNSAKUSAxNy43MTg3NSA3MS44NzUgMjcuOTM3NSA3MS44NzUgClEgMzguMjM0Mzc1IDcxLjg3NSA0NC4yMzQzNzUgNjYuMTU2MjUgClEgNTAuMjUgNjAuNDUzMTI1IDUwLjI1IDUyIApRIDUwLjI1IDQ3LjcwMzEyNSA0OC40ODQzNzUgNDMuNTQ2ODc1IApRIDQ2LjczNDM3NSAzOS40MDYyNSA0Mi42NTYyNSAzNC44MTI1IApRIDM4LjU3ODEyNSAzMC4yMTg3NSAyOS4xMDkzNzUgMjIuMjE4NzUgClEgMjEuMTg3NSAxNS41NzgxMjUgMTguOTM3NSAxMy4yMDMxMjUgClEgMTYuNzAzMTI1IDEwLjg0Mzc1IDE1LjIzNDM3NSA4LjQ1MzEyNSAKegoiIGlkPSJBcmlhbE1ULTUwIj48L3BhdGg+CiAgICAgICA8L2RlZnM+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzciPgogICAgIDxnIGlkPSJsaW5lMmRfMTMiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDM5OC4yOTk2NTMgMzUxLjAwNzUgCkwgMzk4LjI5OTY1MyAyNC44NDc1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTQiPjwvZz4KICAgICA8ZyBpZD0idGV4dF83Ij4KICAgICAgPCEtLSAyMDA1IC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzg3LjE3Nzc3OCAzNjUuMTY1MzEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTMiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzgiPgogICAgIDxnIGlkPSJsaW5lMmRfMTUiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDQ1NC43NjI5MjYgMzUxLjAwNzUgCkwgNDU0Ljc2MjkyNiAyNC44NDc1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMTYiPjwvZz4KICAgICA8ZyBpZD0idGV4dF84Ij4KICAgICAgPCEtLSAyMDEwIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNDQzLjY0MTA1MSAzNjUuMTY1MzEyKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inh0aWNrXzkiPgogICAgIDxnIGlkPSJsaW5lMmRfMTciPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDUxMS4yMjYyIDM1MS4wMDc1IApMIDUxMS4yMjYyIDI0Ljg0NzUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8xOCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzkiPgogICAgICA8IS0tIDIwMTUgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg1MDAuMTA0MzI1IDM2NS4xNjUzMTIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTAiPjwvdXNlPgogICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC01MyI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieHRpY2tfMTAiPgogICAgIDxnIGlkPSJsaW5lMmRfMTkiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDU2Ny42ODk0NzMgMzUxLjAwNzUgCkwgNTY3LjY4OTQ3MyAyNC44NDc1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMjAiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xMCI+CiAgICAgIDwhLS0gMjAyMCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDU1Ni41Njc1OTggMzY1LjE2NTMxMilzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgICA8dXNlIHg9IjE2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ0ZXh0XzExIj4KICAgICA8IS0tIERhdGUgLS0+CiAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMwMS4zNDkwNjIgMzc5Ljc0MjE4NylzY2FsZSgwLjEyIC0wLjEyKSI+CiAgICAgIDxkZWZzPgogICAgICAgPHBhdGggZD0iTSA3LjcxODc1IDAgCkwgNy43MTg3NSA3MS41NzgxMjUgCkwgMzIuMzc1IDcxLjU3ODEyNSAKUSA0MC43MTg3NSA3MS41NzgxMjUgNDUuMTI1IDcwLjU2MjUgClEgNTEuMjY1NjI1IDY5LjE0MDYyNSA1NS42MDkzNzUgNjUuNDM3NSAKUSA2MS4yODEyNSA2MC42NDA2MjUgNjQuMDc4MTI1IDUzLjE4NzUgClEgNjYuODkwNjI1IDQ1Ljc1IDY2Ljg5MDYyNSAzNi4xODc1IApRIDY2Ljg5MDYyNSAyOC4wMzEyNSA2NC45ODQzNzUgMjEuNzM0Mzc1IApRIDYzLjA5Mzc1IDE1LjQzNzUgNjAuMTA5Mzc1IDExLjI5Njg3NSAKUSA1Ny4xMjUgNy4xNzE4NzUgNTMuNTc4MTI1IDQuNzk2ODc1IApRIDUwLjA0Njg3NSAyLjQzNzUgNDUuMDQ2ODc1IDEuMjE4NzUgClEgNDAuMDQ2ODc1IDAgMzMuNTQ2ODc1IDAgCnoKTSAxNy4xODc1IDguNDUzMTI1IApMIDMyLjQ2ODc1IDguNDUzMTI1IApRIDM5LjU0Njg3NSA4LjQ1MzEyNSA0My41NzgxMjUgOS43NjU2MjUgClEgNDcuNjA5Mzc1IDExLjA3ODEyNSA1MCAxMy40ODQzNzUgClEgNTMuMzc1IDE2Ljg0Mzc1IDU1LjI1IDIyLjUzMTI1IApRIDU3LjEyNSAyOC4yMTg3NSA1Ny4xMjUgMzYuMzI4MTI1IApRIDU3LjEyNSA0Ny41NjI1IDUzLjQzNzUgNTMuNTkzNzUgClEgNDkuNzUgNTkuNjI1IDQ0LjQ4NDM3NSA2MS42NzE4NzUgClEgNDAuNjcxODc1IDYzLjE0MDYyNSAzMi4yMzQzNzUgNjMuMTQwNjI1IApMIDE3LjE4NzUgNjMuMTQwNjI1IAp6CiIgaWQ9IkFyaWFsTVQtNjgiPjwvcGF0aD4KICAgICAgIDxwYXRoIGQ9Ik0gNDAuNDM3NSA2LjM5MDYyNSAKUSAzNS41NDY4NzUgMi4yNSAzMS4wMzEyNSAwLjUzMTI1IApRIDI2LjUxNTYyNSAtMS4xNzE4NzUgMjEuMzQzNzUgLTEuMTcxODc1IApRIDEyLjc5Njg3NSAtMS4xNzE4NzUgOC4yMDMxMjUgMyAKUSAzLjYwOTM3NSA3LjE3MTg3NSAzLjYwOTM3NSAxMy42NzE4NzUgClEgMy42MDkzNzUgMTcuNDg0Mzc1IDUuMzQzNzUgMjAuNjI1IApRIDcuMDc4MTI1IDIzLjc4MTI1IDkuODkwNjI1IDI1LjY4NzUgClEgMTIuNzAzMTI1IDI3LjU5Mzc1IDE2LjIxODc1IDI4LjU2MjUgClEgMTguNzk2ODc1IDI5LjI1IDI0LjAzMTI1IDI5Ljg5MDYyNSAKUSAzNC42NzE4NzUgMzEuMTU2MjUgMzkuNzAzMTI1IDMyLjkwNjI1IApRIDM5Ljc1IDM0LjcxODc1IDM5Ljc1IDM1LjIwMzEyNSAKUSAzOS43NSA0MC41NzgxMjUgMzcuMjUgNDIuNzgxMjUgClEgMzMuODkwNjI1IDQ1Ljc1IDI3LjI1IDQ1Ljc1IApRIDIxLjA0Njg3NSA0NS43NSAxOC4wOTM3NSA0My41NzgxMjUgClEgMTUuMTQwNjI1IDQxLjQwNjI1IDEzLjcxODc1IDM1Ljg5MDYyNSAKTCA1LjEyNSAzNy4wNjI1IApRIDYuMjk2ODc1IDQyLjU3ODEyNSA4Ljk4NDM3NSA0NS45Njg3NSAKUSAxMS42NzE4NzUgNDkuMzU5Mzc1IDE2Ljc1IDUxLjE4NzUgClEgMjEuODI4MTI1IDUzLjAzMTI1IDI4LjUxNTYyNSA1My4wMzEyNSAKUSAzNS4xNTYyNSA1My4wMzEyNSAzOS4yOTY4NzUgNTEuNDY4NzUgClEgNDMuNDUzMTI1IDQ5LjkwNjI1IDQ1LjQwNjI1IDQ3LjUzMTI1IApRIDQ3LjM1OTM3NSA0NS4xNzE4NzUgNDguMTQwNjI1IDQxLjU0Njg3NSAKUSA0OC41NzgxMjUgMzkuMzEyNSA0OC41NzgxMjUgMzMuNDUzMTI1IApMIDQ4LjU3ODEyNSAyMS43MzQzNzUgClEgNDguNTc4MTI1IDkuNDY4NzUgNDkuMTQwNjI1IDYuMjE4NzUgClEgNDkuNzAzMTI1IDIuOTg0Mzc1IDUxLjM3NSAwIApMIDQyLjE4NzUgMCAKUSA0MC44MjgxMjUgMi43MzQzNzUgNDAuNDM3NSA2LjM5MDYyNSAKegpNIDM5LjcwMzEyNSAyNi4wMzEyNSAKUSAzNC45MDYyNSAyNC4wNzgxMjUgMjUuMzQzNzUgMjIuNzAzMTI1IApRIDE5LjkyMTg3NSAyMS45MjE4NzUgMTcuNjcxODc1IDIwLjkzNzUgClEgMTUuNDM3NSAxOS45Njg3NSAxNC4yMDMxMjUgMTguMDkzNzUgClEgMTIuOTg0Mzc1IDE2LjIxODc1IDEyLjk4NDM3NSAxMy45MjE4NzUgClEgMTIuOTg0Mzc1IDEwLjQwNjI1IDE1LjY0MDYyNSA4LjA2MjUgClEgMTguMzEyNSA1LjcxODc1IDIzLjQzNzUgNS43MTg3NSAKUSAyOC41MTU2MjUgNS43MTg3NSAzMi40Njg3NSA3LjkzNzUgClEgMzYuNDIxODc1IDEwLjE1NjI1IDM4LjI4MTI1IDE0LjAxNTYyNSAKUSAzOS43MDMxMjUgMTcgMzkuNzAzMTI1IDIyLjc5Njg3NSAKegoiIGlkPSJBcmlhbE1ULTk3Ij48L3BhdGg+CiAgICAgICA8cGF0aCBkPSJNIDI1Ljc4MTI1IDcuODU5Mzc1IApMIDI3LjA0Njg3NSAwLjA5Mzc1IApRIDIzLjM0Mzc1IC0wLjY4NzUgMjAuNDA2MjUgLTAuNjg3NSAKUSAxNS42MjUgLTAuNjg3NSAxMi45ODQzNzUgMC44MjgxMjUgClEgMTAuMzU5Mzc1IDIuMzQzNzUgOS4yODEyNSA0LjgxMjUgClEgOC4yMDMxMjUgNy4yODEyNSA4LjIwMzEyNSAxNS4xODc1IApMIDguMjAzMTI1IDQ1LjAxNTYyNSAKTCAxLjc2NTYyNSA0NS4wMTU2MjUgCkwgMS43NjU2MjUgNTEuODU5Mzc1IApMIDguMjAzMTI1IDUxLjg1OTM3NSAKTCA4LjIwMzEyNSA2NC43MDMxMjUgCkwgMTYuOTM3NSA2OS45Njg3NSAKTCAxNi45Mzc1IDUxLjg1OTM3NSAKTCAyNS43ODEyNSA1MS44NTkzNzUgCkwgMjUuNzgxMjUgNDUuMDE1NjI1IApMIDE2LjkzNzUgNDUuMDE1NjI1IApMIDE2LjkzNzUgMTQuNzAzMTI1IApRIDE2LjkzNzUgMTAuOTM3NSAxNy40MDYyNSA5Ljg1OTM3NSAKUSAxNy44NzUgOC43OTY4NzUgMTguOTIxODc1IDguMTU2MjUgClEgMTkuOTY4NzUgNy41MTU2MjUgMjEuOTIxODc1IDcuNTE1NjI1IApRIDIzLjM5MDYyNSA3LjUxNTYyNSAyNS43ODEyNSA3Ljg1OTM3NSAKegoiIGlkPSJBcmlhbE1ULTExNiI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSA0Mi4wOTM3NSAxNi43MDMxMjUgCkwgNTEuMTcxODc1IDE1LjU3ODEyNSAKUSA0OS4wMzEyNSA3LjYyNSA0My4yMTg3NSAzLjIxODc1IApRIDM3LjQwNjI1IC0xLjE3MTg3NSAyOC4zNzUgLTEuMTcxODc1IApRIDE3IC0xLjE3MTg3NSAxMC4zMjgxMjUgNS44MjgxMjUgClEgMy42NTYyNSAxMi44NDM3NSAzLjY1NjI1IDI1LjQ4NDM3NSAKUSAzLjY1NjI1IDM4LjU3ODEyNSAxMC4zOTA2MjUgNDUuNzk2ODc1IApRIDE3LjE0MDYyNSA1My4wMzEyNSAyNy44NzUgNTMuMDMxMjUgClEgMzguMjgxMjUgNTMuMDMxMjUgNDQuODc1IDQ1Ljk1MzEyNSAKUSA1MS40Njg3NSAzOC44NzUgNTEuNDY4NzUgMjYuMDMxMjUgClEgNTEuNDY4NzUgMjUuMjUgNTEuNDIxODc1IDIzLjY4NzUgCkwgMTIuNzUgMjMuNjg3NSAKUSAxMy4yMzQzNzUgMTUuMTQwNjI1IDE3LjU3ODEyNSAxMC41OTM3NSAKUSAyMS45MjE4NzUgNi4wNjI1IDI4LjQyMTg3NSA2LjA2MjUgClEgMzMuMjUgNi4wNjI1IDM2LjY3MTg3NSA4LjU5Mzc1IApRIDQwLjA5Mzc1IDExLjE0MDYyNSA0Mi4wOTM3NSAxNi43MDMxMjUgCnoKTSAxMy4yMzQzNzUgMzAuOTA2MjUgCkwgNDIuMTg3NSAzMC45MDYyNSAKUSA0MS42MDkzNzUgMzcuNDUzMTI1IDM4Ljg3NSA0MC43MTg3NSAKUSAzNC42NzE4NzUgNDUuNzk2ODc1IDI3Ljk4NDM3NSA0NS43OTY4NzUgClEgMjEuOTIxODc1IDQ1Ljc5Njg3NSAxNy43OTY4NzUgNDEuNzUgClEgMTMuNjcxODc1IDM3LjcwMzEyNSAxMy4yMzQzNzUgMzAuOTA2MjUgCnoKIiBpZD0iQXJpYWxNVC0xMDEiPjwvcGF0aD4KICAgICAgPC9kZWZzPgogICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTY4Ij48L3VzZT4KICAgICAgPHVzZSB4PSI3Mi4yMTY3OTciIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTk3Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxMjcuODMyMDMxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTYiPjwvdXNlPgogICAgICA8dXNlIHg9IjE1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgPC9nPgogICAgPC9nPgogICA8L2c+CiAgIDxnIGlkPSJtYXRwbG90bGliLmF4aXNfMiI+CiAgICA8ZyBpZD0ieXRpY2tfMSI+CiAgICAgPGcgaWQ9ImxpbmUyZF8yMSI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwN2Q3NzEyMGUyMCkiIGQ9Ik0gMzUuMDIyMTg4IDMxOC4yNTc4MjIgCkwgNTkzLjAyMjE4NyAzMTguMjU3ODIyIAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMjIiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xMiI+CiAgICAgIDwhLS0gMCAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIyLjQ2MTI1IDMyMS44MzY3Mjkpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inl0aWNrXzIiPgogICAgIDxnIGlkPSJsaW5lMmRfMjMiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDM1LjAyMjE4OCAyNjkuODIxNDM4IApMIDU5My4wMjIxODcgMjY5LjgyMTQzOCAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzI0Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMTMiPgogICAgICA8IS0tIDEgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyMi40NjEyNSAyNzMuNDAwMzQ0KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja18zIj4KICAgICA8ZyBpZD0ibGluZTJkXzI1Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A3ZDc3MTIwZTIwKSIgZD0iTSAzNS4wMjIxODggMjIxLjM4NTA1NCAKTCA1OTMuMDIyMTg3IDIyMS4zODUwNTQgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8yNiI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzE0Ij4KICAgICAgPCEtLSAyIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMjIuNDYxMjUgMjI0Ljk2Mzk2KXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUwIj48L3VzZT4KICAgICAgPC9nPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJ5dGlja180Ij4KICAgICA8ZyBpZD0ibGluZTJkXzI3Ij4KICAgICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A3ZDc3MTIwZTIwKSIgZD0iTSAzNS4wMjIxODggMTcyLjk0ODY2OSAKTCA1OTMuMDIyMTg3IDE3Mi45NDg2NjkgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2ZmZmZmZjtzdHJva2UtbGluZWNhcDpyb3VuZDsiPjwvcGF0aD4KICAgICA8L2c+CiAgICAgPGcgaWQ9ImxpbmUyZF8yOCI+PC9nPgogICAgIDxnIGlkPSJ0ZXh0XzE1Ij4KICAgICAgPCEtLSAzIC0tPgogICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMjIuNDYxMjUgMTc2LjUyNzU3NSlzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPGRlZnM+CiAgICAgICAgPHBhdGggZD0iTSA0LjIwMzEyNSAxOC44OTA2MjUgCkwgMTIuOTg0Mzc1IDIwLjA2MjUgClEgMTQuNSAxMi41OTM3NSAxOC4xNDA2MjUgOS4yOTY4NzUgClEgMjEuNzgxMjUgNiAyNyA2IApRIDMzLjIwMzEyNSA2IDM3LjQ2ODc1IDEwLjI5Njg3NSAKUSA0MS43NSAxNC41OTM3NSA0MS43NSAyMC45NTMxMjUgClEgNDEuNzUgMjcgMzcuNzk2ODc1IDMwLjkyMTg3NSAKUSAzMy44NDM3NSAzNC44NTkzNzUgMjcuNzM0Mzc1IDM0Ljg1OTM3NSAKUSAyNS4yNSAzNC44NTkzNzUgMjEuNTMxMjUgMzMuODkwNjI1IApMIDIyLjUxNTYyNSA0MS42MDkzNzUgClEgMjMuMzkwNjI1IDQxLjUgMjMuOTIxODc1IDQxLjUgClEgMjkuNTQ2ODc1IDQxLjUgMzQuMDMxMjUgNDQuNDIxODc1IApRIDM4LjUzMTI1IDQ3LjM1OTM3NSAzOC41MzEyNSA1My40Njg3NSAKUSAzOC41MzEyNSA1OC4yOTY4NzUgMzUuMjUgNjEuNDY4NzUgClEgMzEuOTg0Mzc1IDY0LjY1NjI1IDI2LjgxMjUgNjQuNjU2MjUgClEgMjEuNjg3NSA2NC42NTYyNSAxOC4yNjU2MjUgNjEuNDIxODc1IApRIDE0Ljg0Mzc1IDU4LjIwMzEyNSAxMy44NzUgNTEuNzY1NjI1IApMIDUuMDc4MTI1IDUzLjMyODEyNSAKUSA2LjY4NzUgNjIuMTU2MjUgMTIuMzkwNjI1IDY3LjAxNTYyNSAKUSAxOC4xMDkzNzUgNzEuODc1IDI2LjYwOTM3NSA3MS44NzUgClEgMzIuNDY4NzUgNzEuODc1IDM3LjM5MDYyNSA2OS4zNTkzNzUgClEgNDIuMzI4MTI1IDY2Ljg0Mzc1IDQ0LjkzNzUgNjIuNSAKUSA0Ny41NjI1IDU4LjE1NjI1IDQ3LjU2MjUgNTMuMjY1NjI1IApRIDQ3LjU2MjUgNDguNjQwNjI1IDQ1LjA2MjUgNDQuODI4MTI1IApRIDQyLjU3ODEyNSA0MS4wMTU2MjUgMzcuNzAzMTI1IDM4Ljc2NTYyNSAKUSA0NC4wNDY4NzUgMzcuMzEyNSA0Ny41NjI1IDMyLjY4NzUgClEgNTEuMDc4MTI1IDI4LjA3ODEyNSA1MS4wNzgxMjUgMjEuMTQwNjI1IApRIDUxLjA3ODEyNSAxMS43NjU2MjUgNDQuMjM0Mzc1IDUuMjUgClEgMzcuNDA2MjUgLTEuMjY1NjI1IDI2Ljk1MzEyNSAtMS4yNjU2MjUgClEgMTcuNTMxMjUgLTEuMjY1NjI1IDExLjI5Njg3NSA0LjM0Mzc1IApRIDUuMDc4MTI1IDkuOTY4NzUgNC4yMDMxMjUgMTguODkwNjI1IAp6CiIgaWQ9IkFyaWFsTVQtNTEiPjwvcGF0aD4KICAgICAgIDwvZGVmcz4KICAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTEiPjwvdXNlPgogICAgICA8L2c+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9Inl0aWNrXzUiPgogICAgIDxnIGlkPSJsaW5lMmRfMjkiPgogICAgICA8cGF0aCBjbGlwLXBhdGg9InVybCgjcDdkNzcxMjBlMjApIiBkPSJNIDM1LjAyMjE4OCAxMjQuNTEyMjg1IApMIDU5My4wMjIxODcgMTI0LjUxMjI4NSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzMwIj48L2c+CiAgICAgPGcgaWQ9InRleHRfMTYiPgogICAgICA8IS0tIDQgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyMi40NjEyNSAxMjguMDkxMTkxKXNjYWxlKDAuMSAtMC4xKSI+CiAgICAgICA8ZGVmcz4KICAgICAgICA8cGF0aCBkPSJNIDMyLjMyODEyNSAwIApMIDMyLjMyODEyNSAxNy4xNDA2MjUgCkwgMS4yNjU2MjUgMTcuMTQwNjI1IApMIDEuMjY1NjI1IDI1LjIwMzEyNSAKTCAzMy45Mzc1IDcxLjU3ODEyNSAKTCA0MS4xMDkzNzUgNzEuNTc4MTI1IApMIDQxLjEwOTM3NSAyNS4yMDMxMjUgCkwgNTAuNzgxMjUgMjUuMjAzMTI1IApMIDUwLjc4MTI1IDE3LjE0MDYyNSAKTCA0MS4xMDkzNzUgMTcuMTQwNjI1IApMIDQxLjEwOTM3NSAwIAp6Ck0gMzIuMzI4MTI1IDI1LjIwMzEyNSAKTCAzMi4zMjgxMjUgNTcuNDY4NzUgCkwgOS45MDYyNSAyNS4yMDMxMjUgCnoKIiBpZD0iQXJpYWxNVC01MiI+PC9wYXRoPgogICAgICAgPC9kZWZzPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MiI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfNiI+CiAgICAgPGcgaWQ9ImxpbmUyZF8zMSI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwN2Q3NzEyMGUyMCkiIGQ9Ik0gMzUuMDIyMTg4IDc2LjA3NTkgCkwgNTkzLjAyMjE4NyA3Ni4wNzU5IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNmZmZmZmY7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7Ij48L3BhdGg+CiAgICAgPC9nPgogICAgIDxnIGlkPSJsaW5lMmRfMzIiPjwvZz4KICAgICA8ZyBpZD0idGV4dF8xNyI+CiAgICAgIDwhLS0gNSAtLT4KICAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIyLjQ2MTI1IDc5LjY1NDgwNylzY2FsZSgwLjEgLTAuMSkiPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01MyI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ieXRpY2tfNyI+CiAgICAgPGcgaWQ9ImxpbmUyZF8zMyI+CiAgICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwN2Q3NzEyMGUyMCkiIGQ9Ik0gMzUuMDIyMTg4IDI3LjYzOTUxNiAKTCA1OTMuMDIyMTg3IDI3LjYzOTUxNiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojZmZmZmZmO3N0cm9rZS1saW5lY2FwOnJvdW5kOyI+PC9wYXRoPgogICAgIDwvZz4KICAgICA8ZyBpZD0ibGluZTJkXzM0Ij48L2c+CiAgICAgPGcgaWQ9InRleHRfMTgiPgogICAgICA8IS0tIDYgLS0+CiAgICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyMi40NjEyNSAzMS4yMTg0MjIpc2NhbGUoMC4xIC0wLjEpIj4KICAgICAgIDxkZWZzPgogICAgICAgIDxwYXRoIGQ9Ik0gNDkuNzUgNTQuMDQ2ODc1IApMIDQxLjAxNTYyNSA1My4zNzUgClEgMzkuODQzNzUgNTguNTQ2ODc1IDM3LjcwMzEyNSA2MC44OTA2MjUgClEgMzQuMTI1IDY0LjY1NjI1IDI4LjkwNjI1IDY0LjY1NjI1IApRIDI0LjcwMzEyNSA2NC42NTYyNSAyMS41MzEyNSA2Mi4zMTI1IApRIDE3LjM5MDYyNSA1OS4yODEyNSAxNC45ODQzNzUgNTMuNDY4NzUgClEgMTIuNTkzNzUgNDcuNjU2MjUgMTIuNSAzNi45MjE4NzUgClEgMTUuNjcxODc1IDQxLjc1IDIwLjI2NTYyNSA0NC4wOTM3NSAKUSAyNC44NTkzNzUgNDYuNDM3NSAyOS44OTA2MjUgNDYuNDM3NSAKUSAzOC42NzE4NzUgNDYuNDM3NSA0NC44NDM3NSAzOS45Njg3NSAKUSA1MS4wMzEyNSAzMy41IDUxLjAzMTI1IDIzLjI1IApRIDUxLjAzMTI1IDE2LjUgNDguMTI1IDEwLjcxODc1IApRIDQ1LjIxODc1IDQuOTM3NSA0MC4xNDA2MjUgMS44NTkzNzUgClEgMzUuMDYyNSAtMS4yMTg3NSAyOC42MDkzNzUgLTEuMjE4NzUgClEgMTcuNjI1IC0xLjIxODc1IDEwLjY4NzUgNi44NTkzNzUgClEgMy43NjU2MjUgMTQuOTM3NSAzLjc2NTYyNSAzMy41IApRIDMuNzY1NjI1IDU0LjI1IDExLjQyMTg3NSA2My42NzE4NzUgClEgMTguMTA5Mzc1IDcxLjg3NSAyOS40Mzc1IDcxLjg3NSAKUSAzNy44OTA2MjUgNzEuODc1IDQzLjI4MTI1IDY3LjE0MDYyNSAKUSA0OC42ODc1IDYyLjQwNjI1IDQ5Ljc1IDU0LjA0Njg3NSAKegpNIDEzLjg3NSAyMy4xODc1IApRIDEzLjg3NSAxOC42NTYyNSAxNS43OTY4NzUgMTQuNSAKUSAxNy43MTg3NSAxMC4zNTkzNzUgMjEuMTg3NSA4LjE3MTg3NSAKUSAyNC42NTYyNSA2IDI4LjQ2ODc1IDYgClEgMzQuMDMxMjUgNiAzOC4wMzEyNSAxMC40ODQzNzUgClEgNDIuMDQ2ODc1IDE0Ljk4NDM3NSA0Mi4wNDY4NzUgMjIuNzAzMTI1IApRIDQyLjA0Njg3NSAzMC4xMjUgMzguMDc4MTI1IDM0LjM5MDYyNSAKUSAzNC4xMjUgMzguNjcxODc1IDI4LjEyNSAzOC42NzE4NzUgClEgMjIuMTcxODc1IDM4LjY3MTg3NSAxOC4wMTU2MjUgMzQuMzkwNjI1IApRIDEzLjg3NSAzMC4xMjUgMTMuODc1IDIzLjE4NzUgCnoKIiBpZD0iQXJpYWxNVC01NCI+PC9wYXRoPgogICAgICAgPC9kZWZzPgogICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC01NCI+PC91c2U+CiAgICAgIDwvZz4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0idGV4dF8xOSI+CiAgICAgPCEtLSBDdW11bGF0aXZlIFJldHVybnMgKEFic29sdXRlKSAtLT4KICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTUuOTM1NjI1IDI2OS42MjMxMjUpcm90YXRlKC05MClzY2FsZSgwLjEyIC0wLjEyKSI+CiAgICAgIDxkZWZzPgogICAgICAgPHBhdGggZD0iTSA1OC43OTY4NzUgMjUuMDkzNzUgCkwgNjguMjY1NjI1IDIyLjcwMzEyNSAKUSA2NS4yODEyNSAxMS4wMzEyNSA1Ny41NDY4NzUgNC45MDYyNSAKUSA0OS44MTI1IC0xLjIxODc1IDM4LjYyNSAtMS4yMTg3NSAKUSAyNy4wNDY4NzUgLTEuMjE4NzUgMTkuNzk2ODc1IDMuNDg0Mzc1IApRIDEyLjU0Njg3NSA4LjIwMzEyNSA4Ljc2NTYyNSAxNy4xNDA2MjUgClEgNC45ODQzNzUgMjYuMDc4MTI1IDQuOTg0Mzc1IDM2LjMyODEyNSAKUSA0Ljk4NDM3NSA0Ny41MTU2MjUgOS4yNSA1NS44MjgxMjUgClEgMTMuNTMxMjUgNjQuMTU2MjUgMjEuNDA2MjUgNjguNDY4NzUgClEgMjkuMjk2ODc1IDcyLjc5Njg3NSAzOC43NjU2MjUgNzIuNzk2ODc1IApRIDQ5LjUxNTYyNSA3Mi43OTY4NzUgNTYuODI4MTI1IDY3LjMyODEyNSAKUSA2NC4xNTYyNSA2MS44NTkzNzUgNjcuMDQ2ODc1IDUxLjk1MzEyNSAKTCA1Ny43MTg3NSA0OS43NSAKUSA1NS4yMTg3NSA1Ny41NjI1IDUwLjQ4NDM3NSA2MS4xMjUgClEgNDUuNzUgNjQuNzAzMTI1IDM4LjU3ODEyNSA2NC43MDMxMjUgClEgMzAuMzI4MTI1IDY0LjcwMzEyNSAyNC43ODEyNSA2MC43MzQzNzUgClEgMTkuMjM0Mzc1IDU2Ljc4MTI1IDE2Ljk4NDM3NSA1MC4xMDkzNzUgClEgMTQuNzUgNDMuNDUzMTI1IDE0Ljc1IDM2LjM3NSAKUSAxNC43NSAyNy4yNSAxNy40MDYyNSAyMC40Mzc1IApRIDIwLjA2MjUgMTMuNjI1IDI1LjY3MTg3NSAxMC4yNSAKUSAzMS4yOTY4NzUgNi44OTA2MjUgMzcuODQzNzUgNi44OTA2MjUgClEgNDUuNzk2ODc1IDYuODkwNjI1IDUxLjMxMjUgMTEuNDY4NzUgClEgNTYuODQzNzUgMTYuMDYyNSA1OC43OTY4NzUgMjUuMDkzNzUgCnoKIiBpZD0iQXJpYWxNVC02NyI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSA0MC41NzgxMjUgMCAKTCA0MC41NzgxMjUgNy42MjUgClEgMzQuNTE1NjI1IC0xLjE3MTg3NSAyNC4xMjUgLTEuMTcxODc1IApRIDE5LjUzMTI1IC0xLjE3MTg3NSAxNS41NDY4NzUgMC41NzgxMjUgClEgMTEuNTc4MTI1IDIuMzQzNzUgOS42NDA2MjUgNSAKUSA3LjcxODc1IDcuNjcxODc1IDYuOTM3NSAxMS41MzEyNSAKUSA2LjM5MDYyNSAxNC4xMDkzNzUgNi4zOTA2MjUgMTkuNzM0Mzc1IApMIDYuMzkwNjI1IDUxLjg1OTM3NSAKTCAxNS4xODc1IDUxLjg1OTM3NSAKTCAxNS4xODc1IDIzLjA5Mzc1IApRIDE1LjE4NzUgMTYuMjE4NzUgMTUuNzE4NzUgMTMuODEyNSAKUSAxNi41NDY4NzUgMTAuMzU5Mzc1IDE5LjIzNDM3NSA4LjM3NSAKUSAyMS45MjE4NzUgNi4zOTA2MjUgMjUuODc1IDYuMzkwNjI1IApRIDI5LjgyODEyNSA2LjM5MDYyNSAzMy4yOTY4NzUgOC40MjE4NzUgClEgMzYuNzY1NjI1IDEwLjQ1MzEyNSAzOC4yMDMxMjUgMTMuOTM3NSAKUSAzOS42NTYyNSAxNy40Mzc1IDM5LjY1NjI1IDI0LjA3ODEyNSAKTCAzOS42NTYyNSA1MS44NTkzNzUgCkwgNDguNDM3NSA1MS44NTkzNzUgCkwgNDguNDM3NSAwIAp6CiIgaWQ9IkFyaWFsTVQtMTE3Ij48L3BhdGg+CiAgICAgICA8cGF0aCBkPSJNIDYuNTkzNzUgMCAKTCA2LjU5Mzc1IDUxLjg1OTM3NSAKTCAxNC40NTMxMjUgNTEuODU5Mzc1IApMIDE0LjQ1MzEyNSA0NC41NzgxMjUgClEgMTYuODkwNjI1IDQ4LjM5MDYyNSAyMC45Mzc1IDUwLjcwMzEyNSAKUSAyNSA1My4wMzEyNSAzMC4xNzE4NzUgNTMuMDMxMjUgClEgMzUuOTM3NSA1My4wMzEyNSAzOS42MjUgNTAuNjQwNjI1IApRIDQzLjMxMjUgNDguMjUgNDQuODI4MTI1IDQzLjk1MzEyNSAKUSA1MC45ODQzNzUgNTMuMDMxMjUgNjAuODQzNzUgNTMuMDMxMjUgClEgNjguNTYyNSA1My4wMzEyNSA3Mi43MDMxMjUgNDguNzUgClEgNzYuODU5Mzc1IDQ0LjQ4NDM3NSA3Ni44NTkzNzUgMzUuNTkzNzUgCkwgNzYuODU5Mzc1IDAgCkwgNjguMTA5Mzc1IDAgCkwgNjguMTA5Mzc1IDMyLjY3MTg3NSAKUSA2OC4xMDkzNzUgMzcuOTM3NSA2Ny4yNSA0MC4yNSAKUSA2Ni40MDYyNSA0Mi41NzgxMjUgNjQuMTU2MjUgNDMuOTg0Mzc1IApRIDYxLjkyMTg3NSA0NS40MDYyNSA1OC44OTA2MjUgNDUuNDA2MjUgClEgNTMuNDIxODc1IDQ1LjQwNjI1IDQ5Ljc5Njg3NSA0MS43NjU2MjUgClEgNDYuMTg3NSAzOC4xNDA2MjUgNDYuMTg3NSAzMC4xMjUgCkwgNDYuMTg3NSAwIApMIDM3LjQwNjI1IDAgCkwgMzcuNDA2MjUgMzMuNjg3NSAKUSAzNy40MDYyNSAzOS41NDY4NzUgMzUuMjUgNDIuNDY4NzUgClEgMzMuMTA5Mzc1IDQ1LjQwNjI1IDI4LjIxODc1IDQ1LjQwNjI1IApRIDI0LjUxNTYyNSA0NS40MDYyNSAyMS4zNTkzNzUgNDMuNDUzMTI1IApRIDE4LjIxODc1IDQxLjUgMTYuNzk2ODc1IDM3LjczNDM3NSAKUSAxNS4zNzUgMzMuOTg0Mzc1IDE1LjM3NSAyNi45MDYyNSAKTCAxNS4zNzUgMCAKegoiIGlkPSJBcmlhbE1ULTEwOSI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSA2LjM5MDYyNSAwIApMIDYuMzkwNjI1IDcxLjU3ODEyNSAKTCAxNS4xODc1IDcxLjU3ODEyNSAKTCAxNS4xODc1IDAgCnoKIiBpZD0iQXJpYWxNVC0xMDgiPjwvcGF0aD4KICAgICAgIDxwYXRoIGQ9Ik0gNi42NDA2MjUgNjEuNDY4NzUgCkwgNi42NDA2MjUgNzEuNTc4MTI1IApMIDE1LjQzNzUgNzEuNTc4MTI1IApMIDE1LjQzNzUgNjEuNDY4NzUgCnoKTSA2LjY0MDYyNSAwIApMIDYuNjQwNjI1IDUxLjg1OTM3NSAKTCAxNS40Mzc1IDUxLjg1OTM3NSAKTCAxNS40Mzc1IDAgCnoKIiBpZD0iQXJpYWxNVC0xMDUiPjwvcGF0aD4KICAgICAgIDxwYXRoIGQ9Ik0gMjEgMCAKTCAxLjI2NTYyNSA1MS44NTkzNzUgCkwgMTAuNTQ2ODc1IDUxLjg1OTM3NSAKTCAyMS42ODc1IDIwLjc5Njg3NSAKUSAyMy40ODQzNzUgMTUuNzY1NjI1IDI1IDEwLjM1OTM3NSAKUSAyNi4xNzE4NzUgMTQuNDUzMTI1IDI4LjI2NTYyNSAyMC4yMTg3NSAKTCAzOS43OTY4NzUgNTEuODU5Mzc1IApMIDQ4LjgyODEyNSA1MS44NTkzNzUgCkwgMjkuMjAzMTI1IDAgCnoKIiBpZD0iQXJpYWxNVC0xMTgiPjwvcGF0aD4KICAgICAgIDxwYXRoIGlkPSJBcmlhbE1ULTMyIj48L3BhdGg+CiAgICAgICA8cGF0aCBkPSJNIDcuODU5Mzc1IDAgCkwgNy44NTkzNzUgNzEuNTc4MTI1IApMIDM5LjU5Mzc1IDcxLjU3ODEyNSAKUSA0OS4xNzE4NzUgNzEuNTc4MTI1IDU0LjE0MDYyNSA2OS42NDA2MjUgClEgNTkuMTI1IDY3LjcxODc1IDYyLjEwOTM3NSA2Mi44MjgxMjUgClEgNjUuMDkzNzUgNTcuOTUzMTI1IDY1LjA5Mzc1IDUyLjA0Njg3NSAKUSA2NS4wOTM3NSA0NC40Mzc1IDYwLjE1NjI1IDM5LjIwMzEyNSAKUSA1NS4yMTg3NSAzMy45ODQzNzUgNDQuOTIxODc1IDMyLjU2MjUgClEgNDguNjg3NSAzMC43NjU2MjUgNTAuNjQwNjI1IDI5IApRIDU0Ljc4MTI1IDI1LjIwMzEyNSA1OC41IDE5LjQ4NDM3NSAKTCA3MC45NTMxMjUgMCAKTCA1OS4wMzEyNSAwIApMIDQ5LjU2MjUgMTQuODkwNjI1IApRIDQ1LjQwNjI1IDIxLjM0Mzc1IDQyLjcxODc1IDI0Ljc1IApRIDQwLjA0Njg3NSAyOC4xNzE4NzUgMzcuOTIxODc1IDI5LjUzMTI1IApRIDM1Ljc5Njg3NSAzMC45MDYyNSAzMy41OTM3NSAzMS40NTMxMjUgClEgMzEuOTg0Mzc1IDMxLjc4MTI1IDI4LjMyODEyNSAzMS43ODEyNSAKTCAxNy4zMjgxMjUgMzEuNzgxMjUgCkwgMTcuMzI4MTI1IDAgCnoKTSAxNy4zMjgxMjUgMzkuOTg0Mzc1IApMIDM3LjcwMzEyNSAzOS45ODQzNzUgClEgNDQuMTg3NSAzOS45ODQzNzUgNDcuODQzNzUgNDEuMzI4MTI1IApRIDUxLjUxNTYyNSA0Mi42NzE4NzUgNTMuNDIxODc1IDQ1LjYyNSAKUSA1NS4zMjgxMjUgNDguNTc4MTI1IDU1LjMyODEyNSA1Mi4wNDY4NzUgClEgNTUuMzI4MTI1IDU3LjEyNSA1MS42NDA2MjUgNjAuMzkwNjI1IApRIDQ3Ljk1MzEyNSA2My42NzE4NzUgMzkuOTg0Mzc1IDYzLjY3MTg3NSAKTCAxNy4zMjgxMjUgNjMuNjcxODc1IAp6CiIgaWQ9IkFyaWFsTVQtODIiPjwvcGF0aD4KICAgICAgIDxwYXRoIGQ9Ik0gNi41IDAgCkwgNi41IDUxLjg1OTM3NSAKTCAxNC40MDYyNSA1MS44NTkzNzUgCkwgMTQuNDA2MjUgNDQgClEgMTcuNDM3NSA0OS41MTU2MjUgMjAgNTEuMjY1NjI1IApRIDIyLjU2MjUgNTMuMDMxMjUgMjUuNjQwNjI1IDUzLjAzMTI1IApRIDMwLjA3ODEyNSA1My4wMzEyNSAzNC42NzE4NzUgNTAuMjAzMTI1IApMIDMxLjY0MDYyNSA0Mi4wNDY4NzUgClEgMjguNDIxODc1IDQzLjk1MzEyNSAyNS4yMDMxMjUgNDMuOTUzMTI1IApRIDIyLjMxMjUgNDMuOTUzMTI1IDIwLjAxNTYyNSA0Mi4yMTg3NSAKUSAxNy43MTg3NSA0MC40ODQzNzUgMTYuNzUgMzcuNDA2MjUgClEgMTUuMjgxMjUgMzIuNzE4NzUgMTUuMjgxMjUgMjcuMTU2MjUgCkwgMTUuMjgxMjUgMCAKegoiIGlkPSJBcmlhbE1ULTExNCI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSA2LjU5Mzc1IDAgCkwgNi41OTM3NSA1MS44NTkzNzUgCkwgMTQuNSA1MS44NTkzNzUgCkwgMTQuNSA0NC40ODQzNzUgClEgMjAuMjE4NzUgNTMuMDMxMjUgMzEgNTMuMDMxMjUgClEgMzUuNjg3NSA1My4wMzEyNSAzOS42MjUgNTEuMzQzNzUgClEgNDMuNTYyNSA0OS42NTYyNSA0NS41MTU2MjUgNDYuOTIxODc1IApRIDQ3LjQ2ODc1IDQ0LjE4NzUgNDguMjUgNDAuNDM3NSAKUSA0OC43MzQzNzUgMzcuOTg0Mzc1IDQ4LjczNDM3NSAzMS44OTA2MjUgCkwgNDguNzM0Mzc1IDAgCkwgMzkuOTM3NSAwIApMIDM5LjkzNzUgMzEuNTQ2ODc1IApRIDM5LjkzNzUgMzYuOTIxODc1IDM4LjkwNjI1IDM5LjU3ODEyNSAKUSAzNy44OTA2MjUgNDIuMjM0Mzc1IDM1LjI4MTI1IDQzLjgxMjUgClEgMzIuNjcxODc1IDQ1LjQwNjI1IDI5LjE1NjI1IDQ1LjQwNjI1IApRIDIzLjUzMTI1IDQ1LjQwNjI1IDE5LjQ1MzEyNSA0MS44NDM3NSAKUSAxNS4zNzUgMzguMjgxMjUgMTUuMzc1IDI4LjMyODEyNSAKTCAxNS4zNzUgMCAKegoiIGlkPSJBcmlhbE1ULTExMCI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSAzLjA3ODEyNSAxNS40ODQzNzUgCkwgMTEuNzY1NjI1IDE2Ljg0Mzc1IApRIDEyLjUgMTEuNjI1IDE1Ljg0Mzc1IDguODQzNzUgClEgMTkuMTg3NSA2LjA2MjUgMjUuMjAzMTI1IDYuMDYyNSAKUSAzMS4yNSA2LjA2MjUgMzQuMTcxODc1IDguNTE1NjI1IApRIDM3LjEwOTM3NSAxMC45ODQzNzUgMzcuMTA5Mzc1IDE0LjMxMjUgClEgMzcuMTA5Mzc1IDE3LjI4MTI1IDM0LjUxNTYyNSAxOSAKUSAzMi43MTg3NSAyMC4xNzE4NzUgMjUuNTMxMjUgMjEuOTY4NzUgClEgMTUuODc1IDI0LjQyMTg3NSAxMi4xNDA2MjUgMjYuMjAzMTI1IApRIDguNDA2MjUgMjcuOTg0Mzc1IDYuNDY4NzUgMzEuMTI1IApRIDQuNTQ2ODc1IDM0LjI4MTI1IDQuNTQ2ODc1IDM4LjA5Mzc1IApRIDQuNTQ2ODc1IDQxLjU0Njg3NSA2LjEyNSA0NC41IApRIDcuNzE4NzUgNDcuNDY4NzUgMTAuNDUzMTI1IDQ5LjQyMTg3NSAKUSAxMi41IDUwLjkyMTg3NSAxNi4wMzEyNSA1MS45Njg3NSAKUSAxOS41NzgxMjUgNTMuMDMxMjUgMjMuNjQwNjI1IDUzLjAzMTI1IApRIDI5LjczNDM3NSA1My4wMzEyNSAzNC4zNDM3NSA1MS4yNjU2MjUgClEgMzguOTY4NzUgNDkuNTE1NjI1IDQxLjE1NjI1IDQ2LjUgClEgNDMuMzU5Mzc1IDQzLjUgNDQuMTg3NSAzOC40ODQzNzUgCkwgMzUuNTkzNzUgMzcuMzEyNSAKUSAzNS4wMTU2MjUgNDEuMzEyNSAzMi4yMDMxMjUgNDMuNTQ2ODc1IApRIDI5LjM5MDYyNSA0NS43OTY4NzUgMjQuMjY1NjI1IDQ1Ljc5Njg3NSAKUSAxOC4yMTg3NSA0NS43OTY4NzUgMTUuNjI1IDQzLjc5Njg3NSAKUSAxMy4wMzEyNSA0MS43OTY4NzUgMTMuMDMxMjUgMzkuMTA5Mzc1IApRIDEzLjAzMTI1IDM3LjQwNjI1IDE0LjEwOTM3NSAzNi4wMzEyNSAKUSAxNS4xODc1IDM0LjYyNSAxNy40ODQzNzUgMzMuNjg3NSAKUSAxOC43OTY4NzUgMzMuMjAzMTI1IDI1LjI1IDMxLjQ1MzEyNSAKUSAzNC41NzgxMjUgMjguOTUzMTI1IDM4LjI1IDI3LjM1OTM3NSAKUSA0MS45Mzc1IDI1Ljc4MTI1IDQ0LjAzMTI1IDIyLjc1IApRIDQ2LjE0MDYyNSAxOS43MzQzNzUgNDYuMTQwNjI1IDE1LjIzNDM3NSAKUSA0Ni4xNDA2MjUgMTAuODQzNzUgNDMuNTc4MTI1IDYuOTUzMTI1IApRIDQxLjAxNTYyNSAzLjA3ODEyNSAzNi4xNzE4NzUgMC45NTMxMjUgClEgMzEuMzQzNzUgLTEuMTcxODc1IDI1LjI1IC0xLjE3MTg3NSAKUSAxNS4xNDA2MjUgLTEuMTcxODc1IDkuODQzNzUgMy4wMzEyNSAKUSA0LjU0Njg3NSA3LjIzNDM3NSAzLjA3ODEyNSAxNS40ODQzNzUgCnoKIiBpZD0iQXJpYWxNVC0xMTUiPjwvcGF0aD4KICAgICAgIDxwYXRoIGQ9Ik0gMjMuMzkwNjI1IC0yMS4wNDY4NzUgClEgMTYuMTA5Mzc1IC0xMS44NTkzNzUgMTEuMDc4MTI1IDAuNDM3NSAKUSA2LjA2MjUgMTIuNzUgNi4wNjI1IDI1LjkyMTg3NSAKUSA2LjA2MjUgMzcuNTQ2ODc1IDkuODEyNSA0OC4xODc1IApRIDE0LjIwMzEyNSA2MC41NDY4NzUgMjMuMzkwNjI1IDcyLjc5Njg3NSAKTCAyOS42ODc1IDcyLjc5Njg3NSAKUSAyMy43ODEyNSA2Mi42NDA2MjUgMjEuODc1IDU4LjI5Njg3NSAKUSAxOC44OTA2MjUgNTEuNTYyNSAxNy4xODc1IDQ0LjIzNDM3NSAKUSAxNS4wOTM3NSAzNS4xMDkzNzUgMTUuMDkzNzUgMjUuODc1IApRIDE1LjA5Mzc1IDIuMzkwNjI1IDI5LjY4NzUgLTIxLjA0Njg3NSAKegoiIGlkPSJBcmlhbE1ULTQwIj48L3BhdGg+CiAgICAgICA8cGF0aCBkPSJNIC0wLjE0MDYyNSAwIApMIDI3LjM0Mzc1IDcxLjU3ODEyNSAKTCAzNy41NDY4NzUgNzEuNTc4MTI1IApMIDY2Ljg0Mzc1IDAgCkwgNTYuMDYyNSAwIApMIDQ3LjcwMzEyNSAyMS42ODc1IApMIDE3Ljc4MTI1IDIxLjY4NzUgCkwgOS45MDYyNSAwIAp6Ck0gMjAuNTE1NjI1IDI5LjM5MDYyNSAKTCA0NC43ODEyNSAyOS4zOTA2MjUgCkwgMzcuMzEyNSA0OS4yMTg3NSAKUSAzMy44OTA2MjUgNTguMjUgMzIuMjM0Mzc1IDY0LjA2MjUgClEgMzAuODU5Mzc1IDU3LjE3MTg3NSAyOC4zNzUgNTAuMzkwNjI1IAp6CiIgaWQ9IkFyaWFsTVQtNjUiPjwvcGF0aD4KICAgICAgIDxwYXRoIGQ9Ik0gMTQuNzAzMTI1IDAgCkwgNi41NDY4NzUgMCAKTCA2LjU0Njg3NSA3MS41NzgxMjUgCkwgMTUuMzI4MTI1IDcxLjU3ODEyNSAKTCAxNS4zMjgxMjUgNDYuMDQ2ODc1IApRIDIwLjkwNjI1IDUzLjAzMTI1IDI5LjU0Njg3NSA1My4wMzEyNSAKUSAzNC4zMjgxMjUgNTMuMDMxMjUgMzguNTkzNzUgNTEuMDkzNzUgClEgNDIuODc1IDQ5LjE3MTg3NSA0NS42MjUgNDUuNjcxODc1IApRIDQ4LjM5MDYyNSA0Mi4xODc1IDQ5Ljk1MzEyNSAzNy4yNSAKUSA1MS41MTU2MjUgMzIuMzI4MTI1IDUxLjUxNTYyNSAyNi43MDMxMjUgClEgNTEuNTE1NjI1IDEzLjM3NSA0NC45MjE4NzUgNi4wOTM3NSAKUSAzOC4zMjgxMjUgLTEuMTcxODc1IDI5LjEwOTM3NSAtMS4xNzE4NzUgClEgMTkuOTIxODc1IC0xLjE3MTg3NSAxNC43MDMxMjUgNi41IAp6Ck0gMTQuNTkzNzUgMjYuMzEyNSAKUSAxNC41OTM3NSAxNyAxNy4xNDA2MjUgMTIuODQzNzUgClEgMjEuMjk2ODc1IDYuMDYyNSAyOC4zNzUgNi4wNjI1IApRIDM0LjEyNSA2LjA2MjUgMzguMzI4MTI1IDExLjA2MjUgClEgNDIuNTMxMjUgMTYuMDYyNSA0Mi41MzEyNSAyNS45ODQzNzUgClEgNDIuNTMxMjUgMzYuMTQwNjI1IDM4LjUgNDAuOTY4NzUgClEgMzQuNDY4NzUgNDUuNzk2ODc1IDI4Ljc2NTYyNSA0NS43OTY4NzUgClEgMjMgNDUuNzk2ODc1IDE4Ljc5Njg3NSA0MC43OTY4NzUgClEgMTQuNTkzNzUgMzUuNzk2ODc1IDE0LjU5Mzc1IDI2LjMxMjUgCnoKIiBpZD0iQXJpYWxNVC05OCI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSAzLjMyODEyNSAyNS45MjE4NzUgClEgMy4zMjgxMjUgNDAuMzI4MTI1IDExLjMyODEyNSA0Ny4yNjU2MjUgClEgMTguMDE1NjI1IDUzLjAzMTI1IDI3LjY0MDYyNSA1My4wMzEyNSAKUSAzOC4zMjgxMjUgNTMuMDMxMjUgNDUuMTA5Mzc1IDQ2LjAxNTYyNSAKUSA1MS45MDYyNSAzOS4wMTU2MjUgNTEuOTA2MjUgMjYuNjU2MjUgClEgNTEuOTA2MjUgMTYuNjU2MjUgNDguOTA2MjUgMTAuOTA2MjUgClEgNDUuOTA2MjUgNS4xNzE4NzUgNDAuMTU2MjUgMiAKUSAzNC40MjE4NzUgLTEuMTcxODc1IDI3LjY0MDYyNSAtMS4xNzE4NzUgClEgMTYuNzUgLTEuMTcxODc1IDEwLjAzMTI1IDUuODEyNSAKUSAzLjMyODEyNSAxMi43OTY4NzUgMy4zMjgxMjUgMjUuOTIxODc1IAp6Ck0gMTIuMzU5Mzc1IDI1LjkyMTg3NSAKUSAxMi4zNTkzNzUgMTUuOTY4NzUgMTYuNzAzMTI1IDExLjAxNTYyNSAKUSAyMS4wNDY4NzUgNi4wNjI1IDI3LjY0MDYyNSA2LjA2MjUgClEgMzQuMTg3NSA2LjA2MjUgMzguNTMxMjUgMTEuMDMxMjUgClEgNDIuODc1IDE2LjAxNTYyNSA0Mi44NzUgMjYuMjE4NzUgClEgNDIuODc1IDM1Ljg0Mzc1IDM4LjUgNDAuNzk2ODc1IApRIDM0LjEyNSA0NS43NSAyNy42NDA2MjUgNDUuNzUgClEgMjEuMDQ2ODc1IDQ1Ljc1IDE2LjcwMzEyNSA0MC44MTI1IApRIDEyLjM1OTM3NSAzNS44OTA2MjUgMTIuMzU5Mzc1IDI1LjkyMTg3NSAKegoiIGlkPSJBcmlhbE1ULTExMSI+PC9wYXRoPgogICAgICAgPHBhdGggZD0iTSAxMi4zNTkzNzUgLTIxLjA0Njg3NSAKTCA2LjA2MjUgLTIxLjA0Njg3NSAKUSAyMC42NTYyNSAyLjM5MDYyNSAyMC42NTYyNSAyNS44NzUgClEgMjAuNjU2MjUgMzUuMDYyNSAxOC41NjI1IDQ0LjA5Mzc1IApRIDE2Ljg5MDYyNSA1MS40MjE4NzUgMTMuOTIxODc1IDU4LjE1NjI1IApRIDEyLjAxNTYyNSA2Mi41NDY4NzUgNi4wNjI1IDcyLjc5Njg3NSAKTCAxMi4zNTkzNzUgNzIuNzk2ODc1IApRIDIxLjUzMTI1IDYwLjU0Njg3NSAyNS45MjE4NzUgNDguMTg3NSAKUSAyOS42ODc1IDM3LjU0Njg3NSAyOS42ODc1IDI1LjkyMTg3NSAKUSAyOS42ODc1IDEyLjc1IDI0LjYyNSAwLjQzNzUgClEgMTkuNTc4MTI1IC0xMS44NTkzNzUgMTIuMzU5Mzc1IC0yMS4wNDY4NzUgCnoKIiBpZD0iQXJpYWxNVC00MSI+PC9wYXRoPgogICAgICA8L2RlZnM+CiAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtNjciPjwvdXNlPgogICAgICA8dXNlIHg9IjcyLjIxNjc5NyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE3Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxMjcuODMyMDMxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDkiPjwvdXNlPgogICAgICA8dXNlIHg9IjIxMS4xMzI4MTIiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNyI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjY2Ljc0ODA0NyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA4Ij48L3VzZT4KICAgICAgPHVzZSB4PSIyODguOTY0ODQ0IiB4bGluazpocmVmPSIjQXJpYWxNVC05NyI+PC91c2U+CiAgICAgIDx1c2UgeD0iMzQ0LjU4MDA3OCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE2Ij48L3VzZT4KICAgICAgPHVzZSB4PSIzNzIuMzYzMjgxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDUiPjwvdXNlPgogICAgICA8dXNlIHg9IjM5NC41ODAwNzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExOCI+PC91c2U+CiAgICAgIDx1c2UgeD0iNDQ0LjU4MDA3OCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAxIj48L3VzZT4KICAgICAgPHVzZSB4PSI1MDAuMTk1MzEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTI3Ljk3ODUxNiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtODIiPjwvdXNlPgogICAgICA8dXNlIHg9IjYwMC4xOTUzMTIiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgIDx1c2UgeD0iNjU1LjgxMDU0NyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE2Ij48L3VzZT4KICAgICAgPHVzZSB4PSI2ODMuNTkzNzUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNyI+PC91c2U+CiAgICAgIDx1c2UgeD0iNzM5LjIwODk4NCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICAgPHVzZSB4PSI3NzIuNTA5NzY2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTAiPjwvdXNlPgogICAgICA8dXNlIHg9IjgyOC4xMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNSI+PC91c2U+CiAgICAgIDx1c2UgeD0iODc4LjEyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgICA8dXNlIHg9IjkwNS45MDgyMDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQwIj48L3VzZT4KICAgICAgPHVzZSB4PSI5MzkuMjA4OTg0IiB4bGluazpocmVmPSIjQXJpYWxNVC02NSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTAwNS45MDgyMDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTk4Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxMDYxLjUyMzQzOCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE1Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxMTExLjUyMzQzOCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTExIj48L3VzZT4KICAgICAgPHVzZSB4PSIxMTY3LjEzODY3MiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA4Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxMTg5LjM1NTQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE3Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxMjQ0Ljk3MDcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE2Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxMjcyLjc1MzkwNiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAxIj48L3VzZT4KICAgICAgPHVzZSB4PSIxMzI4LjM2OTE0MSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDEiPjwvdXNlPgogICAgIDwvZz4KICAgIDwvZz4KICAgPC9nPgogICA8ZyBpZD0ibGluZTJkXzM1Ij4KICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwN2Q3NzEyMGUyMCkiIGQ9Ik0gNjAuMzg1ODI0IDMwMi4xMTIzNzcgCkwgNjEuMjUxNjM1IDMwNC45NjE1OTkgCkwgNjIuMjEwMjEyIDMwNi4wODE2OSAKTCA2My4xMzc4NjcgMzA3LjY2OTc3NCAKTCA2NC4wOTY0NDQgMjk2Ljk5NzM1IApMIDY1LjAyNDA5OSAyOTYuNjQ3NTQyIApMIDY1Ljk4MjY3NiAyOTkuNzE3NDQgCkwgNjYuOTQxMjUzIDI5OS4zNTMyNDcgCkwgNjcuODY4OTA4IDI5OS4zMzg3NjQgCkwgNjguODI3NDg1IDI5Ni4zODA4MDMgCkwgNjkuNzU1MTQgMjkxLjA4NDEzOSAKTCA3MC43MTM3MTcgMjkyLjA0NjQ3MyAKTCA3MS42NzIyOTQgMjg5Ljc1NTU3NyAKTCA3Mi41NjkwMjcgMjkzLjE5MzAxMSAKTCA3My41Mjc2MDQgMjkzLjEyNTczMiAKTCA3NC40NTUyNTkgMjkyLjc4MjIyMiAKTCA3NS40MTM4MzYgMjkyLjA5OTk5NSAKTCA3Ni4zNDE0OTEgMjkxLjY5NjM3NSAKTCA3Ny4zMDAwNjggMjg5Ljk5MDg4MSAKTCA3OS4xODYzIDI4Mi4zMjAzNSAKTCA4MC4xNDQ4NzcgMjg0LjYyNjg0MiAKTCA4MS4wNzI1MzIgMjgwLjk5NDExMyAKTCA4Mi4wMzExMDkgMjc4LjM1ODI1NCAKTCA4My44NTU0OTggMjgwLjI4MTgwOCAKTCA4NC44MTQwNzUgMjgyLjQ0NTg0OSAKTCA4NS43NDE3MyAyODEuMjM0OTM5IApMIDg2LjcwMDMwNyAyNzguODcyMjEyIApMIDg4LjU4NjUzOSAyNzcuMDgxMTggCkwgODkuNTQ1MTE2IDI3OC4xODgyOTEgCkwgOTAuNDcyNzcxIDI3Ny44MDMwNzYgCkwgOTEuNDMxMzQ4IDI3OS41MjI3MTMgCkwgOTIuMzU5MDAzIDI3Ny40NDI2MTIgCkwgOTQuMjc2MTU3IDI3OS45Mzc4MTMgCkwgOTUuMTQxOTY4IDI4Mi4zOTAyOTIgCkwgOTYuMTAwNTQ1IDI4MS42MDIzNzggCkwgOTcuMDI4MiAyODMuNTUyODE0IApMIDk3Ljk4Njc3NyAyODIuMTk3OTUxIApMIDk4LjkxNDQzMiAyODIuMDUyOTgxIApMIDk5Ljg3MzAwOSAyODEuMDQzOTA2IApMIDEwMC44MzE1ODYgMjgwLjM4NDkyOSAKTCAxMDEuNzU5MjQxIDI4MC44OTIwNTggCkwgMTAyLjcxNzgxOCAyODMuOTE5MzMyIApMIDEwMy42NDU0NzMgMjgyLjg0Mjk3OSAKTCAxMDQuNjA0MDUgMjg2LjU0OTQyOCAKTCAxMDUuNTYyNjI3IDI4MS40NzE0MDYgCkwgMTA2LjQyODQzOCAyODMuNTkyNzI1IApMIDEwNy4zODcwMTUgMjgxLjk1MTA3MSAKTCAxMDguMzE0NjcgMjgyLjMxODAyNSAKTCAxMDkuMjczMjQ3IDI3OS43Mjk4MjcgCkwgMTEwLjIwMDkwMiAyNzkuMTk2MzQ5IApMIDExMS4xNTk0NzkgMjc2LjcwMzI3OSAKTCAxMTIuMTE4MDU2IDI3Ny43MTk0MjYgCkwgMTEzLjA0NTcxMSAyODAuOTk5MjQ4IApMIDExNC4wMDQyODggMjgzLjY2ODk2NCAKTCAxMTQuOTMxOTQzIDI3OC4wMTgwMzcgCkwgMTE1Ljg5MDUyIDI4MC4zMzE0MDcgCkwgMTE2Ljg0OTA5NyAyODEuODkzODY4IApMIDExNy43NDU4MzEgMjg1LjEyMjk3NiAKTCAxMTguNzA0NDA3IDI4NS43Mjg0MzEgCkwgMTE5LjYzMjA2MyAyNzkuMzkwOTY2IApMIDEyMC41OTA2MzkgMjc1Ljc4ODI2OCAKTCAxMjEuNTE4Mjk1IDI3Mi45NTY1OCAKTCAxMjMuNDM1NDQ4IDI3OC4xNTY1NjUgCkwgMTI0LjM2MzEwNCAyNzguMzE4MDAzIApMIDEyNS4zMjE2OCAyODAuNDA1NzU3IApMIDEyNi4yNDkzMzYgMjc4LjY2MDMwMyAKTCAxMjcuMjA3OTEyIDI3OS4yNDk5NjggCkwgMTI4LjE2NjQ4OSAyNzguODA5NjMzIApMIDEyOS45OTA4NzggMjc3LjExMzkyMyAKTCAxMzAuOTE4NTMzIDI3NS44MDQ4MzMgCkwgMTMxLjg3NzExIDI3My4yNTU1MjkgCkwgMTMyLjgwNDc2NSAyNzIuODg0MTY3IApMIDEzMy43NjMzNDIgMjY5Ljk4NjI2NyAKTCAxMzQuNzIxOTE5IDI2OS45ODYyNjcgCkwgMTM1LjY0OTU3NCAyNzIuMzYxMiAKTCAxMzYuNjA4MTUxIDI3MC4yMzY3OCAKTCAxMzcuNTM1ODA2IDI2My43MjQzMTQgCkwgMTM4LjQ5NDM4MyAyNjQuMzI3MDU3IApMIDEzOS40NTI5NiAyNjAuOTQ3Nzk1IApMIDE0MC4zMTg3NzEgMjU4Ljg0MTg3OCAKTCAxNDEuMjc3MzQ4IDI1Ny4wNTI0NDUgCkwgMTQyLjIwNTAwMyAyNTQuMDQ2MDQ3IApMIDE0My4xNjM1OCAyNTUuMzA0MTMzIApMIDE0NC4wOTEyMzUgMjUzLjkwOTE2NSAKTCAxNDUuMDQ5ODEyIDI1NC4yMzIwOTEgCkwgMTQ2LjAwODM4OSAyNDYuMTA1MTkyIApMIDE0Ni45MzYwNDQgMjQ1LjMyNTc1NCAKTCAxNDcuODk0NjIxIDI0NC4xOTkzMTcgCkwgMTQ4LjgyMjI3NiAyNDEuOTk3NjQxIApMIDE0OS43ODA4NTMgMjM5LjE1NDYxOSAKTCAxNTAuNzM5NDMgMjM5LjQwOTU0IApMIDE1MS42MDUyNDEgMjM3LjYxNTYwMiAKTCAxNTIuNTYzODE4IDIzOS4zOTQ5MTIgCkwgMTUzLjQ5MTQ3MyAyMzcuMDI1NzQzIApMIDE1NC40NTAwNSAyMzUuNTE5OTUzIApMIDE1NS4zNzc3MDUgMjM4Ljk3NjIyOCAKTCAxNTYuMzM2MjgyIDIzNi4wMTYyMzIgCkwgMTU3LjI5NDg1OSAyMzQuNzQ4MjY1IApMIDE1OC4yMjI1MTQgMjMxLjIzOTA5NyAKTCAxNjAuMTA4NzQ2IDIyNi42MjM0OTcgCkwgMTYxLjA2NzMyMyAyMjcuODcyMDkgCkwgMTYyLjAyNTkgMjI4LjMyNDc3NyAKTCAxNjIuOTIyNjM0IDIyNy40MTA4NzkgCkwgMTYzLjg4MTIxMSAyMjkuMTU5OTY1IApMIDE2NC44MDg4NjYgMjI4LjY4Mjc3IApMIDE2NS43Njc0NDMgMjI3Ljk3Mzk1MiAKTCAxNjYuNjk1MDk4IDIyOS4wOTE3MTggCkwgMTY4LjYxMjI1MiAyMjIuOTI3MzE3IApMIDE2OS41Mzk5MDcgMjIyLjY2Nzg0MyAKTCAxNzAuNDk4NDg0IDIyMC4yNDYwMjQgCkwgMTcxLjQyNjEzOSAyMTkuNDA3Mjk5IApMIDE3Mi4zODQ3MTYgMjE5LjMyNDg2IApMIDE3My4zNDMyOTIgMjE4LjY5MzEwNSAKTCAxNzQuMjA5MTA0IDIxNy4yMzc5MyAKTCAxNzUuMTY3NjgxIDIxNC41MzM1ODIgCkwgMTc2LjA5NTMzNiAyMTMuNTU3MDU2IApMIDE3Ny4wNTM5MTMgMjExLjI1OTY3IApMIDE3Ny45ODE1NjggMjEwLjQ1NTQzMiAKTCAxNzguOTQwMTQ1IDIxNC44NTg3MzUgCkwgMTc5Ljg5ODcyMiAyMTMuNjQ3ODI2IApMIDE4MC44MjYzNzcgMjE1LjUzODAwNyAKTCAxODEuNzg0OTU0IDIxMS4zNDQzODUgCkwgMTgyLjcxMjYwOSAyMDguODM1NzE5IApMIDE4My42NzExODYgMjA3LjY2MTUyNCAKTCAxODQuNjI5NzYzIDIwNC45MTk4MzEgCkwgMTg1LjQ5NTU3NCAyMDAuNTk1MTQgCkwgMTg2LjQ1NDE1MSAxOTguNTk0MTg1IApMIDE4Ny4zODE4MDYgMTk4Ljc0OTQyMyAKTCAxODguMzQwMzgzIDE5Ni40MTMyNCAKTCAxODkuMjY4MDM4IDE5MS40MjEwNDcgCkwgMTkxLjE4NTE5MiAxODQuMjk0NjAyIApMIDE5Mi4xMTI4NDcgMTg4LjcwNjA5MSAKTCAxOTMuMDcxNDI0IDE4Ni45ODA5OCAKTCAxOTMuOTk5MDc5IDE4Ni43MjQ3MDMgCkwgMTk0Ljk1NzY1NiAxODkuMjk0Mzk5IApMIDE5NS45MTYyMzMgMTg1LjE4OTYwOSAKTCAxOTYuNzgyMDQ1IDE4Ny4yMDc4MDggCkwgMTk4LjY2ODI3NyAxOTIuMTMwMzAxIApMIDE5OS42MjY4NTMgMTkzLjQ2NzQ4NCAKTCAyMDAuNTU0NTA5IDE5MS45NjM5NyAKTCAyMDEuNTEzMDg2IDE5Ni43OTI0OTcgCkwgMjAyLjQ3MTY2MiAxOTMuMTA1Mjc3IApMIDIwMy4zOTkzMTggMTk0LjM3NjE1MSAKTCAyMDQuMzU3ODk0IDE5NC4yMTMwNjUgCkwgMjA1LjI4NTU1IDE5NS42NzU4OTMgCkwgMjA2LjI0NDEyNiAxOTMuMzI5NDg5IApMIDIwNy4yMDI3MDMgMTg4LjkyNjE4NiAKTCAyMDguMDk5NDM3IDE5MC43MjAxMjQgCkwgMjA5LjA1ODAxNCAxOTEuMzQxMTI3IApMIDIwOS45ODU2NjkgMTkzLjEwNTM3NCAKTCAyMTAuOTQ0MjQ2IDE4OS40NDM1MzUgCkwgMjExLjg3MTkwMSAxOTAuNTI2NzY2IApMIDIxMi44MzA0NzggMTkwLjM2NTMyNyAKTCAyMTMuNzg5MDU1IDE5MC4zNjUzMjcgCkwgMjE0LjcxNjcxIDE4OC40MzQzMTQgCkwgMjE1LjY3NTI4NyAxODguNDM0MzE0IApMIDIxNi42MDI5NDIgMTg4LjkwNzYzNCAKTCAyMTcuNTYxNTE5IDE4OC43MjI4MDEgCkwgMjE4LjUyMDA5NiAxODguODg0NzcyIApMIDIxOS4zODU5MDcgMTg4LjcyMjIyIApMIDIyMC4zNDQ0ODQgMTg5LjY2ODI3OSAKTCAyMjEuMjcyMTM5IDE4OC45OTMyMjIgCkwgMjIyLjIzMDcxNiAxODcuMTYyMjc4IApMIDIyMy4xNTgzNzEgMTg2LjAxMzkgCkwgMjI0LjExNjk0OCAxODIuMTc3MzUgCkwgMjI1LjA3NTUyNSAxODMuNjU4NTgzIApMIDIyNi4wMDMxOCAxODIuNzE3MzY4IApMIDIyNi45NjE3NTcgMTgzLjAyMjk1MyAKTCAyMjcuODg5NDEyIDE4MC41NjI2NzUgCkwgMjI4Ljg0Nzk4OSAxNzkuMDUyNTI2IApMIDIyOS44MDY1NjYgMTgxLjA3NjczIApMIDIzMS42MzA5NTQgMTgxLjMzMDUzNyAKTCAyMzIuNTU4NjA5IDE4My45NjEyNjIgCkwgMjMzLjUxNzE4NiAxODEuNTA2NyAKTCAyMzQuNDQ0ODQxIDE4MC45ODk2NDIgCkwgMjM1LjQwMzQxOCAxODEuOTMzMjMxIApMIDIzNi4zNjE5OTUgMTg0LjE3ODY0NSAKTCAyMzcuMjg5NjUgMTg0Ljk2NTczNiAKTCAyMzguMjQ4MjI3IDE4Mi4xNjc5NTQgCkwgMjM5LjE3NTg4MiAxODEuMTc2MDczIApMIDI0MS4wOTMwMzYgMTgwLjQ3MTg1NyAKTCAyNDEuOTU4ODQ4IDE3OC4wMjU1NzcgCkwgMjQyLjkxNzQyNSAxNzYuNzMzOTI0IApMIDI0My44NDUwOCAxNzYuODg4MTk0IApMIDI0NC44MDM2NTcgMTc2LjI2OTE3NyAKTCAyNDUuNzMxMzEyIDE3Ni41MjU4OSAKTCAyNDYuNjg5ODg5IDE3NC42NDQ4NjMgCkwgMjQ3LjY0ODQ2NiAxNzMuNDM3NzMxIApMIDI0OC41NzYxMjEgMTY5LjU2MjgyMSAKTCAyNDkuNTM0Njk4IDE2OS44NDA0MSAKTCAyNTAuNDYyMzUzIDE2OC4zMDQ5NzYgCkwgMjUxLjQyMDkzIDE2Ny43MDk2NDUgCkwgMjUyLjM3OTUwNiAxNjkuNDc4Mzk2IApMIDI1My4yNzYyNCAxNjguOTEzNTMxIApMIDI1NC4yMzQ4MTcgMTY5LjgzNDc5MSAKTCAyNTUuMTYyNDcyIDE2OC45NjQ2OCAKTCAyNTYuMTIxMDQ5IDE2Ni4yNTc5NTggCkwgMjU3LjA0ODcwNCAxNjYuMzM4ODk1IApMIDI1OC4wMDcyODEgMTYzLjMxMTYyMSAKTCAyNTguOTY1ODU4IDE2MS43NTc0OTEgCkwgMjYwLjg1MjA5IDE2Mi43MjQ0NzUgCkwgMjYxLjc3OTc0NSAxNjEuODEzMDQ4IApMIDI2Mi43MzgzMjIgMTYwLjQ3MzY4NSAKTCAyNjMuNjk2ODk5IDE1OS41ODg0MTMgCkwgMjY0LjU2MjcxIDE1Ni45ODAzMDcgCkwgMjY1LjUyMTI4NyAxNTYuNDUyMzUxIApMIDI2Ni40NDg5NDIgMTU1LjYyMzM2MiAKTCAyNjcuNDA3NTE5IDE1NS4yNzQwMzkgCkwgMjY4LjMzNTE3NCAxNTMuODMxMzYxIApMIDI2OS4yOTM3NTEgMTUyLjU3NzczMSAKTCAyNzAuMjUyMzI4IDE1Mi4xMzMzNzUgCkwgMjcxLjE3OTk4MyAxNTAuNzUwNzU5IApMIDI3Mi4xMzg1NiAxNTEuMjkzNzc5IApMIDI3My4wNjYyMTUgMTUzLjgxOTkzIApMIDI3NC4wMjQ3OTIgMTUyLjM2NDUxNCAKTCAyNzQuOTgzMzY5IDE1NS4xMDYyMDcgCkwgMjc2LjgwNzc1NyAxNTguNzM4OTM2IApMIDI3Ny43MzU0MTIgMTU2Ljg3NTk3NSAKTCAyNzguNjkzOTg5IDE2MS43NDUyMzcgCkwgMjc5LjYyMTY0NCAxNjEuMzgwNTU5IApMIDI4MC41ODAyMjEgMTU5LjkzODk5NSAKTCAyODEuNTM4Nzk4IDE1Ny45NzkxNjIgCkwgMjgyLjQ2NjQ1MyAxNjIuMjA5MjU3IApMIDI4My40MjUwMyAxNjAuNzA1MDE3IApMIDI4NC4zNTI2ODUgMTU4LjM3MDcyMiAKTCAyODUuMzExMjYyIDE1Ny40NTc2NDggCkwgMjg2LjI2OTgzOSAxNTIuNDQ3MDAxIApMIDI4OC4wOTQyMjggMTU0LjQxNDQ4NyAKTCAyODkuMDIxODgzIDE1Mi41NDEyNTggCkwgMjg5Ljk4MDQ2IDE0OS43MDcxOTcgCkwgMjkwLjkwODExNSAxNTEuNTg2MjM4IApMIDI5MS44NjY2OTIgMTUwLjU1NTY1NyAKTCAyOTIuODI1MjY5IDE0OS43OTg4MzggCkwgMjkzLjc1MjkyNCAxNDYuNzQ4NjA1IApMIDI5NC43MTE1MDEgMTQ1LjA4NjU1OSAKTCAyOTUuNjM5MTU2IDE0Mi41NjE0MjUgCkwgMjk2LjU5NzczMyAxNDAuMzAxMDQ1IApMIDI5Ny41NTYzMSAxMzcuNTUxMzYgCkwgMjk4LjQ1MzA0MyAxMzkuMzUyNzA5IApMIDI5OS40MTE2MiAxMzYuNTc1NDE1IApMIDMwMC4zMzkyNzUgMTM4LjM2OTM1MyAKTCAzMDEuMjk3ODUyIDEzOC4xNjIzMzYgCkwgMzAyLjIyNTUwNyAxMzQuOTk2NDM3IApMIDMwMy4xODQwODQgMTM3LjU0NTc0MSAKTCAzMDQuMTQyNjYxIDEzNi45MjQ3MzggCkwgMzA1LjA3MDMxNiAxMzcuMjU5OTE4IApMIDMwNi4wMjg4OTMgMTM1Ljc5ODQ5NSAKTCAzMDYuOTU2NTQ4IDEzNC45ODc4NjQgCkwgMzA3LjkxNTEyNSAxMzQuMzAyMTk4IApMIDMwOC44NzM3MDIgMTMzLjkwMzU2NyAKTCAzMDkuNzM5NTEzIDEzMy45MDM1NjcgCkwgMzEwLjY5ODA5IDEzNC44MDUwNjUgCkwgMzExLjYyNTc0NSAxNDAuMzIzMTMyIApMIDMxMi41ODQzMjIgMTQwLjU1Mzc4NiAKTCAzMTMuNTExOTc3IDEzOC43MTM2ODcgCkwgMzE0LjQ3MDU1NCAxMzMuOTQ5NDM2IApMIDMxNS40MjkxMzEgMTM0LjM2MjU1IApMIDMxNi4zNTY3ODYgMTMxLjY2Njc3NSAKTCAzMTcuMzE1MzYzIDEzNC44NjkxOTUgCkwgMzE4LjI0MzAxOCAxMzEuMzMyOTAzIApMIDMxOS4yMDE1OTUgMTI3LjE1MDM3MyAKTCAzMjAuMTYwMTcyIDEyOS45NDQ3NjQgCkwgMzIxLjAyNTk4MyAxMzAuMDQzNjIzIApMIDMyMS45ODQ1NiAxMjQuNjA3NjU2IApMIDMyMy44NzA3OTIgMTMyLjg5OTc3MSAKTCAzMjQuNzk4NDQ4IDEyOC41OTc2NTIgCkwgMzI1Ljc1NzAyNCAxMzMuMjIwMjI2IApMIDMyNi43MTU2MDEgMTM0LjMzMTE2MyAKTCAzMjcuNjQzMjU2IDEyNC41NjY1ODIgCkwgMzI4LjYwMTgzMyAxMjUuODEzNDggCkwgMzI5LjUyOTQ4OCAxMjAuOTg5NTU1IApMIDMzMC40ODgwNjUgMTE5LjM4ODczMyAKTCAzMzEuNDQ2NjQyIDEyMy40MjUwODIgCkwgMzMyLjMxMjQ1NCAxMjYuMzkyNTM3IApMIDMzMy4yNzEwMzEgMTI1Ljk5NjkwOCAKTCAzMzQuMTk4Njg2IDExOC41MDU2ODkgCkwgMzM1LjE1NzI2MyAxMTcuMzUwMzM2IApMIDMzNi4wODQ5MTggMTIwLjY1OTI2NyAKTCAzMzcuMDQzNDk1IDExOC4xMDk5NjQgCkwgMzM4LjAwMjA3MiAxMTguMTA5OTY0IApMIDMzOC45Mjk3MjcgMTIwLjE4Mzc2NyAKTCAzMzkuODg4MzA0IDEyMC4yNzg3NTEgCkwgMzQwLjgxNTk1OSAxMjQuNTYwOTYzIApMIDM0MS43NzQ1MzYgMTI3LjI4NzU5MyAKTCAzNDIuNzMzMTEzIDEyNi4zODg1NjUgCkwgMzQzLjYyOTg0NiAxMjguOTI2MjQ0IApMIDM0NC41ODg0MjMgMTI0Ljk4MTQ4OCAKTCAzNDUuNTE2MDc4IDEyMC4yODAwMSAKTCAzNDYuNDc0NjU1IDExOS4xODM3MDEgCkwgMzQ3LjQwMjMxIDEyNC4yNjMxNzcgCkwgMzQ5LjMxOTQ2NCAxMTAuMjM4NjY0IApMIDM1MS4yMDU2OTYgMTAzLjA0Nzg0NiAKTCAzNTIuMTMzMzUxIDEwMi4wODY1MjkgCkwgMzUzLjA5MTkyOCA5NC4xMTkxOCAKTCAzNTQuMDUwNTA1IDk2LjY4OTg5MyAKTCAzNTQuOTE2MzE2IDk0Ljc1Nzk1OSAKTCAzNTUuODc0ODkzIDk1LjUzMzc2NSAKTCAzNTYuODAyNTQ4IDkwLjQwMzIzOCAKTCAzNTcuNzYxMTI1IDg4LjQ3MTgzNyAKTCAzNTguNjg4NzggOTIuNTg3MDg5IApMIDM1OS42NDczNTcgOTcuNzM2ODk0IApMIDM2MC42MDU5MzQgOTYuNjU4NTA2IApMIDM2MS41MzM1ODkgMTA0LjI5NTM3NCAKTCAzNjIuNDkyMTY2IDEwNC40OTMzMzMgCkwgMzYzLjQxOTgyMSAxMDYuNzQ2MjA3IApMIDM2NC4zNzgzOTggMTA0LjI0NDQ2NyAKTCAzNjUuMzM2OTc1IDEwOC42NzA4NzUgCkwgMzY2LjIwMjc4NyAxMDYuMjI3Njk1IApMIDM2Ny4xNjEzNjMgOTYuMTI1NzA2IApMIDM2OC4wODkwMTkgOTUuNDU4MDEgCkwgMzY5LjA0NzU5NSAxMDIuMzc5MTM0IApMIDM2OS45NzUyNTEgMTE1LjUyMjg3OSAKTCAzNzAuOTMzODI4IDEyNC4zNjM2ODIgCkwgMzcxLjg5MjQwNCAxMjUuMjg0MDcgCkwgMzcyLjgyMDA2IDE0MS45ODQ2NDUgCkwgMzczLjc3ODYzNiAxNjkuMzQ1NjMyIApMIDM3NC43MDYyOTIgMTU5LjIzMzQ3MSAKTCAzNzUuNjY0ODY5IDE1NC41MjM0MiAKTCAzNzYuNjIzNDQ1IDE0OS4xNDE2MDUgCkwgMzc3LjQ4OTI1NyAxNjMuMDM4MjQ2IApMIDM3OC40NDc4MzQgMTYxLjI1OTI3NCAKTCAzNzkuMzc1NDg5IDE0NC45NTc4MTUgCkwgMzgwLjMzNDA2NiAxNDIuNjgxODg3IApMIDM4MS4yNjE3MjEgMTQ0LjAxOTYwMyAKTCAzODIuMjIwMjk4IDE0NS4wNTEzOTUgCkwgMzgzLjE3ODg3NSAxMzkuMTk0NTE1IApMIDM4NC4xMDY1MyAxMzkuODczNzg3IApMIDM4NS4wNjUxMDcgMTMyLjI0MjY4MyAKTCAzODUuOTkyNzYyIDEzMS40NjQ0MDggCkwgMzg2Ljk1MTMzOSAxMjIuNDA3OTE4IApMIDM4Ny45MDk5MTYgMTIyLjkzOTM2MiAKTCAzODguODA2NjQ5IDEyMC43NTE2ODQgCkwgMzg5Ljc2NTIyNiAxMTguODQyMTI4IApMIDM5MC42OTI4ODEgMTE4LjU5NDgxMiAKTCAzOTEuNjUxNDU4IDExNi45NDI3OTIgCkwgMzkyLjU3OTExMyAxMTIuOTk5ODc3IApMIDM5My41Mzc2OSAxMTQuNzkxNDkgCkwgMzk0LjQ5NjI2NyAxMTUuMjgxMDg1IApMIDM5NS40MjM5MjIgMTExLjA5MzYxNCAKTCAzOTYuMzgyNDk5IDEwMy45NjE2OTYgCkwgMzk3LjMxMDE1NCAxMDEuNzY2MDc0IApMIDM5OC4yNjg3MzEgMTAwLjMyMzU5IApMIDM5OS4yMjczMDggMTAxLjIzMjgzOCAKTCA0MDAuMDkzMTE5IDEwMi4yNTk2OSAKTCA0MDEuMDUxNjk2IDk3LjgzMzEzNyAKTCA0MDEuOTc5MzUxIDg4Ljk3MTExOSAKTCA0MDIuOTM3OTI4IDg5LjQ4NjM4NSAKTCA0MDMuODY1NTgzIDg3LjQwMzA4OCAKTCA0MDQuODI0MTYgODEuMTAzNjQ2IApMIDQwNS43ODI3MzcgNzguMjgyNDIgCkwgNDA2LjcxMDM5MiA3Ny4zODMwNTMgCkwgNDA3LjY2ODk2OSA4MS4yNjE3NDIgCkwgNDA4LjU5NjYyNCA4MS45OTg3NSAKTCA0MDkuNTU1MjAxIDc1LjM1MDI3NSAKTCA0MTAuNTEzNzc4IDcwLjU0NDkwMSAKTCA0MTEuMzc5NTkgNjkuMTk0NDQ2IApMIDQxMi4zMzgxNjcgNzEuNzgxNTMxIApMIDQxMy4yNjU4MjIgNjkuMjM0NTAzIApMIDQxNC4yMjQzOTkgNjguMDkyNTY3IApMIDQxNS4xNTIwNTQgNjcuMjk1NjkyIApMIDQxNi4xMTA2MzEgNjIuMDk1MzY4IApMIDQxNy4wNjkyMDggNjEuMjgxMjAxIApMIDQxNy45OTY4NjMgNjMuMTAzMDg3IApMIDQxOC45NTU0NCA1OS42NTQ1NjIgCkwgNDIwLjg0MTY3MiA1Ni40NjUwMjYgCkwgNDIyLjY2NjA2IDU1LjE0NDY5OCAKTCA0MjMuNjI0NjM3IDUzLjEyMTgwMSAKTCA0MjQuNTUyMjkyIDQ4Ljg2MzY2MiAKTCA0MjUuNTEwODY5IDQ4LjkyNzA2NSAKTCA0MjYuNDM4NTI0IDUwLjQyMzk5MSAKTCA0MjcuMzk3MTAxIDQ5Ljk2NTI5OSAKTCA0MjguMzU1Njc4IDUwLjU0MDI4NyAKTCA0MjkuMjgzMzMzIDQ5LjkzMDI3OSAKTCA0MzAuMjQxOTEgNDIuMTQ0ODU3IApMIDQzMS4xNjk1NjUgNDEuOTUzMjQzIApMIDQzMi4xMjgxNDIgMzkuNjcyOTU1IApMIDQzMy4wODY3MTkgNDYuNDA0MjU2IApMIDQzMy45ODM0NTIgNTAuMDMwMTU1IApMIDQzNC45NDIwMjkgNTAuMDQ5Mjg3IApMIDQzNS44Njk2ODQgNDYuODg0MTE1IApMIDQzNi44MjgyNjEgNDYuMDI4ODI1IApMIDQzNy43NTU5MTYgNTAuMDAxMDQ1IApMIDQzOC43MTQ0OTMgNTEuNjUzOTM2IApMIDQzOS42NzMwNyA1NC43MjYyNTYgCkwgNDQxLjU1OTMwMiA3Mi40MzI5NTIgCkwgNDQyLjQ4Njk1NyA2NC4yMzk3NDMgCkwgNDQzLjQ0NTUzNCA2NS45NDM1OSAKTCA0NDQuNDA0MTExIDY2LjgzMDUwOSAKTCA0NDUuMjY5OTIyIDgwLjgxOTM3MiAKTCA0NDYuMjI4NDk5IDgxLjQ3NTAwNyAKTCA0NDcuMTU2MTU0IDc1LjcyNjE5IApMIDQ0OC4xMTQ3MzEgNzcuNDQ1MzkxIApMIDQ0OS4wNDIzODYgNzUuODk1NDI2IApMIDQ1MC4wMDA5NjMgNzYuNzI2MzA0IApMIDQ1MC45NTk1NCA3NC40MjA3MzIgCkwgNDUxLjg4NzE5NSA3My45NDM4NzYgCkwgNDUyLjg0NTc3MiA4MC43MDE1NzUgCkwgNDUzLjc3MzQyNyA4Mi40ODQ1MTggCkwgNDU0LjczMjAwNCA3OC44NDg0OTYgCkwgNDU1LjY5MDU4MSA4NC4wNjc1NjUgCkwgNDU2LjU1NjM5MyA4MC4xMzcxNDYgCkwgNDU3LjUxNDk3IDc5LjA2NzkxMyAKTCA0NTkuNDAxMjAyIDg0LjU3MjY1OSAKTCA0NjAuMzI4ODU3IDgzLjY5NjczNiAKTCA0NjEuMjg3NDM0IDc4LjczMTMyOCAKTCA0NjIuMjQ2MDExIDc5LjI2MjQzMyAKTCA0NjMuMTczNjY2IDc0LjcwODc4NCAKTCA0NjQuMTMyMjQzIDc3LjMxNjMwOCAKTCA0NjYuOTc3MDUyIDc0LjIzOTA5NiAKTCA0NjYuOTc3MDUyIDc0LjIzOTA5NiAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojNGM3MmIwO3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJsaW5lMmRfMzYiPgogICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A3ZDc3MTIwZTIwKSIgZD0iTSAyNDQuODAzNjU3IDMxNi45ODMxNyAKTCAyNDUuNzMxMzEyIDMyMy4xOTI5NTcgCkwgMjQ2LjY4OTg4OSAzMjYuMDQyMTc5IApMIDI0Ny42NDg0NjYgMzEzLjkzMzA4MyAKTCAyNDguNTc2MTIxIDI5NS43Njk0MzkgCkwgMjQ5LjUzNDY5OCAyODMuNDQwMTk5IApMIDI1MC40NjIzNTMgMjg4LjM1NDAyMiAKTCAyNTEuNDIwOTMgMjcyLjcyOTM2NSAKTCAyNTIuMzc5NTA2IDI2NS4wNTA0MDYgCkwgMjUzLjI3NjI0IDI2NC4wMzA2NzQgCkwgMjU0LjIzNDgxNyAyNzQuMDE3NTc5IApMIDI1NS4xNjI0NzIgMjc3LjE2Mjc5NSAKTCAyNTcuMDQ4NzA0IDI5MC45MjExNSAKTCAyNTguOTY1ODU4IDI4MS4zNDEwMTUgCkwgMjU5Ljg5MzUxMyAyNzkuODI3Mzc4IApMIDI2MC44NTIwOSAyNzkuODI3Mzc4IApMIDI2MS43Nzk3NDUgMjgwLjU2MTI4NiAKTCAyNjIuNzM4MzIyIDI3OS44MTYwOTIgCkwgMjYzLjY5Njg5OSAyODIuMDE3NzY4IApMIDI2NC41NjI3MSAyOTIuNzgxMzk4IApMIDI2NS41MjEyODcgMjkwLjgwNDQxOSAKTCAyNjYuNDQ4OTQyIDI4Ny4wMDU1MDUgCkwgMjY3LjQwNzUxOSAyNzkuOTYwMTkgCkwgMjY4LjMzNTE3NCAyODUuMzQyMDA2IApMIDI2OS4yOTM3NTEgMjg3LjkzNjc5MSAKTCAyNzIuMTM4NTYgMjkwLjczMTkwOSAKTCAyNzMuMDY2MjE1IDI4Ni44NTY5OTkgCkwgMjc0LjAyNDc5MiAyOTAuNDQ0ODc1IApMIDI3NS44NDkxOCAyOTAuNDQ0ODc1IApMIDI3Ni44MDc3NTcgMjkyLjM4MjMzMSAKTCAyNzcuNzM1NDEyIDI5NS40MDk2MDUgCkwgMjc4LjY5Mzk4OSAzMDYuMTczMjM1IApMIDI3OS42MjE2NDQgMzA0Ljc4OTM1OSAKTCAyODAuNTgwMjIxIDMxMS41MTY2NCAKTCAyODEuNTM4Nzk4IDMwOS45NTQxNzkgCkwgMjgyLjQ2NjQ1MyAzMTIuMjI0NjM1IApMIDI4My40MjUwMyAzMTEuNDMwNjE3IApMIDI4NC4zNTI2ODUgMzIyLjM2Nzg0MyAKTCAyODUuMzExMjYyIDMyMi4zNjc4NDMgCkwgMjg2LjI2OTgzOSAzMjYuNDA0MTkzIApMIDI4Ny4xMzU2NTEgMzI3LjUwNTAwNiAKTCAyODguMDk0MjI4IDMyNi4zNzg1NyAKTCAyODkuMDIxODgzIDMyOC41ODAyNDYgCkwgMjg5Ljk4MDQ2IDMxNy4wNDc3ODUgCkwgMjkwLjkwODExNSAzMTguOTEwNzQ1IApMIDI5MS44NjY2OTIgMzE4LjkxMDc0NSAKTCAyOTIuODI1MjY5IDMyMy43NTQzODMgCkwgMjkzLjc1MjkyNCAzMTEuOTE0NCAKTCAyOTQuNzExNTAxIDMxNS4zNzQxNjIgCkwgMjk1LjYzOTE1NiAzMjIuODI1OTA2IApMIDI5Ni41OTc3MzMgMzIyLjgyNTkwNiAKTCAyOTguNDUzMDQzIDMxNC4zODYyNTQgCkwgMjk5LjQxMTYyIDI5My44OTM5MzQgCkwgMzAwLjMzOTI3NSAyOTcuODIxMjA0IApMIDMwMS4yOTc4NTIgMjg5Ljk4NTg5MiAKTCAzMDIuMjI1NTA3IDI3OC4zMzY2NTEgCkwgMzA0LjE0MjY2MSAyODEuMzQ4OTU4IApMIDMwNS4wNzAzMTYgMjcyLjM5ODczOCAKTCAzMDYuOTU2NTQ4IDI3OC4zNTg1NDQgCkwgMzA3LjkxNTEyNSAyNzQuMzIyMTk1IApMIDMwOC44NzM3MDIgMjc3LjExNjU4NyAKTCAzMDkuNzM5NTEzIDI3OS4wOTM1NjcgCkwgMzEwLjY5ODA5IDI3NC45NzEzNCAKTCAzMTEuNjI1NzQ1IDI3Mi4xMjIxMTggCkwgMzEyLjU4NDMyMiAyNTYuNDI1MTQ1IApMIDMxMy41MTE5NzcgMjU4LjExODcyMyAKTCAzMTQuNDcwNTU0IDIzNi4zNTc0NjcgCkwgMzE1LjQyOTEzMSAyMzcuODEwNTU4IApMIDMxNi4zNTY3ODYgMjI2LjU3NTMwMyAKTCAzMTcuMzE1MzYzIDIzMi44NTc4NDEgCkwgMzE4LjI0MzAxOCAyMzUuMTg2NTE3IApMIDMxOS4yMDE1OTUgMjMzLjIyOTQ5MyAKTCAzMjAuMTYwMTcyIDIyOS40Njc0MzkgCkwgMzIxLjAyNTk4MyAyMzAuNzc2NTI5IApMIDMyMS45ODQ1NiAyMTguODkxNjk0IApMIDMyMi45MTIyMTUgMjEzLjQ4OTg3NSAKTCAzMjMuODcwNzkyIDIxMS43MDc5NDggCkwgMzI0Ljc5ODQ0OCAyMDkuMjA4MDAxIApMIDMyNS43NTcwMjQgMjE3LjIzMTE5OCAKTCAzMjYuNzE1NjAxIDIyMy4xMDc2OTQgCkwgMzI3LjY0MzI1NiAyMTEuMTUwNTkxIApMIDMyOC42MDE4MzMgMjA4LjIyNDg4OCAKTCAzMjkuNTI5NDg4IDE5Ny44MDE4NjIgCkwgMzMwLjQ4ODA2NSAyMDAuODI5MTM2IApMIDMzMS40NDY2NDIgMTk1LjQ0NzMyMSAKTCAzMzIuMzEyNDU0IDIxNC40NTg2MDIgCkwgMzMzLjI3MTAzMSAyMTkuODQwNDE3IApMIDMzNC4xOTg2ODYgMjE1LjgwNDA2OCAKTCAzMzUuMTU3MjYzIDIxMC4wMDgyNjcgCkwgMzM2LjA4NDkxOCAyMTYuNDc4Nzg3IApMIDMzNy4wNDM0OTUgMjI0LjgwMDQ0OCAKTCAzMzguMDAyMDcyIDIxNi41NTU5NDYgCkwgMzM4LjkyOTcyNyAyMTMuOTEzOTgzIApMIDMzOS44ODgzMDQgMjIxLjIyMTE5MyAKTCAzNDAuODE1OTU5IDIyOS4zMzQ5MTcgCkwgMzQxLjc3NDUzNiAyMzAuNTE2MjgxIApMIDM0Mi43MzMxMTMgMjU3LjE1NjI5MiAKTCAzNDMuNjI5ODQ2IDI1NC40NjUzNiAKTCAzNDQuNTg4NDIzIDI0OS4zNjY4MDEgCkwgMzQ1LjUxNjA3OCAyNTEuNjczMjkzIApMIDM0Ni40NzQ2NTUgMjUzLjQ4OTY1OCAKTCAzNDcuNDAyMzEgMjUyLjIzMTU3MSAKTCAzNDguMzYwODg3IDI2MC44MTUyMjUgCkwgMzQ5LjMxOTQ2NCAyNjcuNTIxODI0IApMIDM1MC4yNDcxMTkgMjY0LjA2MjA2MSAKTCAzNTEuMjA1Njk2IDI3MC41MjAyMyAKTCAzNTMuMDkxOTI4IDMwNS44MDY0NzUgCkwgMzU0LjA1MDUwNSAzMDUuODk4NzQ2IApMIDM1NC45MTYzMTYgMzE2LjYyMTMwMiAKTCAzNTUuODc0ODkzIDI5NC4zMDI1OTEgCkwgMzU2LjgwMjU0OCAzMDYuMzMwNDExIApMIDM1Ny43NjExMjUgMjgzLjg0MjA3NiAKTCAzNTguNjg4NzggMjU2Ljk2NTc5MiAKTCAzNTkuNjQ3MzU3IDI0Mi43MTk3NzkgCkwgMzYwLjYwNTkzNCAyMzguMzE2NDc2IApMIDM2MS41MzM1ODkgMjM2Ljk3MTAxIApMIDM2Mi40OTIxNjYgMjAzLjU4OTE4NyAKTCAzNjMuNDE5ODIxIDIwNC43NTE2NiAKTCAzNjQuMzc4Mzk4IDIwNS41NDU2NzggCkwgMzY1LjMzNjk3NSAxODguNTkyOTQzIApMIDM2Ni4yMDI3ODcgMTgxLjcxNjE4OCAKTCAzNjcuMTYxMzYzIDE3NS45NTYxODEgCkwgMzY4LjA4OTAxOSAxNTcuNzA0NzcgCkwgMzY5LjA0NzU5NSAxNTUuNDk1MzkzIApMIDM2OS45NzUyNTEgMTU0LjU1MjY3NiAKTCAzNzAuOTMzODI4IDE2NS4wNDM1MTIgCkwgMzcxLjg5MjQwNCAxNDMuMDY0MDAxIApMIDM3Mi44MjAwNiAxNDYuOTgzNzE2IApMIDM3My43Nzg2MzYgMTUyLjE2MjQzNyAKTCAzNzQuNzA2MjkyIDE1Ni4yNTU2NTEgCkwgMzc1LjY2NDg2OSAxNTUuNjk2NzkyIApMIDM3Ni42MjM0NDUgMTUyLjc1MDA2NyAKTCAzNzcuNDg5MjU3IDE2NC45NzIwMiAKTCAzNzguNDQ3ODM0IDE2MC4zMjgwODUgCkwgMzc5LjM3NTQ4OSAxNjUuMDc0MjY5IApMIDM4MC4zMzQwNjYgMTYwLjc1MjA5NyAKTCAzODEuMjYxNzIxIDE1OS44MDMyMjggCkwgMzgyLjIyMDI5OCAxNDkuNTIzNzIgCkwgMzgzLjE3ODg3NSAxNDkuMjc5NDU1IApMIDM4NS4wNjUxMDcgMTM5LjA1NDE5NSAKTCAzODUuOTkyNzYyIDEzOS40ODAzMzkgCkwgMzg2Ljk1MTMzOSAxNDMuMjkyMTg1IApMIDM4Ny45MDk5MTYgMTMzLjM5OTU4NiAKTCAzODguODA2NjQ5IDEzOS45ODY5MzUgCkwgMzg5Ljc2NTIyNiAxMzQuNDU1NjQ1IApMIDM5MC42OTI4ODEgMTM4Ljk2Mzg2MSAKTCAzOTEuNjUxNDU4IDEzOC41NzkyMjggCkwgMzkyLjU3OTExMyAxNTIuNjExMTAzIApMIDM5My41Mzc2OSAxNTkuMzA2MjIzIApMIDM5NC40OTYyNjcgMTgxLjYwNjE0IApMIDM5NS40MjM5MjIgMTg1LjUxNjYwMyAKTCAzOTYuMzgyNDk5IDE3MS41OTQ3NzUgCkwgMzk3LjMxMDE1NCAxNjEuNDU2OTQzIApMIDM5OC4yNjg3MzEgMTU5LjU5Mzk4MyAKTCAzOTkuMjI3MzA4IDE2NC45NzU3OTggCkwgNDAwLjA5MzExOSAxNzIuNTEwMzY4IApMIDQwMS45NzkzNTEgMTc0LjQ0MTQ3OSAKTCA0MDIuOTM3OTI4IDE4MC41Nzg5NSAKTCA0MDMuODY1NTgzIDE4MS4xNDg4MDQgCkwgNDA0LjgyNDE2IDE1NC43MjAyMTcgCkwgNDA1Ljc4MjczNyAxNTMuMzUyMzI1IApMIDQwNi43MTAzOTIgMTU1LjIyNjkxIApMIDQwNy42Njg5NjkgMTY1LjAzOTk3NiAKTCA0MDguNTk2NjI0IDE2My41NDExMTIgCkwgNDA5LjU1NTIwMSAxNjguMjg1MjYzIApMIDQxMC41MTM3NzggMTU5LjIwODcyIApMIDQxMS4zNzk1OSAxNjQuMTM4MDkxIApMIDQxMi4zMzgxNjcgMTU3LjI5ODE0NyAKTCA0MTMuMjY1ODIyIDE1OC45NzA3NTIgCkwgNDE0LjIyNDM5OSAxNTAuODg1OTkzIApMIDQxNS4xNTIwNTQgMTQ3LjYwNzQzMSAKTCA0MTYuMTEwNjMxIDE1My45ODA2NDIgCkwgNDE3LjA2OTIwOCAxNTQuNDQ3NjY2IApMIDQxNy45OTY4NjMgMTU4LjU1NzAwOSAKTCA0MTguOTU1NDQgMTQ5Ljg3MDg2MyAKTCA0MTkuODgzMDk1IDE1NC42MTQ2MjYgCkwgNDIwLjg0MTY3MiAxNTAuOTQ3MzEzIApMIDQyMS44MDAyNDkgMTQxLjgxMzIyOSAKTCA0MjIuNjY2MDYgMTI3LjA5Mjg3OSAKTCA0MjMuNjI0NjM3IDEyNy4wOTI4NzkgCkwgNDI0LjU1MjI5MiAxMjYuMDU1Mjc0IApMIDQyNS41MTA4NjkgMTI4LjAwNTcxMSAKTCA0MjYuNDM4NTI0IDEzMC43MTU0MzYgCkwgNDI3LjM5NzEwMSAxMzEuMDI5NCAKTCA0MjguMzU1Njc4IDEzMS45MzIyMDYgCkwgNDI5LjI4MzMzMyAxMjguMjUyMzQ5IApMIDQzMC4yNDE5MSAxMjMuNDY0MjY3IApMIDQzMS4xNjk1NjUgMTMxLjIwNjI5IApMIDQzMi4xMjgxNDIgMTI4LjY1OTQ1NyAKTCA0MzMuMDg2NzE5IDEzNS41MjIzNTkgCkwgNDMzLjk4MzQ1MiAxMjQuNTUzNjk4IApMIDQzNC45NDIwMjkgMTI3LjkzODgyIApMIDQzNi44MjgyNjEgMTE4LjQzMDAzMSAKTCA0MzcuNzU1OTE2IDEwNS40MjY3MDMgCkwgNDM4LjcxNDQ5MyAxMDMuNzgxODAzIApMIDQzOS42NzMwNyAxMDQuMTIyNjk4IApMIDQ0MC42MDA3MjUgMTAyLjYzNDk3NSAKTCA0NDEuNTU5MzAyIDEwNC44Mjc3ODcgCkwgNDQyLjQ4Njk1NyAxMDYuNjAxMjg1IApMIDQ0My40NDU1MzQgMTExLjI0ODc1NiAKTCA0NDQuNDA0MTExIDExNC4xMTk1OCAKTCA0NDUuMjY5OTIyIDExNS4zNjE1MzggCkwgNDQ2LjIyODQ5OSAxMTUuNTQzNjEgCkwgNDQ4LjExNDczMSAxMTAuMzgwMDQ5IApMIDQ0OS4wNDIzODYgMTE0LjAzNzQ4MSAKTCA0NTAuMDAwOTYzIDExMy41NzQxMzggCkwgNDUwLjk1OTU0IDExMi41NTAzMzggCkwgNDUxLjg4NzE5NSAxMTMuMDM0MzYzIApMIDQ1Mi44NDU3NzIgMTEzLjEzOTEzMSAKTCA0NTMuNzczNDI3IDExNC44ODg5OTIgCkwgNDU0LjczMjAwNCAxMTMuMTA5ODI3IApMIDQ1Ni41NTYzOTMgOTcuNDc5ODQyIApMIDQ1Ny41MTQ5NyA5OC43MDA0ODcgCkwgNDU4LjQ0MjYyNSA5Ny40NzQ5NSAKTCA0NTkuNDAxMjAyIDEwMS42MDY1NzMgCkwgNDYwLjMyODg1NyA5OS4wMjE0MjcgCkwgNDYxLjI4NzQzNCAxMDEuMjA1OTA4IApMIDQ2Mi4yNDYwMTEgMTEyLjc4NTQ0OSAKTCA0NjMuMTczNjY2IDEwNy4yNTUxNzYgCkwgNDY0LjEzMjI0MyA5My4zMzA1MzkgCkwgNDY1LjA1OTg5OCA5Mi4xNDAzMTIgCkwgNDY2LjAxODQ3NSA4Ny4wNjQzMjQgCkwgNDY2Ljk3NzA1MiA4OC41MjcyNDggCkwgNDY3Ljg0Mjg2MyA3My41NjAzMDggCkwgNDY4LjgwMTQ0IDc1LjEyNjgzOCAKTCA0NjkuNzI5MDk1IDczLjAwNTUxOCAKTCA0NzAuNjg3NjcyIDc2LjYwNjYxOCAKTCA0NzEuNjE1MzI3IDc3LjkxNjI0MSAKTCA0NzIuNTczOTA0IDg0Ljc2NTA0OSAKTCA0NzMuNTMyNDgxIDg5LjkwNjA4NyAKTCA0NzQuNDYwMTM2IDg5LjYyMjM5NSAKTCA0NzYuMzQ2MzY4IDk3LjM0MDE1MSAKTCA0NzcuMzA0OTQ1IDg5LjE5Njc4NCAKTCA0NzguMjYzNTIyIDg2Ljg2NDM3OSAKTCA0ODAuMTE4ODMyIDgxLjQwNTU5OCAKTCA0ODEuMDQ2NDg3IDc3LjY2MDk4MSAKTCA0ODIuMDA1MDY0IDgxLjczMzMxOSAKTCA0ODIuOTMyNzE5IDcyLjU5Mzk1NCAKTCA0ODMuODkxMjk2IDcyLjM0ODM4MiAKTCA0ODQuODQ5ODczIDY3LjAxMDQwMSAKTCA0ODUuNzc3NTI4IDY3LjE0NTgzIApMIDQ4Ni43MzYxMDUgNzIuNTQ0NjQ2IApMIDQ4Ny42NjM3NiA3MS4wOTI1MjMgCkwgNDg5LjU4MDkxNCA2Ni4zNDgzMjUgCkwgNDkwLjQ0NjcyNSA2NC43ODA0MzkgCkwgNDkxLjQwNTMwMiA2MS43MjY2MjIgCkwgNDkyLjMzMjk1NyA2My40Nzc4ODggCkwgNDkzLjI5MTUzNCA2MS4wNTUyOTMgCkwgNDk0LjIxOTE5IDYxLjQ4MDMyMyAKTCA0OTUuMTc3NzY2IDUzLjM3OTUzMSAKTCA0OTYuMTM2MzQzIDYxLjUyNjYyOCAKTCA0OTcuMDYzOTk4IDU2LjcxNjEyIApMIDQ5OC4wMjI1NzUgNTIuNDk4MDM3IApMIDQ5OC45NTAyMzEgNDkuNjczNjYzIApMIDQ5OS45MDg4MDcgNDkuMDUwMTQyIApMIDUwMC44NjczODQgNTUuODU4Nzk2IApMIDUwMS43MzMxOTYgNTMuNTA5MzQxIApMIDUwMi42OTE3NzMgNTUuOTI3NzIxIApMIDUwMy42MTk0MjggNTQuNTAzOTgyIApMIDUwNC41NzgwMDUgNjAuNDk3NDAzIApMIDUwNS41MDU2NiA1OC43OTE0MjUgCkwgNTA2LjQ2NDIzNyA1OC40ODM0MTggCkwgNTA3LjQyMjgxNCA3Mi42MzkzODcgCkwgNTA4LjM1MDQ2OSA3Ni43MDQ2MDUgCkwgNTA5LjMwOTA0NiA2OC42NTU0OTUgCkwgNTEwLjIzNjcwMSA3My42NzUyNDggCkwgNTExLjE5NTI3OCA3Mi42NTkxMDEgCkwgNTEyLjE1Mzg1NSA3My4zNjY4NTMgCkwgNTEzLjAxOTY2NiA2My42OTMwNDIgCkwgNTEzLjk3ODI0MyA2OS42Nzk3NzkgCkwgNTE0LjkwNTg5OCA3MC40MjY5MSAKTCA1MTUuODY0NDc1IDY5LjAxNzYwNSAKTCA1MTYuNzkyMTMgNjguMDY5NTExIApMIDUxNy43NTA3MDcgNzEuNzg5MDM4IApMIDUxOC43MDkyODQgODAuMDkzMDY5IApMIDUxOS42MzY5MzkgOTEuNjgyMTUyIApMIDUyMC41OTU1MTYgODguOTEyMzE3IApMIDUyMS41MjMxNzEgODUuMDQ5NTE2IApMIDUyMi40ODE3NDggODIuMzExOTQgCkwgNTIzLjQ0MDMyNSA5MS4wMjc1MzQgCkwgNTU0LjQ4NTg0OSA5Ni4wNzM0OTEgCkwgNTU1LjQxMzUwNCA5Mi41MTczNDEgCkwgNTU2LjM3MjA4MSA5NS4xMjg5ODIgCkwgNTU3LjMzMDY1OCA4OS45NDAyODMgCkwgNTU4LjE5NjQ2OSA5MS42OTQ4OTEgCkwgNTU5LjE1NTA0NiA5NC40OTc2MTQgCkwgNTYwLjA4MjcwMSA5Mi40MTI2NjkgCkwgNTYxLjA0MTI3OCA5NS4zNjIyNTIgCkwgNTYxLjk2ODkzMyA5NC4wOTAzNjEgCkwgNTYyLjkyNzUxIDk4Ljg5NjA3MyAKTCA1NjMuODg2MDg3IDk0LjMxOTE3NCAKTCA1NjQuODEzNzQyIDkwLjQ3MDk1MiAKTCA1NjUuNzcyMzE5IDg1LjE3MDk5NCAKTCA1NjYuNjk5OTc0IDc3LjQ4MDMxMyAKTCA1NjcuNjU4NTUxIDc0Ljg3MzYxMyAKTCA1NjcuNjU4NTUxIDc0Ljg3MzYxMyAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojNTVhODY4O3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJsaW5lMmRfMzciPgogICAgPHBhdGggY2xpcC1wYXRoPSJ1cmwoI3A3ZDc3MTIwZTIwKSIgZD0iTSA2MC4zODU4MjQgMzA3LjU4NTM5OCAKTCA2MS4yNTE2MzUgMzEzLjYzOTk0NiAKTCA2My4xMzc4NjcgMzA5LjA5NzkyMSAKTCA2NC4wOTY0NDQgMzA0LjgyNDEzNiAKTCA2NS4wMjQwOTkgMzAyLjIwNTk1NiAKTCA2NS45ODI2NzYgMzA0LjcyMjEyOSAKTCA2Ni45NDEyNTMgMzA5LjM2NjY5NCAKTCA2OC44Mjc0ODUgMzEyLjM3MjEyNCAKTCA2OS43NTUxNCAzMDYuODEzODU1IApMIDcwLjcxMzcxNyAzMDkuNjYzMDc3IApMIDcxLjY3MjI5NCAzMDEuMjA1OTM5IApMIDcyLjU2OTAyNyAyOTkuODk2ODQ4IApMIDczLjUyNzYwNCAyOTcuMzQ3NTQ1IApMIDc0LjQ1NTI1OSAzMDAuNDEzMTMyIApMIDc1LjQxMzgzNiAzMDAuNDEzMTMyIApMIDc2LjM0MTQ5MSAzMDEuMDY3NzAxIApMIDc3LjMwMDA2OCAzMDIuNDEzMTY3IApMIDc4LjI1ODY0NSAzMDEuMDI5MjkxIApMIDc5LjE4NjMgMzAyLjM5MzY5NiAKTCA4MC4xNDQ4NzcgMjk1LjM3MzkwNyAKTCA4MS4wNzI1MzIgMzAwLjg5MTk3NCAKTCA4Mi4wMzExMDkgMjk2LjA0ODMzNSAKTCA4Mi45ODk2ODYgMjg0LjU3NjU2NSAKTCA4My44NTU0OTggMjg2LjYzNzY3OSAKTCA4NC44MTQwNzUgMjgyLjg3MDM5NCAKTCA4NS43NDE3MyAyODMuMzc0OTU1IApMIDg2LjcwMDMwNyAyODIuODY1MTE0IApMIDg3LjYyNzk2MiAyODIuODY1MTE0IApMIDg4LjU4NjUzOSAyNzguNzg2MjM4IApMIDg5LjU0NTExNiAyNzkuMTYyNDQzIApMIDkwLjQ3Mjc3MSAyODAuMTIxNTggCkwgOTEuNDMxMzQ4IDI4NS4wMTQxNCAKTCA5Mi4zNTkwMDMgMjc1LjEwOTE5IApMIDkzLjMxNzU4IDI3Ny4zOTM5MzQgCkwgOTQuMjc2MTU3IDI3Ni45MTQzNjUgCkwgOTUuMTQxOTY4IDI3My4xMTU0NTEgCkwgOTYuMTAwNTQ1IDI2NS44MDU5NjUgCkwgOTcuMDI4MiAyNjIuMzE4NTQ1IApMIDk3Ljk4Njc3NyAyNTQuNzI3Nzg5IApMIDk4LjkxNDQzMiAyNTcuNjY1MjEzIApMIDEwMC44MzE1ODYgMjQ1LjYzMDg1NSAKTCAxMDEuNzU5MjQxIDI0Ni43MDcyMDggCkwgMTAyLjcxNzgxOCAyNTYuMzM5NDYxIApMIDEwMy42NDU0NzMgMjU4LjA1NzA2NCAKTCAxMDQuNjA0MDUgMjUyLjI3MzYxNCAKTCAxMDUuNTYyNjI3IDI0OC4zOTg3MDMgCkwgMTA2LjQyODQzOCAyNTQuMjU4OTI1IApMIDEwNy4zODcwMTUgMjUxLjQ5MTEyNCAKTCAxMDguMzE0NjcgMjQ2LjQ1MTEyNSAKTCAxMDkuMjczMjQ3IDI1MC4zNjIxMjEgCkwgMTEwLjIwMDkwMiAyNDQuNDcxMTkxIApMIDExMS4xNTk0NzkgMjQ2LjUxMzcwNSAKTCAxMTIuMTE4MDU2IDIzOC4xNjY4MDggCkwgMTEzLjA0NTcxMSAyMzkuMjE5NzY2IApMIDExNC4wMDQyODggMjQyLjE3OTc2MiAKTCAxMTQuOTMxOTQzIDIzOC45MTI0MzcgCkwgMTE1Ljg5MDUyIDIzMC40NzY5MDIgCkwgMTE2Ljg0OTA5NyAyMTYuODAzNDU2IApMIDExNy43NDU4MzEgMjI1LjY5NTUwNCAKTCAxMTguNzA0NDA3IDIzMS4wNzczMTkgCkwgMTE5LjYzMjA2MyAyMzcuOTM5MTU3IApMIDEyMC41OTA2MzkgMjI4Ljk2OTQ2NSAKTCAxMjEuNTE4Mjk1IDIyOC40NjQ5MDMgCkwgMTIyLjQ3Njg3MSAyMjIuOTcyMTIgCkwgMTIzLjQzNTQ0OCAyMTguNzU2MzYzIApMIDEyNC4zNjMxMDQgMjE3LjkyMTI3MSAKTCAxMjUuMzIxNjggMjI0LjczNTIwNSAKTCAxMjYuMjQ5MzM2IDIyMy4yODIxMTMgCkwgMTI4LjE2NjQ4OSAyMjQuMjI3MjUyIApMIDEyOS4wMzIzMDEgMjI0LjUxNTAxMyAKTCAxMjkuOTkwODc4IDIyMy41MzY1MDEgCkwgMTMwLjkxODUzMyAyMTguNzg4NzY3IApMIDEzMS44NzcxMSAyMTUuMjUwMDUzIApMIDEzMy43NjMzNDIgMjIzLjQ3MTY0NSAKTCAxMzQuNzIxOTE5IDIyNy45NjU3NjYgCkwgMTM1LjY0OTU3NCAyMzMuNzQ1MDk5IApMIDEzNi42MDgxNTEgMjM0LjQzMjYwNSAKTCAxMzguNDk0MzgzIDIyOC40ODAxMTIgCkwgMTM5LjQ1Mjk2IDIyNC4xODEwNDQgCkwgMTQwLjMxODc3MSAyMjUuNTQ5OTA1IApMIDE0MS4yNzczNDggMjI2LjY1MDcxOCAKTCAxNDIuMjA1MDAzIDIyNC40NTQxNzcgCkwgMTQzLjE2MzU4IDIyOS4zNzk5MTUgCkwgMTQ0LjA5MTIzNSAyMzQuODYzMzAxIApMIDE0NS4wNDk4MTIgMjM0LjUxOTc5IApMIDE0Ni4wMDgzODkgMjI2LjA2MDQ3MiAKTCAxNDYuOTM2MDQ0IDIyOS44OTk5MjggCkwgMTQ3Ljg5NDYyMSAyMjkuNjQzMzEyIApMIDE0OC44MjIyNzYgMjMxLjkxODg1MyAKTCAxNDkuNzgwODUzIDIzMC44OTU1MzggCkwgMTUwLjczOTQzIDIyOS4yMjUzMDYgCkwgMTUxLjYwNTI0MSAyMjkuMjg5ODcyIApMIDE1Mi41NjM4MTggMjI2LjMyNDQwMiAKTCAxNTMuNDkxNDczIDIyNC40NjE0NDIgCkwgMTU1LjM3NzcwNSAyMTIuMzg2NTQyIApMIDE1Ni4zMzYyODIgMjE4LjU1OTgwOCAKTCAxNTcuMjk0ODU5IDIxNS4wNzY3NDcgCkwgMTU4LjIyMjUxNCAyMTcuMTE2MTYxIApMIDE1OS4xODEwOTEgMjE3LjQzNTUwMiAKTCAxNjAuMTA4NzQ2IDIwOS4wOTM2OTEgCkwgMTYxLjA2NzMyMyAyMTEuMTU5Njk3IApMIDE2Mi4wMjU5IDIxMS44NzkwMjYgCkwgMTYyLjkyMjYzNCAyMTYuMDY1NDc5IApMIDE2My44ODEyMTEgMjE5LjU0NDMyNiAKTCAxNjQuODA4ODY2IDIxOS4zMTM2NzIgCkwgMTY1Ljc2NzQ0MyAyMjUuMDc5OTI2IApMIDE2Ni42OTUwOTggMjI4LjAyNTM5MSAKTCAxNjcuNjUzNjc1IDIzOC40NzkyNzEgCkwgMTY4LjYxMjI1MiAyMzQuMTI0NDUyIApMIDE2OS41Mzk5MDcgMjMzLjcxMzk1NCAKTCAxNzAuNDk4NDg0IDIzMC41MzkxNDMgCkwgMTcyLjM4NDcxNiAyMzkuNDAwOTE4IApMIDE3My4zNDMyOTIgMjE4LjA3MDI2MSAKTCAxNzQuMjA5MTA0IDIxOC43MjA0MjMgCkwgMTc1LjE2NzY4MSAyMjYuMjk4OTI1IApMIDE3Ni4wOTUzMzYgMjI5LjExMTM4MyAKTCAxNzcuMDUzOTEzIDIyOS41Mjg5NTQgCkwgMTc3Ljk4MTU2OCAyMjEuMTA1MjM3IApMIDE3OC45NDAxNDUgMjI0LjA0NzMxMSAKTCAxNzkuODk4NzIyIDIyOS4wNDQ3MzUgCkwgMTgxLjc4NDk1NCAyMzcuMTg3Mjc5IApMIDE4Mi43MTI2MDkgMjMxLjAwMzg5IApMIDE4My42NzExODYgMjMzLjc0NTU4MyAKTCAxODQuNjI5NzYzIDIyOC45OTg4MTcgCkwgMTg1LjQ5NTU3NCAyMzMuODg2ODcyIApMIDE4Ni40NTQxNTEgMjI2Ljk2NzM5NSAKTCAxODguMzQwMzgzIDIzMi40MTY0ODkgCkwgMTg5LjI2ODAzOCAyMzQuMzczNTEyIApMIDE5MC4yMjY2MTUgMjQyLjYzMzE3NSAKTCAxOTEuMTg1MTkyIDIzNy4wNDQzNDMgCkwgMTkyLjExMjg0NyAyNDEuNDk4MjYyIApMIDE5My4wNzE0MjQgMjM3LjMyOTA1MiAKTCAxOTQuOTU3NjU2IDIzOC40NzU1NDEgCkwgMTk1LjkxNjIzMyAyMzMuMzQwMTIyIApMIDE5Ni43ODIwNDUgMjI1LjM1NjExMSAKTCAxOTcuNzQwNjIxIDIyOS4wMTE3MDEgCkwgMTk4LjY2ODI3NyAyMjUuMTU2NTUzIApMIDE5OS42MjY4NTMgMjI2LjA3OTE2OSAKTCAyMDAuNTU0NTA5IDIyNi41NDk0MzggCkwgMjAxLjUxMzA4NiAyMTIuMzk4NDA5IApMIDIwMi40NzE2NjIgMjE0LjI0NzEyOSAKTCAyMDMuMzk5MzE4IDIxNy43MDY4OTEgCkwgMjA0LjM1Nzg5NCAyMjkuMzgxMzE5IApMIDIwNS4yODU1NSAyMzUuOTg2Mjk5IApMIDIwNi4yNDQxMjYgMjIyLjYwMjU1MSAKTCAyMDcuMjAyNzAzIDIyNC4xMDA1OTEgCkwgMjA4LjA5OTQzNyAyMjcuMjk1MzEgCkwgMjA5LjA1ODAxNCAyMTUuMDQ3MDA3IApMIDIwOS45ODU2NjkgMjE5LjU3OTU4NyAKTCAyMTAuOTQ0MjQ2IDIyNS4wMTYzMjkgCkwgMjExLjg3MTkwMSAyMjIuNzg5MzcgCkwgMjEyLjgzMDQ3OCAyMjUuNDUwNzA3IApMIDIxMy43ODkwNTUgMjMwLjA2OTA2OCAKTCAyMTQuNzE2NzEgMjMzLjIxNDI4NCAKTCAyMTUuNjc1Mjg3IDIzNC4wMjE1NzMgCkwgMjE2LjYwMjk0MiAyMzguODY1MjEyIApMIDIxNy41NjE1MTkgMjI4Ljg3MDQxMiAKTCAyMTguNTIwMDk2IDIyNS44MTEyNjcgCkwgMjE5LjM4NTkwNyAyMjMuOTk0OTAzIApMIDIyMC4zNDQ0ODQgMjIzLjQxMTM0MSAKTCAyMjEuMjcyMTM5IDIyNC41NjQ2MTIgCkwgMjIyLjIzMDcxNiAyMjIuMzIwMDIxIApMIDIyMy4xNTgzNzEgMjE3LjE5MTQ4IApMIDIyNC4xMTY5NDggMjE3LjE5MTQ4IApMIDIyNS4wNzU1MjUgMjE5Ljg3MDkzMiAKTCAyMjYuMDAzMTggMjIxLjUyMjE3NyAKTCAyMjYuOTYxNzU3IDIyMy45MTU1MTYgCkwgMjI3Ljg4OTQxMiAyMjUuNzMxODggCkwgMjI4Ljg0Nzk4OSAyMTkuNDQxNDQ3IApMIDIyOS44MDY1NjYgMjIxLjc3OTc2MiAKTCAyMzAuNjcyMzc3IDIyMi4zNzA0NDMgCkwgMjMxLjYzMDk1NCAyMjQuNzYyMzc3IApMIDIzMi41NTg2MDkgMjI2Ljc3NTI5NyAKTCAyMzMuNTE3MTg2IDIyNy40Mzg4MjcgCkwgMjM0LjQ0NDg0MSAyMzIuMTQ3OTA5IApMIDIzNS40MDM0MTggMjMyLjI5Njk0OCAKTCAyMzYuMzYxOTk1IDI0Mi4xMzU1ODggCkwgMjM3LjI4OTY1IDI0OC43ODM3MjQgCkwgMjM4LjI0ODIyNyAyNDkuMDAzODY3IApMIDIzOS4xNzU4ODIgMjQ3Ljg3NzQzMSAKTCAyNDAuMTM0NDU5IDI1NC40ODI0MSAKTCAyNDEuMDkzMDM2IDI0Ny4wODk0NjggCkwgMjQxLjk1ODg0OCAyMzUuODI1MTk5IApMIDI0Mi45MTc0MjUgMjM1LjgyNTE5OSAKTCAyNDMuODQ1MDggMjM2LjAwNzk5OCAKTCAyNDQuODAzNjU3IDIzNi4wMDc5OTggCkwgMjQ1LjczMTMxMiAyMzkuNzMzODcgCkwgMjQ2LjY4OTg4OSAyMzEuODYyOTU4IApMIDI0Ny42NDg0NjYgMjMzLjYyNDI5OCAKTCAyNDguNTc2MTIxIDIzNi4zNjU5OTEgCkwgMjQ5LjUzNDY5OCAyMzQuNjIyMjgyIApMIDI1MC40NjIzNTMgMjM0LjYyMjI4MiAKTCAyNTEuNDIwOTMgMjI3Ljk3NDE0NiAKTCAyNTIuMzc5NTA2IDIxMi4xMDcwNjQgCkwgMjUzLjI3NjI0IDIxMC45NzQ3NjcgCkwgMjU0LjIzNDgxNyAyMDguNDkwODUyIApMIDI1Ni4xMjEwNDkgMjI3LjAwMjA3NiAKTCAyNTcuMDQ4NzA0IDIzMC42NTc2NjcgCkwgMjU4LjAwNzI4MSAyMjMuNzM4MTkgCkwgMjU4Ljk2NTg1OCAyMjQuNzc2MTMzIApMIDI1OS44OTM1MTMgMjI0Ljc3NjEzMyAKTCAyNjAuODUyMDkgMjE5LjM5NDMxOCAKTCAyNjEuNzc5NzQ1IDIwNy40NDY2NjEgCkwgMjYyLjczODMyMiAyMTIuNjgzMDIxIApMIDI2My42OTY4OTkgMjA5Ljc0NzQ4NiAKTCAyNjQuNTYyNzEgMjEyLjY1MzY2OSAKTCAyNjUuNTIxMjg3IDIxMi42NTM2NjkgCkwgMjY2LjQ0ODk0MiAyMDYuNjkyMjY0IApMIDI2Ny40MDc1MTkgMTk3LjUzNTgwMSAKTCAyNjguMzM1MTc0IDE5NS4yODI5MjggCkwgMjY5LjI5Mzc1MSAxOTYuMzU5MjgyIApMIDI3MC4yNTIzMjggMjAzLjU4MDcxMSAKTCAyNzEuMTc5OTgzIDIwMi4yNzE2MiAKTCAyNzIuMTM4NTYgMTk3LjgxMDM4NyAKTCAyNzMuMDY2MjE1IDIwMS4zODE4NDQgCkwgMjc0LjAyNDc5MiAyMDEuMzgxODQ0IApMIDI3NC45ODMzNjkgMTk2LjI4MzI4NSAKTCAyNzUuODQ5MTggMjAwLjk2NTQ4NSAKTCAyNzYuODA3NzU3IDIwMC45NjU0ODUgCkwgMjc3LjczNTQxMiAxNzAuNjEyMDAxIApMIDI3OC42OTM5ODkgMTg0LjE1ODMwMiAKTCAyNzkuNjIxNjQ0IDE4Ni4zODUyNjEgCkwgMjgwLjU4MDIyMSAxODEuNzE2NjcyIApMIDI4MS41Mzg3OTggMTc2LjQ1Nzg4NSAKTCAyODIuNDY2NDUzIDE3MC42NDU1MTkgCkwgMjgzLjQyNTAzIDE3MS45OTQ4MTIgCkwgMjg0LjM1MjY4NSAxODEuNDEyOTc2IApMIDI4NS4zMTEyNjIgMTgzLjA4MzIwOCAKTCAyODYuMjY5ODM5IDE1OC44ODgwNzEgCkwgMjg3LjEzNTY1MSAxNjIuMzc1NDkxIApMIDI4OC4wOTQyMjggMTU3LjM2NDg0NCAKTCAyODkuMDIxODgzIDE0Mi45ODUyOTIgCkwgMjg5Ljk4MDQ2IDEzNi41Nzc2OTEgCkwgMjkwLjkwODExNSAxMzYuMDU5NjY0IApMIDI5MS44NjY2OTIgMTMwLjE2NTI5NSAKTCAyOTIuODI1MjY5IDEzMy4xNDQ1NjkgCkwgMjkzLjc1MjkyNCAxMjkuMjMwNTIxIApMIDI5NC43MTE1MDEgMTM4LjA1NzcxMyAKTCAyOTUuNjM5MTU2IDEzNS44NTQ1MzYgCkwgMjk2LjU5NzczMyAxNDQuMzcwODE1IApMIDI5Ny41NTYzMSAxNDQuNjkzNzQgCkwgMjk4LjQ1MzA0MyAxNDIuNzMwMjc1IApMIDI5OS40MTE2MiAxMTMuNDc5NzM2IApMIDMwMC4zMzkyNzUgMTE0LjY1NjMwNCAKTCAzMDEuMjk3ODUyIDExNS4yNTEyIApMIDMwMi4yMjU1MDcgMTE0LjYzODA5MiAKTCAzMDIuMjI1NTA3IDExNC42MzgwOTIgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6I2M0NGU1MjtzdHJva2UtbGluZWNhcDpyb3VuZDtzdHJva2Utd2lkdGg6MS43NTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0ibGluZTJkXzM4Ij4KICAgIDxwYXRoIGNsaXAtcGF0aD0idXJsKCNwN2Q3NzEyMGUyMCkiIGQ9Ik0gMjU0LjIzNDgxNyAyOTcuOTQ1NzgyIApMIDI1NS4xNjI0NzIgMzA2LjIwMjAwNiAKTCAyNTcuMDQ4NzA0IDMyNi4xNzYwMDkgCkwgMjU4LjAwNzI4MSAzMjAuOTExMTY3IApMIDI1OC45NjU4NTggMzE5Ljk2MTQyNyAKTCAyNTkuODkzNTEzIDMxNi4yMzU1NTUgCkwgMjYwLjg1MjA5IDMxNy45NjU0MTIgCkwgMjYxLjc3OTc0NSAzMjYuOTM1MTA0IApMIDI2My42OTY4OTkgMzI2LjkzNTEwNCAKTCAyNjUuNTIxMjg3IDMzNi4xODIwNDUgCkwgMjY2LjQ0ODk0MiAzMTcuMzQ1NjY4IApMIDI2Ny40MDc1MTkgMzA3LjY1ODM5MSAKTCAyNjguMzM1MTc0IDMxNC4xMTY1NiAKTCAyNjkuMjkzNzUxIDMwNC44MDE4NTYgCkwgMjcwLjI1MjMyOCAzMDYuMzY0MzE3IApMIDI3MS4xNzk5ODMgMzA5LjU5MzQyNSAKTCAyNzIuMTM4NTYgMjk3LjQ4NDMyOSAKTCAyNzMuMDY2MjE1IDMwNC40MDM4MDYgCkwgMjc0LjAyNDc5MiAyODkuODcyODkgCkwgMjc0Ljk4MzM2OSAyODYuMTQ3MDE4IApMIDI3NS44NDkxOCAyODAuMzgwNzY0IApMIDI3Ni44MDc3NTcgMjg4LjYyNTI2NiAKTCAyNzcuNzM1NDEyIDI4Mi40MTU0NzkgCkwgMjc4LjY5Mzk4OSAyOTAuMTIxMjcyIApMIDI3OS42MjE2NDQgMjkxLjQzMDM2MiAKTCAyODAuNTgwMjIxIDI5Ni44MTIxNzcgCkwgMjgxLjUzODc5OCAyOTguMzI1ODE0IApMIDI4Mi40NjY0NTMgMjkwLjUxMzUxIApMIDI4My40MjUwMyAyOTAuNTEzNTEgCkwgMjg0LjM1MjY4NSAyODcuODIyNTc4IApMIDI4NS4zMTEyNjIgMjkwLjM3MTg4MiAKTCAyODYuMjY5ODM5IDMwMS4xMzU1MTIgCkwgMjg3LjEzNTY1MSAyOTcuNjc1NzUgCkwgMjg4LjA5NDIyOCAyOTQuNDQ2NjQxIApMIDI4OS4wMjE4ODMgMzAzLjUyODQ2MyAKTCAyODkuOTgwNDYgMjk2LjA3NjcxOSAKTCAyOTAuOTA4MTE1IDMwNC4xNDk0NjYgCkwgMjkxLjg2NjY5MiAzMDkuOTYxODMyIApMIDI5Mi44MjUyNjkgMzA5Ljk2MTgzMiAKTCAyOTMuNzUyOTI0IDMxMS4wNjI2NDYgCkwgMjk0LjcxMTUwMSAzMTYuNjk0NzggCkwgMjk1LjYzOTE1NiAzMTkuMjQ0MDg0IApMIDI5Ni41OTc3MzMgMzEzLjg2MjI2OSAKTCAyOTcuNTU2MzEgMzEzLjg2MjI2OSAKTCAyOTguNDUzMDQzIDMwNC4xNzQ5OTIgCkwgMjk5LjQxMTYyIDMwOC4yMTEzNDEgCkwgMzAwLjMzOTI3NSAzMDguMjExMzQxIApMIDMwMS4yOTc4NTIgMjkwLjU5ODEyOCAKTCAzMDIuMjI1NTA3IDMwMS44OTk5MzUgCkwgMzAzLjE4NDA4NCAzMDYuMTExODE4IApMIDMwNC4xNDI2NjEgMzE0LjE4NDU2NSAKTCAzMDUuMDcwMzE2IDMxMC4wMzI4ODggCkwgMzA2LjAyODg5MyAzMTcuNjgwNzUxIApMIDMwNi45NTY1NDggMzExLjYyNjIwMyAKTCAzMDcuOTE1MTI1IDMxNC4zMTcxMzUgCkwgMzA4Ljg3MzcwMiAzMDAuMDcxMTIyIApMIDMwOS43Mzk1MTMgMzAwLjA3MTEyMiAKTCAzMTEuNjI1NzQ1IDMwNC41NzkyOTEgCkwgMzEyLjU4NDMyMiAyOTAuMDQ4Mzc1IApMIDMxMy41MTE5NzcgMjg2LjMyMjUwMyAKTCAzMTQuNDcwNTU0IDI3NS45NDMyNjQgCkwgMzE1LjQyOTEzMSAyODAuMjE3MDQ5IApMIDMxNi4zNTY3ODYgMjc4LjY1NDU4OCAKTCAzMTcuMzE1MzYzIDI2Ni41NDU0OTIgCkwgMzE4LjI0MzAxOCAyNzIuNjAwMDQgCkwgMzE5LjIwMTU5NSAyNjAuMTQ0OTYyIApMIDMyMC4xNjAxNzIgMjU5LjA0NDE0OSAKTCAzMjEuMDI1OTgzIDI2MC4xMjA1MDIgCkwgMzIxLjk4NDU2IDI2NC41MjM4MDUgCkwgMzIzLjg3MDc5MiAyNTkuNzk1NDk0IApMIDMyNC43OTg0NDggMjY2LjQwMDQ3MyAKTCAzMjUuNzU3MDI0IDI2MC4wMjcyNjIgCkwgMzI2LjcxNTYwMSAyNjAuMDI3MjYyIApMIDMyNy42NDMyNTYgMjYzLjQwNjUyMyAKTCAzMjguNjAxODMzIDI3My4wOTM4IApMIDMyOS41Mjk0ODggMjU5LjQ3MTA2NyAKTCAzMzAuNDg4MDY1IDIzNS44NDM1NTcgCkwgMzMxLjQ0NjY0MiAyMjguNjk3MjA0IApMIDMzMi4zMTI0NTQgMjQ5LjQ1NTYzNCAKTCAzMzMuMjcxMDMxIDIyMC4zOTM4MDMgCkwgMzM0LjE5ODY4NiAyMzQuMDE2NTM2IApMIDMzNS4xNTcyNjMgMjE1LjA2MzE4NSAKTCA0MzAuMjQxOTEgMTgzLjAwMTAxMSAKTCA0MzEuMTY5NTY1IDE4Ny41MTU1MjQgCkwgNDMyLjEyODE0MiAxODguNDIwODk3IApMIDQzMy4wODY3MTkgMTkzLjQ5NTE5IApMIDQzMy45ODM0NTIgMTg2LjI4MTI2OCAKTCA0MzQuOTQyMDI5IDE4OS41MTAzNzcgCkwgNDM1Ljg2OTY4NCAxOTkuMTIwNzg1IApMIDQzNi44MjgyNjEgMTk1Ljc5OTc5MyAKTCA0MzcuNzU1OTE2IDIxMS40NzQwMDEgCkwgNDM4LjcxNDQ5MyAyMDMuNTQxNzE5IApMIDQzOS42NzMwNyAyMDcuMDc5NDY0IApMIDQ0MC42MDA3MjUgMjE1Ljk5NzkxIApMIDQ0MS41NTkzMDIgMjMyLjIwNjE3OCAKTCA0NDIuNDg2OTU3IDI0NS4yMzU4NTYgCkwgNDQzLjQ0NTUzNCAyMjcuNzk4NzU3IApMIDQ0NC40MDQxMTEgMjM3LjA1ODYzMiAKTCA0NDUuMjY5OTIyIDI1NS41NTI1MTUgCkwgNDQ2LjIyODQ5OSAyNTUuNTUyNTE1IApMIDQ0Ny4xNTYxNTQgMjQ3LjAwNDg5OCAKTCA0NDguMTE0NzMxIDI0OC40NTc5ODkgCkwgNDQ5LjA0MjM4NiAyNDEuOTY2NDk3IApMIDQ1MC4wMDA5NjMgMjQ5LjAxMTgxMSAKTCA0NTAuOTU5NTQgMjMzLjc1OTQ4NCAKTCA0NTEuODg3MTk1IDIyNi43MDU2NDUgCkwgNDUyLjg0NTc3MiAyMjMuODMyMzAyIApMIDQ1My43NzM0MjcgMjI4LjAzMDEzOCAKTCA0NTQuNzMyMDA0IDIyNi42MTU5NDEgCkwgNDU1LjY5MDU4MSAyMjcuOTkwMDMzIApMIDQ1Ni41NTYzOTMgMjE5LjE1MTI2NCAKTCA0NTcuNTE0OTcgMjAwLjMxMTg4NCAKTCA0NTguNDQyNjI1IDE5My41MzMyNjEgCkwgNDU5LjQwMTIwMiAxOTQuNTcxODgyIApMIDQ2MC4zMjg4NTcgMTgxLjgzNTYzMiAKTCA0NjEuMjg3NDM0IDE4NS45NjExMDQgCkwgNDYyLjI0NjAxMSAxODkuMzAxNTY4IApMIDQ2My4xNzM2NjYgMTcxLjE4Mjc3NiAKTCA0NjQuMTMyMjQzIDE2Ni43NDM4NzIgCkwgNDY1LjA1OTg5OCAxNjYuMTQ1ODc2IApMIDQ2Ni4wMTg0NzUgMTY0LjAxOTM3MyAKTCA0NjYuOTc3MDUyIDE2Mi40MzUwMTkgCkwgNDY3Ljg0Mjg2MyAxNjUuMTk4NzUxIApMIDQ2OC44MDE0NCAxNTQuMzY1MTMgCkwgNDY5LjcyOTA5NSAxNDcuNzE2OTk0IApMIDQ3MC42ODc2NzIgMTQ4LjEzNDU2NCAKTCA0NzIuNTczOTA0IDEyNC43NTU3NzUgCkwgNDczLjUzMjQ4MSAxMjYuMzQxMTQ2IApMIDQ3NC40NjAxMzYgMTI4Ljk5NzQ5NCAKTCA0NzUuNDE4NzEzIDEyNy41NjIzMjQgCkwgNDc2LjM0NjM2OCAxMzAuOTg4ODU5IApMIDQ3Ny4zMDQ5NDUgMTMyLjczODgxNyAKTCA0NzguMjYzNTIyIDEzNC4wMzU2NTMgCkwgNDc5LjE2MDI1NSAxMzAuMTA0Nzk4IApMIDQ4MC4xMTg4MzIgMTMyLjQ0NjUwNCAKTCA0ODcuNjYzNzYgMTQ0LjM4NzIzNSAKTCA0ODguNjIyMzM3IDE0Ni4xNTc2MzMgCkwgNDg5LjU4MDkxNCAxNDMuNDgxNTcxIApMIDQ5MC40NDY3MjUgMTQwLjIxODY1NCAKTCA0OTEuNDA1MzAyIDE0NC4yMjU5OSAKTCA0OTIuMzMyOTU3IDE0OC43MTU2NTUgCkwgNDkzLjI5MTUzNCAxNjQuOTg4MDA0IApMIDQ5NC4yMTkxOSAxNzEuMDA2NzA5IApMIDQ5NS4xNzc3NjYgMTgyLjYyNDkwMyAKTCA0OTYuMTM2MzQzIDE2OS43MDg1MTcgCkwgNDk3LjA2Mzk5OCAxNjcuNjY5MTAzIApMIDQ5OC4wMjI1NzUgMTc1LjQ5NzE5OCAKTCA0OTguOTUwMjMxIDE3Ny4wNTMzNjIgCkwgNTAwLjg2NzM4NCAxODMuOTI5MTAxIApMIDUwMS43MzMxOTYgMTc1LjU0NTg3NyAKTCA1MDIuNjkxNzczIDE4MS4zMDI2MzggCkwgNTAzLjYxOTQyOCAxNjguOTExOTMzIApMIDUwNS41MDU2NiAxOTQuNTQzODg2IApMIDUwNi40NjQyMzcgMTkxLjU1ODA3MyAKTCA1MDguMzUwNDY5IDE5Ny4zNTYyOTYgCkwgNTA5LjMwOTA0NiAyMDUuMTM0NDA0IApMIDUxMC4yMzY3MDEgMTk2LjcxMDY4OCAKTCA1MTEuMTk1Mjc4IDIwMS4zNzQ5MTggCkwgNTEyLjE1Mzg1NSAxODkuODYxMzQ3IApMIDUxMy4wMTk2NjYgMTkzLjM4OTg0MSAKTCA1MTMuOTc4MjQzIDE5MC4yNzYwNTkgCkwgNTE0LjkwNTg5OCAxOTYuNDUyNTIyIApMIDUxNS44NjQ0NzUgMjI5Ljk4NTQxOCAKTCA1MTYuNzkyMTMgMjI0LjMzMDQ3IApMIDUxNy43NTA3MDcgMjMxLjU2Mjg0NiAKTCA1MTguNzA5Mjg0IDI0Ni4wMDQ1NDEgCkwgNTE5LjYzNjkzOSAyMzAuODc2MTE1IApMIDUyMC41OTU1MTYgMjI5LjQ5MjIzOSAKTCA1MjEuNTIzMTcxIDIyOC40Njk2OTggCkwgNTIyLjQ4MTc0OCAyMzMuNDI0MDE0IApMIDUyMy40NDAzMjUgMjIzLjE0OTY0IApMIDUyNC4zMzcwNTggMTk4LjkzMTQ0NyAKTCA1MjUuMjk1NjM1IDIwNy44MTE0MzUgCkwgNTI2LjIyMzI5IDIwMi4xMDc4MDkgCkwgNTI3LjE4MTg2NyAyMDMuNjczMTI3IApMIDUyOC4xMDk1MjIgMTg1LjM5NTIyMiAKTCA1MjkuMDY4MDk5IDE3Ny40MzMwNTUgCkwgNTMwLjAyNjY3NiAxNzcuNDMzMDU1IApMIDUzMC45NTQzMzEgMTc4LjAwMjkwOSAKTCA1MzEuOTEyOTA4IDE3Mi44MTMyOSAKTCA1MzIuODQwNTYzIDE3MS43NzE2NjUgCkwgNTMzLjc5OTE0IDE1Ni45ODU4MjkgCkwgNTM0Ljc1NzcxNyAxNTYuOTg1ODI5IApMIDUzNS42MjM1MjkgMTUxLjUxNzIxNiAKTCA1MzYuNTgyMTA1IDE0Ny42NTYzNTIgCkwgNTM3LjUwOTc2MSAxNDIuNzgwMjEzIApMIDUzOC40NjgzMzggMTQyLjQ4NDg0NyAKTCA1MzkuMzk1OTkzIDE0MS44OTc3NSAKTCA1NDAuMzU0NTcgMTQxLjYxNjQzMiAKTCA1NDEuMzEzMTQ2IDE1MS43MDA0OTkgCkwgNTQyLjI0MDgwMiAxNTEuMzM2MzA2IApMIDU0My4xOTkzNzggMTY3LjI0MDc4IApMIDU0NC4xMjcwMzQgMTU5LjcwNjIxIApMIDU0NS4wODU2MTEgMTY0Ljc4MjczMSAKTCA1NDYuMDQ0MTg3IDE2MC45MzI4MTMgCkwgNTQ2LjkwOTk5OSAxNjQuNTQ3NDc1IApMIDU0Ny44Njg1NzYgMTY5Ljc1NTY5NCAKTCA1NDguNzk2MjMxIDE2OS4xNzIxMzMgCkwgNTQ5Ljc1NDgwOCAxNzAuOTAxOTkgCkwgNTUwLjY4MjQ2MyAxNzYuMjgzODA1IApMIDU1MS42NDEwNCAxNzYuNTM5NDUyIApMIDU1Mi41OTk2MTcgMTc5LjcwNDUyOCAKTCA1NTMuNTI3MjcyIDE4MS44MzkwNzEgCkwgNTU0LjQ4NTg0OSAxOTEuMTQxODExIApMIDU1NS40MTM1MDQgMTk0LjU0MjY3NSAKTCA1NTYuMzcyMDgxIDE5Ni42Mzg1MTcgCkwgNTU3LjMzMDY1OCAyMDAuNTk4NTMxIApMIDU1OC4xOTY0NjkgMTk3LjQzMjkyMiAKTCA1NTkuMTU1MDQ2IDE5OS43OTA2NiAKTCA1NjAuMDgyNzAxIDE5OC4xMzgzOTggCkwgNTYxLjA0MTI3OCAxNjcuNzgwODQ2IApMIDU2MS45Njg5MzMgMTI4Ljc2MjY3NCAKTCA1NjIuOTI3NTEgMTQ3LjA5Mzk1NyAKTCA1NjMuODg2MDg3IDExOS45OTgzNTMgCkwgNTY0LjgxMzc0MiAxMjIuMzA0ODQ1IApMIDU2NS43NzIzMTkgMTE5LjA3NTczNyAKTCA1NjYuNjk5OTc0IDExNC41MzQ4MjYgCkwgNTY3LjY1ODU1MSAxMTYuMjY0NjgzIApMIDU2Ny42NTg1NTEgMTE2LjI2NDY4MyAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojODE3MmIyO3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF8zIj4KICAgIDxwYXRoIGQ9Ik0gMzUuMDIyMTg4IDM1MS4wMDc1IApMIDM1LjAyMjE4OCAyNC44NDc1IAoiIHN0eWxlPSJmaWxsOm5vbmU7Ij48L3BhdGg+CiAgIDwvZz4KICAgPGcgaWQ9InBhdGNoXzQiPgogICAgPHBhdGggZD0iTSA1OTMuMDIyMTg3IDM1MS4wMDc1IApMIDU5My4wMjIxODcgMjQuODQ3NSAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJwYXRjaF81Ij4KICAgIDxwYXRoIGQ9Ik0gMzUuMDIyMTg4IDM1MS4wMDc1IApMIDU5My4wMjIxODggMzUxLjAwNzUgCiIgc3R5bGU9ImZpbGw6bm9uZTsiPjwvcGF0aD4KICAgPC9nPgogICA8ZyBpZD0icGF0Y2hfNiI+CiAgICA8cGF0aCBkPSJNIDM1LjAyMjE4OCAyNC44NDc1IApMIDU5My4wMjIxODggMjQuODQ3NSAKIiBzdHlsZT0iZmlsbDpub25lOyI+PC9wYXRoPgogICA8L2c+CiAgIDxnIGlkPSJ0ZXh0XzIwIj4KICAgIDwhLS0gQ3VtdWxhdGl2ZSBSZXR1cm5zIG92ZXIgVGltZSBmb3IgZGlmZmVyZW50IHBlcm1ub3MgLS0+CiAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTMwLjU0NDY4NyAxOC44NDc1KXNjYWxlKDAuMTYgLTAuMTYpIj4KICAgICA8ZGVmcz4KICAgICAgPHBhdGggZD0iTSAyNS45MjE4NzUgMCAKTCAyNS45MjE4NzUgNjMuMTQwNjI1IApMIDIuMzQzNzUgNjMuMTQwNjI1IApMIDIuMzQzNzUgNzEuNTc4MTI1IApMIDU5LjA3ODEyNSA3MS41NzgxMjUgCkwgNTkuMDc4MTI1IDYzLjE0MDYyNSAKTCAzNS40MDYyNSA2My4xNDA2MjUgCkwgMzUuNDA2MjUgMCAKegoiIGlkPSJBcmlhbE1ULTg0Ij48L3BhdGg+CiAgICAgIDxwYXRoIGQ9Ik0gOC42ODc1IDAgCkwgOC42ODc1IDQ1LjAxNTYyNSAKTCAwLjkyMTg3NSA0NS4wMTU2MjUgCkwgMC45MjE4NzUgNTEuODU5Mzc1IApMIDguNjg3NSA1MS44NTkzNzUgCkwgOC42ODc1IDU3LjM3NSAKUSA4LjY4NzUgNjIuNTkzNzUgOS42MjUgNjUuMTQwNjI1IApRIDEwLjg5MDYyNSA2OC41NjI1IDE0LjA3ODEyNSA3MC42NzE4NzUgClEgMTcuMjgxMjUgNzIuNzk2ODc1IDIzLjA0Njg3NSA3Mi43OTY4NzUgClEgMjYuNzY1NjI1IDcyLjc5Njg3NSAzMS4yNSA3MS45MjE4NzUgCkwgMjkuOTM3NSA2NC4yNjU2MjUgClEgMjcuMjAzMTI1IDY0Ljc1IDI0Ljc1IDY0Ljc1IApRIDIwLjc1IDY0Ljc1IDE5LjA5Mzc1IDYzLjAzMTI1IApRIDE3LjQzNzUgNjEuMzI4MTI1IDE3LjQzNzUgNTYuNjQwNjI1IApMIDE3LjQzNzUgNTEuODU5Mzc1IApMIDI3LjU0Njg3NSA1MS44NTkzNzUgCkwgMjcuNTQ2ODc1IDQ1LjAxNTYyNSAKTCAxNy40Mzc1IDQ1LjAxNTYyNSAKTCAxNy40Mzc1IDAgCnoKIiBpZD0iQXJpYWxNVC0xMDIiPjwvcGF0aD4KICAgICAgPHBhdGggZD0iTSA0MC4yMzQzNzUgMCAKTCA0MC4yMzQzNzUgNi41NDY4NzUgClEgMzUuMjk2ODc1IC0xLjE3MTg3NSAyNS43MzQzNzUgLTEuMTcxODc1IApRIDE5LjUzMTI1IC0xLjE3MTg3NSAxNC4zMjgxMjUgMi4yNSAKUSA5LjEyNSA1LjY3MTg3NSA2LjI2NTYyNSAxMS43OTY4NzUgClEgMy40MjE4NzUgMTcuOTIxODc1IDMuNDIxODc1IDI1Ljg3NSAKUSAzLjQyMTg3NSAzMy42NDA2MjUgNiAzOS45Njg3NSAKUSA4LjU5Mzc1IDQ2LjI5Njg3NSAxMy43NjU2MjUgNDkuNjU2MjUgClEgMTguOTUzMTI1IDUzLjAzMTI1IDI1LjM0Mzc1IDUzLjAzMTI1IApRIDMwLjAzMTI1IDUzLjAzMTI1IDMzLjY4NzUgNTEuMDQ2ODc1IApRIDM3LjM1OTM3NSA0OS4wNzgxMjUgMzkuNjU2MjUgNDUuOTA2MjUgCkwgMzkuNjU2MjUgNzEuNTc4MTI1IApMIDQ4LjM5MDYyNSA3MS41NzgxMjUgCkwgNDguMzkwNjI1IDAgCnoKTSAxMi40NTMxMjUgMjUuODc1IApRIDEyLjQ1MzEyNSAxNS45MjE4NzUgMTYuNjQwNjI1IDEwLjk4NDM3NSAKUSAyMC44NDM3NSA2LjA2MjUgMjYuNTYyNSA2LjA2MjUgClEgMzIuMzI4MTI1IDYuMDYyNSAzNi4zNDM3NSAxMC43NjU2MjUgClEgNDAuMzc1IDE1LjQ4NDM3NSA0MC4zNzUgMjUuMTQwNjI1IApRIDQwLjM3NSAzNS43OTY4NzUgMzYuMjY1NjI1IDQwLjc2NTYyNSAKUSAzMi4xNzE4NzUgNDUuNzUgMjYuMTcxODc1IDQ1Ljc1IApRIDIwLjMxMjUgNDUuNzUgMTYuMzc1IDQwLjk2ODc1IApRIDEyLjQ1MzEyNSAzNi4xODc1IDEyLjQ1MzEyNSAyNS44NzUgCnoKIiBpZD0iQXJpYWxNVC0xMDAiPjwvcGF0aD4KICAgICAgPHBhdGggZD0iTSA2LjU5Mzc1IC0xOS44NzUgCkwgNi41OTM3NSA1MS44NTkzNzUgCkwgMTQuNTkzNzUgNTEuODU5Mzc1IApMIDE0LjU5Mzc1IDQ1LjEyNSAKUSAxNy40Mzc1IDQ5LjA3ODEyNSAyMSA1MS4wNDY4NzUgClEgMjQuNTYyNSA1My4wMzEyNSAyOS42NDA2MjUgNTMuMDMxMjUgClEgMzYuMjgxMjUgNTMuMDMxMjUgNDEuMzU5Mzc1IDQ5LjYwOTM3NSAKUSA0Ni40Mzc1IDQ2LjE4NzUgNDkuMDE1NjI1IDM5Ljk1MzEyNSAKUSA1MS42MDkzNzUgMzMuNzM0Mzc1IDUxLjYwOTM3NSAyNi4zMTI1IApRIDUxLjYwOTM3NSAxOC4zNTkzNzUgNDguNzUgMTEuOTg0Mzc1IApRIDQ1LjkwNjI1IDUuNjA5Mzc1IDQwLjQ1MzEyNSAyLjIxODc1IApRIDM1LjAxNTYyNSAtMS4xNzE4NzUgMjkgLTEuMTcxODc1IApRIDI0LjYwOTM3NSAtMS4xNzE4NzUgMjEuMTA5Mzc1IDAuNjg3NSAKUSAxNy42MjUgMi41NDY4NzUgMTUuMzc1IDUuMzc1IApMIDE1LjM3NSAtMTkuODc1IAp6Ck0gMTQuNTQ2ODc1IDI1LjY0MDYyNSAKUSAxNC41NDY4NzUgMTUuNjI1IDE4LjU5Mzc1IDEwLjg0Mzc1IApRIDIyLjY1NjI1IDYuMDYyNSAyOC40MjE4NzUgNi4wNjI1IApRIDM0LjI4MTI1IDYuMDYyNSAzOC40NTMxMjUgMTEuMDE1NjI1IApRIDQyLjYyNSAxNS45Njg3NSA0Mi42MjUgMjYuMzc1IApRIDQyLjYyNSAzNi4yODEyNSAzOC41NDY4NzUgNDEuMjAzMTI1IApRIDM0LjQ2ODc1IDQ2LjE0MDYyNSAyOC44MTI1IDQ2LjE0MDYyNSAKUSAyMy4xODc1IDQ2LjE0MDYyNSAxOC44NTkzNzUgNDAuODkwNjI1IApRIDE0LjU0Njg3NSAzNS42NDA2MjUgMTQuNTQ2ODc1IDI1LjY0MDYyNSAKegoiIGlkPSJBcmlhbE1ULTExMiI+PC9wYXRoPgogICAgIDwvZGVmcz4KICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTY3Ij48L3VzZT4KICAgICA8dXNlIHg9IjcyLjIxNjc5NyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE3Ij48L3VzZT4KICAgICA8dXNlIHg9IjEyNy44MzIwMzEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOSI+PC91c2U+CiAgICAgPHVzZSB4PSIyMTEuMTMyODEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTciPjwvdXNlPgogICAgIDx1c2UgeD0iMjY2Ljc0ODA0NyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA4Ij48L3VzZT4KICAgICA8dXNlIHg9IjI4OC45NjQ4NDQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTk3Ij48L3VzZT4KICAgICA8dXNlIHg9IjM0NC41ODAwNzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNiI+PC91c2U+CiAgICAgPHVzZSB4PSIzNzIuMzYzMjgxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDUiPjwvdXNlPgogICAgIDx1c2UgeD0iMzk0LjU4MDA3OCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE4Ij48L3VzZT4KICAgICA8dXNlIHg9IjQ0NC41ODAwNzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgPHVzZSB4PSI1MDAuMTk1MzEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICAgPHVzZSB4PSI1MjcuOTc4NTE2IiB4bGluazpocmVmPSIjQXJpYWxNVC04MiI+PC91c2U+CiAgICAgPHVzZSB4PSI2MDAuMTk1MzEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgIDx1c2UgeD0iNjU1LjgxMDU0NyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE2Ij48L3VzZT4KICAgICA8dXNlIHg9IjY4My41OTM3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE3Ij48L3VzZT4KICAgICA8dXNlIHg9IjczOS4yMDg5ODQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNCI+PC91c2U+CiAgICAgPHVzZSB4PSI3NzIuNTA5NzY2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTAiPjwvdXNlPgogICAgIDx1c2UgeD0iODI4LjEyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE1Ij48L3VzZT4KICAgICA8dXNlIHg9Ijg3OC4xMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgICA8dXNlIHg9IjkwNS45MDgyMDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMSI+PC91c2U+CiAgICAgPHVzZSB4PSI5NjEuNTIzNDM4IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTgiPjwvdXNlPgogICAgIDx1c2UgeD0iMTAxMS41MjM0MzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgPHVzZSB4PSIxMDY3LjEzODY3MiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICA8dXNlIHg9IjExMDAuNDM5NDUzIiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICAgPHVzZSB4PSIxMTI2LjQ3MjY1NiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtODQiPjwvdXNlPgogICAgIDx1c2UgeD0iMTE4My44MDY2NDEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwNSI+PC91c2U+CiAgICAgPHVzZSB4PSIxMjA2LjAyMzQzOCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA5Ij48L3VzZT4KICAgICA8dXNlIHg9IjEyODkuMzI0MjE5IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgIDx1c2UgeD0iMTM0NC45Mzk0NTMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgICA8dXNlIHg9IjEzNzIuNzIyNjU2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDIiPjwvdXNlPgogICAgIDx1c2UgeD0iMTQwMC41MDU4NTkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMSI+PC91c2U+CiAgICAgPHVzZSB4PSIxNDU2LjEyMTA5NCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICA8dXNlIHg9IjE0ODkuNDIxODc1IiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICAgPHVzZSB4PSIxNTE3LjIwNTA3OCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAwIj48L3VzZT4KICAgICA8dXNlIHg9IjE1NzIuODIwMzEyIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDUiPjwvdXNlPgogICAgIDx1c2UgeD0iMTU5NS4wMzcxMDkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMiI+PC91c2U+CiAgICAgPHVzZSB4PSIxNjIxLjA3MDMxMiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAyIj48L3VzZT4KICAgICA8dXNlIHg9IjE2NDguODUzNTE2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgIDx1c2UgeD0iMTcwNC40Njg3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICA8dXNlIHg9IjE3MzcuNzY5NTMxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgIDx1c2UgeD0iMTc5My4zODQ3NjYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMCI+PC91c2U+CiAgICAgPHVzZSB4PSIxODQ5IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTYiPjwvdXNlPgogICAgIDx1c2UgeD0iMTg3Ni43ODMyMDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgICA8dXNlIHg9IjE5MDQuNTY2NDA2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTIiPjwvdXNlPgogICAgIDx1c2UgeD0iMTk2MC4xODE2NDEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgPHVzZSB4PSIyMDE1Ljc5Njg3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICA8dXNlIHg9IjIwNDkuMDk3NjU2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDkiPjwvdXNlPgogICAgIDx1c2UgeD0iMjEzMi4zOTg0MzgiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMCI+PC91c2U+CiAgICAgPHVzZSB4PSIyMTg4LjAxMzY3MiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTExIj48L3VzZT4KICAgICA8dXNlIHg9IjIyNDMuNjI4OTA2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTUiPjwvdXNlPgogICAgPC9nPgogICA8L2c+CiAgIDxnIGlkPSJsZWdlbmRfMSI+CiAgICA8ZyBpZD0icGF0Y2hfNyI+CiAgICAgPHBhdGggZD0iTSA0My40MjIxODcgMTAyLjQ4NzUgCkwgMTYyLjUzOTA2MiAxMDIuNDg3NSAKUSAxNjQuOTM5MDYzIDEwMi40ODc1IDE2NC45MzkwNjMgMTAwLjA4NzUgCkwgMTY0LjkzOTA2MyAzMy4yNDc1IApRIDE2NC45MzkwNjMgMzAuODQ3NSAxNjIuNTM5MDYyIDMwLjg0NzUgCkwgNDMuNDIyMTg3IDMwLjg0NzUgClEgNDEuMDIyMTg4IDMwLjg0NzUgNDEuMDIyMTg4IDMzLjI0NzUgCkwgNDEuMDIyMTg4IDEwMC4wODc1IApRIDQxLjAyMjE4OCAxMDIuNDg3NSA0My40MjIxODcgMTAyLjQ4NzUgCnoKIiBzdHlsZT0iZmlsbDojZWFlYWYyO29wYWNpdHk6MC44O3N0cm9rZTojY2NjY2NjO3N0cm9rZS1saW5lam9pbjptaXRlcjtzdHJva2Utd2lkdGg6MC4zOyI+PC9wYXRoPgogICAgPC9nPgogICAgPGcgaWQ9ImxpbmUyZF8zOSI+CiAgICAgPHBhdGggZD0iTSA0NS44MjIxODcgNDAuMDcyNSAKTCA2OS44MjIxODcgNDAuMDcyNSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojNGM3MmIwO3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICAgPC9nPgogICAgPGcgaWQ9ImxpbmUyZF80MCI+PC9nPgogICAgPGcgaWQ9InRleHRfMjEiPgogICAgIDwhLS0gcGVybW5vOiAxMDEzNyAtLT4KICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNzkuNDIyMTg4IDQ0LjI3MjUpc2NhbGUoMC4xMiAtMC4xMikiPgogICAgICA8ZGVmcz4KICAgICAgIDxwYXRoIGQ9Ik0gOS4wMzEyNSA0MS44NDM3NSAKTCA5LjAzMTI1IDUxLjg1OTM3NSAKTCAxOS4wNDY4NzUgNTEuODU5Mzc1IApMIDE5LjA0Njg3NSA0MS44NDM3NSAKegpNIDkuMDMxMjUgMCAKTCA5LjAzMTI1IDEwLjAxNTYyNSAKTCAxOS4wNDY4NzUgMTAuMDE1NjI1IApMIDE5LjA0Njg3NSAwIAp6CiIgaWQ9IkFyaWFsTVQtNTgiPjwvcGF0aD4KICAgICAgPC9kZWZzPgogICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMiI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTQ0LjUzMTI1IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDkiPjwvdXNlPgogICAgICA8dXNlIHg9IjIyNy44MzIwMzEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjgzLjQ0NzI2NiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTExIj48L3VzZT4KICAgICAgPHVzZSB4PSIzMzkuMDYyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTgiPjwvdXNlPgogICAgICA8dXNlIHg9IjM2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgICAgPHVzZSB4PSIzOTQuNjI4OTA2IiB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgIDx1c2UgeD0iNDUwLjI0NDE0MSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8dXNlIHg9IjUwNS44NTkzNzUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPHVzZSB4PSI1NjEuNDc0NjA5IiB4bGluazpocmVmPSIjQXJpYWxNVC01MSI+PC91c2U+CiAgICAgIDx1c2UgeD0iNjE3LjA4OTg0NCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTUiPjwvdXNlPgogICAgIDwvZz4KICAgIDwvZz4KICAgIDxnIGlkPSJsaW5lMmRfNDEiPgogICAgIDxwYXRoIGQ9Ik0gNDUuODIyMTg3IDU3LjA4MjUgCkwgNjkuODIyMTg3IDU3LjA4MjUgCiIgc3R5bGU9ImZpbGw6bm9uZTtzdHJva2U6IzU1YTg2ODtzdHJva2UtbGluZWNhcDpyb3VuZDtzdHJva2Utd2lkdGg6MS43NTsiPjwvcGF0aD4KICAgIDwvZz4KICAgIDxnIGlkPSJsaW5lMmRfNDIiPjwvZz4KICAgIDxnIGlkPSJ0ZXh0XzIyIj4KICAgICA8IS0tIHBlcm1ubzogMTAwNTEgLS0+CiAgICAgPGcgc3R5bGU9ImZpbGw6IzI2MjYyNjsiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDc5LjQyMjE4OCA2MS4yODI1KXNjYWxlKDAuMTIgLTAuMTIpIj4KICAgICAgPHVzZSB4bGluazpocmVmPSIjQXJpYWxNVC0xMTIiPjwvdXNlPgogICAgICA8dXNlIHg9IjU1LjYxNTIzNCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTAxIj48L3VzZT4KICAgICAgPHVzZSB4PSIxMTEuMjMwNDY5IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTQiPjwvdXNlPgogICAgICA8dXNlIHg9IjE0NC41MzEyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTA5Ij48L3VzZT4KICAgICAgPHVzZSB4PSIyMjcuODMyMDMxIiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTAiPjwvdXNlPgogICAgICA8dXNlIHg9IjI4My40NDcyNjYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMzM5LjA2MjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTU4Ij48L3VzZT4KICAgICAgPHVzZSB4PSIzNjYuODQ1NzAzIiB4bGluazpocmVmPSIjQXJpYWxNVC0zMiI+PC91c2U+CiAgICAgIDx1c2UgeD0iMzk0LjYyODkwNiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDkiPjwvdXNlPgogICAgICA8dXNlIHg9IjQ1MC4yNDQxNDEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPHVzZSB4PSI1MDUuODU5Mzc1IiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTYxLjQ3NDYwOSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTMiPjwvdXNlPgogICAgICA8dXNlIHg9IjYxNy4wODk4NDQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyBpZD0ibGluZTJkXzQzIj4KICAgICA8cGF0aCBkPSJNIDQ1LjgyMjE4NyA3NC4wOTI1IApMIDY5LjgyMjE4NyA3NC4wOTI1IAoiIHN0eWxlPSJmaWxsOm5vbmU7c3Ryb2tlOiNjNDRlNTI7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7c3Ryb2tlLXdpZHRoOjEuNzU7Ij48L3BhdGg+CiAgICA8L2c+CiAgICA8ZyBpZD0ibGluZTJkXzQ0Ij48L2c+CiAgICA8ZyBpZD0idGV4dF8yMyI+CiAgICAgPCEtLSBwZXJtbm86IDEwMDU3IC0tPgogICAgIDxnIHN0eWxlPSJmaWxsOiMyNjI2MjY7IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSg3OS40MjIxODggNzguMjkyNSlzY2FsZSgwLjEyIC0wLjEyKSI+CiAgICAgIDx1c2UgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEyIj48L3VzZT4KICAgICAgPHVzZSB4PSI1NS42MTUyMzQiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwMSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTExLjIzMDQ2OSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTE0Ij48L3VzZT4KICAgICAgPHVzZSB4PSIxNDQuNTMxMjUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTEwOSI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjI3LjgzMjAzMSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTEwIj48L3VzZT4KICAgICAgPHVzZSB4PSIyODMuNDQ3MjY2IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMTEiPjwvdXNlPgogICAgICA8dXNlIHg9IjMzOS4wNjI1IiB4bGluazpocmVmPSIjQXJpYWxNVC01OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMzY2Ljg0NTcwMyIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMzIiPjwvdXNlPgogICAgICA8dXNlIHg9IjM5NC42Mjg5MDYiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ5Ij48L3VzZT4KICAgICAgPHVzZSB4PSI0NTAuMjQ0MTQxIiB4bGluazpocmVmPSIjQXJpYWxNVC00OCI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTA1Ljg1OTM3NSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8dXNlIHg9IjU2MS40NzQ2MDkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTUzIj48L3VzZT4KICAgICAgPHVzZSB4PSI2MTcuMDg5ODQ0IiB4bGluazpocmVmPSIjQXJpYWxNVC01NSI+PC91c2U+CiAgICAgPC9nPgogICAgPC9nPgogICAgPGcgaWQ9ImxpbmUyZF80NSI+CiAgICAgPHBhdGggZD0iTSA0NS44MjIxODcgOTEuMTAyNSAKTCA2OS44MjIxODcgOTEuMTAyNSAKIiBzdHlsZT0iZmlsbDpub25lO3N0cm9rZTojODE3MmIyO3N0cm9rZS1saW5lY2FwOnJvdW5kO3N0cm9rZS13aWR0aDoxLjc1OyI+PC9wYXRoPgogICAgPC9nPgogICAgPGcgaWQ9ImxpbmUyZF80NiI+PC9nPgogICAgPGcgaWQ9InRleHRfMjQiPgogICAgIDwhLS0gcGVybW5vOiAxMDAyOCAtLT4KICAgICA8ZyBzdHlsZT0iZmlsbDojMjYyNjI2OyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNzkuNDIyMTg4IDk1LjMwMjUpc2NhbGUoMC4xMiAtMC4xMikiPgogICAgICA8dXNlIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMiI+PC91c2U+CiAgICAgIDx1c2UgeD0iNTUuNjE1MjM0IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDEiPjwvdXNlPgogICAgICA8dXNlIHg9IjExMS4yMzA0NjkiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExNCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMTQ0LjUzMTI1IiB4bGluazpocmVmPSIjQXJpYWxNVC0xMDkiPjwvdXNlPgogICAgICA8dXNlIHg9IjIyNy44MzIwMzEiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTExMCI+PC91c2U+CiAgICAgIDx1c2UgeD0iMjgzLjQ0NzI2NiIgeGxpbms6aHJlZj0iI0FyaWFsTVQtMTExIj48L3VzZT4KICAgICAgPHVzZSB4PSIzMzkuMDYyNSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTgiPjwvdXNlPgogICAgICA8dXNlIHg9IjM2Ni44NDU3MDMiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTMyIj48L3VzZT4KICAgICAgPHVzZSB4PSIzOTQuNjI4OTA2IiB4bGluazpocmVmPSIjQXJpYWxNVC00OSI+PC91c2U+CiAgICAgIDx1c2UgeD0iNDUwLjI0NDE0MSIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNDgiPjwvdXNlPgogICAgICA8dXNlIHg9IjUwNS44NTkzNzUiIHhsaW5rOmhyZWY9IiNBcmlhbE1ULTQ4Ij48L3VzZT4KICAgICAgPHVzZSB4PSI1NjEuNDc0NjA5IiB4bGluazpocmVmPSIjQXJpYWxNVC01MCI+PC91c2U+CiAgICAgIDx1c2UgeD0iNjE3LjA4OTg0NCIgeGxpbms6aHJlZj0iI0FyaWFsTVQtNTYiPjwvdXNlPgogICAgIDwvZz4KICAgIDwvZz4KICAgPC9nPgogIDwvZz4KIDwvZz4KIDxkZWZzPgogIDxjbGlwcGF0aCBpZD0icDdkNzcxMjBlMjAiPgogICA8cmVjdCBoZWlnaHQ9IjMyNi4xNiIgd2lkdGg9IjU1OCIgeD0iMzUuMDIyMTg4IiB5PSIyNC44NDc1Ij48L3JlY3Q+CiAgPC9jbGlwcGF0aD4KIDwvZGVmcz4KPC9zdmc+)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

##  {#section-3}

The End.

</div>

</div>

<div class="jp-Cell-inputWrapper" markdown="1">

<div class="jp-InputPrompt jp-InputArea-prompt" markdown="1">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
markdown="1" mime-type="text/markdown">

------------------------------------------------------------------------

</div>

</div>
