## Table of content

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Table of content](#table-of-content)
- [Basic](#basic)
	- [how to develop the scripts](#how-to-develop-the-scripts)
	- [how to use package/library/toolbox](#how-to-use-packagelibrarytoolbox)
	- [how to assign the value to a variable](#how-to-assign-the-value-to-a-variable)
	- [how to quit the environment](#how-to-quit-the-environment)
	- [how to comment the codes](#how-to-comment-the-codes)
	- [how to check help information](#how-to-check-help-information)
	- [how to clear variable in workspace](#how-to-clear-variable-in-workspace)
	- [how to debug your program](#how-to-debug-your-program)
- [General Operation on Array](#general-operation-on-array)
	- [how to create vector](#how-to-create-vector)
	- [how to check the dimension of the array](#how-to-check-the-dimension-of-the-array)
	- [how to transpose matrix](#how-to-transpose-matrix)
	- [how to index in the array](#how-to-index-in-the-array)
	- [how to find the index based on certain criterion](#how-to-find-the-index-based-on-certain-criterion)
	- [how to sort the numeric (string) array](#how-to-sort-the-numeric-string-array)
	- [how to concatenate the array (matrix)](#how-to-concatenate-the-array-matrix)
- [Basic Algorithmic Operation](#basic-algorithmic-operation)
- [File I/O](#file-io)
	- [how to read file](#how-to-read-file)
	- [how to write into file](#how-to-write-into-file)
- [Plots and Figure Customization](#plots-and-figure-customization)
	- [pre-requirement](#pre-requirement)
	- [general line plots](#general-line-plots)
	- [general bar plots](#general-bar-plots)
	- [general scatter plots](#general-scatter-plots)
	- [overlap one plot over another](#overlap-one-plot-over-another)
	- [customizing your figures](#customizing-your-figures)
	- [](#)
- [Advanced Plots and Visualization](#advanced-plots-and-visualization)
- [Object Oriented Programming](#object-oriented-programming)
- [Dealing with Efficiency and Performance](#dealing-with-efficiency-and-performance)

<!-- /TOC -->
----
## Basic

Both `python`, `R` and `Matlab` are dynamic programming high level language, which mean that one does not need to compile the script before running it. The codes are usually akin to writing a mathematical equation, excpet that some times one do not always use `=` to indicate assignment.

Except for __Matlab__ which is commercial software, both `python` and `R` are open source and are free for use.

### how to develop the scripts
- __python__: python script can be written with any note editor and save as `.py` file. For more complex development, one can use `PyCharm` software for a integrated development environment (IDE)
- __R__: R script can be written with any note editor and save as `.R` file. For complex development, one can use `RStudio` software
- __Matlab__: Matlab script can be written with any note editor and save as `.m` file. However, it is more common to directly write your script with Matlab software.

### how to use package/library/toolbox
- __python__: use `import` to load packages that are either installed or in your working directory
- __R__: use `library(library_name)` to load external library which should be installed via `install.packages("library_name")`
- __Matlab__: Matlab generally do not need to load external packages as most of them are integrated with Matlab software. Only functions may need to be `add` into your working space

### how to assign the value to a variable
- __python__: use `=` to assign the value.
- __R__: `<-`, `=`, `<<-` and `->` all work. `<-` is more general and is used for global scope, while `=` is more used for local scope.
- __Matlab__: use `=` for assignment.

### how to quit the environment
- __python__: use `quit`, `exit` or "CTRL + D"
- __R__: use `quit()`
- __Matlab__: use `exit`

### how to comment the codes
- __python__: use `#` to comment, e.g.,
```python
a = [[0,1,2], [3,4,5]] # this is the comment
```
- __R__: use `#` to comment, e.g.,
```r
a <- c(1,2,3) # this is the comment
```
- __Matlab__: use `%` to comment, e.g.,
```matlab
a = [1 2 3 ; 4 5 6]; % this is the comment
```

### how to check help information
- __python__: use `help()` to show basic information
- __R__: use `?function_name` to show help information
- __Matlab__: use `help function_name` to show help information

### how to clear variable in workspace
- __python__: use `del`
- __R__: use `rm()`
- __Matlab__: use `clear` or `cleanvars`

### how to debug your program


## General Operation on Array

### how to create vector
- __python__: use `[]` to create `list` or `numpy` array to achieve this, e.g.,
```python
>>> a = [[0,1,2], [3,4,5]] # normal way
>>> a = numpy.array([[0,1,2], [3,4,5]]) # numpy array
>>> a = numpy.array(range(0, 100)) # a sequence from 0 to 99
```
- __R__: use function `c()`, e.g.,
```r
a <- c(1,2,3) # a vector
b <- matrix(c(1,2,3,4,5,6), nrows = 2) # a 2 by 2 matrix
```
- __Matlab__: use `[]`, e.g.,
```matlab
a = [1,2,3,4];
b = [1 2 3 ; 4 5 6];
```

### how to check the dimension of the array
- __python__:
- __R__:
- __Matlab__:

### how to transpose matrix
- __python__: for numpy array, use `transpose()` function
- __R__: use `t()` function
- __Matlab__: use `'` or `trans()` function


### how to index in the array
- __python__: for numpy array, the index has the format of `[ini_index:end_index:step_index]`. Notice that the python index starts from __0__ and `end_index` is not included, e.g.,
```pytho
>>> x = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
>>> x[1:7:2]
array([1, 3, 5])
```
- __R__: the index of R is similar to Matlab, except that R use `[]` instead of `()`.
```r
>>> a <- c(2,4,2,1,4)
>>> a[3]
2
```
- __Matlab__: use either subscript indexing (i.e., row and column position) or single value indexing. Index starts from 1.
```matlab
>> a = (1:10);
>> a(1:3)
ans =
 			1 2 3
```

### how to find the index based on certain criterion
- __python__: use `[]` to create `list`, e.g.,
```python
a = numpy.array([[0,1,2], [3,4,5]])
idx1 = numpy.where(a==3) # ordinal index
idx2 = a == 3 # logical index
```
- __R__: use function `which()`, e.g.,
```r
a <- c(1,2,3)
idx1 <- which(a==3) # ordinal index
idx2 <- a == 3 # logical index
```
- __Matlab__: use `find()` or logical operator, e.g.,
```matlab
a = [1 2 3 ; 4 5 6];
idx1 = find(a==3); % ordinal index
idx2 = a==3; % logical index
```

### how to sort the numeric (string) array
- __python__: use `sorted()` function
- __R__:
- __Matlab__: use `sort()` function

### how to concatenate the array (matrix)
- __python__: use `sorted()` function
- __R__:
- __Matlab__: use `sort()` function



## Basic Algorithmic Operation


## File I/O

### how to read file
- __python__:  
- __R__: use `read.csv()` function
- __Matlab__: since R2014 release, user can use `readtable` to directly read file into table variable

### how to write into file


## Plots and Figure Customization

### pre-requirement
- __python__: plots in python usually requires `matplotlib` package. Other 3rd party packages may also be used for creating more fancy and even interactive plots. Examples are `plotly`
- __R__: although R comes with some build-in plot functions, it is more common to import other library to create appealing and fancy plots. Those libraries can be `ggplot` or `plotly` libraries;
- __Matlab__: Matlab usually provides adequate functions for making plots, by customizing figures with handle properties one can eventually create a professional looking plots. For web-based interactive plots, `plotly` api is a good candidiate to achieve this task

Since most of time we produce static figures for publication purpose, below I will only use `ggplot` for __R__ and `matplotlib` for __python__ in the examples.

### general line plots

### general bar plots

### general scatter plots

### overlap one plot over another


### customizing your figures

###


## Advanced Plots and Visualization

## Object Oriented Programming


## Dealing with Efficiency and Performance
