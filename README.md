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
记录当前的工作路径(会输出当前所在路径，记下来，待会有用)$ pwd这里表示我当前的工作路径为 /root/systemc-2.3.1
## Expe
riment 
