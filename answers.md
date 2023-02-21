# Big O Answers

## Snippet 1 -
### Big O: O(n)
### Explanation: loop pulls all n values for comparison
### Space - O(1) - item isn't saved, no other variables
```python
def largest(array, value):
  for item in array:
    if item > value:
      return False
  return True 
```


## Snippet 2 -
### Big O: O(n)
### Explanation: runs the n loop twice, but not exponentially
### Space: O(1) - doesn't create any new variables

```python
def info_dump(customers):
  
  print('Customer Names:')
  for customer in customers: 
    print(customer['name'])
  
  print('Customer Locations:')
  for customer in customers: 
    print(customer['country'])
  
```

## Snippet 3 -
### Big O: O(1)
### Explanation: constant time lookup of array, then comparison
### Space - O(1) - same

```python
def first_element_is_red(array):
  return array[0] == 'red' 
```

## Snippet 4 -
### Big O: O(n^2)
### Explanation: nested for loops over array; if statements are constant time
### Space - O(1)

```python
def duplicates(array):
  for index1, item1 in enumerate(array):
    for index2, item2 in enumerate(array):
      if index1 == index2:
        continue
      if item1 == item2:
        return True
  return False
``` 

## Snippet 5 -
### Big O: O(n*m)
### Explanation: nested for loops
### Space: O(n/m) - space depends on size of two variables

```python
words = ['chocolate', 'coconut', 'rainbow']
endings = ['cookie', 'pie', 'waffle']

for word in words:
  for ending in endings:
    print(word + ending)

```

## Snippet 6 -
### Big O: O(n)
### Explanation: loop over n elements
# Space: O(n) - space for variable

```python
numbers = [1,2,3,4,5,6,7,8,9,10]

def print_array(array):
  for item in array:
    print(item)

```

## Snippet 7 -
### Big O: O(n^2)
### Explanation: worst case would require about the full range each i
### Space: O(n) - assuming space for arr; arr is accessed but not resized

```python
# this is insertion sort
def insertionSort(arr): 
  for i in range(1, len(arr)): 
    key = arr[i] 
    j = i-1
    while j >=0 and key < arr[j] : 
      arr[j+1] = arr[j] 
      j -= 1
    arr[j+1] = key 
```

## Snippet 8 -
### Big O: O(n^2)
### Explanation: worst case
### Space: O(n) - my_list; min_idx constant

```python
for i in range(len(my_list)):
  min_idx = i
  for j in range(i+1, len(my_list)):
      if my_list[min_idx] > my_list[j]:
          min_idx = j

  my_list[i], my_list[min_idx] = my_list[min_idx], my_list[i]
```
