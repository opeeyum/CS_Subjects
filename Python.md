---
basicDs:
  - List
  - Tuple
  - Set
  - Dictionary
List:
 - Ordered collection of heterogeneous data types.
 - Ordered means every element has an index(subscript) associated to it.
 - Denotion: **[ ]**
 - List can have duplicate elements.
 - List is ***mutatable***, that is element(s) of list can be modified.
Tuple:
 - Ordered collection of heterogeneous data types.
 - Ordered means every element has an index(subscript) associated to it.
 - Denotion: **( )**
 - Tuple can have duplicate elements.
 - Tuple is ***immutatable***, that is element(s) of tuple ***cannot*** be modified.
#### Set
 - Unordered collection of heterogeneous data types.
 - Unordered means element(s)don't have an index(subscript) associated to it.
 - Denotion: **{ }**
 - Set ***cannot*** have duplicate elements.
 - Set is ***mutatable***, that is element(s) of tuple can be modified.
#### Dictionary
 - Ordered collection of Key-Value pair.
 - Ordered means dictionary remembers the order in which elements get inserted into the dictionary.
 - Denotion: **{ }**
 - Dictionary **cannot** have duplicate **Keys**.
 - Dictionary is ***mutatable***, that is values associated to key(s) can be modified.
---

# Data-types in Python
1. String  : str
2. Integer : int
3. Float   : float
4. Boolean : bool
5. Complex 

### Operator's

### Conditional Statement
```
if <condition>:
  pass

elif <condition>:
  pass
 
else:
  pass
```

### Loops
**For loop**:
```
for i in range(n):
  pass
```
**While loop**:
```
while <condition>:
  pass
```
`Note: Python don't support do while loop.`

### Basic data Structures


### Functions
**Declaration**:
```
def <function_name>(<input arguements>):
  pass
```
For example:
```
def add(a, b):
  return a+b
```
**Declaration with data type of input argument(s) and return variable**:
```
def add(a:int, b:float)->int:
  return a+b
```
