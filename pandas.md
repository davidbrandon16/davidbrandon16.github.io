# Pandas on python

## import
```python
import pandas as pd
```

## Syntax on pandas
* DataFrame
```python 
    pd.DataFrame(data, colums=[])
    #convert to array to data
```
* read_csv
```python
    pd.read_csv("filename.csv",delimiters=",")
    #delimiters is not use when your file seperate with comma
```

* iloc (Index location) 
```python
    #df.iloc[row,column]
    df.iloc[0,0]
```
* loc (locaction)
> differences between iloc that  iloc must be index
```python
    #df.loc[row,column]
    df.loc[0,"name"]
```

* Get Specified column only
```python
    df[["column1","column3","..."]]
```

* Rename Column
```python
    df.rename(colums={"old":"new","old1":"new1"})
```

* group by 
> * to group the value must be countable
> * the value can be (sum, mean , and etc)
> * not save to current data frame need assignd to new one
```python
    new_df = df.groupby(["column1","column2","..."]).mean()
```

* sort value
> default asc is true
```python
    new_df = df.sort_value(by=["column1","column2","..."], ascending=False)
```

* filter row by value
> show all age with name is David from data frame
```python
    df.loc[df.name=="David","age"]
```