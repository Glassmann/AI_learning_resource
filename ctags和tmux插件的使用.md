# ctags和tmux插件的使用

### ctags的安装

在Linux的环境下我们在看源代码的时候有的时候想要去了解一些系统自己带的或者自己写的函数的定义，这个时候就需要用ctags这个插件了。

```shell
sudo apt-get install ctags
```

ctags生成相对路径

```shell
ctags -R
```

ctags生成绝对路径

```shell
ctags -R `pwd`
```

### tmux的安装

安装命令

```shell
sudo apt install tmux
```

修改tmux 的相应配置文件

```shell
vim .tmux.conf
```

在配置文件中修改为如下内容

```shell
unbind C-b
set -g prefix C-a

bind h select-pane -L
bind j select-pane -D
bind k select-pane -U
bind l select-pane -R
```

