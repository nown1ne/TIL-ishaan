# Functions:
### Basic Function:
```python
def my_func()
  print('SUP')

my_func()           # SUP
```

### Returning with Funtions:
```python
def my_fun(add1,add2)
  return add1+add2

r = my_fun(1,2)
print(r)          # 3
```

### Positional Keyword Arguments:
- * args (Non-Keyword Arguments)
  - The special syntax *args in function definitions in Python is used to pass a variable number of arguments to a function. It is used to pass a non-keyworded, variable-length argument list. 
- ** kwargs (Keyword Arguments)
  - The special syntax ** kwargs in function definitions in Python is used to pass a keyworded, variable-length argument list. We use the name kwargs with the double star. The reason is that the double star allows us to pass through keyword arguments (and any number of them).

```python
def student_info(*args,**kwargs)
  print(args)
  print(kwargs)

student_info('Math','Art', name = 'John', age = 22)
O/P
# {'Math', 'Art'} // Tuples
# {'name' = 'John', 'age' = 22}

course = ['Math', 'Art']
info = {name = 'John', age = 22}

student_info(course,info)
O/P
# (['Math', 'Art'],{'name' = 'John', 'age' = 22}) 
# {}

student_info(*course,**info)      # Unpackes the values
# {'Math', 'Art'} // Tuples
# {'name' = 'John', 'age' = 22}
```

### Example:
```python
# Number of days per month. First value placeholder for indexing purposes.
month_days = [0, 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]


def is_leap(year):
    """Return True for leap years, False for non-leap years."""

    return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)


def days_in_month(year, month):
    """Return number of days in that month in that year.""" #Doc String which explains the functions functionality

    if not 1 <= month <= 12:
        return 'Invalid Month'

    if month == 2 and is_leap(year):
        return 29

    return month_days[month]
```
