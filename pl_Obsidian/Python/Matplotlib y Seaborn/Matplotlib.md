## Visualizing data with Matplotlib

DataFrames provide a great way to explore and analyze tabular data, but sometimes a picture is worth a thousand rows and columns. The **Matplotlib** library provides the foundation for plotting data visualizations that can greatly enhance your ability to analyze the data.

Let's start with a simple bar chart that shows the grade of each student.

**Note**: This first graph may take one to two minutes to render. Subsequent graphs will render more quickly.
```Python
# Ensure plots are displayed inline in the notebook

%matplotlib inline

  

from matplotlib import pyplot as plt

  

# Create a bar plot of name vs grade

plt.bar(x=df_students.Name, height=df_students.Grade)

  

# Display the plot

plt.show()
```
![[Pasted image 20230810021106.png]]

Well, that worked, but the chart could use some improvements to make it clearer what we're looking at.

Note that you used the **pyplot** class from Matplotlib to plot the chart. This class provides many ways to improve the visual elements of the plot. For example, the following code:

- Specifies the color of the bar chart.
- Adds a title to the chart (so we know what it represents)
- Adds labels to the X and Y axes (so we know which axis shows which data)
- Adds a grid (to make it easier to determine the values for the bars)
- Rotates the X markers (so we can read them)
```Python
# Create a bar plot of name vs grade

plt.bar(x=df_students.Name, height=df_students.Grade, color='orange')

  

# Customize the chart

plt.title('Student Grades')

plt.xlabel('Student')

plt.ylabel('Grade')

plt.grid(color='#95a5a6', linestyle='--', linewidth=2, axis='y', alpha=0.7)

plt.xticks(rotation=90)

  

# Display the plot

plt.show()
```
![[Pasted image 20230810021247.png]]

**A figure can contain multiple subplots**, each on its own _axis_.

For example, the following code creates a figure with two subplots: one is a bar chart showing student grades, and the other is a pie chart comparing the number of passing grades to non-passing grades.
```Python
# Create a figure for 2 subplots (1 row, 2 columns)

fig, ax = plt.subplots(1, 2, figsize = (10,4))

  

# Create a bar plot of name vs grade on the first axis

ax[0].bar(x=df_students.Name, height=df_students.Grade, color='orange')

ax[0].set_title('Grades')

ax[0].set_xticklabels(df_students.Name, rotation=90)

  

# Create a pie chart of pass counts on the second axis

pass_counts = df_students['Pass'].value_counts()

ax[1].pie(pass_counts, labels=pass_counts)

ax[1].set_title('Passing Grades')

ax[1].legend(pass_counts.keys().tolist())

  

# Add a title to the Figure

fig.suptitle('Student Data')

  

# Show the figure

fig.show()
```
![[Pasted image 20230810021528.png]]