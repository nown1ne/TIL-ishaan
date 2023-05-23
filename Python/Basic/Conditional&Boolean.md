# Conditions:
- This sections contains code and explination for:
  - if conditionals
  - elif conditionals (else if)
  - else conditionals

### if:
Runs only when the condition is true
```python
# Comparisons:
# Equal:            ==
# Not Equal:        !=
# Greater Than:     >
# Less Than:        <
# Greater or Equal: >=
# Less or Equal:    <=
# Object Identity:  is

condition = 'Python'
if condition == 'Python':
    print('Evaluated to True')        # Evaluated to True
else:
    print('Evaluated to False')       # Printed when condition != python
    
# is comaparision 
a = [1,2,3]
b = [1,2,3]
print(a==b)                           # True
print(a is b)                         # False (as these are 2 different objects in memory[id(a)!=id(b)])

a = b
print(a is b)                         # True (as [id(a)==id(b)])
```

### elif:
Multiple checks are possible
```python
condition = 'Java'
if condition == 'Python':
    print('Python')           # Printed when condition == python
elif condition == 'Java':
    print('Java')             # Java
else:
  print('Nonce')              # Printed when condition != python && condition != Java
```

### Conditions: 
- and
- or
- not

# Boolean: 
### False Values:
**Values which compute to false**
- False
- None
- Zero of any numeric type
- Any empty sequence. For example, '', (), [].
- Any empty mapping. For example, {}.
