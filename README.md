# Experiment:Introduction To Lab
# Name: Prajin S
# Register Number : 212223230151
# Department : Artificial Intelligence and data Sceince
# Codes for Lab Introduction
```
ACTIVITY 1:

1. Write a Python program to select the 'name' and 'score' columns from the following DataFrame.

       Sample DataFrame:

              exam_data = {'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],

               'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],

              'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1] } 

 

2. For the above dataframe, Write a program to select the data who's attempt is greater than 3.

3. Write python code for indexing rows and columns based on the following conditions:

Assume we have the following dataframe:

data = {'name': ['Alice', 'Bob', 'Charlie', 'Dave'],

        'age': [25, 35, 40, 28],

        'gender': ['F', 'M', 'M', 'M'],

        'salary': [50000, 70000, 60000, 80000]}

df = pd.DataFrame(data)

a. Select rows where age is greater than 30:

b. Select rows where name contains 'e':

c. Select rows where gender is 'M' and salary is greater than 65000:

d. Select columns 'name' and 'age'

ACTIVITY 2:

1. Write python code for indexing rows and columns using iloc or loc method based on the following conditions:

a.  select the rows where clients with primary education have subscribed to a deposit?

b.  select the rows where clients who have not subscribed to a deposit?

c. select the rows where clients who have subscribed to a deposit either have a housing or a personal loan?

d. select the rows where clients with secondary education who have not subscribed to a deposit?

e. select the rows where  clients who have subscribed to a term deposit as an outcome of the successful marketing campaign? 

f. select the rows where unemployed clients who have not subscribed to deposit?

e. Select columns 'name' and 'salary' where age is less than or equal to 30:
```
```

import pandas as pd
df=pd.DataFrame({"a":[4,5,6],"b":[7,8,9],"c":[10,11,12]},index=[1,2,3])
print(df)

import pandas as pd
dt=[1,2,3,4]
df=pd.DataFrame(dt)
print(df)

import pandas as pd
data=[['Alex',10],['Bob',12]]
df=pd.DataFrame(data,columns=['name','age'],index=['a1','b2'])
print(df)

import pandas as pd
data={'cars':["BMW","Volvo","Ford"],'passings':[3,7,2]}
vr=pd.DataFrame(data)
print(vr)

import pandas as pd
data=[{'a':1,'b':2},{'a':5,'b':10,'c':20}]
df=pd.DataFrame(data)
print(df)
df=pd.DataFrame(data,index=['first','second'])
print(df)
df1=pd.DataFrame(data,index=['first','second'],columns=['a','b'])
print(df1)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Height':[5.3,6.2,5.0,5.8],'Qualification':['Msc','MA','Msc','Msc']}
df=pd.DataFrame(data)
add=['delhi','Bengalore','Chennai','patna']
df['Address']=add
print(df)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Height':[5.3,6.2,5.0,5.8],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
del df['add']
df

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Height':[5.3,6.2,5.0,5.8],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.drop(['add'],axis=1,inplace=True)
df

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Height':[5.3,6.2,5.0,5.8],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.pop('add')
df.pop('Height')
df

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,24,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
print(df)
df.rename(columns={'add':'City'},inplace=True)
df

import pandas as pd
df=pd.DataFrame([[1,2],[3,4]],columns=['a','b'])
df2=pd.DataFrame([[5,6],[7,8]],columns=['a','b'])
df=pd.concat([df,df2])
df

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,24,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
print(df)
df.drop(2,axis=0,inplace=True)
df

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,24,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df=df['Name']
print(df)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,24,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
print(df[['Name','Qualification']])

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,24,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.filter(items=['Name','Age'])

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,24,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.filter(like='ge')

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,24,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.filter(regex='g|f',axis=1)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df=df.drop_duplicates(subset=['Qualification'])
df

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df=df.drop_duplicates(subset=['Qualification'],keep='last')
df

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
dfs=df.sample(n=2)
print(dfs)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
dfs=df.sample(frac=.5)
print(dfs)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
tops=df.nlargest(2,columns='Age')
print(tops)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
tops=df.nsmallest(2,columns='Age')
print(tops)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df=df.query('Age>=30')
print(df)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df=df.query('Name.str.contains("i") and Age > 25')
print(df)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df=df.query('Qualification == ["Msc" , "MA"] and Age<25')
print(df)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.loc[:,'Age']

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.loc[:,['Name','Age']]

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.iloc[:,3]

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df_fil=df[(df['Qualification']=='Msc')&(df['Age']>22)]
print(df_fil)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df_fil=df[(df['Name'].str.startswith('A','C'))]
print(df_fil)

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
print(df.tail(3))

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
df.info()

import pandas as pd
data={'Name':['Jai','Jeeva','Jaydeep','Jeyan'],'Age':[27,22,22,32],'Qualification':['Msc','MA','Msc','Msc'],'add':['delhi','Bengalore','Chennai','patna']}
df=pd.DataFrame(data)
gro=df.groupby('Qualification').mean()['Age']
print(gro)

import pandas as pd
data={'name':{'Alice','Bob','Charlie','Dave','Emily','Frank'},'gender':{'F','M','M','M','F','M'},'age':[25,35,40,28,30,45],'salary':[50000,70000,60000,80000,65000,90000]}
df=pd.DataFrame(data)
groped=df.groupby('gender').mean()['salary']
print(groped)
```
# Result:
Codes for lab introduction are worked out and ran successfully.
