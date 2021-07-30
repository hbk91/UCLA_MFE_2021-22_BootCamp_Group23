<div class="cell markdown" markdown="1">

<h2><p align=center> Assignment - Module 3 </p></h2>
<h3><p align=center> 30 July 2021 </p></h3>
<h3><p align=center> Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu </p></h3>

<br /><br />

</div>

<div class="cell code" markdown="1" execution_count="1">

~~~ python
# Importing Libraries

import pandas as pd
import numpy as np
from pprint import pprint
from functools import reduce
import dateparser
import matplotlib.pyplot as plt
plt.style.use('seaborn')
~~~

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q1. List Comprehension: First generate a list using the range(20) function. Next, create a second list that calculates 0.5 ⋅ *n* ⋅ (*n*+1) for each item *n* in the first list. Solve this using a while loop and also the list comprehension method. Check if the outputs match for the two methods. {#q1-list-comprehension-first-generate-a-list-using-the-range20-function-next-create-a-second-list-that-calculates-05-cdot-n-cdot-n1-for-each-item-n-in-the-first-list-solve-this-using-a-while-loop-and-also-the-list-comprehension-method-check-if-the-outputs-match-for-the-two-methods}

</div>

<div class="cell markdown" markdown="1">

#### Answer 1 {#answer-1}

</div>

<div class="cell code" markdown="1" execution_count="2">

~~~ python
# While Loop Method

input_list = range(20)
ans_q1_whileLoop = []
i = 0
while i<len(input_list):
    ans_q1_whileLoop.append(0.5*input_list[i]*(input_list[i]+1))
    i = i+1

print('The Answer:\n\n {}'.format(ans_q1_whileLoop))
print('\nThe Length of the list is: {}'.format(len(ans_q1_whileLoop)))
~~~

<div class="output stream stdout" markdown="1">

    The Answer:

     [0.0, 1.0, 3.0, 6.0, 10.0, 15.0, 21.0, 28.0, 36.0, 45.0, 55.0, 66.0, 78.0, 91.0, 105.0, 120.0, 136.0, 153.0, 171.0, 190.0]

    The Length of the list is: 20

</div>

</div>

<div class="cell code" markdown="1" execution_count="3">

~~~ python
# List Comprehension Method

input_list = range(20)
ans_q1_lc = [0.5*n*(n+1) for n in input_list]

print('The Answer:\n\n {}'.format(ans_q1_lc))
print('\nThe Length of the list is: {}'.format(len(ans_q1_lc)))
~~~

<div class="output stream stdout" markdown="1">

    The Answer:

     [0.0, 1.0, 3.0, 6.0, 10.0, 15.0, 21.0, 28.0, 36.0, 45.0, 55.0, 66.0, 78.0, 91.0, 105.0, 120.0, 136.0, 153.0, 171.0, 190.0]

    The Length of the list is: 20

</div>

</div>

<div class="cell code" markdown="1" execution_count="4">

~~~ python
# Check if the two lists are equal

print('Check if the lists are equal: {}'.format(ans_q1_whileLoop == ans_q1_lc))
~~~

<div class="output stream stdout" markdown="1">

    Check if the lists are equal:True

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q2. Lambda function: Create a numpy array of integers from 1 to 50. Use the lambda function to compute *x*<sup>3</sup> + *x*<sup>2</sup> + *x* + 1 for each element *x* of the array. Compare your output using the list comprehension method. {#q2-lambda-function-create-a-numpy-array-of-integers-from-1-to-50-use-the-lambda-function-to-compute-x3x2x1-for-each-element-x-of-the-array-compare-your-output-using-the-list-comprehension-method}

</div>

<div class="cell code" markdown="1" execution_count="5">

~~~ python
# A General Purpose Function for calculating sum of a geometric power series where a = 1 & r = pow 

def sum_geom_pow(elem, pow): return sum([elem**p for p in range(pow+1)])
~~~

</div>

<div class="cell code" markdown="1" execution_count="6">

~~~ python
# Lambda Function Method

input_arr = np.arange(50)+1
max_pow = 3

cubic_func = lambda x: sum_geom_pow(x, max_pow)
ans_q2_lambda = cubic_func(input_arr)
print('The Answer is:\n')
pprint(ans_q2_lambda)
~~~

<div class="output stream stdout" markdown="1">

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

<div class="cell code" markdown="1" execution_count="7">

~~~ python
# List Comprehension Method

input_arr = np.arange(50)+1
max_pow = 3

ans_q2_lc = np.array([sum_geom_pow(x, max_pow) for x in input_arr])
print('The Answer is:\n')
pprint(ans_q2_lc)
~~~

<div class="output stream stdout" markdown="1">

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

<div class="cell code" markdown="1" execution_count="8">

~~~ python
# Check if the two outputs are same

print('Check if the arrays are equal: {}'.format((ans_q2_lambda == ans_q2_lc).all()))
~~~

<div class="output stream stdout" markdown="1">

    Check if the arrays are equal: True

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q3. For Loop: Create a list with range(50). Return *x*<sup>3</sup> + *x*<sup>2</sup> + *x* + 1 for every element *x* in the list with an exception that for the last 5 elements return *x*<sup>4</sup> + *x*<sup>3</sup> + *x*<sup>2</sup> + *x* + 1. Use a for loop to do this operation. Hint: You might want to read up on "enumerate" and how that can be used with a for loop. {#q3-for-loop-create-a-list-with-range50-return-x3x2x1-for-every-element-x-in-the-list-with-an-exception-that-for-the-last-5-elements-return-x4x3x2x1-use-a-for-loop-to-do-this-operation-hint-you-might-want-to-read-up-on-enumerate-and-how-that-can-be-used-with-a-for-loop}

</div>

<div class="cell markdown" markdown="1">

#### Answer 3 {#answer-3}

</div>

<div class="cell code" markdown="1" execution_count="9">

~~~ python
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
~~~

<div class="output stream stdout" markdown="1">

    The Answer: 

    [1, 4, 15, 40, 85, 156, 259, 400, 585, 820, 1111, 1464, 1885, 2380, 2955, 3616, 4369, 5220, 6175, 7240, 8421, 9724, 11155, 12720, 14425, 16276, 18279, 20440, 22765, 25260, 27931, 30784, 33825, 37060, 40495, 44136, 47989, 52060, 56355, 60880, 65641, 70644, 75895, 81400, 87165, 4193821, 4576955, 4985761, 5421361, 5884901]

</div>

</div>

<div class="cell code" markdown="1" execution_count="10">

~~~ python
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
~~~

<div class="output stream stdout" markdown="1">

    The Answer: 

    [1, 4, 15, 40, 85, 156, 259, 400, 585, 820, 1111, 1464, 1885, 2380, 2955, 3616, 4369, 5220, 6175, 7240, 8421, 9724, 11155, 12720, 14425, 16276, 18279, 20440, 22765, 25260, 27931, 30784, 33825, 37060, 40495, 44136, 47989, 52060, 56355, 60880, 65641, 70644, 75895, 81400, 87165, 4193821, 4576955, 4985761, 5421361, 5884901]

</div>

</div>

<div class="cell code" markdown="1" execution_count="11">

~~~ python
print(ans_q3_forLoop == ans_q3_lc)
~~~

<div class="output stream stdout" markdown="1">

    True

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q4. List comprehension with logical statements: First generate a list using the range(30) function. Next, create a second list that creates elements based on the logic below. Hint: You can do this by including an if statement inside your list comprehension. {#q4-list-comprehension-with-logical-statements-first-generate-a-list-using-the-range30-function-next-create-a-second-list-that-creates-elements-based-on-the-logic-below-hint-you-can-do-this-by-including-an-if-statement-inside-your-list-comprehension}

$$
f(x)=\\begin{cases}
x^2;\\quad \\text{if x is even}\\\\
x^3;\\quad \\text{if x is odd}
\\end{cases}
$$

</div>

<div class="cell markdown" markdown="1">

### Answer 4: {#answer-4}

</div>

<div class="cell code" markdown="1" execution_count="12">

~~~ python
input_list = range(30)

ans_q4 = [x**2 if x % 2 == 0 else x**3 for x in input_list]

print('The Answer: \n\n{}'.format(ans_q4))
~~~

<div class="output stream stdout" markdown="1">

    The Answer: 

    [0, 1, 4, 27, 16, 125, 36, 343, 64, 729, 100, 1331, 144, 2197, 196, 3375, 256, 4913, 324, 6859, 400, 9261, 484, 12167, 576, 15625, 676, 19683, 784, 24389]

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q5. Fibonacci sequence: Construct a function "fibonacci" that takes in the required variable integer "*n*" and returns the *n*<sub>*t**h*</sub> term in a Fibonacci sequence (1,1,2,3,5,...). For example, if your call your function and pass in the argument n = 6, i.e fibonacci(n=6) it should return the value 8. You can use a for or a while loop inside your function. Print the function output for n=30, 50, and 100. {#q5-fibonacci-sequence-construct-a-function-fibonacci-that-takes-in-the-required-variable-integer-n-and-returns-the-n_th-term-in-a-fibonacci-sequence-11235-for-example-if-your-call-your-function-and-pass-in-the-argument-n--6-ie-fibonaccin6-it-should-return-the-value-8-you-can-use-a-for-or-a-while-loop-inside-your-function-print-the-function-output-for-n30-50-and-100}

</div>

<div class="cell markdown" markdown="1">

#### Answer 5 {#answer-5}

</div>

<div class="cell code" markdown="1" execution_count="13">

~~~ python
# Method 1 of generating the nth element of the Fibonacci series

pos_list = [6, 30, 50, 100]

def get_fib_nth_elem_m1(elem_pos=0):
    if isinstance(elem_pos, int) and elem_pos >= 0:
        return reduce(lambda x, _:(x[1],x[0]+x[1]), range(elem_pos), (0,1))[0]
    else:
        raise TypeError('Element Position entered is not an integer greater than or equal to 0')

for pos in pos_list:
   print('Fibonacci Series Value at position {}: {:,}\n'.format(pos, get_fib_nth_elem_m1(pos)))
~~~

<div class="output stream stdout" markdown="1">

    Fibonacci Series Value at position 6: 8

    Fibonacci Series Value at position 30: 832,040

    Fibonacci Series Value at position 50: 12,586,269,025

    Fibonacci Series Value at position 100: 354,224,848,179,261,915,075

</div>

</div>

<div class="cell code" markdown="1" execution_count="14" tags="[]">

~~~ python
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
~~~

<div class="output stream stdout" markdown="1">

    Fibonacci Series Value at position 6: 8

    Fibonacci Series Value at position 30: 832,040

    Fibonacci Series Value at position 50: 12,586,269,025

    Fibonacci Series Value at position 100: 354,224,848,179,261,915,075

</div>

</div>

<div class="cell code" markdown="1" execution_count="15">

~~~ python
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
~~~

<div class="output stream stdout" markdown="1">

    Fibonacci Series Value at position 6: 8

    Fibonacci Series Value at position 30: 832,040

    Fibonacci Series Value at position 50: 12,586,269,025

    Fibonacci Series Value at position 100: 354,224,848,179,261,915,075

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q6. Net Present Value: Code up a function that computes the net present value of a stream of cash-flows and call this function NPV. The function will take three inputs - cash-flows, dates, and interest rate (constant). We will use the formula specified below to compute the NPV of a stream of cash-flows on specific dates. The time periods *t*<sub>1</sub>, *t*<sub>2</sub>, .., *t*<sub>*N*</sub> are computed as differences from first date. Make sure you annualize the difference in days (convert them to years). Check out this wikipedia link if you want to read up some more (<https://en.wikipedia.org/wiki/Net_present_value>). {#q6-net-present-value-code-up-a-function-that-computes-the-net-present-value-of-a-stream-of-cash-flows-and-call-this-function-npv-the-function-will-take-three-inputs---cash-flows-dates-and-interest-rate-constant-we-will-use-the-formula-specified-below-to-compute-the-npv-of-a-stream-of-cash-flows-on-specific-dates-the-time-periods-t_1t_2t_n-are-computed-as-differences-from-first-date-make-sure-you-annualize-the-difference-in-days-convert-them-to-years-check-out-this-wikipedia-link-if-you-want-to-read-up-some-more-httpsenwikipediaorgwikinet_present_value}

$$NPV(CF) = CF_0 + \\frac{CF_1}{(1+r)^{t_1}} + \\frac{CF_2}{(1+r)^{t_2}} + ... \\frac{CF_N}{(1+r)^{t_N}}$$

**Run this function for the following input:**

Compute : NPV(CF=\[-100,50,40,30\],date=\[01-Jan-2020,31-Mar-2021,30-Jun-2021,31-Dec-2024\],*r*=0.05)

</div>

<div class="cell markdown" markdown="1">

#### Answer 6:<br> {#answer-6-}

#### Notes on Parsing Dates: {#notes-on-parsing-dates}

-   Date Formats are available
    [here](https://docs.python.org/2/library/datetime.html#strftime-and-strptime-behavior)
    for parsing string as dates
-   [dateparser library](https://dateparser.readthedocs.io/en/latest/).
    It can even parse dates even without providing a date format
-   More date formats can be supplied as additional list elements in
    `date_formats` argument of `dateparser.parse`

</div>

<div class="cell code" markdown="1" execution_count="16">

~~~ python
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
~~~

</div>

<div class="cell code" markdown="1" execution_count="17">

~~~ python
cash_flows = [-100, 50, 40, 30]
cash_flow_dates = ['01-Jan-2020', '31-Mar-2021', '30-Jun-2021', '31-Dec-2024']
interest_rate = 0.05

print('NPV of the cash flows: {:,.2f}'.format(NPV(cash_flows, cash_flow_dates, interest_rate)))
~~~

<div class="output stream stdout" markdown="1">

    NPV of the cash flows: 7.74

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q7. Pandas .rolling() is a very useful function to know (check out the doc string of pandas.Series.rolling for a better understanding of what the function does). In this problem, we will calculate the 1-year rolling sum of returns for the data in stock_data.csv file. Clean the data (remove strings and drop NaN values). Use the pandas rolling function (window=12) to calculate the sum of 1-year returns. Add this column to the original dataframe. {#q7-pandas-rolling-is-a-very-useful-function-to-know-check-out-the-doc-string-of-pandasseriesrolling-for-a-better-understanding-of-what-the-function-does-in-this-problem-we-will-calculate-the-1-year-rolling-sum-of-returns-for-the-data-in-stock_datacsv-file-clean-the-data-remove-strings-and-drop-nan-values-use-the-pandas-rolling-function-window12-to-calculate-the-sum-of-1-year-returns-add-this-column-to-the-original-dataframe}

</div>

<div class="cell markdown" markdown="1">

#### Answer 7 {#answer-7}

</div>

<div class="cell code" markdown="1" execution_count="18">

~~~ python
# Setting the Input File Path

input_file_folder = 'Data'          # Folder Name within current directory where the file is stored
input_file_name = 'stock_data.csv'  # Name of the File
cwd = os.getcwd() 
input_file_path = os.path.join(cwd, input_file_folder, input_file_name)
~~~

</div>

<div class="cell markdown" markdown="1">

-   More details on dtpyes & converters used below while reading data is
    available [here](https://pbpython.com/pandas_dtypes.html)
-   In the above link, specifying dtypes vs. specifying converters while
    reading data is quite useful

</div>

<div class="cell code" markdown="1" execution_count="19">

~~~ python
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
~~~

<div class="output execute_result" markdown="1" execution_count="19">

    (2913, 6)

</div>

</div>

<div class="cell code" markdown="1" execution_count="20">

~~~ python
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
~~~

<div class="output stream stdout" markdown="1">

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

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q8. Combining Pandas apply and lambda functions: Load and clean the stock_data.csv file. Compute the market cap by multiplying the price and outstanding shares. You need to segregate PERMNOs into large-cap, mid-cap, and small-cap stocks. First, you have to write a function that takes in a value *x* (market cap) as an input. For segregating use the following criteria mentioned below. Use the pandas apply along with lambda function, to pass the function pass you have just coded up. {#q8-combining-pandas-apply-and-lambda-functions-load-and-clean-the-stock_datacsv-file-compute-the-market-cap-by-multiplying-the-price-and-outstanding-shares-you-need-to-segregate-permnos-into-large-cap-mid-cap-and-small-cap-stocks-first-you-have-to-write-a-function-that-takes-in-a-value-x-market-cap-as-an-input-for-segregating-use-the-following-criteria-mentioned-below-use-the-pandas-apply-along-with-lambda-function-to-pass-the-function-pass-you-have-just-coded-up}

$$
f(x)=\\begin{cases}
\\text{small cap}    ,\\quad  \\text{if x} &lt; 100000\\\\
\\text{mid cap}      ,\\quad  100000 \\le \\text{if x} &lt; 1000000\\\\
\\text{large cap}    ,\\quad  \\text{if x} \\ge  1000000
\\end{cases}
$$

</div>

<div class="cell markdown" markdown="1">

#### Answer 8 {#answer-8}

</div>

<div class="cell code" markdown="1" execution_count="21">

~~~ python
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
~~~

<div class="output stream stdout" markdown="1">

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

<div class="cell markdown" markdown="1">

#### Q9.Plot and Subplots: For the 4 PERMNOs - (10137, 10051, 10057, 10028), calculate the cumulative sum of returns and plot them in a 4-by-4 sub plot. Also, plot all their cumulative sum of returns in one plot. Hint: To compute the cumulative sum, you can use the .cumsum() function of pandas. You can also use the .plot() function of pandas dataframe instead of using matplotlib's plt function. {#q9plot-and-subplots-for-the-4-permnos---10137-10051-10057-10028-calculate-the-cumulative-sum-of-returns-and-plot-them-in-a-4-by-4-sub-plot-also-plot-all-their-cumulative-sum-of-returns-in-one-plot-hint-to-compute-the-cumulative-sum-you-can-use-the-cumsum-function-of-pandas-you-can-also-use-the-plot-function-of-pandas-dataframe-instead-of-using-matplotlibs-plt-function}

</div>

<div class="cell markdown" markdown="1">

#### Answer 9 {#answer-9}

</div>

<div class="cell code" markdown="1" execution_count="24">

~~~ python
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
~~~

<div class="output display_data" markdown="1">

![](0fbd205ca738a1b9e32081dc59353acd5830c2a8.png)

</div>

</div>

<div class="cell code" markdown="1" execution_count="25">

~~~ python
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
~~~

<div class="output display_data" markdown="1">

![](bb5cece72b04eb75172a3f00358d6c2e81239fb9.png)

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:1px solid black">

</div>

<div class="cell markdown" markdown="1">

<h2><p align=center>The End.</p></h2>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:1px solid black">

</div>
