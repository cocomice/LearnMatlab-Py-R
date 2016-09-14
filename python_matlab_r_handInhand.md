##Table of content

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Table of content](#table-of-content)
	- [how to comment the codes](#how-to-comment-the-codes)
	- [how to create vector](#how-to-create-vector)
	- [how to find the index based on certain criterion](#how-to-find-the-index-based-on-certain-criterion)
	- [how to sort the numeric (string) array](#how-to-sort-the-numeric-string-array)
	- [how to concatenate the array (matrix)](#how-to-concatenate-the-array-matrix)
	- [how to read `csv` file](#how-to-read-csv-file)
	- [how to index in the array](#how-to-index-in-the-array)

<!-- /TOC -->

----
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


### how to create vector
- __python__: use `[]` to create `list`, e.g.,
```python
>>> a = [[0,1,2], [3,4,5]] # normal way
>>> a = numpy.array([[0,1,2], [3,4,5]]) # numpy array
>>> a = numpy.array(range(0, 100)) # a sequence from 0 to 99
```
- __R__: use function `c()`, e.g.,
```r
a <- c(1,2,3)
```
- __Matlab__: use `[]`, e.g.,
```matlab
a = [1 2 3 ; 4 5 6];
```

### how to find the index based on certain criterion
- __python__: use `[]` to create `list`, e.g.,
```python
a = numpy.array([[0,1,2], [3,4,5]])
idx = numpy.where(a==3)
```
- __R__: use function `c()`, e.g.,
```r
a <- c(1,2,3)
idx1 <- which(a==3)
```
- __Matlab__: use `find()` or logical operator, e.g.,
```matlab
a = [1 2 3 ; 4 5 6];
idx1 = find(a==3); % find()
idx2 = a==3; % logical operator  
```

### how to clear variable in workspace
- __python__: use `del`
- __R__: use `rm()`
- __Matlab__: use `clear` or `cleanvars`

### how to sort the numeric (string) array
- __python__: use `sorted()` function
- __R__:
- __Matlab__: use `sort()` function

### how to concatenate the array (matrix)
- __python__: use `sorted()` function
- __R__:
- __Matlab__: use `sort()` function


### how to read `csv` file
- __python__:  
- __R__: use `read.csv()` function
- __Matlab__: since R2014 release, user can use `readtable` to directly read file into table variable

### how to index in the array
- __python__: for numpy array, the index has the format of `[ini_index:end_index:step_index]`. Notice that the python index starts from __0__ and `end_index` is not included, e.g.,
```python
>>> x = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
>>> x[1:7:2]
array([1, 3, 5])
```
- __R__:
_ __Matlab__: use either subscript indexing (i.e., row and column position) or single value indexing. Index starts from 1.
```matlab
>> a = (1:10);
>> a(1:3)
ans =
 			1 2 3
```
