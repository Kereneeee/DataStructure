```python
#暖身
#Leedcode 題目
from typing import List
def two_sum(nums:List[int],target:int) -> List[int]:
    for i in range(len(nums)):
        for j in range(i+1,len(nums)):
            if nums[i]+nums[j] == target:
                return [i,j]
print(two_sum([2,7,6,5],9)) 
```

    [0, 1]
    

# **DataStructure and Algorithm W1**

https://detexify.kirelabs.org/classify.html (用來切換LaTex的)


### **The introduction of DataStructure and Algorithm**
Data Organization
- Ways to arrage data in memory and on storage media
- How individual data element are group and found relative to one another

Algorithm
- The procedure to use data

Data Structure = Data Organization + Algorithm

### **Why we should learn datastructure?**
Efficiency
- Quick access to the data (食材/工具)
- The order of operations (食譜步驟)
- The number of operations (運算的數量)

### **Data Structure VS. Database**
![DataStructure vs. database.png](<datastructure_algorithm_files/DataStructure vs. database.png>)

### **The basic concept**
The 4 Primary Operations
- INSERTION 插入
- DELETION 刪除
- SEARCH 搜尋
- TEAVERSAL 遍歷 (Step through all the items in the group and perform some operation)

![Datastructure-closet.jpeg](datastructure_algorithm_files/Datastructure-closet.jpeg)  
- 陣列(Array)--索引存取
- 佇列(Queue)--先進先出
- 堆疊(Stack)--後進先出


```python
#串列元素相加
def sum(arr,n):
    total = 0               #1
    for i in range(n):      #n
        total += arr[i]     #n
    return total            #1

# 2n + 2
# Big-O = O(n)
```


```python
#矩陣相加
def add(a,b,c,n):
    for i in range(n):                      #n
        for j in range(n):                  #n(n)
            c[i][j] = a[i][j] + b[i][j]     #n(n)

# 2n^2 + n
# Big-O = O(n^2)
```


```python
# 矩陣相乘
def multiply(a,b,c,n):
    for i in range(n):                      #n
        for j in range(n):                  #n(n)
            sum = 0                         #n(n)
            for k in range(n):              #n(n)(n)
                sum = a[i][k] + b[k][j]     #n(n)(n)
            c[i][j] = sum                   #n(n)

# 2n^3 + 3N^2 + n
# Big-O = O(n^3)
```


```python
#循序搜尋
def search(data,target,n):
    for i in range(n):              #n
        if target == data[i]:       #n
            return i                #1

# 2n + 1
# Big-O = O(n)
```

### **Big-O**
<描述一個演算法的**上界**>
執行時間 = 次數 x 所需時間
- 簡化--時間固定，只計算每一敘述執行次數就可以了
- Big-O : 次數加總後的最高次方項

### **Big-Omega notation**
<衡量**至少**所需花費的時間>


### **Big-Theta**
<同時找到**上限**upper bound和**下限**lower bound>

