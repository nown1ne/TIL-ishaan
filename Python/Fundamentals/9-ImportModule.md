# Importing Modules:
# Local Library: 
### My_module:
The basic module we will be using for this example
```python

print('Imported my_module...')
test = 'Test String'

def find_index(to_search, target):
    '''Find the index of a value in a sequence'''
    for i, value in enumerate(to_search):
        if value == target:
            return i

    return -1
```

### How to import the module:

```python
import my_module as mm    # Imports the module and helps in seeting this up
# if no name specified then original module name must be used to call the Funtions

courses = ['History', 'Math', 'Physics', 'CompSci']

O/P
# Imported my_module...

index = mm.find_index(courses, 'Math')

O/P
# Imported my_module...
# 1
```

### Import function form a module
```python
form my_module import my_function,test         # Imports only the function (access to only that function)

courses = ['History', 'Math', 'Physics', 'CompSci']

index = find_index(courses, 'Math')
O/P
# Imported my_module...
# 1

print(test)                                     # Test String

# To import everything use *
form my_module import *                         # Not used, frowned upon as it hard to tell which function i imported form thr module and which funtion is used in file 
```

### sys.path funtion:
- Lists the directories on local machine where python checks for importing files
```python

import sys
print(sys.path)
```

### Adding paths for imorting files (Not supported):
```python
import sys
sys.path.append('$PATH')
```

### Python Path Environment Variable:
```bash
nano ~/bash_profile
```

# Standard Library:
### Location of Standard Library
```python
import os

print(os.__file__)
```
