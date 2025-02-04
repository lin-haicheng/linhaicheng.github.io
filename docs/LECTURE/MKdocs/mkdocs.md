# MkDocs

## 安装  

(文章定义，代码块里有$符号在最前面的代码指定是在终端输入执行的命令)

首先确认电脑是否有安装 pip ，是 Python 包管理工具，该工具提供了对Python 包的查找、下载、安装、卸载的功能，一般电脑安装了 Python 2.7.9 + 或 Python 3.4+ 以上版本都自带 pip 工具。

pip 官网：<https://pypi.org/project/pip/>

你可以通过以下命令来判断是否已安装：

```
$ pip --version     # Python2.x 版本命令
$ pip -V            # Python2.x 版本命令，-V就是--version的缩写，注意这个V是大写喔

$ pip3 --version    # Python3.x 版本命令
$ pip3 -V           # Python3.x 版本命令，-V就是--version的缩写，注意这个V是大写喔
```

如果没有版本显示，那就代表你的电脑没有pip，有多种方法可以安装:

1、安装一个python3版本的python，一劳永逸还不用担心python2版本的一些bug。

2、是一个骚操作，使用`python -m pip install --upgrade pip`命令，这个命令的作用是模拟一个pip模块，并且安装更新pip到最新版本，之后就可以用来安装东西啦。

使用pip安装MkDocs的Material主题命令进行安装：    

```
$ pip install mkdocs-material  
```

!!! Info "注意有坑"
    MkDocs 这个静态网站框架支持 **python2.6/2.7/3.3/3.4/3.5** 及以上版本，但是如果你的电脑系统使用的是python3以下的版本安装了可能会无法使用VScode的终端输入 `mkdocs serve` 命令渲染临时网页的功能，当然是有方法可以绕过的，但是会生成大量的臃肿文件，最好就是安装并更换系统为python3以上的版本。  
    
    1、创建虚拟环境  
    在Linux和Mac环境下，打开VScode终端，如果要创建当前目录为虚拟环境，那么执行下面的命令，venv是macOS自带的一个虚拟背景管理工作：  
    
    ```
    python3 -m venv .  
    ```
    
    2、 启用虚拟环境  
    执行下面的激活虚拟环境的命令：  
    
    ```
    source ./bin/activate  
    ```
    
    3、在虚拟环境里进行mkdocs的安装
    
    ```
    pip install mkdocs-material  
    ```



## 生成mkdocs配置文件

在终端使用命令行直接生成  

使用cd命令切换到你想新建文件的目录(文件夹)，以下命令是我在终端从**家目录**去到**桌面**的命令   

```
$ cd Desktop  
```

编写生成命令  

```
mkdocs new <file> #生成配置文件  
命令格式mkdocs是网站框架，new是函数新建文件，<file>是新建文件想命名的名称。  
```

例：

```
$ mkdocs new mkdocs-newfile
```

在终端输入命令运行后显示如下：  

```
$ mkdocs new mkdocs-newfile  
INFO    -  Creating project directory: mkdocs-newfile  
INFO    -  Writing config file: mkdocs-newfile/mkdocs.yml  
INFO    -  Writing initial docs: mkdocs-newfile/docs/index.md  
```

这个命令会在你当前的目录下生成一个名为mkdocs-newfile的文件夹，里面有两个文件**配置文件mkdocs.yml** ，docs文件夹下的**说明文件index.md**。  

**补充**：也可以先新建文件夹，使用cd命令进入这个新建的文件夹,输入`mkdocs new .`这个命令的作用是在当前文件夹生成配置文件（点号就是当前目录/文件夹的意思）跟上面的结果其实是一样的，都是用这个文件夹当做mkdocs的核心。  

```
$ mkdir mkdocs-newfile
$ cd mkdocs-newfile
$ mkdocs new .
INFO    -  Writing config file: ./mkdocs.yml
INFO    -  Writing initial docs: ./docs/index.md
```




