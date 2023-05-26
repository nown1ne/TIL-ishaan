### Print function:
```python
#Prints string
print('Message')  # Message

#Print variable
age = kids
print(age)        # Kids
```

### String variable:
  **Using \* functions:**
  ```python
  # Use \' to show ' if string defined in single quotes
  age = 'Ishaan\'s playground' ((or)) "Ishaan's playground"
  print(age)     # Ishaan's playground
  ```

  **Multiline output:**
  ```python
  # Use """ to give multi line output
  message = """Hello my name            # Hello my name 
  is Ishaan, i like                     # is Ishaan, i like
  dogs"""                               # dogs
  ```
1) Functions of String variable:
- Length Funtion
```python
print(len(age))        # 4
```
- Accessing Specific elements(Slicing):
```python
print(age[0])                                 # K
print(age[0:2]) ((or)) print(age[:2])         # Ki (inclusive:non-inclusive)
print(age[2:4]) ((or)) print(age[2:])         # ds (inclusive:non-inclusive)
```
- Lower and upper case:
```python
print(age.lower())    # kids
print(age.upper())    # KIDS
```
- Count Function:
```python
message = lllmmmok
# count specific elements in a string
print(message.count('l'))     # 3
print(message.count('ok'))  # 1
```
- Find Function:
```python
# Prints the starting index of string in find function
print(message.find('ok'))     # 6
```
- Replace Function:
```python
message = "hello world"
message = message.replace('World','Universe')
print(message)      # hello Universe
```
- fstrings
```python
greeting = 'Sup'
Name = 'Ishaan'

message = '{}, {}. Welcome!'.format(greeting,Name)
((or))
message = f'{greeting}, {Name}. Welcome!'

print(message)    #Sup, Ishaan. Welcome!

# edit inside the placeholders{}
message = f'{greeting}, {Name.upper()}. Welcome!'

print(message)    #Sup, ISHAAN. Welcome!
```
- dir Function
Shows all the attributes and function we have access to for the particular variable passed
```python
message = 'lol'
print(dir(message))
```
- help Function
Gives inforamtion about the various procceses which can run on a particular data type, can't pass variable
```python
print(help(str))    # help for string 
print(help(int))    # help for integer
```
