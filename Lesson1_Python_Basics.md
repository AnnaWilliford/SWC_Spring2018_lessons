Software Carpentry Workshop
----

Lesson 1: Introduction to Python
----  

SWC workshop, February 2018  
Instructor: Balan Ramesh  
Time: 3 hours  

---

Good morning! I welcome you all to the workshop once again and I am glad you could make it safe to the workshop in such a rainy weather.
I am Balan Ramesh. I am a graduate student in Dr. Demuth's lab here in UTA. I am interested in studying Sex chromosome evolution in Tribolium species. I work on whole genome sequences and I use various tools including programming languages Python, Shell and R.

Now before we get started with python, I want to decide the pace of my lessons, so that its easy for most you. So, I would like to know how many of you have no programming experience? 
How many of you have some programming experience?

I can say this workshop will be of immense help to people with no programming experience and for people with some programming experience, I assume the later parts of the workshop will be of great use.

Let's make a folder `SWC_spring2018` on your Desktop. We will be working with this folder for the next 2 days so it is better if you leave it on the Desktop where it is easily accesible. It also helps for everyone to have the folder in the same location as it will make it easier to navigate to your files when we start using command line interface later today.

:+1: Do it with students and make sure everyone is with you - put up red sticky notes if having problems, green when done with the task. 

Now let's download datasets (Data.zip) for the workshop and put it in `SWC_spring2018` folder. You should find the link to the datasets in the etherpad. Its a zip file.

