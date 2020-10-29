# DataFrame.dropna
Tag: preprocesssing, pandas, dataframe, delete
Drop row/columns that has NA/NULL
## Usage: 
DataFrame.dropna(axis=0, how='any', thresh=None, subset=None, inplace=False)
## Parameter:
* axis: possible values are {0 or ‘index’, 1 or ‘columns’}, default 0. If 0, drop rows with null values. If 1, drop columns with missing values.

* how: possible values are {‘any’, ‘all’}, default ‘any’. 
    * If ‘any’, drop the row/column if any of the values is null. 
    * If ‘all’, drop the row/column if all the values are missing.
* thresh: an int value to specify the threshold for the drop operation. e.g.: axis=0，thresh=10：if containing data < 10, remove row
* subset: specifies the rows/columns to look for null values.
* inplace: a boolean value. If True, the source DataFrame is changed and None is returned.

Example 1:
```
     Name   ID Salary Role
0  Pankaj    1    100  CEO
1  Meghna    2    200  NaN
2   David    3    NaN  NaT
3    Lisa  NaT    NaT  NaT

df1 = df.dropna(subset=['ID'])
print(df1)

     Name ID Salary Role
0  Pankaj  1    100  CEO
1  Meghna  2    200  NaN
2   David  3    NaN  NaT
```

Example 2:
```
     Name   ID Salary Role
0  Pankaj    1    100  NaT
1  Meghna    2    200  NaT
2   David  NaT    NaN  NaT
3     NaT  NaT    NaT  NaT

df1 = df.dropna(thresh=2)
print(df1)

     Name ID Salary Role
0  Pankaj  1    100  NaT
1  Meghna  2    200  NaT
