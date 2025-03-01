---
redirect_from:
  - "/chapters/03/3/calls"
interact_link: content/chapters/03/3/Calls.ipynb
kernel_name: python3
has_widgets: false
title: 'Call Expressions'
prev_page:
  url: /chapters/03/2/1/Growth
  title: 'Example: Growth Rates'
next_page:
  url: /chapters/03/4/Introduction_to_DataFrames
  title: 'Introduction to DataFrames'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---


# Call Expressions

*Call expressions* invoke functions, which are named operations. The name of the function appears first, followed by expressions in parentheses. 



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
abs(-12)
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
12
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
round(5 - 1.3)
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
4
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
max(2, 2 + 3, 4)
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
5
```


</div>
</div>
</div>



In this last example, the `max` function is *called* on three *arguments*: 2, 5, and 4. The value of each expression within parentheses is passed to the function, and the function *returns* the final value of the full call expression. The `max` function can take any number of arguments and returns the maximum.

A few functions are available by default, such as `abs` and `round`, but most functions that are built into the Python language are stored in a collection of functions called a *module*. An *import statement* is used to provide access to a module, such as `math` or `operator`.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
import math
import operator
math.sqrt(operator.add(4, 5))
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
3.0
```


</div>
</div>
</div>



An equivalent expression could be expressed using the `+` and `**` operators instead.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
(4 + 5) ** 0.5
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
3.0
```


</div>
</div>
</div>



Operators and call expressions can be used together in an expression. The *percent difference* between two values is used to compare values for which neither one is obviously `initial` or `changed`. For example, in 2014 Florida farms produced 2.72 billion eggs while Iowa farms produced 16.25 billion eggs (http://quickstats.nass.usda.gov/). The percent difference is 100 times the absolute value of the difference between the values, divided by their average. In this case, the difference is larger than the average, and so the percent difference is greater than 100.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
florida = 2.72
iowa = 16.25
100*abs(florida-iowa)/((florida+iowa)/2)
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
142.6462836056932
```


</div>
</div>
</div>



Learning how different functions behave is an important part of learning a programming language. A Jupyter notebook can assist in remembering the names and effects of different functions. When editing a code cell, press the *tab* key after typing the beginning of a name to bring up a list of ways to complete that name. For example, press *tab* after `math.` to see all of the functions available in the `math` module. Typing will narrow down the list of options. To learn more about a function, place a `?` after its name. For example, typing `math.log?` will bring up a description of the `log` function in the `math` module.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
math.log?
```
</div>

</div>



    log(x[, base])

    Return the logarithm of x to the given base.
    If the base not specified, returns the natural logarithm (base e) of x.



The square brackets in the example call indicate that an argument is optional. That is, `log` can be called with either one or two arguments.



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
math.log(16, 2)
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
4.0
```


</div>
</div>
</div>



<div markdown="1" class="cell code_cell">
<div class="input_area" markdown="1">
```python
math.log(16)/math.log(2)
```
</div>

<div class="output_wrapper" markdown="1">
<div class="output_subarea" markdown="1">


{:.output_data_text}
```
4.0
```


</div>
</div>
</div>



The list of [Python's built-in functions](https://docs.python.org/3/library/functions.html) is quite long and includes many functions that are never needed in data science applications. The list of [mathematical functions in the `math` module](https://docs.python.org/3/library/math.html) is similarly long. This text will introduce the most important functions in context, rather than expecting the reader to memorize or understand these lists.

