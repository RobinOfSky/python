## 字符串 string
###字符串的介绍
用单引号或者双引号括起来的就叫做字符串 \
例如： 
```python 
name='robinary'
loc="tianjin"
```
### 字符串的输出
```print("name is:%s"%name)```

### 字符串的输入
```name=input('请输入要要输入的name')```

### 字符串的下标和切片
字符串的下标从左到右是从0开始，依次递增；但是从右往左是从-1开始的
[开始下标：结束下标：步长值]：**步长值表示在开始下标和结束下标之间经过步长值后输出的一个字符，一直循环输出字符，直到到结束下标的前一个字符**
> 注意：左闭右开的;如果没有开始下标值，那么开始下标默认从0开始；如果没有结束下标值，那么结束下标就是到尾部

> 注意：\
> 如果步长值是正值，从左往右取字符; 开始默认下标为0 结束默认下标为len-1\
> 如果步长值是负值，从右往左取字符; 开始默认下标为-1 结束下标默认为开始，怒能认为是0，也不能认为-1
```python
name="robinary"
print(name[::]) #这个表示输出整个字符串robinary
print(name[1:4]) #这个表示输出下标1开始到下标3结尾的字符串obi

#这四个都是从左到右输入name这个字符串，不会逆序输出的。
print(name[1:]) #这个表示输出从下表1开始的后面的所有的obinary
print(name[-4:] #这个表示输出小标-4开始的后面所有的nary
print(name[:4]) #这个表示输出下标从0开始到3结尾的所有的nary
print(name[:-3]) #这个表示输出下标从0开始到下标为-3的所有的robin

#带有正步长值的输出
print(name[1:4:2])# 输出值是oi

#带有负步长值的输出（注意
print(name[::-2])#输出为yaio
print(name[2:-7:-2]) #输出为b

#面试题：逆序答应字符串
print(name[::-1])或者print(name[-1::-1])
```
###字符串的常见函数操作

**find函数**：查找字符串中是否包含参数字符串，如果包含返回第一个字符的下标，否则返回-1
```python
str="welcome to study string"
str.find('str')  #结果为17
```
**index函数**：和find函数一样，但是index函数找不到会报错
```python
str="welcome to study string"
str.index('strya') 
```

**count函数**：返回出现字符串的次数 
```python
str.count('ing')
```
**split函数**：对字符串进行切割，可以有次数限制
```python
str.split(" ",2)
```
**capitalize()**：将字符串的第一个字符大写
```python
str.capitalize()
```
**title函数**：字符串的每一个单词的首字母大写
```python
str.title()
```
**startwith()**:字符串是否以给定参数开头，也就是第一个单词的前缀表达式
```python
str.startwith("wel")
```
**endwith()**字符串是否以参数结尾
```python
str.endwith("ya")
```
**lower**将字符串全部小写
```python
str.lower()
```
**upper**将字符串全部大写
```python
str.upper()
```
**ljust**返回一个原字符串左对齐，不足的空格填充
```python
str.ljust(20)
```
**rjust**返回一个原字符串右对齐，不足的空格填充
```python
str.rjust(20)
```
**center**使其居中显示，不足的空格填充
```python
str.ceter(20)
```
**lstrip**删除str左边空白字符
```python
str.lstrip()
```
**rstrip**删除str右边空白字符
```python
str.rstrip()
```
**strip**删除str两端的空格
```python
str.strip()
```
**rfind**和find()类似，但是从右边开始
```python
str.rfind("is")
```
**aprtition**将字符串分为三部分
```python
str.partition("er")
```
**rpartiton**从右边开始
```python
str.rpartition("er")
```
**splitlines**按行来划分，返回一个各行元素组成的列表
```python
str.splitlines()
```
**isalpha**如果都是字母返回True,否则返回False
```python
str.isalpha()
```
**isdigit**如果都是数字返回True,否则返回False
```python
str.isdigit()
```
**isalnum**如果都是字母或者数字返回True,否则返回False
```python
str.isalnum()
```
**isspace**如国只包含空格，返回True,否则返回False
```python
str.isspace()
```
**join**如果都是字母返回True,否则返回False
```python
str=" "
li="cwx is good boy"
str.join(li)
```
结果为：'c w x   i s   g o o d   b o y'

## 元组
里面的内容不可变和字符串一样；
创建一个元组```tuple=('name',185,4598.18,'a') ```
输出一个元组：print(tuple)
元组也是一个序列，所以可以对其这样输出想要的值：```tuple[1],tuple[:2],tuple[-2:]等 ```

删除一个元组，只能删除整个元组，不能删除其中的元素```del tuple  ```

元组的基本操作：
```python
tuple1=(1,2,3)
tuple1=(4,5,6)

元组的连接操作：tuple1+tuple2
元组的复制操作：tuple1*4
计算元祖的个数：count(tuple1)
元素是否存在：2 in tuple1 存在返回Ture 否则False
迭代：for x in tupel1:print(x)
```

元组的内含函数：
```
长度：len(tuple1)
最大值：max(tuple1)
最小值：min(tuple2)
将列表转换为元组tuple(list)
```

## 字典
```python
dic={'name':'cwx','sex':'man'}
```
字典注意的几个要点：
1. 键是唯一的，如果有重复，输出这个键的时候，只会输出这个相同键的最后一个值
2. 键只能是不能变类型，不能是列表等其他可变的键

修改字典得值：dic['name']='robin'
删除字典的值：del dic['name']
删除整个字典：dic.clear()

字典的内置函数：
1. len(dic)求字典的长度，即键的个数
2. str(dic)输出字典


##集合set
创建一个集合set ```a=set('sdwed) /b=set(('robin','cwx','tiger'))```
创建一个空集合只能使用set()创建，而不能使用{}，因为{}创建的是一个空字典

集合的基本操作：
1. 添加元素：add('a') add函数只能把里面的参数直接作为一个元素添加到集合中；但是update()函数，里面能放多个参数，并把每一个参数都添加到集合中。
2. 删除元素：remove() 不存在会报错
discard() 不存在不会报错
3. 清空集合：clear()
4. 长度：len()
5. 拷贝集合：copy()
6. 随机移除元素：pop()
7. 返回两个集合的并集：union()

