# Pandas

## Importing Libraries
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import glob
import re
import math
```

# Series

## Printing a Series from Numpy Array
```
v = np.array([1, 2, 3, 4, 5])
s1 = pd.Series(v)
s1
```
<img width="102" height="228" alt="image" src="https://github.com/user-attachments/assets/c193c0cc-bb56-44a8-9550-6869c16b13bf" />


## Printing a Series from list
```
s0 = pd.Series([1,2,3],index = ['a','b','c'])
s0
```
<img width="111" height="174" alt="image" src="https://github.com/user-attachments/assets/7e388d32-d22d-4511-b704-10a6b64950ef" />

## Index in Series
```
s1.index = ['a' , 'b' , 'c' , 'd' , 'e']
s1
```
<img width="102" height="205" alt="image" src="https://github.com/user-attachments/assets/831a3c6d-56d6-411e-b872-43284de7f4b7" />

## Series from Dictionary
```
dict1 = {'a1' :10 , 'a2' :20 , 'a3':30 , 'a4':40}
s3 = pd.Series(dict1)
s3
```
<img width="106" height="174" alt="image" src="https://github.com/user-attachments/assets/01750fea-1f78-48ca-bbde-88abb8e258ac" />

## Printing 99 in indexes
```
pd.Series(99, index=[0, 1, 2, 3, 4, 5])
```
<img width="91" height="231" alt="image" src="https://github.com/user-attachments/assets/60b32498-a179-42c5-8422-d7fffc87fc3e" />

## Slicing

### Returning first elements three elements of series
```
s[0:3]
```
<img width="113" height="140" alt="image" src="https://github.com/user-attachments/assets/f055e302-1833-486b-9bc5-1f27c3fb5f9c" />

### Returning last element of series
```
s[-1:]
```
<img width="105" height="69" alt="image" src="https://github.com/user-attachments/assets/0beb6f89-e32a-425b-87ce-606194fb73c6" />

## Operation on Series
```
v1 = np.array([10,20,30])
v2 = np.array([1,2,3])
s1 = pd.Series(v1) 
s2 = pd.Series(v2)
s1 , s2
```
<img width="118" height="133" alt="image" src="https://github.com/user-attachments/assets/b7deac24-471e-408c-831f-d103ba26a715" />

### Addition of two series
```
s1.add(s2)
```
<img width="71" height="126" alt="image" src="https://github.com/user-attachments/assets/1cc9129a-e0f1-4bdf-bd2d-a2133f33729f" />

### Subtraction of two series
```
s1.sub(s2)
# or
s1.subtract(s2)
```
<img width="54" height="124" alt="image" src="https://github.com/user-attachments/assets/ecdb29da-3a6f-4c8a-be88-b24aba85f89f" />

### Multiplication of two series
```
s1.mul(s2)
# or
s1.multiply(s2)
```
<img width="70" height="135" alt="image" src="https://github.com/user-attachments/assets/8772bf1f-1c0b-4f64-9b42-adf549aeaecd" />

### Division
```
s1.divide(s2)
# or
s1.div(s2)
```
<img width="73" height="127" alt="image" src="https://github.com/user-attachments/assets/894222e2-cce6-432a-9894-0d8075232aef" />

# DataFrame

## Creating a dataframe from a list
```
lang = ['Java' , 'Python' , 'C' , 'C++']
df = pd.DataFrame(lang)
df
```
<img width="89" height="156" alt="image" src="https://github.com/user-attachments/assets/df325f23-90c9-44f6-b601-574fd458ab2a" />

## Adding column in dataframe
```
rating = [1,2,3,4]
df[1] = rating
df
```
<img width="105" height="152" alt="image" src="https://github.com/user-attachments/assets/a7481fcd-c100-4917-ba97-675060f73c39" />

## dataframe from dictionary
```
data = [{'a': 1, 'b': 2},{'a': 5, 'b': 10, 'c': 20}]

