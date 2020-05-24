# Python Data Structures & Algorithms

## Arrays/Lists:

**Initialise 2d array**:
```python
arr = [[0 for i in range(m)] for j in range(n)] # Access arr[m][n]
```

**Adding & Deleting from a list**:
```python
arr.clear()
arr.pop(0)  # O(n) When deleting first element
stack.pop() # O(1) When deleting last element
stack.append(item) # O(1)
output.insert(0, item) # O(n) Insert item at index 0
``` 

**Iterating over multiple lists in parallel**: 
```python
for item1, item2 in zip(list1, list2): # Lists must be the same length
```

**Slicing from index to index**: 
```python
output[::-1] # Will reverse the list
output[2:5]  # Will only include index 2, 3, 4 (NOT 5)
output[2:]   # Will include index values from 2 until the end
output[:4]   # Will include first 4 elements
output[-3:]  # Will include last 3 elements
```

## Queues:

**Use Deque (Doubly linked list)**:
```python
from collections import deque
queue = deque()
queue.appendleft # O(1) Add to queue
queue.popleft # O(1) Remove first element from queue
```

## Strings:

**Replace a substring**:
```python
word.replace('abc', 'def')
```

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

**Convert list into string**:
```python
''.join(list1)  # Will concat each value together
'-'.join(list1) # Will concat each value with '-' in between each value
```

## Hashmaps/Dictionaries:

**Delete from Dictionary**:
```python
del my_dict['key'] # O(1) Deletes key and it's values
del my_dict['key'][0] # Deletes value
```

**Sorting Dictionary**:
```python
sorted(my_dict.items()) # Will sort based on key
sorted(my_dict.items(), key=lambda x:x[1]) # Will sort based on value
sorted(my_dict.items(), key=lambda x : (x[1], x[0])) # Will sort based on value, then sort keys alphabetically
```

**Values**:
```python
my_dict.items() # Returns a list of tuples of (key, value) pairs
my_dict.keys() # Returns a list of keys
my_dict.values() # Returns a list of values
```

**Collections**:
```python
from collections import defaultdict # A dictionary that will not throw an error at missing key lookups
from collections import Counter
count = Counter()
...
count.most_common(1)[0] # Will return (key, value) with the highest value
```


## Sets:


## Classes:

* __repr__

## Search:

**Iterative Binary Search**:
```python
def binarySearch(list1, value):
    low, high = 0, len(list1) - 1
    while low < high:
        # mid = low + (high - low) // 2
        mid = (low + high) // 2
        if value == list1[mid]:
            return mid
        elif value > list1[mid]:
            low = mid + 1
        else:
            high = mid - 1
    return low
```

**Recursive Binary Search**:

## Sorting:

**Bubble Sort**:
```python
def bubbleSort(arr):
    for i in range(0, len(arr) - 1):
        swapped = False
        for j in range(0, len(arr) - 1 - i):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        if swapped == False:
            break
```
**Merge Sort**:
```python
def mergeSort(arr): 
    if len(arr) <= 1: 
        return

    mid = (0 + len(arr)) // 2
    left = arr[:mid] 
    right = arr[mid:] 

    mergeSort(left) 
    mergeSort(right) 

    arr.clear()
    i, j = 0, 0
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            arr.append(left[i])
            i += 1
        else:
            arr.append(right[j])
            j += 1            

    arr += left[i:] + right[j:]
```

## Trees:

**Height of BST**:
```python
def height(root):
    if root == None:
        return 0
    elif root.left == root.right == None:
        return 0
    return 1 + max(height(root.left), height(root.right))
```

**Validate BST**:
``python
def helper(root, low, high):
    if root == None:
        return True
    elif root.data <= low or root.data >= high:
        return False
    return helper(root.left, low, root.data) and helper(root.right, root.data, high)

def checkBST(root):
    return helper(root, float("-inf"), float("inf"))
```
## Graphs:

## Linked Lists:

## String Manipulation:

## Dynamic Programming:

* Longest Common Subsequence

## Recursion:

