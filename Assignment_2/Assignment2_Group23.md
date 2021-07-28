<div class="cell markdown" markdown="1">

<h2><p align=center> Assignment - Module 2 </p></h2>
<h3><p align=center> 27 July 2021 </p></h3>
<h3><p align=center> Group 23: Aman Jindal | Yuhang Jiang | Daniel Gabriel Tan | Qining Liu </p></h3>

<br /><br />

</div>

<div class="cell code" markdown="1" execution_count="1">

~~~ python
import pandas as pd
import numpy as np
import datetime as dt
import os
import re
from pprint import pprint
from functools import reduce
~~~

</div>

<div class="cell markdown" markdown="1">

#### Q1. Pandas Mul Function - Use this dataframe created in the code chunk below. We have three columns with random float values. The goal is to multiply columns 1 and 2 with columns 3. Firstly, notice how running the function (df\[\['col1','col2'\]\]\*df\['col3'\]) returns a matrix of NaN values. Now, use the .mul() function by passing df\[\['col1','col2'\]\].mul(df\['col3'\],axis=0). Notice how we get the same NaN matrix when we change axis=1 instead. {#q1-pandas-mul-function---use-this-dataframe-created-in-the-code-chunk-below-we-have-three-columns-with-random-float-values-the-goal-is-to-multiply-columns-1-and-2-with-columns-3-firstly-notice-how-running-the-function-dfcol1col2dfcol3-returns-a-matrix-of-nan-values-now-use-the-mul-function-by-passing-dfcol1col2muldfcol3axis0-notice-how-we-get-the-same-nan-matrix-when-we-change-axis1-instead}

</div>

<div class="cell code" markdown="1" execution_count="2">

~~~ python
# Creating a dataframe for problem 1
np.random.seed(123)
df = pd.DataFrame() # Creating a blank data-frame
df['col1'] = np.random.rand(10)
df['col2'] = np.random.rand(10)
df['col3'] = np.random.rand(10)
df
~~~

<div class="output execute_result" markdown="1" execution_count="2">

           col1      col2      col3
    0  0.696469  0.343178  0.634401
    1  0.286139  0.729050  0.849432
    2  0.226851  0.438572  0.724455
    3  0.551315  0.059678  0.611024
    4  0.719469  0.398044  0.722443
    5  0.423106  0.737995  0.322959
    6  0.980764  0.182492  0.361789
    7  0.684830  0.175452  0.228263
    8  0.480932  0.531551  0.293714
    9  0.392118  0.531828  0.630976

</div>

</div>

<div class="cell markdown" markdown="1">

#### Answer 1: {#answer-1}

</div>

<div class="cell code" markdown="1" execution_count="3">

~~~ python
df[['col1','col2']]*df['col3']
~~~

<div class="output execute_result" markdown="1" execution_count="3">

       col1  col2   0   1   2   3   4   5   6   7   8   9
    0   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    1   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    2   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    3   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    4   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    5   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    6   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    7   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    8   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    9   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN

</div>

</div>

<div class="cell code" markdown="1" execution_count="4">

~~~ python
df[['col1','col2']].mul(df['col3'],axis=0)
~~~

<div class="output execute_result" markdown="1" execution_count="4">

           col1      col2
    0  0.441841  0.217712
    1  0.243056  0.619278
    2  0.164344  0.317726
    3  0.336866  0.036465
    4  0.519776  0.287564
    5  0.136646  0.238342
    6  0.354829  0.066023
    7  0.156321  0.040049
    8  0.141256  0.156124
    9  0.247417  0.335571

</div>

</div>

<div class="cell code" markdown="1" execution_count="5">

~~~ python
df[['col1','col2']].mul(df['col3'],axis=1)
~~~

<div class="output execute_result" markdown="1" execution_count="5">

       col1  col2   0   1   2   3   4   5   6   7   8   9
    0   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    1   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    2   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    3   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    4   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    5   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    6   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    7   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    8   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN
    9   NaN   NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN NaN

