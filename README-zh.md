GameShell: 教你用Unix Shell的“小游戏”！
===========================================

![Illustration inspired by the game](Images/illustration-small.png)

对老师来说，让零基础的大一新生学会使用Unix Shell着实让人痛苦。GameShell因此被开发出来用于帮助
[Université Savoie Mont Blanc](https://univ-smb.fr)的学生们在 *真正的*
Shell中实践，让教学充满乐趣的同时激发学生的自主学习意识。 

Rodolphe Lepigre 最初的想法是用一个配置文件来运行一个标准的bash会话，它定义了 "missions"（任务），"missions"在经过"checked"（检查）后将推进游戏的进程。

以下是效果展示

![GameShell's first mission](Images/gameshell_first_mission_small.gif)


GameShell现在支持英语、法语、意大利语、中文...


欢迎通过以下渠道来评论，提问，提建议！提出[issues](https://github.com/phyver/GameShell/issues) 或者提交
[pull requests](https://github.com/phyver/GameShell/pulls). 

我们也很期待你创造出全新任务来让我们玩耍哟~

翻译与校对
---------------
本游戏的中文版本仍然在校对中，如果您有兴趣参与项目的翻译/校对，请clone本仓库
``` bash
git clone https://github.com/bxhsiman/GameShell.git
```
进入仓库目录
``` bash
cd GameShell
```
使用以下命令执行游戏将进入中文版本
``` bash
bash start.sh -L zh
```
将zh修改为其他语言将进入游戏的其他版本，建议以英文版本作为翻译对照
``` bash 
bash start.sh -L en 
```
如有问题或更好的翻译，请提交[issue](https://github.com/bxhsiman/GameShell/issues)或直接发起[pr](https://github.com/bxhsiman/GameShell/pulls)

**感谢您的参与**

开始
---------------

GameShell 可以在任何标准Linux系统上运行，macOS 和 BSD应该也没问题，但是我们没有经过太多的测试. 
在Debian与Ubuntu上，项目除了依赖已有的`bash`，还需要`gettext-base` 、`awk` (`awk`通常会被默认安装). 
一些"任务"可能需要额外的依赖，如果不满足依赖项，这些"任务"会被跳过.
在Debian与Ubuntu上，运行以下指令来安装所有游戏与任务的依赖项。
```sh
$ sudo apt install gettext man-db procps psmisc nano tree bsdmainutils x11-apps wget
```
 [用户手册](doc/user_manual.md) 中有其他系统的依赖安装方法， (如macOS, BSD, ...)。

如果全部依赖已经安装完毕，你可以运行以下两个命令来运行最新版本的游戏。
```sh
$ wget https://github.com/phyver/GameShell/releases/download/latest/gameshell.sh
$ bash gameshell.sh
```
第一个命令将以自解压文件的方式下载游戏的最新版本，而第二个指令将初始化并且运行游戏。

如果需要游玩中文版本，可以使用
``` sh
bash gameshell.sh -L zh
```

游戏的新手教程附加在游戏当中~

**Note:** 当你通过 ( `control-d` 或者 `gsh exit`) 退出游戏的时候
你的游戏存档将被保存在名为`gameshell-save.sh`的新文件当中 。
**运行这个文件来继续游戏！**


如果你不希望在你的电脑上运行外部shell脚本，你可以用以下指令来生成一个Docker image:
```sh
$ mkdir GameShell; cd GameShell
$ wget --quiet https://github.com/phyver/GameShell/releases/download/latest/Dockerfile
$ docker build -t gsh .
$ docker run -it gsh
```
游戏在退出的时候**不会保存** 。如果您想从GameShell内部运行X程序，则需要带上附加flags。详见 用户手册的[这个章节](./doc/deps.md#running-GameShell-from-a-docker-container) 


文档
-------------

要了解有关GameShell的更多信息，请参阅以下文档：
-  [The user manual](doc/user_manual.md) 如何在所有支持平台运行游戏（如：Linux、macOS、BSD）、如何从源代码运行游戏、如何生成自定义游戏存档（如果您想使用GameShell来授课的话可能会用到）等等。
-  [The developer manual](doc/dev_manual.md) 提供了有关如何创建新任务、如何翻译任务以及如何参与游戏开发的信息。


是谁在开发GameShell？
----------------------------

### 开发者

The game is currently being developed by:
* [Pierre Hyvernat](http://www.lama.univ-smb.fr/~hyvernat) (main developer,
  [pierre.hyvernat@univ-smb.fr](mailto:pierre.hyvernat@univ-smb.fr)),
* [Rodolphe Lepigre](https://lepigre.fr).

### 任务贡献者

* Pierre Hyvernat
* Rodolphe Lepigre
* Christophe Raffalli
* Xavier Provencal
* Clovis Eberhart
* Sébastien Tavenas
* Tiemen Duvillard

### 翻译

#### 意大利语版本

* Daniele Scasciafratte (@mte90)
* Paolo Mauri (@maupao)
* Marco Ciampa (@ciampix)
* Antonio Vivace (@avivace)
* Lorenzo Millucci (@lmillucci)
* Sirio Negri (@ziriuz84)
* Domenico Mammola (@domenicomammola)
* Leonardo Canello (@anulo2)
* @michirod
* @serhack
* WhiteShield (@wshield05)
* @gioisco

#### 中文版本

* @bxhsiman

### 特别鸣谢

* 所有在早期版本当中捉到了 *很多* 虫子的同学们！
* Joan Stark (a.k.a, jgs), 90年代末设计了很多ASCII艺术品，你在GameShell当中遇到的大部分ASCII艺术品都来自于她~

许可协议
-------

GameShell 以[GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html)发布

**请在使用GameShell的时候附上本仓库链接**

GameShell 是开源的，是可以免费使用的，如果你很想支持我的工作，可以考虑给我寄一张明信片~

```
  Pierre Hyvernat
  Laboratoire de Mathématiques, CNRS UMR 5127
  Université de Savoie
  73376 Le Bourget du Lac
  FRANCE
```

Licence
-------

GameShell is released under the [GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html).

Please link to this repository if you use GameShell.

GameShell is open source and free to use. One way you can acknowledge the work
it required is by sending an actual postcard to

```
  Pierre Hyvernat
  Laboratoire de Mathématiques, CNRS UMR 5127
  Université de Savoie
  73376 Le Bourget du Lac
  FRANCE
```

