## day01作业

#### 第二章作业

1.列举你了解的编码及他们之间的区别？

```python
ASCII: python2默认的编码，一个字母是8位
Unicode(万国码)：一个字母是32位
UTF-8：万国码的压缩码，最少用一个字节，最多用4个字节，一个中文是三个字节，24位
GBK: 专门用作汉文的编码，其中一个中文用两个字节
```

2.列举你了解的Python2和Python3的区别？

```python
区别一：默认解释器编码不同
python2:ASCII
python3:UTF-8
区别二：输入的语法不同
python2：raw_input
python3：input
区别三：输出的语法不同
python2：print 你想要输出的内容
python3：print（你想要输出的内容）
```

3.你了解的python都有那些数据类型？

```python
一、字符串（str）
二、整型（int）
三、布尔类型（bool）
```

4.补充代码，实现以下功能。

```
value =  _____ 
print(value)  # 要求输出  51devops"niubi
```

```python
value = ' 51devops"niubi'
print(value)
```

5.用print打印出下面内容：

```
⽂能提笔安天下,
武能上⻢定乾坤.
⼼存谋略何⼈胜,
古今英雄唯是君。
```

```python
print('''
⽂能提笔安天下,
武能上⻢定乾坤.
⼼存谋略何⼈胜,
古今英雄唯是君。
''')
```

6.变量名的命名规范和建议？

```python
命名规范：
一、只能由数字、字母、下划线组成；
二、不能以数字开头；
三、不能使用python关键字；
建议：
一、见名知意；
二、若需要用多个单词组成，用下划线连接；
```

7.如下那个变量名是正确的？

```
name = '51devops' 对
_ = 'echo' 对
_9 = "zhangsan" 对
9name = "xxx" 
devops(edu = 666
```

8.简述你了解if条件语句的基本结构。

```python
主要有三类：if ...
if ... else ...
if ...elif...else...
```

9.设定一个理想数字比如：66，让用户输入数字，如果比66大，则显示猜测的结果大了；如果比66小，则显示猜测的结果小了;只有等于66，显示猜测结果正确。

```python
number = input('请输入猜测的数字：')
number = int(number)
if number > 66:
    print('大了')
elif number < 66:
    print('小了')
else:
    print('猜对了')
```

10.写程序，成绩有ABCDE5个等级，与分数的对应关系如下.

```
A    90-100
B    80-89
C    60-79
D    40-59
E    0-39
```

要求用户输入0-100的数字后，你能正确打印他的对应成绩.

```python
score = input('请输入成绩(0-100):')
score = int(score)
if score >= 90:
    print('A')
elif score >= 80:
    print('B')
elif score >= 60:
    print('C')
elif score >= 40:
    print('D')
else:
    print('E')
```

11.模拟10086客服电话（条件语句的嵌套）

```python

```

#### 第三章作业

1.猜数字，设定一个理想数字比如：66，让用户输入数字，如果比66大，则显示猜测的结果大了；如果比66小，则显示猜测的结果小了;只有等于66，显示猜测结果正确，然后退出循环。

```python
while True:
    num = input('请输入数字：')
    num = int(num)
    if num > 66:
        print('猜测的结果大了')
    elif num < 66 :
        print('猜测的结果小了')
    else:
        print('猜测的结果正确')
        break
```

2.在上一题的基础，设置：给用户三次猜测机会，如果三次之内猜测对了，则显示猜测正确，退出循环，如果三次之内没有猜测正确，则自动退出循环，并显示‘大笨蛋’。

```python
count = 1
while count <= 3:
    num = input('请输入数字：')
    num = int(num)
    if num > 66:
        print('猜测的结果大了')
    elif num < 66:
        print('猜测的结果小了')
    else:
        print('猜测的结果正确')
        break
    count += 1
else:
        print('大笨蛋')
```

3.使用两种方法实现输出 1 2 3 4 5 6 8 9 10 。

```python
num = 1
while num <= 10:
    if num == 7:
        num = num + 1
        continue
    print(num)
    num = num + 1
```

4.求1-100的所有数的和

```python
count = 1
sum = 0
while count <= 100:
    sum = sum + count
    count = count + 1
print(sum)
```

5.输出 1-100 内的所有奇数

```python
num = 0
count = 1
while count <= 100:
    num = num + 1
    if num % 2 == 1:
        print(num)
    count = count + 1
```

6.输出 1-100 内的所有偶数

```python
num = 0
count = 1
while count <= 100:
    num = num + 1
    if num % 2 == 0:
        print(num)
    count = count + 1
```

7.求1-2+3-4+5 … 99的所有数的和

```python
sum = 0
count = 1
while count <= 99:
    if count % 2 == 1:
        sum = sum + count
    elif count % 2 == 0:
        sum = sum - count
    count = count + 1
print(sum)
```

8.⽤户登陆（三次输错机会）且每次输错误时显示剩余错误次数（提示：使⽤字符串格式化）

```python
count = 1
while count <= 3:
    username = input("用户名")
    password = input("密码")
    if username == "Agoni" and password == "123":
        print("登陆成功")
        break
    else:
        print("用户名或密码错误")
    print("当前输入%s次,剩余%s次" % (count, 3 - count))
    count = count + 1
```

9.猜年龄游戏
要求：允许用户最多尝试3次，3次都没猜对的话，就直接退出，如果猜对了，打印恭喜信息并退出。

```python
count = 1
while count <= 3:
    age = int(input("请输入年龄:"))
    if age > 18:
        print("猜大了")
    elif age < 18:
        print("猜小了")
    else:
        print("猜测正确")
        break
    count = count + 1
    if count > 3:
        choice = input("是否还想继续玩? Y or N")
        if choice == "Y":
            count = 1
        else:
            break
```

10.猜年龄游戏升级版
要求：允许用户最多尝试3次，每尝试3次后，如果还没猜对，就问用户是否还想继续玩，如果回答Y，就继续让其猜3次，以此往复，如果回答N，就退出程序，如何猜对了，就直接退出。

```python

```

#### 第四章作业

1. 有变量name = “szk zeNb “ 完成如下操作：

   - 移除 name 变量对应的值两边的空格,并输出处理结果
   - 判断 name 变量是否以 “sz” 开头,并输出结果（用切片）
   - 判断name变量是否以”Nb”结尾,并输出结果（用切片）
   - 将 name 变量对应的值中的 所有的”z” 替换为 “p”,并输出结果
   - 将name变量对应的值中的第一个”z”替换成”p”,并输出结果
   - 将 name 变量对应的值根据 所有的”z” 分割,并输出结果
   - 将name变量对应的值根据第一个”z”分割,并输出结果
   - 将 name 变量对应的值变大写,并输出结果
   - 将 name 变量对应的值变小写,并输出结果
   - 请输出 name 变量对应的值的第 2 个字符?
   - 请输出 name 变量对应的值的前 3 个字符?
   - 请输出 name 变量对应的值的后 2 个字符?

2. 有字符串s = “123a4b5c”

   - 通过对s切片形成新的字符串 “123”
   - 通过对s切片形成新的字符串 “a4b”
   - 通过对s切片形成字符串s5,s5 = “c”
   - 通过对s切片形成字符串s6,s6 = “ba2”

3. 使用while和for循环字符串 s=”asdfer” 中每个元素。

4. 使用while和for循环分别对字符串 message = “伤情最是晚凉天，憔悴厮人不堪言。” 进行打印。

5. 获取用户输入的内容，并计算前四位”l”出现几次,并输出结果。

6. 获取用户两次输入的内容，并将所有的数据获取并进行相加，如：

   ```
   """
   要求：
       将num1中的的所有数字找到并拼接起来：1232312
       将num1中的的所有数字找到并拼接起来：1218323
       然后将两个数字进行相加。
   """
   num1 = input("请输入：") # asdfd123sf2312
   num2 = input("请输入：") # a12dfd183sf23
   ```