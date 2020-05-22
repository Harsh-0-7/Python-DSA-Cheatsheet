# Python Data Structures

## Arrays/Lists:

**Prepending an item to a list**: 
```python
output.insert(0, item)
``` 

**Iterating over multiple lists in parallel**: 
```python
for item1, item2 in zip(list1, list2):
```

**Slicing from index to index**: 
```python
output[::-1] # Will reverse the list
output[2:5]  # Will only include index 2, 3, 4 (NOT 5)
output[2:]   # Will include index values from 2 until the end
output[:4]   # Will include first 4 elements
output[-3:]  # Will include last 3 elements
```

## Strings:

**Count the occurances of a letter**:
```python
word.count('a') # Number of times a is in the string
```

**If Strings starts or ends with a substring**:
```python
word.startswith('a')
word.endswith('bcd')
```

**Letter positioning**:
```python
ord('a') # Will return 97
chr(97)  # Will return 'a'
```

**Case Conversion**:
```python
word.lower() # To lowercase
word.upper() # To uppercase
```

**Find index of substring**:
```python
word.find('abc') # Returns the starting index of substring, otherwise -1 if not found
```

**Strip spaces**:
```python
word.strip()  # Remove whitespace from both ends
word.rstrip() # Remove whitespace from right end
word.lstrip() # Remove whitespace from left end
```

## Sorting:

## Search:

## Trees:

## Graphs:

## Stacks:

## Queues:

## Linked Lists:

## String Manipulation:

## Hashmaps/Dictionaries:

## Dynamic Programming:

## Recursion:

