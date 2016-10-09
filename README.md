# ES2016_14353252

$ sudo apt-get update
$ sudo apt-get install ant
$  sudo apt-get install openjdk-7-jdk
$ sudo apt-get install unzip
## How to install
新建dol的文件夹 
$ mkdir dol将dolethz.zip解压到 dol文件夹中
$ unzip dol_ethz.zip -d dol解压systemc
$ tar -zxvf systemc-2.3.1.tgz

解压后进入systemc-2.3.1的目录下
$ cd systemc-2.3.1新建一个临时文件夹objdir
$ mkdir objdir进入该文件夹objdir
$ cd objdir运行configure(能根据系统的环境设置一下参数，用于编译)
$ ../configure CXX=g++ --disable-async-updates
编译
$ sudo make install
记录当前的工作路径(会输出当前所在路径，记下来，待会有用)
$ pwd这里表示我当前的工作路径为 /root/systemc-2.3.1

进入刚刚dol的文件夹
$ cd ../dol修改build_zip.xml文件找到下面这段话，就是说上面编译的systemc位置在哪里，
<property name="systemc.inc" value="YYY/include"/>
<property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/>
把YYY改成上页pwd的结果（注意，对于  64位 系统的机器，lib-linux要改成lib-linux64）


然后是编译
$ ant -f build_zip.xml all若成功会显示build successful接着可以试试运行第一个例子进入build/bin/mian路径下$ cd build/bin/main然后运行第一个例子$ ant -f runexample.xml -Dnumber=1
## Experiment 

从这次实验中我对github有了基础的了解，觉得自己之前真的没有经验，竟然不知道这个的存在，问了室友，她说她以前就有在用，感觉自己没有她的自学能力。但是从这个实验课之后我就可以拓展我的知识，希望以后更加努力。





