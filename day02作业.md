### day02作业

1. 写代码，有如下列表，按照要求实现每一个功能。

```
li = ["pounds", "szk", "haoda", "barry", "devops"]
```

- 计算列表的长度并输出

  ```py
  print (len(li))
  ```

- 请通过步长获取索引为偶数的所有值，并打印出获取后的列表

  ```python
  print (li[::2])
  ```

- 列表中追加元素”seven”,并输出添加后的列表

  ```python
  li.append("seven")
  print(li)
  ```

- 请在列表的第1个位置插入元素”Tony”,并输出添加后的列表

  ```python
  li.insert(0,"Tony")
  print(li)
  ```

- 请修改列表第2个位置的元素为”Kelly”,并输出修改后的列表

  ```python
  li[1]="Kelly"
  print(li)
  ```

- 请删除列表中的元素”haoda”,并输出添加后的列表

  ```python
  li.remove("haoda")
  print(li)
  ```

- 请删除列表中的第2个元素，并输出删除元素后的列表

  ```python
  li.pop(1)
  print(li)
  ```

- 请删除列表中的第2至第4个元素，并输出删除元素后的列表

  ```python
  li_r = li[2:5]
  for i in li_r:
      if i in li:
          li.remove(i)
  print(li)
  ```

2.写代码，有如下列表，利用切片实现每一个功能

```
li = [1, 3, 2, "a", 4, "b", 5,"c"]
```

- 通过对li列表的切片形成新的列表 [1,3,2]

  ```python
  li_n= li[:3]
  print(li_n)
  ```

- 通过对li列表的切片形成新的列表 [“a”,4,”b”]

  ```python
  li_n= li[3:6]
  print(li_n)
  ```

- 通过对li列表的切片形成新的列表 [1,2,4,5]

  ```python
  li_n= li[::2]
  print(li_n)
  ```

- 通过对li列表的切片形成新的列表 [3,”a”,”b”]

  ```python
  li_n= li[1:6:2]
  print(li_n)
  ```

- 通过对li列表的切片形成新的列表 [3,”a”,”b”,”c”]

  ```python
  li_n= li[1::2]
  print(li_n)
  ```

- 通过对li列表的切片形成新的列表 [“c”]

  ```python
  li_n= li[-1]
  print(li_n)
  ```

- 通过对li列表的切片形成新的列表 [“b”,”a”,3]

  ```python
  li_n= li[-3:0:-2]
  print(li_n)
  ```

3.写代码，有如下列表，按照要求实现每一个功能。

```
lis = [2, 3, "k", ["qwe", 20, ["k1", ["tt", 3, "1"]], 89], "ab", "adv"]
```

- 将列表lis中的”k”变成大写，并打印列表。

  ```python
  lis[2] = lis[2].upper()
  lis[3][2][0] = lis[3][2][0].upper()
  print(lis)
  ```

- 将列表中的数字3变成字符串”100”

  ```python
  lis[1] = '100'
  lis[3][2][1][1] = '100'
  print(lis)
  ```

- 将列表中的字符串”tt”变成数字 101

  ```python
  lis[3][2][1][0] = 101
  print(lis)
  ```

- 在 “qwe”前面插入字符串：”火车头”

  ```python
  lis[3].insert(0,"火车头")
  print(lis)
  ```

4.请用代码实现循环输出元素和值：users = [“szk”,”pounds”,”波姐”] ，如：

```
0 szk
1 pounds
2 波姐
```

```python
users = ["szk","pounds","波姐"]
for i in range(len(users)):
    print("%d %s"%(i,users[i],))
```

5.写代码实现以下功能

- 如有变量 googs = [‘汽车’,’飞机’,’火箭’] 提示用户可供选择的商品：

  ```
  0,汽车
  1,飞机
  2,火箭
  ```

- 用户输入索引后，将指定商品的内容拼接打印，如：用户输入0，则打印 您选择的商品是汽车。

  ```python
  googs = ['汽车','飞机','火箭']
  for i in range(len(googs)):
      print("%d,%s"%(i,googs[i]))
  buy = int(input("请输入购买的物品："))
  print("您选择的商品是%s"%(googs[buy]))
  ```

6.请用代码实现

```
li = "szk"
```

利用下划线将列表的每一个元素拼接成字符串”s_z_k”

```python
li = "szk"
li1 = "_".join(li)
print(li1)
```

7.利用for循环和range找出 0 ~ 100 以内所有的偶数，并追加到一个列表。

```python
li = []
for i in range(101):
    if i % 2 == 0:
        li.append(i)
    else:
        continue
print(li)
```

8.利用for循环和range 找出 0 ~ 50 以内能被3整除的数，并追加到一个列表。

```python
li = []
for i in range(50):
    if i == 0:
        continue
    elif i % 3 ==0:
        li.append(i)
print(li)
```

### 练习题

1.利用for循环和range从100~1，倒序打印

```python
list =[]
for i in range(100,0,-1):
    list.append(i)
print(list)
```

2.利用for循环和range循环1-30的数字，将能被3整除的添加到一个列表中，将能被4整除的添加到另外一个列表中。

```python
lis =[]
lis2 = []
for i in range(1,30):
    lis.append(i)
for j in range(len(lis)):
    if lis[j] % 3 == 0:
        print(lis[j])
for k in range(len(lis)):
    if lis[k] % 4 == 0:
        print(lis[k])
```

