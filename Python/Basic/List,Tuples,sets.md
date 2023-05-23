# List:
- Like Vectors, can be modified
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
### Looping:
```python
courses = ['History', 'Math', 'Physics', 'CompSci']

#basic for loop
for item in courses               # History
  print(item)                     # Math
                                  # Physics
                                  # CompSci

# Printing Index plus courses with specific start value (if no value specified start = 0)
for index, course in enumerate(course, start = 1)
  print(index, course)            # 1 History
                                  # 2 Math
                                  # 3 Physics
                                  # 4 CompSci
```

### List to Str(Join Function) and Str to List(Splitting Function):
Converting a List to a String by joining the List Elements using the String(,)
Converting
```python
courses = ['History', 'Math', 'Physics', 'CompSci']

# List to Str
courses_str = ', '.join(courses)
print(courses_str)                  # History, Math, Physics, CompSci

# Str to List
new_list = courses_str.split(', ')
print(new_list)                     # ['History', 'Math', 'Physics', 'CompSci']
```

# Tuples:
- Like arrays, can't be modified

```python
# Mutable
list_1 = ['History', 'Math', 'Physics', 'CompSci']
list_2 = list_1

print(list_1)       # ['History', 'Math', 'Physics', 'CompSci']
print(list_2)       # ['History', 'Math', 'Physics', 'CompSci']

list_1[0] = 'Art'

#Can't change the individual list (problem with lists)
print(list_1)       # ['Art', 'Math', 'Physics', 'CompSci']
print(list_2)       # ['Art', 'Math', 'Physics', 'CompSci']


# Immutable
tuple_1 = ('History', 'Math', 'Physics', 'CompSci')
tuple_2 = tuple_1

print(tuple_1)      # ('History', 'Math', 'Physics', 'CompSci')
print(tuple_2)      # ('History', 'Math', 'Physics', 'CompSci')

tuple_1[0] = 'Art'

# ERROR (tuple does'nt support item assignment)
print(tuple_1)      
print(tuple_2)      

```

# Set:
- Values that are unordered and non-duplicates

```python
cs_courses = {'History', 'Math', 'Physics', 'CompSci'}
print(cs_courses)             # No partiular Order of elements

```

### In function:
Sets are optimized for this operation
```python
cs_courses = {'History', 'Math', 'Physics', 'CompSci'}
print('Math' in cs_courses)             # True
```

### Intersection, difference and Union Method:
To find common elements between 2 sets
```python
cs_courses = {'History', 'Math', 'Physics', 'CompSci'}
art_courses = {'History', 'Art', 'Home_Science', 'CompSci'}
# Intersection
print(cs_courses.intersection(art_courses))             # {'History', 'CompSci'}

# Difference
print(cs_courses.difference(art_courses))               # {'Physics', 'Math'}

# Union
print(cs_courses.union(art_courses))               # {'History', 'Math', 'Physics', 'CompSci', 'Art', 'Home_Science'}
```

## Empty Values:
```python
# Empty Lists
empty_list = []
empty_list = list()

# Empty Tuples
empty_tuple = ()
empty_tuple = tuple()

# Empty Sets
empty_set = {} # This isn't right! It's a dict
empty_set = set()
```
