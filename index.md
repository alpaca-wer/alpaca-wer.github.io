# Java开发环境搭建
### 一、配置文件的创建
① 终端根目录创建(编辑)配置文件：【 vim .bash_profile 】
② 使文件进入可编辑文本状态：i
③ 结束可编辑状态：esc
④ 保存文本并退出：:wq
⑤ 终端更新配置文件：source .bash_profile
    
### 二、多Java版本环境搭建
① 终端进入配置文件，并打开可编辑状态：【 vim .bash_profile 】 => i
② 或直接利用文本阅读器软件打开：【 open .bash_profile 】
③ 配置文件中Java不同版本配置详细内容：
    
export JAVA_7_HOME=/Library/Java/JavaVirtualMachines/jdk1.7.0_80.jdk/Contents/Home

export JAVA_8_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home

export JAVA_HOME=$JAVA_7_HOME

alias jdk7='export JAVA_HOME=$JAVA_7_HOME'

alias jdk8='export JAVA_HOME=$JAVA_8_HOME'
    
④ 保存文件并终端更新配置文件：操作见 配置文件的创建
⑤ 验证Java环境(查看版本号)：【 java -version 】
    
**************** 注解 ****************
1.jdk默认安装路径：/Library/Java/JavaVirtualMachines/
2.具体安装的jdk版本号：jdk1.7.0_80.jdk 及 jdk1.8.0_121.jdk
3.JDK默认HOME路径：/Contents/Home
4.默认选择JDK7版本：export JAVA_HOME=$JAVA_7_HOME
5.alias：控制台指令别名化，如根目录下执行指令jdk8，切换jdk8环境，执行指令alias -p查看所有别名化指令
    
### 三、终端Java使用
例：拿桌面 Test.java 文件为例：该文件定义了一个Test类，主函数中打印"Hello world"
① 打开终端进入桌面(文件所在)目录：【 cd desktop 】
② 编译Test.java文件为可执行文件Test.class：【 javac Test.java 】
③ 执行Test.class文件类Test：【 java Test 】
④ 控制台输出：Hello world
