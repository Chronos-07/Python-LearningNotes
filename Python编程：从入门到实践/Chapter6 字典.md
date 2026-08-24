1、字典是一系列键-值对，每一个键关联一个值，一个字典里可以包含多个键-值对。可以使用键来访问相关联的值。值可以是任何形式，数字，字符串，列表或字典。
2、访问字典的值，依次指定字典名和放在方括号里的值，例如
	```color={'red':'first'}
	print(color['red']) #注意这种引用方式
	>>>first	```
3、添加键值对就是直接对键进行赋值，例如
	```color={'red':'first','blue':'second','yellow':'third'}
	color[green]='forth'
	print(color)
	>>>{'red':'first','blue':'second','yellow':'third','green':'forth'}```
4、修改字典中的值就是直接对键进行赋新值，例如
	```color={'red':'first','blue':'second','yellow':'third'}
	color['red']=forth
	print(color)
	>>>{'red':'forth','blue':'second','yellow':'third'}```
5、永久删除字典中的键-值对用`del`语句，例如
	```color={'red':'first','blue':'second','yellow':'third'}
	del color['red']
	print(color)
	>>>{'blue':'second','yellow':'third'}	```
6、遍历字典用`for`循环，声明两个变量，用于存储键-值对中的键和值。这两个变量可以使用任何名称，例如
	```color={'red':'first','blue':'second','yellow':'third'}
	for key,value in color.items():
		print(key+value)
	>>>redfirst
	>>>bluesecond
	>>>yellowthird	```
方法`items()`返回一个键-值对列表，循环存入指定的两个变量中
7、遍历字典中的所有键用方法`keys()`，其作用是生成一个键的列表。例如
	```colors={'red':'first','blue':'second','yellow':'third'}
	for color in colors.keys():
		print(color)
	>>>red
	>>>blue
	>>>yellow```
想要按顺序遍历字典中的所有键，可以使用函数`sorted()`。和列表排序函数`sort()`排序原理基本相同。例如
	```colors={'red':'first','blue':'second','yellow':'third'}
	for color in sorted(colors.keys()):
		print(color)
	>>>blue
    >>>red
    >>>yellow```
8、遍历值和遍历键的原理相同，只不过方法关键字改为`values()`，同时也可以用`sorted()`进行排序遍历。
9、字典的嵌套。可以在字典中嵌套列表，在列表中嵌套字典或者在字典中嵌套字典。
