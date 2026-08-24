1、用户输入使用`input()`函数，例如
	```message=input("Input somthing")
	print(message)
	输入内容敲回车即可输出	```
2、使用`int()`来获取数值输入，把字符串转变为整型数字表示。将数值输入用于计算和比较前，必须将其转换为数字表示。例如
	```age=input("Input age")
	age=int(age)
	if age>=18:
		print("True")	```
3、求模运算符%，返回两数相除的余数。
4、`while`循环的特点是不针对每个元素，而是不断运行，直到条件不满足为止。例如
	```num=1
	while num<3:
		print(num)
		num+=1	```
5、标志的使用。在程序中定义一个变量，称为标志，可以为`True`或`False`，程序通过判断标志的值来决定是否满足条件运行。例如
	```active=True
	while active:
		message=input("message")
		if message='quit':
			active=False
		else:
			print(message)```
6、使用`break`语句退出循环（包括`for` 和`while`），`break`跳过当前循环并继续执行后续代码
7、使用`continue`语句退出循环，结束本轮循环，跳过剩余代码，直接进行下一轮的循环。
8、在列表之间移动元素，使用`whlie+列表名`的形式，例如
	```current_colors=['red','blue','yellow']
	colors=[]
	while current_colors: #这里的循环将不断进行，直到这个列表变成空表
		colors=current_colors.pop()
	print(colors)
	>>>yellow
	blue
	red```
9、删除包含特定值的所有列表元素，使用`while+remove()`，例如
	```colors=['red','blue','yellow','red']
	while 'red' in colors:
		colors.remove('red')
	print(colors)
	>>>['blue', 'yellow']	```
10、使用用户输入填充字典，就是综合`input()+while+字典添加键-值对`，外加用标志控制循环。