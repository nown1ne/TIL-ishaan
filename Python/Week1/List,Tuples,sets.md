# List:
### Printing Specific Values:
```python
courses = ['History', 'Math', 'Physics', 'CompSci']
print(courses)      # ['History', 'Math', 'Physics', 'CompSci']

print(courses[0])   # History
print(courses[-1])  # CompSci (for index == -1 it points to last element)

print(courses[0:2]) ((or)) print(courses[:2])   # ['History', 'Math']
print(courses[2:-1]) ((or)) print(courses[2:])  # ['Physics', 'CompSci']

```
### Append and Pop:
Inserts at end of the List
```python
courses = ['History', 'Math', 'Physics', 'CompSci']
courses.append('Art')
print(courses)            # ['History', 'Math', 'Physics', 'CompSci', 'Art']

popped = courses.pop()
print(popped)             # Art
print(courses)            # ['History', 'Math', 'Physics', 'CompSci']
```

### Insert and Extend Function:
Insert at any position, if no value given then the value is appended
```python
courses = ['History', 'Math', 'Physics', 'CompSci']

courses.insert(0, 'Art')
print(courses)            # ['Art', 'History', 'Math', 'Physics', 'CompSci']

courses_2 = ['Art', 'Entertainment']

courses.insert(0, courses_2)
print(courses)            # [['Art', 'Entertainment'], 'Art', 'History', 'Math', 'Physics', 'CompSci']
print(courses[0])         # ['Art', 'Entertainment']

courses.extend(courses_2) # Individual Items are added to the List, not the list as a whole
print(courses)            # [['Art', 'Entertainment'], 'Art', 'History', 'Math', 'Physics', 'CompSci','Art', 'Entertainment']
```

### Remove Function:
Romove a perticular set value from the List
```python
courses = ['History', 'Math', 'Physics', 'CompSci']

courses.remove('Math')
print(courses)           #  ['History', 'Physics', 'CompSci']
```

### Reverse Function:
Reverses the order of the List
```python
courses = ['History', 'Math', 'Physics', 'CompSci']

courses.reverse()
print(courses)          # ['CompSci', 'Physics', 'Math', 'History']
```

### Sort and Reverse Sort Function:
Sorts the List wrt to the values Present
```python
courses = [3,2,4,1]

# Sort
courses.sort()
print(courses)          # [1,2,3,4]

# Reverse sort
courses.sort(reverse=True)
print(courses)          # [4,3,2,1]
```

### Sorted Function:
When we don't want to sort the original list, but obtain another sorted list
```python
courses = [3,2,4,1]

sorted_courses = sorted(courses)
print(courses)            # [3,2,4,1]
print(sorted_courses)     # [1,2,3,4]
```

### Min/Max/Sum:
Built-in functions that return the min, max and the sum of the List of Elements
```python
courses = [3,2,4,1]

print(min(courses))   # 1

print(max(courses))   # 4

print(sum(courses))   # 10
```

### Index Function and In Operator:
Used to find the index of a perticular element by value
```python
courses = ['History', 'Math', 'Physics', 'CompSci']

print(courses.index('CompSci'))     # 3

print('Math' in courses)            # True
print('Art' in courses)             # False
```


