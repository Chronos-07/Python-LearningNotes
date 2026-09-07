1、函数的定义、编写与调用，定义使用关键字`def`，函数内部就是一些简单的行为代码，调用函数则依次指定函数名以及用括号括起的必要信息。例如
	```def greet():
		print("Hello")
	greet()
	>>>Hello	```
2、在上述括号中添加信息，使函数能够接收给函数的任何值，叫做传参。定义函数时，括号中的参数为形式参数，调用时括号中的参数叫做实际参数，例如
	```def greet(user):
	print("Hello"+user)
	greet(Tom)
	>>>HelloTom	```
3、函数定义可以包括多个形参，传参过程中也可以包括多个实参。在调用函数时，每个实参必须关联到函数定义中的一个形参。最简单的关联方式时位置关联，基于实参的顺序进行关联，例如
	```def pet(size,age):
		print("The pet's size is "+size+" and is"+age+" years old")
	pet(large,forteen)
	>>>The pet's size is large and isforteen years old	```
4、函数可以在一个程序中调用多次，改变实参即可
5、函数传参还可以用关键字实参，这种传参方法不需要考虑形参与实参的位置是否匹配，例如
	```def pet(size,age):
		print("The pet's size is "+size+" and is"+age+" years old")
	pet(size='large',age='forteen')
	pet(age='forteen',size='large') #以上两种方法完全等效
	>>>The pet's size is large and isforteen years old	
	>>>The pet's size is large and isforteen years old		```
6、给形参确定默认值，在调用函数时，如果不指定形参对应的实参，则使用默认值，否则使用规定值。例如
	```def pet(size,age='forteen'):
		print("The pet's size is "+size+" and is"+age+" years old")
	pet(size='large')
	>>>The pet's size is large and isforteen years old
	或者更简单的调用
	pet('large')
	但是这个实参依然被视为位置实参，将关联函数定义的第一个形参```
使用默认值时仍需注意，在形参列表中默认值应该从右向左定义
7、函数具有返回值，函数能够处理一部分数据并返回一个特定值。盗用有返回值的函数时，要提供一个变量，用于存储返回的值，例如
	```def name(f_name,l_name):
		full_name=f_name+l_name
		return full_name
	people=name.('jimi','hendrix')
	print(people)
	>>>jimihendrix```
8、返回的不一定是值，还可以是字典等
9、对函数传递列表来实现对列表元素的整体操作，例如
	```def greet_users(names):
		for name in names:
			msg="Hello, "+name.title()+"!"
			print(mag)
	usernames=['hannah','ty','margot']
	greet_users(usernames)
	>>>Hello, Hannah!
	>>>Hello, Ty!
	>>>Hello, Margot!	```
10、传递任意数量的实参可以选用形参`*toppings`,其中`toppings`可以替换为任意参数名，例如
	```def make_pizza(*toppings):
		print(toppings)
	make_pizza('red')
	make_pizza('red','blue',,'yellow')
	>>>red
	>>>redblueyellow	```
任意数量形参和位置实参可以结合使用，注意将接纳任意数量实参的形参放在最后
11、使用任意数量的关键字实参，可以将函数编写成能够接受任意数量的键-值对，使用形参`**user_info`,其中`user_info`可以替换为任意参数名，例如
	```def bulid_profile(first,last,**user_info):
		profile{}
		profile['first_name']=first
		profile['last_name']=last
		for key,value in user_info.items():
			profile[key]=value
		return profile
	>>>{'first_name':'albert','last_name':'einstein','location':'princeton','field':'physics'}	```
12、将函数单独储存在模块文件中，并在主程序使用`import`语句引入整个模块，或使用`from module_name import function_name`导入特定的函数，其中`function_name`之间可使用逗号隔开，来导入任意数量的函数。
13、使用`as`给函数指定别名，如果要导入的函数名称和程序中现有的名称冲突或者函数名称过长，可以指定别名，例如
	```from pizza import make_pizza as mp	```
同样，可以使用这种方法对模块进行起别名
14、导入模块中的所有函数，使用`*`运算符，例如
	```from pizza import *	```