</div>

</div>

<div class="cell markdown" markdown="1">

-   This is happening because when we set axis = 1, pandas tries to
    multiply along the columns. Thus, for each row we have only two
    values (`col1` and `col2`), however there are 10 values from `col3`
    to be multiplied.

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q2. Load CSV data (stock_data.csv) - parse dates using the pd.to_datetime command, read the stock returns as numeric values using the pd.to_numeric command, drop all NaN values using the dropna(), and reset the index. We will be working with this dataframe (unless stated otherwise) for the remainder of the questions below.<br> {#q2-load-csv-data-stock_datacsv---parse-dates-using-the-pdto_datetime-command-read-the-stock-returns-as-numeric-values-using-the-pdto_numeric-command-drop-all-nan-values-using-the-dropna-and-reset-the-index-we-will-be-working-with-this-dataframe-unless-stated-otherwise-for-the-remainder-of-the-questions-below-}

#### Answer 2: {#answer-2}

</div>

<div class="cell code" markdown="1" execution_count="6">

~~~ python
input_file_folder = 'Data' # Folder Name within current directory where the file is stored
input_file_name = 'stock_data.csv' # Name of the File
cwd = os.getcwd() 
input_file_path = os.path.join(cwd, input_file_folder, input_file_name)
~~~

</div>

<div class="cell code" markdown="1" execution_count="7">

~~~ python
# Reading the Data
df = pd.read_csv(filepath_or_buffer=input_file_path, sep=',',header=0)
df.dtypes
~~~

<div class="output execute_result" markdown="1" execution_count="7">

    permno                int64
    company_name         object
    date                 object
    total_returns        object
    price                object
    share_outstanding     int64
    dtype: object

</div>

</div>

<div class="cell code" markdown="1" execution_count="8">

~~~ python
# Converting `total_returns` to numeric, `price` to numeric, `date` to datetime  

df['total_returns'] = pd.to_numeric(df['total_returns'], errors='coerce')
df['price'] = pd.to_numeric(df['price'], errors='coerce')
df['date'] = pd.to_datetime(df['date'], errors='coerce')
df.dtypes
~~~

<div class="output execute_result" markdown="1" execution_count="8">

    permno                        int64
    company_name                 object
    date                 datetime64[ns]
    total_returns               float64
    price                       float64
    share_outstanding             int64
    dtype: object

</div>

</div>

<div class="cell code" markdown="1" execution_count="9">

~~~ python
# Dropping NaN rows and resetting the index

df.dropna(axis=0, how='any', inplace=True)
df.reset_index(drop=True, inplace=True)
print('DataFrame Shape: {}'.format(df.shape))
~~~

<div class="output stream stdout" markdown="1">

    DataFrame Shape: (2913, 6)

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q3. Aggregating - For each PERMNO, calculate the following statistics for the total_returns - sum, mean, std dev, and median. Hint - use .groupby('permno') and then aggregate by the stats(.agg() function might be useful).<br> {#q3-aggregating---for-each-permno-calculate-the-following-statistics-for-the-total_returns---sum-mean-std-dev-and-median-hint---use-groupbypermno-and-then-aggregate-by-the-statsagg-function-might-be-useful-}

#### Answer 3: {#answer-3}

</div>

<div class="cell code" markdown="1" execution_count="10">

~~~ python
cols_to_group = ['total_returns']               # Columns to Group
cols_to_groupby = ['permno']                    # Columns to Groupby 

std_pop_lambda = lambda x:x.std(ddof=0)         # Creating a custom function
std_pop_lambda.__name__ = 'Std_Pop_Lambda'      # Naming the lambda Function
def std_pop(x): return x.std(ddof=0)            # Another way to achieve the above. Need not name the function separately 

col_stats_reqd = ['sum', 'mean', std_pop,'median']      # Statistics required permno wise for Total Returns

df_returns_groups = df.groupby(by=cols_to_groupby)[cols_to_group]
df_returns_groups_stats = df_returns_groups.agg(col_stats_reqd).round(4)
display(df_returns_groups_stats.head())
~~~

<div class="output display_data" markdown="1">

           total_returns                        
                     sum    mean std_pop  median
    permno                                      
    10001         1.0360  0.0113  0.0870  0.0050
    10006         1.8390  0.0163  0.0882  0.0037
    10014         1.8046  0.0668  0.1621  0.0714
    10028         4.1703  0.0184  0.1986  0.0000
    10029         0.4969  0.0155  0.1406 -0.0187

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q4. Filtering Text - You can parse the company name column to search for companies that match your key words. A basic filter would be to check for "OIL", "GAS", and "ENERGY" companies. Write a program that returns the number of unique PERMNOs that match the above 3 key-words. Hint: Try using df\['company_name'\].str.contains(). If you are interested in text parsing in Python, regex (regular expression) is a powerful library you may want to try out! <br> {#q4-filtering-text---you-can-parse-the-company-name-column-to-search-for-companies-that-match-your-key-words-a-basic-filter-would-be-to-check-for-oil-gas-and-energy-companies-write-a-program-that-returns-the-number-of-unique-permnos-that-match-the-above-3-key-words-hint-try-using-dfcompany_namestrcontains-if-you-are-interested-in-text-parsing-in-python-regex-regular-expression-is-a-powerful-library-you-may-want-to-try-out--}

#### Answer 4: {#answer-4}

</div>

<div class="cell code" markdown="1" execution_count="11">

~~~ python
col_reqd = 'permno'                         # Column name whose Unique Values are required
col_to_search = 'company_name'              # Column name in which keywords needs to be searched 
info_to_collate = ['Count', 'permnos']      # Values that will be collated for all the keywords
regex_dict = {'OIL': r'\boil\b',           # Regex patterns for keywords viz. oil, gas & energy
              'GAS': r'\bgas\b',
              'ENERGY': r'\benergy\b'}

answer_dict = {}
for key, pattern in regex_dict.items():
    mask = df[col_to_search].str.contains(pattern, flags=re.IGNORECASE, regex=True)
    unique_values_list = df.loc[mask, col_reqd].unique().tolist()
    answer_dict[key] = dict(zip(info_to_collate,
                                [len(unique_values_list),unique_values_list]))    
    
    
print('Dictionary of Permnos for specified Keywords\n\n')
pprint(answer_dict, sort_dicts=False)
~~~

<div class="output stream stdout" markdown="1">

    Dictionary of Permnos for specified Keywords


    {'OIL': {'Count': 0, 'permnos': []},
     'GAS': {'Count': 1, 'permnos': [10001]},
     'ENERGY': {'Count': 2, 'permnos': [10001, 10137]}}

</div>

</div>

<div class="cell markdown" markdown="1">

#### Q5. Merging - Create a new dataframe with the last available date and price for each PERMNO. For example, the only entry for PERMNO 10001 is 31-Jul-2017 (date) and 12.95 (price). Merge this new dataframe onto the original dataframe. Fill the missing/NaN values using pandas fillna function with a method of your choice.<br> {#q5-merging---create-a-new-dataframe-with-the-last-available-date-and-price-for-each-permno-for-example-the-only-entry-for-permno-10001-is-31-jul-2017-date-and-1295-price-merge-this-new-dataframe-onto-the-original-dataframe-fill-the-missingnan-values-using-pandas-fillna-function-with-a-method-of-your-choice-}

#### Answer 5: {#answer-5}

</div>

<div class="cell code" markdown="1" execution_count="12">

~~~ python
col_to_groupby = 'permno'                       # Column name whose Unique Values are required
col_max = 'date'                                # Column whose max values id required to be figured out 
cols_to_retain = ['permno','date','price']      # Columns which are required post filtering    

df_filtered = df.loc[df.groupby(cols_to_groupby)[col_max].agg(pd.Series.idxmax),
                     cols_to_retain]          

df_merged = pd.merge(left=df, right=df_filtered, how='outer',
                     left_index=True, right_index=True,
                     suffixes=['_original','_filtered'], sort=False)

df_merged['permno_filtered'].fillna(df_merged['permno_original'], inplace=True)
df_merged['date_filtered'].fillna(df_merged['date_original'], inplace=True)
df_merged['price_filtered'].fillna(df_merged['price_original'], inplace=True)

display(df_merged.head())
print('\nDataFrame Shape: {}'.format(df_merged.shape))
~~~

<div class="output display_data" markdown="1">

       permno_original company_name date_original  total_returns  price_original  \
    0            10001   ENERGY INC    2009-12-31       0.162621         10.3000   
    1            10001   ENERGY INC    2010-01-31      -0.018932         10.0600   
    2            10001   ENERGY INC    2010-02-28      -0.000656         10.0084   
    3            10001   ENERGY INC    2010-03-31       0.020643         10.1700   
    4            10001   ENERGY INC    2010-04-30       0.124385         11.3900   

       share_outstanding  permno_filtered date_filtered  price_filtered  
    0               4361          10001.0    2009-12-31         10.3000  
    1               4361          10001.0    2010-01-31         10.0600  
    2               4361          10001.0    2010-02-28         10.0084  
    3               4361          10001.0    2010-03-31         10.1700  
    4               6070          10001.0    2010-04-30         11.3900  

</div>

<div class="output stream stdout" markdown="1">


    DataFrame Shape: (2913, 9)

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q6. Lagged Market Cap - Create three new columns that contain the 6-month, 1-year, and 5-year lagged market cap. For example: PERMNO 10001 on 30-Jun-2016 will have the market cap as on 31-Dec-2015 (7.45 ⋅ 10505 = 78262.25) as its 6-month lag market cap. Perform a similar exercise to generate the 1-year and the 5-year lag market caps. <br> {#q6-lagged-market-cap---create-three-new-columns-that-contain-the-6-month-1-year-and-5-year-lagged-market-cap-for-example-permno-10001-on-30-jun-2016-will-have-the-market-cap-as-on-31-dec-2015-745-cdot-10505--7826225-as-its-6-month-lag-market-cap-perform-a-similar-exercise-to-generate-the-1-year-and-the-5-year-lag-market-caps--}

#### Answer 6: {#answer-6}

</div>

<div class="cell code" markdown="1" execution_count="13">

~~~ python
# Method 1 of Solving Question 6

lag_freqs = [6, 12, 60]                                 # List of lag frequencies in months
df['market_cap'] = df['price']*df['share_outstanding']

dfs_to_add = [df.set_index('date').groupby('permno')['market_cap']
                .shift(periods=lag, freq='M')
                .rename('market_cap_lag'+str(lag)+'months')
                .reset_index() for lag in lag_freqs]

df_ans_m1 = reduce(lambda left,right: pd.merge(left, right, how='left',
                                               on=['permno','date']), [df] + dfs_to_add)

df_ans_m1.fillna(np.nan,inplace=True)
display(df_ans_m1.tail())
print('\nDataFrame Shape: {}'.format(df_ans_m1.shape))
~~~

<div class="output display_data" markdown="1">

          permno          company_name       date  total_returns  price  \
    2908   10137  ALLEGHENY ENERGY INC 2010-07-31       0.102514  22.80   
    2909   10137  ALLEGHENY ENERGY INC 2010-08-31      -0.010965  22.55   
    2910   10137  ALLEGHENY ENERGY INC 2010-09-30       0.094013  24.52   
    2911   10137  ALLEGHENY ENERGY INC 2010-10-31      -0.053834  23.20   
    2912   10137  ALLEGHENY ENERGY INC 2011-01-31       0.063531  25.78   

          share_outstanding  market_cap  market_cap_lag6months  \
    2908             169579  3866401.20             3552344.85   
    2909             169615  3824818.25             3840760.50   
    2910             169615  4158959.80             3900110.00   
    2911             169615  3935068.00             3693234.60   
    2912             169939  4381027.42             3866401.20   

          market_cap_lag12months  market_cap_lag60months  
    2908              4270548.79              4632333.00  
    2909              4476046.03              4908238.40  
    2910              4494689.16              5000048.64  
    2911              3867602.06              4599654.12  
    2912              3552344.85              5665655.87  

</div>

<div class="output stream stdout" markdown="1">


    DataFrame Shape: (2913, 10)

</div>

</div>

<div class="cell code" markdown="1" execution_count="14">

~~~ python
# Method 2 of Solving Question 6

lag_freqs = [6, 12, 60]                                 # List of lag frequencies in months
col_to_groupby = 'permno'
time_freq = 'M'                                         # Time Frequency of Data is Monthly

df['market_cap'] = df['price']*df['share_outstanding']
df.index.name = 'original_index'                        # Setting an index name for ease of reference
df_permno_groups = df.groupby(col_to_groupby)
df_ans_m2 = pd.DataFrame()                              # DataFrame to collate answers

for name, df_group in df_permno_groups:
    df_group.reset_index(inplace=True)
    df_group.set_index('date', drop=False, inplace=True)

    for lag in lag_freqs:
        df_group['market_cap_lag'+str(lag)+'months'] = df_group['market_cap'].shift(periods=lag, freq=time_freq)

    df_group.fillna(np.nan, inplace=True) 
    df_group.set_index(df.index.name, inplace=True)
    df_ans_m2 = pd.concat([df_ans_m2, df_group]) 

df_ans_m2.index.name = None
df.index.name = None
display(df_ans_m2.tail())
print('\nDataFrame Shape: {}'.format(df_ans_m2.shape))
~~~

<div class="output display_data" markdown="1">

          permno          company_name       date  total_returns  price  \
    2908   10137  ALLEGHENY ENERGY INC 2010-07-31       0.102514  22.80   
    2909   10137  ALLEGHENY ENERGY INC 2010-08-31      -0.010965  22.55   
    2910   10137  ALLEGHENY ENERGY INC 2010-09-30       0.094013  24.52   
    2911   10137  ALLEGHENY ENERGY INC 2010-10-31      -0.053834  23.20   
    2912   10137  ALLEGHENY ENERGY INC 2011-01-31       0.063531  25.78   

          share_outstanding  market_cap  market_cap_lag6months  \
    2908             169579  3866401.20             3552344.85   
    2909             169615  3824818.25             3840760.50   
    2910             169615  4158959.80             3900110.00   
    2911             169615  3935068.00             3693234.60   
    2912             169939  4381027.42             3866401.20   

          market_cap_lag12months  market_cap_lag60months  
    2908              4270548.79              4632333.00  
    2909              4476046.03              4908238.40  
    2910              4494689.16              5000048.64  
    2911              3867602.06              4599654.12  
    2912              3552344.85              5665655.87  

</div>

<div class="output stream stdout" markdown="1">


    DataFrame Shape: (2913, 10)

</div>

</div>

<div class="cell markdown" markdown="1">

<hr markdown="1" style="border:.05px solid black">

<br>

</div>

<div class="cell markdown" markdown="1">

#### Q7. Resampling Frequency - Convert the monthly dataframe that you loaded above into quarterly data and annual data. Hint: First, load and clean the data as per procedure mentioned above. Second, create a new column containing quarters corresponding to the given month (ex: 30-Nov-2010 is a quarter 4). Lastly, create a new dataframe "df_quarter" by aggregating data using the groupby command. For the quarterly dataframe your columns will be {permno, date, quarter, total_returns, market_cap}. Note that you will need to add the monthly returns to generate quarterly returns. Also note that you will need the quarter end market cap for each PERMNO each quarter. For example : In the Quarterly dataframe, PERMNO 10001 as of 31-Mar-2010 will have total returns 0.001055 (-0.018932-0.000656+0.020643) and the market cap 44351.37 (10.17$\\cdot$4361). Perform the same procedure for creating data at an annual frequency.<br> {#q7-resampling-frequency---convert-the-monthly-dataframe-that-you-loaded-above-into-quarterly-data-and-annual-data-hint-first-load-and-clean-the-data-as-per-procedure-mentioned-above-second-create-a-new-column-containing-quarters-corresponding-to-the-given-month-ex-30-nov-2010-is-a-quarter-4-lastly-create-a-new-dataframe-df_quarter-by-aggregating-data-using-the-groupby-command-for-the-quarterly-dataframe-your-columns-will-be-permno-date-quarter-total_returns-market_cap-note-that-you-will-need-to-add-the-monthly-returns-to-generate-quarterly-returns-also-note-that-you-will-need-the-quarter-end-market-cap-for-each-permno-each-quarter-for-example--in-the-quarterly-dataframe-permno-10001-as-of-31-mar-2010-will-have-total-returns-0001055--0018932-00006560020643-and-the-market-cap-4435137-1017cdot4361-perform-the-same-procedure-for-creating-data-at-an-annual-frequency-}

#### Answer 7: {#answer-7}

</div>

<div class="cell code" markdown="1" execution_count="15">

~~~ python
# Quarterly Data Conversion

df_quarterly = pd.merge(left=df.drop(['total_returns'], axis=1), 
                        right=df.groupby('permno')
                                .resample('Q', on='date')['total_returns']
                                .sum().reset_index(), 
                        how='right', on=['permno','date']).reset_index(drop=True)

display(df_quarterly.head())
print('\nDataFrame Shape: {}'.format(df_quarterly.shape))
~~~

<div class="output display_data" markdown="1">

       permno     company_name       date  price  share_outstanding  market_cap  \
    0   10001       ENERGY INC 2009-12-31  10.30             4361.0    44918.30   
    1   10001       ENERGY INC 2010-03-31  10.17             4361.0    44351.37   
    2   10001       ENERGY INC 2010-06-30  10.86             6080.0    66028.80   
    3   10001  GAS NATURAL INC 2010-09-30  11.12             6073.0    67531.76   
    4   10001  GAS NATURAL INC 2010-12-31  10.52             7834.0    82413.68   

       total_returns  
    0       0.162621  
    1       0.001055  
    2       0.085793  
    3       0.048630  
    4      -0.033330  

</div>

<div class="output stream stdout" markdown="1">


    DataFrame Shape: (1037, 7)

</div>

</div>

<div class="cell code" markdown="1" execution_count="16">

~~~ python
# Yearly Data Conversion

df_yearly = pd.merge(left=df.drop(['total_returns'], axis=1), 
                     right=df.groupby('permno')
                             .resample('Y', on='date')['total_returns']
                             .sum().reset_index(), 
                     how='right', on=['permno','date']).reset_index(drop=True)

display(df_yearly.head())
print('\nDataFrame Shape: {}'.format(df_yearly.shape))
~~~

<div class="output display_data" markdown="1">

       permno     company_name       date  price  share_outstanding  market_cap  \
    0   10001       ENERGY INC 2009-12-31  10.30             4361.0    44918.30   
    1   10001  GAS NATURAL INC 2010-12-31  10.52             7834.0    82413.68   
    2   10001  GAS NATURAL INC 2011-12-31  11.42             8154.0    93118.68   
    3   10001  GAS NATURAL INC 2012-12-31   9.33             8157.0    76104.81   
    4   10001  GAS NATURAL INC 2013-12-31   8.03            10452.0    83929.56   

       total_returns  
    0       0.162621  
    1       0.102148  
    2       0.136491  
    3      -0.143090  
    4      -0.080232  

</div>

<div class="output stream stdout" markdown="1">


    DataFrame Shape: (277, 7)

</div>

</div>

<div class="cell markdown" markdown="1">

<br><br>

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
