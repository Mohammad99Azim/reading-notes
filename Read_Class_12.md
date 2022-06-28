# Pandas 

The pandas package is the most important tool at the disposal of Data Scientists and Analysts working in Python today. The powerful machine learning and glamorous visualization tools may get all the attention, but pandas is the backbone of most data projects.

 Pandas is the best tool for handling this real-world messy data. And pandas is one of the open-source python packages built on top of NumPy.
 
 
 Handling data using pandas is very fast and effective by using pandas Series and data frame, these two pandas data structures will help you to manipulate data in various ways.

Based on the features available in pandas we can say pandas is best for handling data. It can handle missing data, cleaning up the data and it supports multiple file formats. This means it can read or load data in many formats like CSV, Excel, SQL, etc.,


 ### Example
 
 ```
titanic_d = pd.read_csv("../input/datafolder/titanic.csv")
titanic_d
```

Output :


```
	PassengerId	Survived	Pclass	Name	Sex	Age	SibSp	Parch	Ticket	Fare	Cabin	Embarked
0	1	0	3	Braund, Mr. Owen Harris	male	22.0	1	0	A/5 21171	7.2500	NaN	S
1	2	1	1	Cumings, Mrs. John Bradley (Florence Briggs Th...	female	38.0	1	0	PC 17599	71.2833	C85	C
2	3	1	3	Heikkinen, Miss. Laina	female	26.0	0	0	STON/O2. 3101282	7.9250	NaN	S
3	4	1	1	Futrelle, Mrs. Jacques Heath (Lily May Peel)	female	35.0	1	0	113803	53.1000	C123	S
4	5	0	3	Allen, Mr. William Henry	male	35.0	0	0	373450	8.0500	NaN	S
...	...	...	...	...	...	...	...	...	...	...	...	...
886	887	0	2	Montvila, Rev. Juozas	male	27.0	0	0	211536	13.0000	NaN	S
887	888	1	1	Graham, Miss. Margaret Edith	female	19.0	0	0	112053	30.0000	B42	S
888	889	0	3	Johnston, Miss. Catherine Helen "Carrie"	female	NaN	1	2	W./C. 6607	23.4500	NaN	S
889	890	1	1	Behr, Mr. Karl Howell	male	26.0	0	0	111369	30.0000	C148	C
890	891	0	3	Dooley, Mr. Patrick	male	32.0	0	0	370376	7.7500	NaN	Q
891 rows × 12 columns
```


In the above code, variable data stores CSV data which is a titanic passengers  by using the read_csv function available in the pandas package. 
data.shape is used to give you the columns and row count.


The above block has the top 5 rows of data set that can be displayed by pandas dataframe.head() function.


There are many more features that help us to deal with large data for both machine learning data science operations. Which are merging and joining data sets, Visualization, grouping, masking, and also is very helpful for performing mathematical operations on our data sets.

 ### Example
 
A check on how pandas interpreted each of the column data types can be done by requesting the pandas dtypes attribute

```
titanic_d.dtypes
```

Output:

```
PassengerId      int64
Survived         int64
Pclass           int64
Name            object
Sex             object
Age            float64
SibSp            int64
Parch            int64
Ticket          object
Fare           float64
Cabin           object
Embarked        object
dtype: object
```

For each of the columns, the used data type is enlisted. The data types in this DataFrame are integers (int64), floats (float64) and strings (object).

Note !!!


When asking for the dtypes, no brackets are used! dtypes is an attribute of a DataFrame and Series.



And there is alot of things Pandas have to deal with data and merge it take what we need from it every thing you need to deal with data you will find it in pandas
