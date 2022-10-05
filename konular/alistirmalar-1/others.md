# Others

Group Elements of Same Indices

```
inputLists = [[10, 20, 30], [40, 50, 60], [70, 80, 90]]
outputLists = []
index = 0

for i in range(len(inputLists[0])):
    outputLists.append([])
    for j in range(len(inputLists)):
        outputLists[index].append(inputLists[j][ index])
    index = index + 1

print(outputLists)
# Output : [[10, 40, 70], [20, 50, 80], [30, 60, 90]]
```

Find Missing Number using Python

```
def findMissingNumbers(n):
    numbers = set(n)
    length = len(n)
    output = []
    for i in range(1, length + 1):
        if i not in numbers:
            output.append(i)
    return output

listOfNumbers = [1, 2, 3, 5, 6, 7, 8, 9]
print(findMissingNumbers(listOfNumbers))
```

Index of the Maximum Value in a List

```
def maximum(x):
    maximum_index = 0
    current_index = 1
    while current_index < len(x):
        if x[current_index] > x[maximum_index]:
            maximum_index = current_index
        current_index = current_index + 1
    return maximum_index
a = [23, 76, 45, 20, 70, 65, 15, 54]
print(maximum(a))
```

İki listede birbirinden benzersiz olanları listeyen fonksiyon \[1,2,3] ve \[1,2,4] -> \[3]

```
list1 = [1, 2, 3]
list2 = [1, 2, 4]

def difference(data_1, data_2):
    diff = []
    for item in data_1:
        if item not in data_2:
            diff.append(item)

    return diff

print(difference(list1, list2))
```

İki listedeki benzersiz olanları listeleyen fonksiyon \[1,2,3] ve \[1,2,4] -> \[3, 4]

```
list1 = [1, 2, 3]
list2 = [1, 2, 4]

def symmetric_difference(data_1, data_2):
    diff = []
    for item in data_1:
        if item not in data_2:
            diff.append(item)

    for item in data_2:
        if item not in data_1:
            diff.append(item)

    return diff

print(symmetric_difference(list1, list2))
```

