# Ex NO : 02 Outlier Detection and Removal

## DATE : 

## AIM:
To read a given dataset and remove outliers and save a new dataframe.

## ALGORITHM:
### STEP 1 :
Remove outliers using IQR
### STEP 2 :
 After removing outliers in step 1, you get a new dataframe.
### STEP 3 :
 use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result
### STEP 4 :
for the data set height_weight.csv find the following
### STEP 5 :
Using IQR detect weight outliers and print them
### STEP 6 :
 Using IQR, detect height outliers and print them

## CODE:
DEVELOPED BY : YUGENDARAN . G

REGISTER NO : 212221220063
```
import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

df = pd.read_csv("/content/heights.csv")

sns.boxplot(data=df)

sns.scatterplot(data=df)

max =df['height'].quantile(0.90)

min =df['height'].quantile(0.15)

max

min

dq = df[((df['height']>=min)&(df['height']<=max))]

dq

low = min-1.5*iqr

high = max+1.5*iqr

dq = df[((df['height']>=min)&(df['height']<=max))]

dq

## ZSCORE:

import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}

df = pd.DataFrame(data)

df

sns.boxplot(data=df)

z = np.abs(stats.zscore(df))

print(df[z['weight']>3])

val = [12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]

out=[]

def d_o(val):

  ts=3
  
  m=np.mean(val)
  
  sd=np.std(val)
  
  for i in val:
  
    z=(i-m)/sd
    
    if np.abs(z)>ts:
    
      out.append(i)
      
  return out

  op = d_o(val)

  op
```
  ## OUTPUT:

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/ce20a1d1-83d7-4ba9-ba68-d1b6a6a9fc74)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/d99857a5-ba5d-4205-b136-fe5db64f82e4)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/3575c862-ddc9-4676-bc2a-eb0b028c0335)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/77c62ada-fc65-4dd1-bf90-6fb4fad91bd0)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/1baf73cc-50a3-4b5c-9811-68c7a104cc09)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/2d457791-498c-43e7-920f-2e9d9027cdc2)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/188ebebc-0dcf-443e-afbd-15986f2b10a4)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/5d623ceb-b7ea-4993-bd0f-626bc7e4bc72)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/849cecb5-3c55-48bf-999f-8dbc43f85049)

  ![image](https://github.com/Yugendaran/ODD2023---Datascience---Ex-02/assets/128135616/bb55307b-ca2e-447a-9cba-f1a18fcf8066)


  ## RESULT:
  Thus, the given data is read,remove outliers and save a new dataframe was created and executed successfully.










