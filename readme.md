# Splunk Practise Questions
## Statistical Processing Questions
Q1. The ___ command will always have _time as the X-axis.
Ans. | timechart

Question
02/15
If you use the stats command with two functions and a BY clause, which function is the BY clause applied to?
a. both functions
b. both functions if they are both aggregate functions
c. the first function
d. the second function

Ans. both fns

Question
03/15
The ___(X,Y) eval function returns X to the power of Y.
pow

Question
04/15
To display the least common values of a field, use the ___ command.
a. stats
b. top
c. rare
d. timechart with common=f option

Ans. C

Question
05/15
When using the top command, add the BY clause to ___.
a. specify which search mode to return results by
b. return results grouped by the field you specify in the BY clause
c. return a percentage of events
d. specify how many results to return

Ans. b


Question
06/15
True or False: Using an OVER and a BY clause with the chart command will create a multiseries data series.
FALSE
TRUE

Ans. T

Question
07/15
True or False: You can use wildcards (*) with the rename command to rename multiple fields that match a pattern.
Ans. T

Question
08/15
Which of these functions lists ALL values of the field X?
a. values(X)
b. list(X)

Ans. b

Question
09/15
By default, the sort command lists results in ___ order.
a. descending
b. ascending

Ans. b

Question
10/15
True or False: Only one field can be created when using the eval command.
FALSE
TRUE

Ans. F


Question
11/15
When you use the stats command with a BY clause, what is returned?
a. numerical statistics on each field if and only if all of the values of that field are numerical
b. one row
c. an error message because you did not include a statistical function
d. a statistical output for each value of the named field

Ans. d

Question
12/15
When renaming fields with spaces or special characters, use the rename command and include the new field name in ___.
a. double quotes
b. single quotes
c. parenthesis
d. None of the above

Ans. a

Question
13/15
Which of these eval functions takes no arguments?
a. random
b. min
c. max
d. pow

Ans.a

Question
14/15
Use ___=false with the chart command if you want to hide the OTHER column.
Ans. useother

Question
15/15
To round numerical values, use the ___ function of the eval command.
Ans. round()





# 


## 
```
conda activate --stack myenv
conda info --envs
conda env list
conda install -n myenv pip
conda activate myenv
conda install --file requirements.txt
```

# About Project and ScreenShots from Project
Have you experienced getting delayed Doctors appointment to get treated? Or had to go through a GP who later refers you to a specialized doc? Confused to which doc to consult?

Solution: Text categorization of medical health records using NLP to predict which doctor to consult with.
![image](https://user-images.githubusercontent.com/61950234/111899149-1103e380-8a01-11eb-9d7e-d1fdefac4d30.png)


### Citation for Dataset:
[mtsamples.com](https://www.mtsamples.com/) 


