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

### 练习题

1. 根据需求写代码

   dic = {'k1': "v1", "k2": "v2", "k3": [11,22,33]}

   （1）请在字典中添加一个键值对，"k4": "v4"，输出添加后的字典

   ```python
   dic["k4"] = "v4"
   print(dic)
   ```

   （2）请在修改字典中 "k1" 对应的值为 "alex"，输出修改后的字典

   ```python
   dic["k1"] = "alex"
   print(dic)
   ```

   （3）请在k3对应的值中追加一个元素 44，输出修改后的字典

   ```python
   dic['k3'].append(44)
   print(dic)
   ```

   （4）请在k3对应的值的第 1 个位置插入个元素 18，输出修改后的字典

   ```python
   dic['k3'].insert(0,18)
   print(dic)
   ```

2. 根据需求写代码

   ```
   dic1 = {
    'name':['pounds',2,3,5],
    'job':'teacher',
    '51devops':{'szk':['python1','python2',100]}
    }
   ```

   (1) 将name对应的列表追加⼀个元素’xxx’。

   ```python
   dic1["name"].append("xxx")
   print(dic1)
   ```

   (2) 将name对应的列表中的 pounds ⾸字⺟⼤写。

   ```python
   dic1["name"][0] = dic1["name"][0].capitalize()
   print(dic1)
   ```

   (3) 51devops 对应的字典加⼀个键值对 ’haoda’,’linux’。

   ```python
   dic1.get("51devops")["haoda"]="linux"
   print(dic1)
   ```

   (4) 将51devops对应的字典中的szk对应的列表中的python2删除

   ```python
   dic1["51devops"]["szk"].pop(1)
   print(dic1)
   ```

3.判断以下值那个能做字典的key ？那个能做集合的元素？

- 1

- -1

- “”

- None

- [1,2]

- (1,)

- {11,22,33,4}

- {‘name’:’szk’,’age’:18}

  ```py
  1	字典的key 集合的元素
  -1	字典的key 集合的元素
  “”	字典的key 集合的元素
  None	字典的key 集合的元素
  [1,2]	都不行
  (1,)	字典的key 集合的元素
  {11,22,33,4} 都不行
  {‘name’:’szk’,’age’:18}	都不行
  ```

4.将字典的键和值分别追加到 key_list 和 value_list 两个列表中，如：

```
key_list = []
value_list = []
info = {'k1':'v1','k2':'v2','k3':'v3'}
```

```python
key_list = []
value_list = []
info = {'k1':'v1','k2':'v2','k3':'v3'}
for k, v in info.items():
    key_list.append(k)
    value_list.append(v)
print(key_list)
print(value_list)
```

5.字典dic = {‘k1’: “v1”, “k2”: “v2”, “k3”: [11,22,33]}

a. 请循环输出所有的key

```python
for i in dic:
    print(i)
```

b. 请循环输出所有的value

```python
for i in dic:
    print(dic[i])
```

c. 请循环输出所有的key和value

```python
for i in dic:
    print(i)
    print(dic[i])
```

d. 请在字典中添加一个键值对，"k4": "v4"，输出添加后的字典

```python
dic.setdefault('k4','v4')
print(dic)
```

e. 请在修改字典中 "k1" 对应的值为 "szk"，输出修改后的字典

```python
dic["k1"] = 'szk'
print(dic)
```

f. 请在k3对应的值中追加一个元素 44，输出修改后的字典

```python
dic["k3"].append(44)
print(dic)
```

g. 请在k3对应的值的第 1 个位置插入个元素 18，输出修改后的字典

```python
dic["k3"].insert(0,18)
print(dic)
```

6.请循环打印k2对应的值中的每个元素。

```
info = {
    'k1':'v1',
    'k2':[('pounds'),('szk'),('51devops')],
}
```

```python
for i in info["k2"]:
    print(i)
```

7.输出商品列表，用户输入序号，显示用户选中的商品

```
"""
商品列表：
  goods = [
		{"name": "电脑", "price": 1999},
		{"name": "鼠标", "price": 10},
		{"name": "游艇", "price": 20},
		{"name": "美女", "price": 998}
	]
要求:
1：页面显示 序号 + 商品名称 + 商品价格，如：
      1 电脑 1999 
      2 鼠标 10
	  ...
2：用户输入选择的商品序号，然后打印商品名称及商品价格
3：如果用户输入的商品序号有误，则提示输入有误，并重新输入。
4：用户输入Q或者q，退出程序。
"""
```

```py
goods=[{'name':'电脑','price':1999},
    {'name':'鼠标','price':10},
    {'name':'游艇','price':20},
    {'name':'美女','price':996},]

while True:
    for value in goods:
        print(goods.index(value)+1,value['name'],value['price'])
    str_input = input('请输入你选择的序号，按Q或q退出:')
    if str_input.isdigit() and 0 < int(str_input) < len(goods):
        print(goods[int(str_input)-1]['name'],goods[int(str_input)-1]['price'])
    elif str_input.strip().upper() == 'Q':
        break
    else:
        print('输入有误，请重新输入！')
```

