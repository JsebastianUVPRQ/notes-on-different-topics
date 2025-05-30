NumPy provides a lot of the functionality and tools you need to work with numbers, such as arrays of numeric values. However, when you start to deal with two-dimensional tables of data, the **Pandas** package offers a more convenient structure to work with: the **DataFrame**.

Run the following cell to import the Pandas library and create a DataFrame with three columns. The first column is a list of student names, and the second and third columns are the NumPy arrays containing the study time and grade data.
```Python
import pandas as pd

  

df_students = pd.DataFrame({'Name': ['Dan', 'Joann', 'Pedro', 'Rosie', 'Ethan', 'Vicky', 'Frederic', 'Jimmie',
				'Rhonda', 'Giovanni', 'Francesca', 'Rajab', 'Naiyana', 'Kian', 'Jenny',                 'Jakeem','Helena','Ismat','Anila','Skye','Daniel','Aisha'],
				 'StudyHours':student_data[0],
				'Grade':student_data[1]})
#[0] y [1] son los arrays definidos en la primera parte de los apuntes de numpy
  

df_students
```

Pandas includes an index for each arrow. We can use **loc** method to get a row:
```Python
# Get the data for index value 5

df_students.loc[5]
```
Look carefully at the `iloc[0:5]` results and compare them to the `loc[0:5]` results you obtained previously. Can you spot the difference?

The **loc** method returned rows with index _label_ in the list of values from _0_ to _5_, which includes _0_, _1_, _2_, _3_, _4_, and _5_ (six rows). However, the **iloc** method returns the rows in the _positions_ included in the range 0 to 5. Since integer ranges don't include the upper-bound value, this includes positions _0_, _1_, _2_, _3_, and _4_ (five rows).

**iloc** identifies data values in a DataFrame by _position_, which extends beyond rows to columns. So, for example, you can use it to find the values for the columns in positions 1 and 2 in row 0, like this:

```Python
df_students.iloc[0,[1,2]]
```

``` Fortran
StudyHours 10 
Grade 50 
Name: 0, dtype: object
```

Here's another useful trick. You can use the **loc** method to find indexed rows based on a filtering expression that references named columns other than the index, like this:
```Python
df_students.loc[df_students['Name']=='Aisha']
```

|Name|StudyHours|Grade|
|---|---|---|
|21|Aisha|12.0|64.0|

# Explore data in the DataFrame