df2 = pd.DataFrame(data)
df3 = pd.DataFrame(data, index=['row1', 'row2'], columns=['a', 'b'])
```
<img width="116" height="95" alt="image" src="https://github.com/user-attachments/assets/b120c4f9-c5ad-4e8d-95aa-08cfcd9f21c6" />
<img width="104" height="98" alt="image" src="https://github.com/user-attachments/assets/e9a23fde-24d0-4bac-8704-5498ef679a9d" />

## Creating a dataframe from dictionary of series
```
dict = {'A' : pd.Series([1, 2, 3],    index=['a', 'b', 'c']),
        'B' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}

df1 = pd.DataFrame(dict)
df1
```
<img width="98" height="147" alt="image" src="https://github.com/user-attachments/assets/77e646db-f34d-4e63-af7c-d9e2c8d58513" />

## Data Selection
```
df
```
<img width="154" height="150" alt="image" src="https://github.com/user-attachments/assets/8b9a5be7-1278-4297-b2b9-bb9d8007a557" />

### Data selection using row label
```
df.loc[1]
```
<img width="146" height="132" alt="image" src="https://github.com/user-attachments/assets/87feda63-c755-416e-9401-10105ea6784f" />

### Data selection using integer
```
df.iloc[1]
```
<img width="141" height="93" alt="image" src="https://github.com/user-attachments/assets/316365c6-0c18-492e-8328-4bedff1eba04" />

## Seting Value

### Set value for all elements of in column C1
```
dframe['C1'] = 888
dframe
```
<img width="516" height="246" alt="image" src="https://github.com/user-attachments/assets/1b91dea9-971c-4d84-bb44-f13ff089a43f" />

## Functions on Dataframe
```
dframe
```
<img width="526" height="242" alt="image" src="https://github.com/user-attachments/assets/b55cef77-d5ee-4da8-a5f0-c26f2dc0a63a" />

### Finding max value
```
dframe.apply(max)
```
<img width="128" height="271" alt="image" src="https://github.com/user-attachments/assets/2d373f2c-bf9d-4002-849a-e35c4d8b049c" />

### Finding min vale
```
dframe.apply(min)
```
<img width="126" height="238" alt="image" src="https://github.com/user-attachments/assets/77dd425e-c5ef-4311-8cb6-c1fd049257b1" />

### Sum of column values
```
dframe.apply(sum)
```
<img width="127" height="241" alt="image" src="https://github.com/user-attachments/assets/939d20bd-aa7d-4946-9693-946280e1a657" />

### Sum of row values
```
dframe.apply(np.sum ,axis=1)
```
<img width="186" height="238" alt="image" src="https://github.com/user-attachments/assets/aa5253b0-a6ff-413b-8746-7f6a8b1ff236" />

## Merging Dataframes
```
daf1 =  pd.DataFrame ({'id': ['1', '2', '3', '4', '5'], 'Name': ['Asif', 'Basit', 'Bran', 'John', 'David']})
daf1
```
<img width="105" height="174" alt="image" src="https://github.com/user-attachments/assets/93671674-595e-4b71-b8f1-8a11661c6479" />

```
daf2 =  pd.DataFrame ({'id': ['1', '2', '6', '7', '8'], 'Score': [40 , 60 , 80 , 90 , 70]})
daf2
```
<img width="102" height="169" alt="image" src="https://github.com/user-attachments/assets/d685c8e7-4955-4f62-b518-9385bc22d520" />

### Inner join
```
pd.merge(daf1, daf2, on='id', how='inner')
```
<img width="143" height="96" alt="image" src="https://github.com/user-attachments/assets/14f95fad-6a76-4489-9747-fb04e8455232" />

### Outer join
```
pd.merge(daf1, daf2, on='id', how='outer')
```
<img width="157" height="264" alt="image" src="https://github.com/user-attachments/assets/6198a9a7-6df9-405f-a110-5a82a6c02234" />