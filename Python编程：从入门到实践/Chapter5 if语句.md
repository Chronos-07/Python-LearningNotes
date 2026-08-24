1、`if`语句的本质是条件测试，根据是否满足条件来决定执行代码，语句后面要加冒号
2、用两个等于号来进行条件比较，用`!=`来表示不相等
3、python对大小写敏感，大小写不同的值会被认为是不相等
4、`if`语句可以检查多个条件，若要检查两个条件是否都为`True`，可用关键字`and`把条件连接起来；如果只需要一个条件满足，则用`or`
5、检查特定条件是否在列表中用关键字`in`，例如
	```colors=['red','blue','yellow']
	if red in colors:
		print("True")
	>>>True```
6、检查特定条件是否不在列表中用关键字`not in`，例如
	```colors=['red','blue','yellow']
	if white not in colors:
		print("False")
	>>>False```
7、`if-else`语句，单层判断，通过则执行`if`语句，否则执行`else`
8、`if-elif-else`语句，逐层判定，`if`不满足则检查`elif`，均不满足则执行`else`。`elif`可以连续使用多层。`else`并不是这个语句的必须
9、`if`语句连续使用多次可以判断每个条件是否满足。
10、`if`语句和循环的嵌套，能够在遍历列表的同时，按照条件筛选元素，例如
	```
	colors=['red','blue','yellow']
	for color in colors:
		if color==red:
			print("True")
		else:
			print("False")```
同时还可以确定列表是否为空表，在`if`语句中将列表名用在条件表达式中时，在列表中至少包含一个元素时返回`True`，在列表空时返回`False`，例如
	```	colors=[]
	if colors:
		print("False")	```
11、在出现多个列表时，`if`语句可以用于寻找列表中的重复部分，例如
	```colors_1=['red','blue','yellow']
	colors_2=['blue','green','white']
	for color in colors_1:
		if color in colors_2:
			print("True")
		else:
			print("False")	```
