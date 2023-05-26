# Dictionaries:
- Works with key value pairs, like Hashmap

```python
student = {'name': 'John', 'age': 25, 'courses': ['Math', 'CompSci']}

print(student['name'])        # John
print(student['courses'])     # ['Math', 'CompSci']
print(len(student))           # 3 (number of keys)
print(student.keys())         # dict_keys(['name', 'age', 'courses'])
print(student.values())       # dict_values(['John', '25, ['Math', 'CompSci']])
print(student.items())        # dict_items([('name', 'John'), ('age', 25), ('courses',['Math', 'CompSci'])])
```

### Get method:
- Done so, when calling a key which is not present it returns given value and program doesn't crash
- If no value is given, the funtion returns None
```python
student = {'name': 'John', 'age': 25, 'courses': ['Math', 'CompSci']}

print(student.get('name'))                    # John
print(student.get('phone','Not Found'))       # Not Found 
```

### Update and add Keys:
```python
student = {'name': 'John', 'age': 25, 'courses': ['Math', 'CompSci']}

# Add keys:
student ['phone'] = '555-5555'
print(student)                    # {'name': 'John', 'age': 25, 'courses': ['Math', 'CompSci'], 'phone': '555-5555'}

# Update Keys:
student ['name'] = 'Michele James'
print(student)                    # {'name': 'Michele James', 'age': 25, 'courses': ['Math', 'CompSci']}

((or))

student.update({'name': 'Jane', 'age': 26 })
print(student)                    # {'name': 'Jane', 'age': 26, 'courses': ['Math', 'CompSci']}
```

### Delete or Pop Keys:
```python
student = {'name': 'John', 'age': 25, 'courses': ['Math', 'CompSci']}

# Delete
del student['age']
print(student)                    # {'name': 'John', 'courses': ['Math', 'CompSci'],}

# Pop
popped = student.pop('name')
print(popped)                    # {'courses': ['Math', 'CompSci'],}
print(student)                   # John
```

### Looping:
```python
for key, value in student.items():
    print(key, value)                   # name John
                                        # age 25
                                        # courses ['Math', 'CompSci']
```