[Dataset](https://raw.githubusercontent.com/AnnaWilliford/2017-11-11-UTA/gh-pages/workshop/SWC_fall2017/Data.zip)

When you unzip this file, you should have `Data` folder with `ByCountry` folder and `gapminder.txt` file in it.
Make sure to cut or copy this to `SWC_spring2018` folder.

:+1: 

Finally, let's make another folder called  `Python_basics` inside `SWC_spring2018` folder. This is where we will save all files for this lesson.

Once you have this folder, let us copy `gapminder.txt` to the `Python_basics folder`.

:+1:

Now we are ready to work with Python.

### Learning objectives of this workshop

- Understand benefits of using Python
- Understand how to work with Jupyter Notebook
- Understand how to go get data from Excel to Python
- Understand building blocks of Python language
- Understand how to extract parts of the dataset
- Understand how to write simple Python scripts

Ultimately, by the end of this workshop, you can create your own reports as a Markdown file or HTML file or pdf file to present it to your superiors.

:hushed::hushed::hushed:

[Reports](https://github.com/AnnaWilliford/SWC_Spring2018_lessons/blob/master/Lesson5_GDP_report_Africa_Americas.ipynb)


You can create the following graphs and leave a good impression.

:astonished::astonished::scream:

[Plots](https://github.com/AnnaWilliford/SWC_Spring2018_lessons/blob/master/Lesson4_Data_Visualization_With_Plotnine.ipynb)


# 1. Introduction to Python and Jupyter Notebook  

## Why Python ?

Python is a general purpose programming language that supports rapid development of scripts and applications.

Python’s main advantages:

* Open Source software, supported by Python Software Foundation
* Available on all platforms
* It is a general-purpose programming language
* Supports multiple programming paradigms
* Very large community with a rich ecosystem of third-party packages

## Jupyter Notebook as IDE for Python

We will be working with Python using Jupyter Notebook. This is a piece of software (also known as integrated development environment, IDE) that makes working in Python much easier. 

Now let us open our terminal or gitbash and type `cd`. This command takes you to your home directory. We will learn more linux commands later in the day.

Now let us open Jupyter Notebook by typing `jupyter-notebook`/ `jupyter notebook` in the terminal/console/gitbash/cmd.

Jupyter Notebook opens in your default browser with a list of files and directories in the home directory with this URl `http://localhost:8888/tree`  

For this workshop, we will have all our files in `SWC_spring2018`. Navigate `Home-->Desktop-->SWC_spring2018-->Python_Basics` and hit New and click Python 3 to create a new file.

Now remember my path will be slightly different because I want to share my file with you all everytime I save. So I have my files in Dropbox.

:+1: 

This opens up to the Notebook User Interface (UI). This has three areas.

* Menubar 
* Toolbar
* Notebook area and cells

We will learn more about these areas and their functions, as we move along. For now, let us get started with some basic math.

We can add new cell using the `+` option in tool bar. Using the Edit Menu, delete or merge multiple cells together.
Now, I will give you few minutes to get used to the GUI.

Now, if a cell is highlighted in `green` :green_heart:, it means the cell is in `edit mode`. Thas is you can add, edit and delete contents of a cell like a normal text editor. But is If the cell is highlighted in `blue` :blue_heart:, it means the cell is in `command mode`. Here you can not add or modify contents of a particular cell, instead, you can work with the notebook as a whole. Its important to know that in command mode, the keys are mapped to different functions like to delete (DD) or merge cells (Shift+M).

 Now let us try the following commands one by one in `edit mode`. Type `3+5` and hit <kbd>Shift</kbd>+<kbd>Enter</kbd>

```python
3+5
print("Welcome All !!!")
```
In general, a function takes an input and transforms it according to the function's definition(rules). You can recognize functions in python by the presence of parantheses. Objects in parantheses are called function's `arguments`.

- Here `print()` is a built-in function. Meaning, the function is loaded in python by default.
- `"Welcome All"` is an argument to the function.

Now,not all functions are present by default. Depending on the need, several built-in modules/packages are imported to the python.

So whenever you catch me saying module or packages or library, I just mean a collection of different sets of built-in functions. 
 
Now if I want to calculate sqrt of a number, the function to calculate the square root is not present by default. So all we have to do is to import the module which has sqrt function and then apply it.

```
import math
math.sqrt(64)
```

Similarly, we can use python shell in interactive mode which opens as follows.


## Python Shell

Open a new tab in the terminal and type `python` and hit enter.
This should open python in interactive mode with `>>>` as shown.


When you type commands in the terminal/console window and press 'ENTER', they are executed immediately and the output is displayed. Here are few examples:  

```python
3+5
print("Welcome All !!!")
import math
math.sqrt(64) 
```

Symbol `>>>` means that the python is ready for the next command. If you enter incomplete commands, python will show SyntaxError or a Nameerror. 

Alright then, now we have Jupyter Notebook as Integrated Development Environment (IDE) and Python Shell in interactive mode.

**Is it same or is it different?** - Same.

**Do we need jupyter notebook for python programming?** - No, it is not needed.

Now that brings us to the next question.

**Which one should I use?**

## IDE for Python vs Interactive/Scripting Mode

Functionality is all the same. 

- But the advantage of Jupyter Notebook or any IDE for that matter is that, it integrates the work of a text editor and an interpreter for the language.  
- Also since it has a Graphical User Interface (GUI), it helps user to navigate through files and folders easier comparing the Python shell. 
- Further, More importantly, there are other functions and advantages like creating reports, exporting as markdown or pdf file, which we will discuss later during the course of the workshop.

For this workshop we will be working with Jupyter Notebook. 

:+1: 

**Now lets get started**

# 2. Building blocks of Python

Let's work in edit mode in Jupyter from now on so that you will have the record of all commands we used in this lesson.

## Variables/objects

One of the main concepts of any programming language is a notion of a variable. Variables are created to store values for future use.
To create a variable in python, use `=` as assignment operator:

```python
a = 5
print(a)

## For Characters or words or sentences, referred as strings in python, We enclose the value within double quotes/single quotes.

DNA = "ACT"
print(DNA)
```
We just created the smallest object in Python.

**Challenge 2.1**
    
```python
=====
TASK: What will be the value of each  variable  after each statement in the following code?
=====
mass = 47.5
height = 24.5
age = 122
mass = mass * 2.3
age = age - 20
height = height + 20      
```

As you can see, a variable is assigned a value equal to the value of the evaluated expression on the right side of the assignment operator. 

**A note on variable names:**
* NO SPACES in names
* DO NOT START with numbers
* Names should be MEANINGFUL - help yourself and others to understand your code! 

### Working with environment

#### List all variable defined in your environment

```python
who
```

#### Delete a specific variable in your environment

```python
del(DNA)
del(a)
```

#### To delete all the variables

```python
reset
```

## Functions

In general, a function takes an input and transforms it according to the function's definition(rules). You can recognize functions in python by the presence of parantheses. Objects in parantheses are called function's `arguments`.

### Print is a widely used function

```python
DNA = "ATG"
print(DNA)
```

- Here `print()` is a function.
- `(DNA)` is an argument to the function.

### To Apply square root function

```python
import math
a = 64
math.sqrt(a)
sqrt_a = math.sqrt(a)
print(sqrt_a)
```

- `math` is the module which has square root function. A module is a collection of several related functions. 
- `sqrt()` is the function
- `(a)` is the argument to the function.
- The square root of the `a` is now assigned to a new variable named `sqrt_a`
- `print()` function takes `sqrt_a` as argument and displays it to the user.

### Help function

help() is a very useful function. When help() is applied to a a module, it lists all the functions in the module and provides a brief summary on the utility of each function. When help() is applied to specific function it gives a quick summary of that particular function.

```python
help(math)
```

### Present directory is given by

```python
pwd
```

## Data types

Variables can hold values of various datatypes. Most common data types are:

  * int
  * float
  * str
  * bool
Let's assign 45 to a variable `age`. 

```python
age = 45

#some useful functions to know more about the object 
a = type(age)
print(a)

dna = "ATC"
a = type(dna)
print(a)

#some useful functions to know more about the object 
len(dna)
```

For example: What data type is stored in `score` variable?
```python
score = 79
print(type(score))
```
The last expression in the above example of nested function. Nested functions are very common in python, but are very difficult to understand at first. You can always split nested function into a series of single function calls. Remember that the variable inside the most inner paranthesis is an argument(input)for the function that will be evaluated first.


Sometimes you will need to convert between data types. There are functions that do that:  
  * int()
  * float()
  * str()
 
**Challenge 2.1: Learn how to read the output of nested help functions** 

```python
TASK: Break the following expression into multiple single function calls.
You will need to assign the output of each function to a variable that
will serve as an input(argument) for the next function. 
What is the value of each variable? What does each function do? 
Assign: `score = 79`

type(str(type(float(score))))
``` 

The conversion between data types is not always possible - why? Let's see what happens here:

```python
score = 79
type(score)
type(str(score))
##################
dna = "ATG"
type(dna)
type(int(dna))
```

## Data structures 

The small objects can be combined to build larger objects. Look at the gapminder dataset again. Our smallest objects can be used to represent a single element in the dataset, like individual year, or individual country, but what would be the simplest object that you can make with multiple elements?

### List

List is a data structure in python that holds different data types as a single list as an ordered sequence. Each value in the list is separated by comma (,) and is indexed. Indexing starts from 0.

For example:

```python
list = [5,6.7,"Texas"]
print(type(list))
```
>  Notice the use of square brackets.
 
 |list   |= |5 | 6.7 | "Texas" |
 |:----- |:-|:-|:----|:--------|
 ||From Left||
 |Index  |= |0 | 1   |  2      |
 ||From Right||
 |Index  |= |-3| -2  |  -1     |
 
```python
list = [5,6.7,"Texas"]
print(type(list[0]))
print(type(list[1]))
print(type(list[2]))
```
Now if you wanted to change a value say 6.7 to 5.4, you can do that. This property of the list is called `**mutable property**`

```python
list = [5,6.7,"Texas"]
list[1] = 5.4
print(list)
```
 
### Tuple

Tuples are similar to list. They can hold different data types as a list of values separated by comma(,).

For example:

```python
tuple = (5,6.7,"Texas")
print(type(tuple))
```

> Notice the use of simple brackets or parantheses.
 
 |tuple  |= |5 | 6.7 | "Texas" |
 |:----- |:-|:-|:----|:--------|
 ||From Left||
 |Index  |= |0 | 1   |  2      |
 ||From Right||
 |Index  |= |-3| -2  |  -1     |
 

> Now if you wanted to change a value say 6.7 to 5.4, you **CANNOT** do that. This property of the tuples makes them `**immutable**`

```python
tuple = (5,6.7,"Texas")
tuple[1] = 5.4
```

```
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-91-6b513665c9a0> in <module>()
----> 1 tuple[1] = 5.4

TypeError: 'tuple' object does not support item assignment
```
> But in list, we can do it. Therefore lists are `mutable`.

```python
list = [5,6.7,"Texas"]
list[1] = 5.4
print(list)
```

### Dictionary

A dictionary is a container that holds pairs of objects - keys and values. Each key-value pair is an element of the dictionary separated from the next element by a comma. Dictionary is not ordered or indexed as lists and tuples. Each value is accessible by its key and key can only be either a string or an integer data type. It can not be a list. But values in the list can be a list or a tuple.

```python
dictionary = {1:"one",2:"two",3:"three","dna":"atc","protein":"hyr"}
print(dictionary["dna"])
print(dictionary[3])
for (key,value) in dictionary.items():
    print (key,"--->",value)
```
> Notice the use of curly brackets

Now lets practice working with various data types by creating a dictionary.

```python
myOrder = 
{
menuItems:["chicken", "soup","salad","tea"],
menuType : ["solid","liquid","solid","liquid"],
menuCost : [4.99,2.99,3.29,1.89]
}
print(myOrder)
```

# 3.Data Frame with Pandas
  
One of the best options for working with tabular data in Python is to use the Python Data Analysis Library (a.k.a. Pandas). The Pandas library provides data structures, produces high quality plots with matplotlib and integrates nicely with other libraries that use NumPy (which is another Python library) arrays.

Python doesn’t load all of the libraries available to it by default. We have to add an import statement to our code in order to use library functions. To import a library, we use the syntax `import libraryName`. If we want to give the library a nickname to shorten the command, we can add as nickNameHere. An example of importing the pandas library using the common nickname pd is below.

```python
import pandas as pd
```

* Let's go back to gapminder dataset. Could you make an informative guess about how this data structure can be represented in python?

* Yes! It is a list of tuples of equal length, or a data frame. Data frames are extremely useful data structures as they represent table-like datasets. Let's look at our myOrder list to see if we can make data frame out of it. Is the list we just made suitable for a data frame? Yes, the elements of the list are vectors of equal size.

Previously we used `list[]` to combine our elements:

```
myOrder = {'menuItems':["chicken", "soup","salad","tea"],'menuType':["solid","liquid","solid","liquid"],'menuCost':[4.99,2.99,3.29,1.89]}
myOrder = pd.DataFrame(data=myOrder)
myOrder
```

### Importing the data using Pandas  

Let's copy the `gapminder.txt` to the present directory so that the original file is untouched.

```python
### For tab separated file
my_file = pd.read_table("gapminder.txt")
```
Similar to tab-separated file, you can use comma separated file as well as excel file.

```python
### For comma separated file
my_file = pd.read_csv("gapminder.csv")

### For excel file
my_file = pd.read_excel("gapminder.xlsx")
```

## Subsetting Dataframes

Now lets look at the top few lines and last few lines in the df.

```python
### Read in the first 10 lines of data frame
file_dataframe = my_file.head(10)

### Read in the last 10 lines of data frame
file_dataframe = my_file.tail(10)
```

:hushed::hushed::hushed:

There are three main options to achieve the selection and indexing activities in Pandas. They are:

1. Selecting data by indexing (.iloc)
2. Selecting data by label(.loc)
3. Selecting data by a conditional statment/logical statements 

### Selecting data by indexing (.iloc)

The first method that we will see is the **integer-based location indexing** or **iloc**. The rows are numbered from 0 through the end of rows. Similarly for columns, they are numbered from 0 through the end of the column.

So the general syntax is

```python
# For a specific row, column - Here in this case, the subset is a series
print(dataframe.iloc[row,column])

# For a set of rows and for a set of columns - Here its a dataframe
print(dataframe.iloc[[<row selection>],[<column selection>]])
```
Now, let us subset our gapminder dataset using iloc to understand its functionality better.

If you want to the first row and third column, we would subset using iloc as follows.

```python
print(my_file.iloc[0,2])  #first row, third column
```

- Remember the indexing starts from 0.

```python

#all rows, second column
print(my_file.iloc[:,2])  

#output as series - Series is a one-dimensional labeled array, like R's named list?
print(my_file.iloc[0,:])  

#same as above; can omit column index if want all columns
print(my_file.iloc[0])    

print(my_file.iloc[[0]])  #now dataframe is returned

#selecting multiple rows and columns:
print(my_file.iloc[0:2,1:3])

#series again
print(my_file.iloc[0:2,3])  

#data frame
print(my_file.iloc[0:2,[3]])  
print(my_file.iloc[[0,2,3],[1,3]])

```

### Selecting data by label(.loc)

The second method is subsetting dataframes using **label based indexing**. Now, the indexing can be set to a specific column or if we dont set the set, the the row numbers are used as labels by default.


```python
#subset by label: 
#data.loc[<row selection>, <column selection>] 
#df.set_index("last_name", inplace=True)  #can set index to unique column, or use row numbers as labels

print(my_file.head())
print(my_file.loc[:, ['year']])
print(my_file.loc[:, ['year','pop']])

#note that 0:2 is interpreted as  labels of the index. This use is not an integer position along the index
print(my_file.loc[0:2,['year']])  

#back to series
print(my_file.loc[0:2,'year']) 
```

### Selecting data by a conditional statment/logical statements 

The third method is selecting data by using conditional statements. Personally, this is the most useful method among the three. The syntax is similar

```python
#Logical selection
#data.loc[<row selection>, <column selection>] where row selection is based on logical Pandas series

#With logical selection, you pass an array or Series of True/False values to the .loc indexer to select the rows where your Series has True values.
print(my_file.head())

#all columns where country is Afghanistan
print(my_file.loc[my_file['country']=="Afghanistan"]) #all columns where country is Afghanistan

#logical Pandas series with TRUE values for rows where Afghanistan is present
ls=my_file['country']=="Afghanistan"  
print(ls.head(13))

#specify columns
print(my_file.loc[my_file['country']=="Afghanistan",['year', 'pop']])
```

**Challenge 3.1** Play with gapminder dataset:

```
TASK: Answer the following questions about `myData` object

1. Can you extract 3rd and 5th column of the dataset?
2. Can you extract the list of countries in this dataset?
### Hint: use unique(). ###
3. Can you get a part of this dataset that includes information about Sweden?
4. Can you extract all countries for which life expectancy is below 70?
5. Can you make a new column that contains population in units of millions of people?
```

**Challenge 3.1** Answers

```
1. my_file.iloc[:,[2,4]]
2. my_file.country.unique()
3. my_file[my_file.country == "Sweden" ]
4. my_file[my_file.lifeExp < 70]
5. my_file["PopM"] = pd.Series((my_file.iloc[:,4])/(10^6), index = my_file.index)
```
# 4.Writing Simple Scripts in Python

An Python script (or any other script) is a series of commands that are executed in the order they are written. The commands that we have executed one by one in python can be written to a text file and then executed all at once by running the file (which is now an pyhton script). Python scripts usually have .py extensions. Here is an example of a simple python script that will plot life expectancy over years for Canada.

```python
##This is  PlotLifeExp.py script

import pandas as pd
import matplotlib.pyplot as plt

#read data into python
my_file = pd.read_table("Data/gapminder.txt")

#my_file is a dataframe - check

#select information about Canada
Canada = my_file.loc[my_file['country'] == "Canada"]

#plot lifeExp 
Canada.plot.line(x='year',y='lifeExp',label = "Life Expectancy",figsize=(8, 6))
plt.suptitle('Life Expectancy in Canada Over the years', fontsize = 20)
plt.xlabel('Year', fontsize = 16)
plt.ylabel('Life Expectancy', fontsize = 16)
plt.show()  
```

You might want to save your plot as .png image. This requires only slight modification of our script.

```python
##This is  PlotLifeExp.py script

import pandas as pd
import matplotlib.pyplot as plt      

#read data into python
my_file = pd.read_table("Data/gapminder.txt")

#my_file is a dataframe - check

#select information about Canada
Canada = my_file.loc[my_file['country'] == "Canada"] 

#plot lifeExp 
Canada.plot.line(x='year',y='lifeExp',label = "Life Expectancy",figsize=(8, 6))
plt.suptitle('Life Expectancy in Canada Over the years', fontsize = 20)
plt.xlabel('Year', fontsize = 16)
plt.ylabel('Life Expectancy', fontsize = 16)
plt.savefig("PlotLifwExp.png")   
```

**Challenge 3.2**  Write your own python script
Write a script to calculate mean gdpPerCap for African and European countries.
Try to make a barplot to display your results.

You might need to read help for 'mean' and 'plot' functions
.mean()
plt.bar()

```python
##This is  MeanGdpPlot.py script

#Import pandas and pylab
import pandas as pd
import matplotlib.pyplot as plt      
import pylab

#read data into python
my_file = pd.read_table("gapminder.txt")

#select information about Africa
Africa = my_file[my_file.continent == "Africa"]

#calculate the mean
Africa_Mean = Africa.iloc[:,5].mean()

#Do the same for Europe
Europe = my_file[my_file.continent == "Europe"]
Europe_Mean = Europe.iloc[:,5].mean()

# Create a List to store the values
continents = ["Africa","Europe"]
mean_gdp = [Africa_Mean, Europe_Mean]

# Set figure width to 10 and height to 8
fig_size = plt.rcParams["figure.figsize"]
fig_size[0] = 10
fig_size[1] = 8
plt.rcParams["figure.figsize"] = fig_size

#Plot the graph with Y axis label and Title
plt.bar(continents,mean_gdp,align='center')
plt.ylabel('Mean GDP/Capita')
plt.title('Mean GDP per Capita in Africa Vs Europe')
pylab.show()
```

## Summary

:white_check_mark: This lesson introduced you to main ideas of programming: variables, functions, data structures and scripts. Now you can write your own simple programs in Python and begin understanding python code written by others. :end:

:soon: Next, we have Reports and Visualization. Using Python Reports our codes,analysis,results and interpretation of the results are made possible. They are created in Markdown format which makes it easier to use and publish.  

:soon: Further, Python has numerous packages which helps us to create different kinds plots from various analyses. We had a sneak peek using line plot :chart_with_upwards_trend: and bar plot:bar_chart:. We will learn more about plots in Visualization later in the day.

This is Balan signing off :wave: for Python Basics. Happy Learning :v:  

:sparkles::boom:
