## Centos安装Anconda3并使用jupyter-notebook
#### 一、安装Anconda

###### 1、下载Linux环境下Anconda安装脚本

```bash
wget --no-check-certificate https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-2020.02-Linux-x86_64.sh
```

###### 2、执行Anconda安装脚本

```bash
bash Anaconda3-2020.02-Linux-x86_64.sh
```

接下来会出现一堆的License许可声明，一路回车向下，出现如下文字，输入yes：

```bash
Do you accept the license terms? [yes|no]
[no] >>> 
Please answer 'yes' or 'no':
>>> yes
```

之后要选择安装目录，如果无需更改直接回车Enter，如需更改要输入绝对路径：

```bash
Anaconda3 will now be installed into this location:
/root/anaconda3

  - Press ENTER to confirm the location
  - Press CTRL-C to abort the installation
  - Or specify a different location below

[/home/datasupport/anaconda3] >>> 
```

看到如下提示则安装成功：

```bash
Thank you for installing Anaconda3!

===========================================================================

Anaconda and JetBrains are working together to bring you Anaconda-powered
environments tightly integrated in the PyCharm IDE.

PyCharm for Anaconda is available at:
https://www.anaconda.com/pycharm
```

###### 3、source刷新环境变量

```bash
source ~/.bashrc
```



#### 二、启动jupyter-notebook

###### 1、启动jupyter-notebook

```bash
conda activate # 进入conda环境 出现(base)则说明安装成功
jupyter-notebook --ip=hostname --no-browser #启动jupyter-notebook
conda deactivate # 退出conda环境
```

###### 2、导入自定义python包

jupyter-notebook导入自定义python包，要求被导入的python包扩展名为.py, 而不是，假如需要导入的自定义python包如下：

```python
#名称：testpk.py
def show():
    print('hello world!')
```

ipython代码如下：

```python
from testpk import *
show()
```

