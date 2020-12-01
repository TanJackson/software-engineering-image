##第一步:下载所需软件
- 编译器eclipse，从官网下载，[eclipse下载官网](https://www.eclipse.org/downloads/ "eclipse下载官网")
- 下载JDK14，从官网下载，[jdk下载官网](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html "jdk下载官网")
- 下载tomcat，从官网下载，[tomcat下载官网](http://tomcat.apache.org/download-70.cgi "Tomcat下载官网")
- 下载数据库工具navicat for mysql，从官网下载，[navicat下载官网](https://www.formysql.com/ "navicat下载官网")
- 下载XAMPP Control Panel，用于简单快速链接mysql

##第二步:基础环境搭建

#### JDK配置
- 右击“我的电脑”-->"属性"-->"高级系统设置"-->"高级"-->"环境变量"
- 在系统变量里新建"JAVA_HOME"变量，变量值为：C:\Program Files\Java\jdk14.0_60（根据自己的jdk的安装路径填写）
- 在系统变量里新建"classpath"变量，变量值为：.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar (注意最前面有一点)
- 找到path变量（已存在不用新建）添加变量值：%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin
- 注意变量值之间用";"隔开。注意原来Path的变量值末尾有没有;号，如果没有，先输入;号再输入。如果你的系统是Windows10，就相对方便多了，不用担心这个";"。

- “Windows+R”-->输入“cmd”-->Enter，输入java -version(记得中间有个空格)，如果显示jdk版本信息就说明环境变量配置成功了。

#### 在eclipse下配置tomcat
tomcat环境配置->[[tomcat配置]][1]

##第三步:数据库的链接
打开已下载好的XAMPP Control Panel，在Mysql一栏点击Start即可，之后便可以打开navicat for mysql直接连接。
##第四步：导入项目并且修改eclipse内项目要求配置
####项目导入:
1. 打开"eclipse"——>"file"——>"new"——>"project"——>"web"——>"Dynamic Web project"——>填入项目名称，到这里就已经创建好文件。
2. 在项目文件上点击右键——>"import"——>"General"——>"Existing Projects into Workspace",弹出窗口后在"Select root directory"下选择源文件所在的目录。
3. 项目要求的JAVA环境配置，右键项目文件——>"Build Path"———>选择“Java Build Path”——>"Libraries"——>点击JRE后edit——>在Alternate JRE上选择你安装的JDK；在"Build Path"上选择"Java Compiler"——>在"Compiler compliance lever"上选择你的JDK版本（低版本不可编译高版本的文件）







[2]: http://programmer.ischoolbar.com/index.php/article/article/id/10.htm "tomcat环境配置"
[1]: http://programmer.ischoolbar.com/index.php/article/article/id/10.htm "eclipse下配置tomcat"
