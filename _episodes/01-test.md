---
# Please do not edit this file directly; it is auto generated.
# Instead, please edit 01-test.md in _episodes_rmd/
title: "Apryle Attempt"
teaching: 45
exercises: 0
questions:
- "this is my addition"
- "How do I read data into R?"
- "How do I assign variables?"
- "What is a data frame?"
- "How do I access subsets of a data frame?"
- "How do I calculate simple statistics like mean and median?"
- "Where can I get help?"
- "How can I plot my data?"
objectives:
- "Read tabular data from a file into a program."
- "Assign values to variables."
- "Select individual values and subsections from data."
- "Perform operations on a data frame of data."
- "Display simple graphs."
keypoints:
- "Use `variable <- value` to assign a value to a variable in order to record it in memory."
- "Objects are created on demand whenever a value is assigned to them."
- "The function `dim` gives the dimensions of a data frame."
- "Use `object[x, y]` to select a single element from a data frame."
- "Use `from:to` to specify a sequence that includes the indices from `from` to `to`."
- "All the indexing and subsetting that works on data frames also works on vectors."
- "Use `#` to add comments to programs."
- "Use `mean`, `max`, `min` and `sd` to calculate simple statistics."
- "Use `apply` to calculate statistics across the rows or columns of a data frame."
- "Use `plot` to create simple visualizations."
source: Rmd
---





## R Markdown - Apryle Changes

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

We are studying inflammation in patients who have been given a new treatment for arthritis,
and need to analyze the first dozen data sets.
The data sets are stored in [comma-separated values]({{ page.root }}/reference.html#comma-separated-values-csv) (CSV) format. Each row holds the observations for just one patient. Each column holds the inflammation measured in a day, so we have a set of values in successive days.
The first few rows of our first file look like this:


~~~
0,0,1,3,1,2,4,7,8,3,3,3,10,5,7,4,7,7,12,18,6,13,11,11,7,7,4,6,8,8,4,4,5,7,3,4,2,3,0,0
0,1,2,1,2,1,3,2,2,6,10,11,5,9,4,4,7,16,8,6,18,4,12,5,12,7,11,5,11,3,3,5,4,4,5,5,1,1,0,1
0,1,1,3,3,2,6,2,5,9,5,7,4,5,4,15,5,11,9,10,19,14,12,17,7,12,11,7,4,2,10,5,4,2,2,3,2,2,1,1
0,0,2,0,4,2,2,1,6,7,10,7,9,13,8,8,15,10,10,7,17,4,4,7,6,15,6,4,9,11,3,5,6,3,3,4,2,3,2,1
0,1,1,3,3,1,3,5,2,4,4,7,6,5,3,10,8,10,6,17,9,14,9,7,13,9,12,6,7,7,9,6,3,2,2,4,2,0,1,1
~~~
{: .output}



~~~
Error in eval(predvars, data, env): object 'tmp' not found
~~~
{: .error}

We want to:

* Load data into memory,
* Calculate the average value of inflammation per day across all patients, and
* Plot the results.

To do all that, we'll have to learn a little bit about programming.

### Loading Data
