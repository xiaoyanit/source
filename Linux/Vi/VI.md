##VI常用命令

[参考博客](http://blog.163.com/iloveecho83@126/blog/static/172997525201102021242312/)

[vi命令大全.pdf](https://github.com/xiaoyanit/xiaoyanit.github.io/blob/master/Linux/Vi/vi%E5%91%BD%E4%BB%A4%E5%A4%A7%E5%85%A8.pdf?raw=true)

1. 显示行号

在命令行模式下输入：set nu

>拓展显示不可视字符:
	
	：set nu		显示行号 
	：set nonu	隐藏行号 
	：set ic		设置搜索时忽略大小写 
	：set noic	搜索时对大小写敏感 
	：set list	显示不可视字符 
	：set nolist	不显示不可视字符 
	：set showmode		显示当前操作模式 
	：set shownomode	不显示当前操作模式 
	：set		显示所有的vi环境变量设置 

######不常用：
	：set readonly		文件只读，除非使用！可写
	：set shiftwidth		反向制表符中的空格数目
	：set showmatch		在vi中输入），}时，光标会暂时的回到相匹配的（，{   （如果没有相匹配的就发出错误信息的铃声），编程时很有用
	：set tabstop		指定tab缩进的字符数目
	：set wrapscan		授索在文件的两端绕回
	：set autoindent		在插入模式下，对每行按与上行同样的标准进行缩进，与shiftwidth选项结合使用
	：set list		把制表符显示为^I ,用$标示行尾（使用list分辨尾部的字符是tab还是空格）


>set 设置可以在命令行输入，也可以写在$HOME下的.exrc (如果是vi)或者.vimrc(如果是vim)中。写进去很方便的。

2.文本输入模式（编辑模式--三种方式）：

	- i 插入 
	- o 打开 
	- a 添加 

3.要保存和退出文件（七种）


		：w		保存文件，不退出vi   
		：w 		new_filename	保存到文件new_filename中  
		：wq		保存修改退出vi   
		：x		保存修改并退出vi   
		：ZZ		保存修改且退出vi   
		：q!		不保存修改，退出vi   
		：wq!	保存修改，退出vi 


4.查找和替换文本，使用以下选项： 
>#### 命令功能 

		/string		向下查找字符串string 
		?string		向上查找字符串string 
		n		查找字符串string的下一个出现 
		N		查找字符串string的上一个出现 
		%s/old/new/g 	全局查找和替换 


5.位置定位

>#### 文本插入	
要插入或者添加文本，使用下面的选项： 
命令含义 

	a    在光标右侧输入文本   
	A	 在光标所在行的末尾输入文本   
	I	 在光标左侧输入文本   
	I	 在光标所在行的开头输入文本   
	O 	 在光标所在行的下一行开始新行   
	O	 在光标所在行的上一行开始新行  
 
>备注：vi编辑器是大小写敏感的，因此，使用命令时注意正确的大小写。

- - -
- - -

>#### 控制光标的移动键 
键功能
 
	h，		左箭头，退格键光标左移一个空格 
	j，		下箭头光标下移一行 
	k，		上箭头光标上移一行 
	l，		右箭头，空格键光标右移一个空格 
	w		光标右移，到下一个字开头 
	b		光标左移，到前一个字开头 
	e		光标右移，到下一个字末尾 
	$		光标右移到行结尾 
	0，^		光标左移到行开头 
	回车键	光标移到下一行开头 
	control-f	下翻一屏 
	control-d	下滚半屏 
	control-b	上翻一屏 
	control-u	上滚半屏 
	control-L	刷新屏幕 
	
 6.文本删除命令 
>####命令功能

	x	删除光标所在处的一个字符  
	dw	删除字（或者删除字的一部分，从光标所在处到字结尾）  
	dd	删除光标所在行  
	D	删除光标光标所在处之右的行  
	5，10d		删除5－10行  

>备注：命令3dw删除光标所在处开始的三个字，同样，3dd删除光标所在行开 始的3行。撤销、重复、修改文本命令 

7.文本编辑命令 
>命令模式，按Esc键即可： 


	cw		修改字（部分字，从光标所在处开始到一个字的结尾）   
	R		从当前光标所在处位置开始替换字符（注：vi将进入编辑模式）  
	C		从光标坐在处开始修改，到行末尾结束  
	s		用字符替换字符串  
	r		替换当前光标所在的字符  
	J		合并当前行以及下面行  
	Xp		转置光标所在处字符与另一字符  
	~		更改光标所在处字符大小写  
	u		放弃最近的修改  
	U		放弃对当前行所作的修改  
	：u		放弃上一个最后行命令（用于最后行模式）  
	：r filename		在当前光标所在处读入文件文本  

8.拷贝和粘贴
>拷贝命令把需要拷贝的文本放入一个临时缓冲区，粘贴命令从临时缓冲区中读取文本，并把文本写道当前文档的指定位置

	yy	（小写）复制一行文本，并将他们放入到临时缓冲区  
	p	（小写）将临时缓冲区中的内容放置到光标后面的位置  
	P	（大写）将临时缓冲区中的内容放置到光标前面的位置  
	：l，3 co 5		拷贝1－3行的文本，并把它放置在第5行后面  
	：4，6 m 8		移动4－6行到第8行，第6行称为第8行，第5行称为第7行，第4行称为第6行  



####参考资料

[vi 命令 用法](http://blog.csdn.net/xueziheng/article/details/2048054)

[linux下vi命令大全](http://www.cnblogs.com/88999660/articles/1581524.html)

[vi 常用命令行](http://www.cnblogs.com/sunormoon/archive/2012/02/10/2345326.html)

[vi命令一览表](http://www.21ds.net/article/23/308)




##查找命令Find
[ linux下查找某个文件位置的方法](http://blog.csdn.net/gray13/article/details/6365654)



find -name xxx
grep -rnw xxx


find . -maxdepth 1 -name "@*" 

>查找当前目录下以@开头的文件或者目录，搜索深度为一级也就是只在当前目录找，不进入子目录，如果你要从/目录开始找就：
`find / -maxdepth 1 -name "@*"` 
如果想搜全盘，就把-maxdepth 1 去掉




####[linux 下查找文件或者内容常有命令](http://www.cnblogs.com/sunleecn/archive/2011/11/01/2232210.html)


	whereis <程序名称> 查找软件的安装路径  
	-b 只查找二进制文件   
	-m 只查找帮助文件    
	-s 只查找源代码  
	-u 排除指定类型文件  
	-f 只显示文件名  
	-B <目录> 在指定目录下查找二进制文件  
	-M <目录> 在指定目录下查找帮助文件  
	-S <目录> 在指定目录下查找源代码  

	locate <文件名称>	在文件索引数据库中搜索文件  
	-d <数据库路径> 搜索指定数据库   
	updatedb	更新文件索引数据库  


	find [路径] <表达式> 查找文件  
	-name <表达式> 根据文件名查找文件  
	-iname <表达式> 根据文件名查找文件，忽略大小写  
	-path <表达式> 根据路径查找文件  
	-ipath <表达式> 根据路径查找文件，忽略大小写  
	-amin <分钟> 过去N分钟内访问过的文件  
	-atime <天数> 过去N天内访问过的文件  
	-cmin <分钟> 过去N分钟内修改过的文件  
	-ctime <天数> 过去N天内修改过的文件  
	-anewer <参照文件> 比参照文件更晚被读取过的文件  
	-cnewer <参照文件> 比参照文件更晚被修改过的文件  
	-size <大小> 根据文件大小查找文件，单位b c w k M G  
	-type <文件类型> 根据文件类型查找文件。b 块设备 c 字符设备 d 目录 p 管道文件   f 普通文件 l 链接 s 端口文件  
	-user <用户名> 按归属用户查找文件   
	-uid <uid> 按UID查找文件  
	-group <群组名> 按归属群组查找文件  
	-gid <gid> 按GID查找文件  
	-empty 查找空文件  


######从文件内容查找匹配指定字符串的行：  
	$ grep "被查找的字符串" 文件名 	从文件内容查找与正则表达式匹配的行：   
	$ grep –e “正则表达式” 文件名 	查找时不区分大小写：    
	$ grep –i "被查找的字符串" 文件名		查找匹配的行数：   
	$ grep -c "被查找的字符串" 文件名 		从文件内容查找不匹配指定字符串的行：
	$ grep –v "被查找的字符串" 文件名		从根目录开始查找所有扩展名为.log的文本文件，并找出包含”ERROR”的行  
	find / -type f -name "*.log" | xargs grep "ERROR"

	系统查找到httpd.conf文件后即时在屏幕上显示httpd.conf文件信息。 
  
	find/-name"httpd.conf"-ls

	在根目录下查找某个文件
	find . -name "test"

	在某个目录下查找包含某个字符串的文件  

	grep -r "zh_CN" ./

##查找命令grep

[转](http://blog.chinaunix.net/uid-25266990-id-199887.html)

从文件内容查找匹配指定字符串的行：
`$ grep "被查找的字符串" 文件名`

例子：在当前目录里第一级文件夹中寻找包含指定字符串的.in文件
`grep "thermcontact" */*.in`

从文件内容查找与正则表达式匹配的行：

`$ grep –e “正则表达式” 文件名`

查找时不区分大小写：

`$ grep –i "被查找的字符串" 文件名`

查找匹配的行数：

`$ grep -c "被查找的字符串" 文件名`


从文件内容查找不匹配指定字符串的行：
`$ grep –v "被查找的字符串" 文件名`


从根目录开始查找所有扩展名为.log的文本文件，并找出包含”ERROR”的行

`find / -type f -name "*.log" | xargs grep "ERROR"`
例子：从当前目录开始查找所有扩展名为.in的文本文件，并找出包含”thermcontact”的行

`find . -name "*.in" | xargs grep "thermcontact"`