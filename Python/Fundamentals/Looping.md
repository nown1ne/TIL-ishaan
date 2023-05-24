# For Loop:
```python
nums = [1,2,3,4,5]

# Break Statement
for num in nums                         # 1
  if num == 3                           # 2
    print ('Sup')                       # Sup
    break

# Continue Statement
for num in nums                         # 1
  if num == 3                           # 2
    print ('Sup')                       # Sup (after finding 3, it skipps the rest and goes to next iteration)
    continue                            # 4
  print(num)                            # 5

# Range Funtion: If you want to run through the loop a set number of times
# range (start value, end(not included))
for i in range(1, 5)                  # 1
  print(i)                            # 2
                                      # 3
                                      # 4
```

# While Loops:
- Runs until a certain condition is met
```python
x = 0

while True:
    if x == 3:                  # 0
        break                   # 1
    print(x)                    # 2
    x += 1
```
