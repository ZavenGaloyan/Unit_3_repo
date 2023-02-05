 # Code
 ```.py
 def mystery(list1, list2:list):
    output = []
    for i in range(len(list1)):
        for z in range(len(list2)):
            if list1[i] == list2[z]:
                output.append(list1[i])
    return output
```
 ## TEST Code
 ```.py
 import pytest
from Quiz_033_NEW import mystery

def test_empty_lists():
  assert mystery([], []) == []

def test_one_common_element():
  assert mystery([1, 2, 3], [3, 4, 5]) == [3]

def test_multiple_common_elements():
  assert mystery([1, 2, 3, 4], [3, 4, 5, 6]) == [3, 4]
 ```
## TEST Evidence
![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Quizzes/Quiz-033.jpg)
