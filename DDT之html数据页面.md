#DDT之html页面数据驱动页面自动化测试
假如我们测试网站的内容是别人的，他们的测试数据和自动化测试用例是放在网上，我们要用他的测试数据和测试用例，我们就要改变（网址）因为是他的文件夹放的路径，这样我们就会感觉很不方便同时感觉我们的测试用例很不健壮。这是我们就可以用html表格+github page 来解决这问题。怎样解决呢？**步骤如下**：  
1.把我们要测试的数据用（前端编辑器）编写成table格式的html代码，制作成一个简单的html**表格形似页面**，html内容格式如下：    
```   
这是我们的html代码
	<table>
		<tr>
		    <td>selenium</td>
		</tr>
		<tr>
		    <td>51Cto</td>
		</tr>
		<tr> 
		    <td>东九网络</td>
		</tr>
		<tr> 
		    <td>金华兰溪
		</tr>
	</table>
```
2.然后我们把这简单的表格页面用git工具推送到我们的github上面，通过github page功能会自动生成一个大家可以访问的http://XXXX.html格式的页面地址。然后我们就可以先打开这个地址的页面，用循环用storeText命令获取我们制作的页面的数据内容保存在数组变量中，再打开我们要测试的**真正被测页面**，把我们获得的**页面的内容**填写到我们测这个页面需要用到的空格中去。实现循环数据驱动测试
```
command                             target                                    value
store                               1                                          n        初始化循环变量
open                                hello.html        打开我们制作的网页     
storeEval               Windows.document.getElementByTargNames("tr").length    rows     找到页面中tr的个数，既是代表总行数
storeEval                           newArray(rows)                             pharse   声明好总行数个数的一个数组
while                               ${n}<=${rows}                                       第几行小于总行数
storText      第几行的下的td         //tr[${n}]/td                              ph      获取页面中第几行的页面数据内容保存变量中
runscript              javascript{storedvars.pharse[storedvars.n]=storedvars['ph']}     把每个变量值保存到对应编号的数组中
storeEval                           ${n}+1                                     n
endwhile
操作被测的真正页面
store                                1                                         n
while                               ${n}<=${rows} rows代表找到的行数
open                               http://www.baidu.com  真正的被测页面、
click                                id=kw
type                                 id=kw                      javascript{storedvars.pharse[storedvars.n]=storedvars['ph']}                        
waitforTitle        javascript{storedvars.pharse[storedvars.n]+"百度搜索"}       
assertTitle         javascript{storedvars.pharse[storedvars.n]+"百度搜索"}     
verifyText                         css=div.num                              *百度为你搜索
storeEval                          ${n}+1                                      n
endwhile
```   
**实现过程：**    
1. 制作html表格数据文件
2. 实现数据捕获
3. 实现数组操作
4. 操作被测的页面
5. 表格行数参数化
