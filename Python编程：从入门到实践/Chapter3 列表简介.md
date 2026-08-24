1、列表用[]表示
2、元素的索引，列表第一个元素索引为0，最后一个元素可以为-1（即为倒数第几个元素）
3、修改列表元素，先指定索引，再指定新值，例如
	```color=['red','blue','yellow']
	color[0]=white
	print(color)
	>>>['white','blue','yellow']```
4、在列表末尾增加元素用方法`append()`，例如
	```已知列表color=['red','blue','yellow']
	color.append(white)
	print(color)
	>>>['red','blue','yellow','white']	```
5、在列表中插入元素用方法`insert()`，在指定索引处添加空间，该索引处及右侧元素集体后移一个索引的位置，例如
	```已知列表color=['red','blue','yellow']
	color.insert(2,'white')
	print(color)
	>>>['red','blue','white','yellow']```
6、在列表中删除元素，使用`del`语句删除列表中任意位置的元素，例如
	```已知列表color=['red','blue','yellow']
	del color[0]
	print(color)
	>>>['blue','yellow']```
7、使用方法`pop()`可删除列表任意位置的元素，与`del`语句不同的是，这种方法仅仅把想要删除的元素从列表中弹出，并赋值给另外一个新的变量，并非物理意义上的删除。例如
	```eg1:删除元素
	已知列表color=['red','blue','yellow']
	color_popped=color.pop(0)
	print(color)
	>>>color=[blue','yellow']
	eg2:弹出元素
	已知列表color=['red','blue','yellow']
	color_popped=color.pop(0)
	print("My favourite color is"+" "+color_popped)
	>>>My favourite color is red	```
8、不知道想要删除元素的索引但是知道其值的时候，用方法`remove()`，与`pop()`类似，可以把删除的元素赋值给新变量并继续使用，需要注意的是，这个方法只能删除第一个指定的值，如果要删除的值可能在列表中出现多次，就要用循环判断，例如
	```eg1:删除元素
	已知列表color=['red','blue','yellow']
	color_removed=color.remove('red')
	print(color)
	>>>color=[blue','yellow']
	eg2:弹出元素
	已知列表color=['red','blue','yellow']
	color_removed=red
	color.remove(color_removed)
	print("My favourite color is"+" "+color_removed)
	>>>My favourite color is red	```
9、使用方法`sort()`对列表进行永久排序，如果列表元素是数字，则默认从小到大排序，如果是字符，则按照Unicode编码先后排序，例如
	```已知列表cars=['bmw','audi','toyota','subaru']
	cars.sort()
	print(cars)
	>>>['audi','bmw','subaru','toyota']```
也可以反向排序，向`sort()`方法传递`reverse=True`，即可完成倒序，例如`cars.sort(reverse=True)`
10、使用方法`sorted`对列表进行临时排序，能够按特定的顺序展示列表元素，不影响在列表中的原始排序。使用方法和`sort()`一样。如果想要倒序，也可以用`recerse=True`
11、倒着打印列表用方法`reverse()`，与上述两种方法不同，此方法只是简单倒序列表，不对其进行排序操作。
12、确定列表的长度用方法`len()`，与列表索引不同，计算长度时不会出现差一错误，列表的长度即为元素个数。例如
	```color=['red','blue','yellow']
	long=len(color)
	print(long)
	>>>3	```