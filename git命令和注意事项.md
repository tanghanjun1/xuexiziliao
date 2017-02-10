#git 命令  知识点
首先在github上创建一个带名字的仓库，并默认添加一个初始化README.md文件（initialize ）和写上仓库描述；这样在github上就有了一个带默认README.md文件的仓库。    
接着在自己的本地C/E/F盘自己创建一个放自己资料的文件夹，然后进入该文件夹后右击鼠标右键，选择 git bash here,然后在出现的git工具中，输入(git clone http://www.github.com/tanghanjun1/仓库名 ) 注意：(tanghanjun)是你的github账户名，(仓库名)是你在  github上创建的仓库的名字；这时，在你本地文件夹里面就有了和github上面一样名字的仓库（即文件夹），然后再  (cd 仓库名  )意思是进入这仓库 ,进入仓库后，输入(git remote -v)查看本地仓库和远程仓库是否连接成功了。只要连接成功后，在这文件夹里面『新建文件夹，删除文件夹，等等』只要这文件夹里面有变动，就都要（git commit - "注释提交的原因"），然后一定要（git push），一定要把我们本地改动过的文件夹推送到远程仓库，让远程的仓库同步更新  
* 克隆仓库步骤：  
    1. git clone http://www.github.com/tanghanjun/仓库名  
    2. cd 仓库名  （作用：进入这仓库）  
    3. git remote -v      （作用： 检查本地和远程仓库是否匹配连接）
    4. 一切的修改本仓库内容，添加，删除，修改等等
    5. git commit -m "提交修改的原因" （作用：提交修改的仓库信息命令）
    6. git push (作用：把本体库和远程库同步)  
 **注意：** 本地仓库只要已有变化，就要先（git commit -m "提交内容注释" ） 提交，然后必须（git push）推送到远程仓库，让两个仓库内容保持一致
* 其他命令                
	1、ls (作用：查看当前文件夹里有什么)  
	2、git add 要添加的内容文件或文件夹  
    * 例子： git add search.md  添加了一个.md文件  
	3、git rm 要删除的文件或文件夹  
    * 例子：git rm readme.md  删除了readme.md文件  
	4、git status (作用：查看当前仓库内文件状态)  
	5、git log (作用：打印出仓储中的所有的提交)  
	6、 git show 提交的编号  （作用：打印单独的一条的提交记录内容  
	7、 vim （作用：进入vim编辑器中编辑内容)  
	
**注意：**Administrator@P5QCAPMFWNKEEMS MINGW64 /f/test/xuexiziliao (master)在git编辑中，一定要看到（master）才意味着这是一个和github匹配的仓库  
**注意：**我们复制的内容或命令，一定要shift+insert才能粘贴到命令上；
	
######git工具中用，进入vim编辑器中编辑内容后，先按ESC键再按英文的冒号加wq（:+wq)保存并推出vim编辑器；（":!q"）不保存退出  
######假如我们的编辑器不小心退不出到编辑状态，按ctrl+c让他恢复git工具编辑