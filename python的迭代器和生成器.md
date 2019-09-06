### python的迭代器和生成器
1. 迭代器：迭代器是一个类，能够迭代对象(访问集合元素的一种方式)。有两个函数__iter__()和___next__().迭代器可以记住遍历位置的对象，迭代器从集合的一个元素开始访问，知道所有的元素被访问结束，只往前不后退。字符串，列表，元组，字典都可以创建迭代器，但是set集合不可以。
2. 创建一个列表迭代器`a=iter([1,2,3,5,6])`输出迭代器`print(next(a))`，也可以for,while循环输出：

```
for i in a:
	print(a)
```
3. 自定义迭代器类（必须包含__iter__()方法）

```python
class iterTest:
	def __init__(self.step):
		self.step=step
	def __iter__(self):
		self.a=1
		return self
	def __next__(self):
		try:
			if self.step<=0:
		except StopIteration:
		self.step += 1
		return self.a
```
4. 生成器：yield函数被称为生成器，跟普通函数不同的是，生成器是一个返回迭代器的函数，只能用于迭代操作。在调用生成器运行的过程中，每次遇到yield函数都会暂停并保存当前所有的信息，返回yield的值，并在下一次执行next（）的时候从单签位置开始。

```
def fibonacci(n):
	a,b,count=0,1,0
	while True:
		if(count>n):
			return
		yield a
		a,b=b,a+b
		count += 1

f=fibonacci(20)
#f是一个迭代器，有生成器返回生成


while True:
	try:
		print(next(f),end=" ")
	except StopIteration:
		sys.exit()
```

