1、变量名只能包含数字，字母和下划线，不能用数字打头
2、变量名不能有空格
3、不能用关键字当作变量名
4、用引号括起来的就是字符串，不管是单引号还是双引号
5、字符串全部大小写改写用`upper()/lower()`，首字母大写用`title`
6、合并、拼接字符串可以用+
     例如：
     ```python
     first_name="ada"
     last_name="lovelace"
     full_name=first_name+" "+last_name
     print(full_name)```
7、使用制表符`\t`来添加空白，使用`\n`来换行
8、删除字符串末尾空白使用方法`rstrip()`，例如
	```language="python "
	lang=language.rstrip()
	print(lang)
	>>>python #without space```
9、删除字符串开头空白使用方法`lstrip`，例如
	```language=" python"
	lang=language.lstrip()
	print(lang)
	>>>python #without space```
10、删除字符串两端空白使用方法`strip`，例如
	```language=" python "
	lang=language.strip()
	print(lang)
	>>>python #without space```
11、整型数据向字符型数据强制转换，防止类型报错用函数`str()`，例如
	```age=23
	message="happy"+str(age)+birthday
	print(message)```