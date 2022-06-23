## ubuntu中解决vscode控制台字体间距过大的问题

在设置中搜索“font family” 将值设为monospace



## ubuntu生成ssh公钥以及查看

```
git config --global user.name "xxx"
git config --global user.email "xx@xx.com"
ssh-keygen -t rsa
cat ~/.ssh/id_rsa.pub
```



## Anaconda创建新环境activate时报错

```
#错误信息
CommandNotFoundError: Your shell has not been properly configured to use 'conda activate'.
To initialize your shell, run

    $ conda init <SHELL_NAME>

Currently supported shells are:
  - bash
  - fish
  - tcsh
  - xonsh
  - zsh
  - powershell

See 'conda init --help' for more information and options.

IMPORTANT: You may need to close and restart your shell after running 'conda init'.

```

**解决方法**

如使用 zsh，则

```
conda init zsh
```

如果使用 bash，则

```
conda init bash
```





## Ubuntu20.04 ROS1与ROS2共存方法

bashrc添加

```shell
#source /opt/ros/noetic/setup.bash
echo "ros noetic(1) or ros2 foxy(2)?"
read edition
if [ "$edition" -eq "1" ];then
  source /opt/ros/noetic/setup.bash
else
  source /opt/ros/foxy/setup.bash
fi
```

