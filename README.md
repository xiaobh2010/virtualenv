# virtualenv
1 什么是VirtualEnv - 虚拟环境
    VirtualEnv是python中的虚拟环境，在做python应用开发时，如果不想在大的python环境中安装各种各样的包，则可以虚拟出一个python环境，可以让虚拟环境专门为某一个应用而存在。允许在虚拟环境中安装各种包且不影响大的python环境
2 安装VirtualEnv
    sudo pip3 install virtualenv
    
3 创建和使用虚拟环境
    1 准备工作
        mkdir my_env
    2 创建虚拟环境    
        virtualenv 虚拟环境
        ex:
            virtualenv default
        创建指定版本的虚拟环境（对于不同的虚拟环境指定不同的虚拟版本）
        virtualenv -p /usr/bin/python2.7 名称
        tarena@tedu:~$ virtualenv -p /usr/bin/python2.7 env2.7

        virtualenv -p /usr/bin/python3.5 名称
        tarena@tedu:~$ virtualenv -p /usr/bin/python3.5 env3.5

     pip3 freeze > requirements.txt （文本文件里面可以看到版本）
    3 启动虚拟环境
    注意：不能在bin目录中启动虚拟环境
    source bin/activate

操作步骤：
tarena@tedu:~$ cd env3.5/
tarena@tedu:~/env3.5$ l
bin/ include/ lib/
tarena@tedu:~/env3.5$ source bin/activate
(env3.5) tarena@tedu:~/env3.5$ 
-----------------------------------------------------------------------------------
(查看当前环境安装的工具)
(env3.5) tarena@tedu:~/env3.5$ pip list
DEPRECATION: The default format will switch to columns in the future. You can use --format=(legacy|columns) (or define a format=(legacy|columns) in your pip.conf under the [list] section) to disable this warning.
pip (9.0.3)
setuptools (39.0.1)
wheel (0.30.0)

    4 退出虚拟环境
        deactivate
        注意：在虚拟环境中使用pip安装和卸载内容时，不要使用sudo进行授权

    5 删除虚拟环境
        rm 虚拟环境目录 -rf




