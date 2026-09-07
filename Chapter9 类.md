1、创建类的关键字为`class`，类中的函数称为方法，例如
	```class Dog():
		def __init__(self,name age):
			self.name=name
			self.age=age
		def sit(self):
			print(self.name.title()+" is now sitting.")
		def roll_over(self):
			print(self.name.title()+" rolled over!")	```
对于上述程序，方法`__init__`是一个特殊的方法，每当根据这个类创建新实例时，会自动运行这个方法。在这个方法中，形参`self`必不可少，而且必须位于其他形参之前。
以`self`为前缀的变量都可以供类中的所有方法使用，可以通过类的任何实例来访问这些变量。可通过实例访问的变量称为属性
2、根据类创建实例，例如
	```mydog=Dog('Tom',6)	```
这行代码使程序调用方法`__init__`，创建一个特定的实例
3、要访问实例的属性，可以使用句点表示法，例如`mydog.name`。还可以使用句点表示法来调用类定义中的任何方法，例如`mydog.sit()`