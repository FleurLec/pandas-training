# pandas-training
## 1. Objects

**Series** : 1-dimensional array of indexed data.  
Rows and columns of a dataframe are series. You access them as  `df['col']` or `df.col`

## 2. Conditions

Always put each conditions inside () 
and : &
or : | 
not : ~


## 3. Index

`df.index` give the list of indexes.  
Indexes cannot be changed. 


## 4. Pandas functions

**Read files** :  `read_csv(filepath, ..., skiprows = None)`

| Function |  Description | 
|----------------------|-----------|
| pd.show_versions()  | all info about pandas, python and package versions | 
| pd.__versions__ | get pandas version
| *[method]*? | get help on the [method] |
| type([df]) | type of the object |
| df.shape / df.shape[0] / df.shape[1]| rows and columns of the df  / nb of lines / columns|
| df.info() | describe content of the dataframe. Specify if None value |



| Function |  Description | 
|----------------------|-----------|
| df[['col1', 'col2']] | select several columns |
| *serie*.**value_counts**(<br> <u>normalize</u>= False, <br>  <u>sort</u> = True, <br> <u>ascending</u> = False, <br> <u>dropna</u> = True) | normalize: give % <br> dropna : by default, you don't see NAs <br> `df[(df["Medal"] == "Gold") & (df["Sex"] == "M") ].value_counts("Team", ascending = False)`|
| df.**sort_values**(by, <br> <u>axis</u> = 0, <br> <u>ascending</u> = True, <br> <u>inplace</u> = False, ...) | axis = 0 : by column <br> `df.sort_values(['Col1', 'Col2'])` <br> `df[(df["Medal"] == "Gold") & (df["Sex"] == "M") ].sort_values("Team")[['Team', 'Games']]`|


| Function |  Description | 
|----------------------|-----------|
| *serie*.str.contains() | To get it non case sensitive, start with (?i) : `.str.contains("(?i)jesse")]` |
| *serie*.str.startswith() | |
| *serie*.str.isnumeric() | |
