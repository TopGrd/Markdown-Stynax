#Markdown语法详解
#标题#
Markdown 支持两种标题的语法，类 Setext 和类 atx 形式。
类 Setext 形式是用底线的形式，利用 `=` 最高阶标题）和 `-`（第二阶标题），例如：
	H1
	========
    H2
	-----
任何数量的=和-都是可以的.

类 Atx 形式则是在行首插入 1 到 6 个 `#` ，对应到标题 1 到 6 阶，例如：  

	#H1
    ##H2
    ...
    ######H6
##区块引用 Blockquotes
	>some tingsome tingsome tingsome tingsome tingsome tingsome tingsome tingsome tingsome tingsome ting
或者  
	>some tingsome tingsome ting
    >some tingsome ting2313  
效果
>some tingsome ting

##列表
无序列表使用星号、加号或是减号作为列表标记：
	
    * apple
    * banana
    * tomato
效果
* apple
* banana
* tomato
有序列表则使用数字接着一个英文句点：
		1. apple
    	2. banana
    	3. tomato
效果
1. apple
2. banana
3. tomato

##代码区块

Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以，例如，下面的输入

    这是一段代码
    这是第二行代码
##分割线
	* * *

	***

	*****

	- - -

	---------------------------------------
得
* * *
##链接
	[this is a link](http://github.com/topgrd)
产生
[this is a link](http://github.com/topgrd)

如果你是要链接到同样主机的资源，你可以使用相对路径：

	See my [About](/about/) page for details
如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：

	[this is a link](http://github.com/topgrd/ "dasda")
 隐式链接标记功能让你可以省略指定链接标记，这种情形下，链接标记会视为等同于链接文字，要用隐式链接标记只要在链接文字后面加上一个空的方括号，如果你要让 "[Google]" 链接到 google.com，你可以简化成：
	
    [Google]: http://google.com
链接的定义可以放在文件中的任何一个地方，我比较偏好直接放在链接出现段落的后面，你也可以把它放在文件最后面，就像是注解一样。
[Google]: http://google.com
[id]: <http://example.com/>  "Optional Title Here"
##强调
Markdown 使用星号（\*）和底线（\_）作为标记强调字词的符号，被 \* 或 \_ 包围的字词会被转成用 <em> 标签包围，用两个 \* 或 \_ 包起来的话，则会被转成 <strong>，例如：  
	
    *single asterisks* 

	_single underscores_
	
    **double asterisks**

	__double underscores__
表现为  
*single asterisks*

_single underscores_

**double asterisks**

__double underscores__```

##代码
如果要标记一小段行内代码，你可以用反引号把它包起来（\`），例如：
```Use the `printf()`function```  
会表现  
Use the `printf()`function
##图片
行内式  
`![Alt text](/path/to/img.jpg)`   
`![Alt text](/path/to/img.jpg "Optional title")`  
参考式  
`![Alt text][id]`  
id的定义  
`[id]: url/to/img "option title attribute"`  
到目前为止， Markdown 还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的 `<img>` 标签。
