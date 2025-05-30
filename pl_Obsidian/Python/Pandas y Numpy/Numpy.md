## Exploring data arrays with NumPy

Let's start by looking at some simple data.

Suppose a college professor takes a sample of student grades from a class to analyze.
```Python

data = [50,50,47,97,49,3,53,42,26,74,82,62,37,15,70,27,36,35,48,52,63,64]

print(data)
```

The data has been loaded into a Python **list** structure, which is a good data type for general data manipulation, but it's not optimized for numeric analysis. For that, we're going to use the **NumPy** package, which includes specific data types and functions for working with _Num_bers in _Py_thon.

Run the following cell to load the data into a NumPy **array**.
```Python
import numpy as np

  

grades = np.array(data)

print(grades)
```

```Python
print (type(data),'x 2:', data * 2)

print('---')

print (type(grades),'x 2:', grades * 2)
```
<class 'list'> x 2: [50, 50, 47, 97, 49, 3, 53, 42, 26, 74, 82, 62, 37, 15, 70, 27, 36, 35, 48, 52, 63, 64, 50, 50, 47, 97, 49, 3, 53, 42, 26, 74, 82, 62, 37, 15, 70, 27, 36, 35, 48, 52, 63, 64] --- 
<class 'numpy.ndarray'> x 2: [100 100 94 194 98 6 106 84 52 148 164 124 74 30 140 54 72 70 96 104 126 128]
```Python
# Define an array of study hours

study_hours = [10.0,11.5,9.0,16.0,9.25,1.0,11.5,9.0,8.5,14.5,15.5,

               13.75,9.0,8.0,15.5,8.0,9.0,6.0,10.0,12.0,12.5,12.0]

  

# Create a 2D array (an array of arrays)

student_data = np.array([study_hours, grades])

  

# display the array
student_data

student_data.shape #Es igual a (2,22)
```
El resultado es un matriz de dos filas y 22 columnas 

```Python
avg_study = student_data[0].mean()

avg_grade = student_data[1].mean()

  

print('Average study hours: {:.2f}\nAverage grade: {:.2f}'.format(avg_study, avg_grade))
```
Average study hours: 10.52 
Average grade: 49.18