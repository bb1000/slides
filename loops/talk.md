---
kernelspec:
    name: python
    display_name: 'Python 3'
---
# loops


---

<!--
layout: false
-->

## Concepts

* loop header
* loop variable
* loop body
* `for` - `in` and  while keywords
* `break` and `continue` keywords
* `else` keyword

---

## Repetition in programming

- It is common to want to repeat a block of code multiple times.
- For example do something over and over until a condition is met
- Or repeat some instruction a certain number of times
    
---

Example:

```{code-cell} python
# print a multiplication table 7

product = 1 * 7
print('1 x 7 =', product)

product = 2 * 7
print('2 x 7 =', product)

product = 3 * 7
print('3 x 7 =', product)
```

- Code is repeated with small variations

---

- Extract what is varying to a variable, such that the repeated code looks the
  same

```{code-cell} python
# print a multiplication table 7

i = 1
product = i * 7
print(f'{i} x 7 =', product)

i = 2
product = i * 7
print(f'{i} x 7 =', product)

i = 3
product = i * 7
print(f'{i} x 7 =', product)

```

---

- Python has a syntax for this type of repetition: a `for`-loop
- In the header of a loop the assignment (`i = `) takes place
- The values given to the loop variable `i` is defined by a sequence after `in`
- A colon terminates the header line

~~~
for i in [1, 2, 3]:
    ...
~~~

- the remaining logic is identical for all turns and  make up the for loop body
- the body of the loop is indented with respect to the for keyword
  

~~~{code-cell} python
for i in [1, 2, 3]:
    product = i * 7
    print(f'{i} x 7 =', product)
~~~

##  What else?

### numbers

~~~python
for i in 1:
    product = i * 7
    print(f'{i} x 7 =', product)
~~~
~~~
TypeError                                 Traceback (most recent call last)
Cell In[4], line 1
----> 1 for i in 1:
      2     product = i * 7
      3     print(f'{i} x 7 =', product)

TypeError: 'int' object is not iterable
~~~

* You can't loop over a number

### strings

~~~{code-cell} python
for i in 'hello':
    product = i * 7
    print(f'{i} x 7 =', product)
~~~

* strings are fine
* the loop variable gets one character at a time
