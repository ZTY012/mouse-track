# <img src="assert/favicon.ico" alt="Custom Icon">鼠标移动轨迹记录

一个好玩但没啥用的python迷你小程序：记录在做不同事情时候的鼠标运动轨迹。

可以看到在剪视频的时候鼠标经常在时间轴位置上横着晃动，可以看到在下棋的时候鼠标在棋盘界面上纠结。等等的。

## 使用方法

```plain
➜  coding git clone https://github.com/Littlefean/mouse-track.git
Cloning into 'mouse-track'...
remote: Enumerating objects: 145, done.
remote: Counting objects: 100% (145/145), done.
remote: Compressing objects: 100% (98/98), done.
Receiving objects:  50% (73/145)used 110 (delta 42), pack-reused 0
Receiving objects: 100% (145/145), 3.29 MiB | 55.20 MiB/s, done.
Resolving deltas: 100% (71/71), done.
➜  coding mouse-track
➜  mouse-track git:(master) python ./main.py
```

运行后弹个窗，点击开始记录之后，最小化窗口，干别的事情去，干完了之后，打开窗口点击结束记录，然后会在当前目录下创建out文件夹并在out文件夹中生成轨迹图片。

## 一些有趣的截图

绿点：鼠标左键点击位置，红色是右键，黄色是中键。

![pycharm](imgs/pycharm.png)

上图是用pycharm开发后端大项目的时候，一上午大约三个半小时的记录，可以看到有很多细小的短横线反复划，那个地方可能是选中代码进行修改的地方。中间还能看到很多黄点，黄点表示鼠标中键点击进行代码跳转。

![pycharm-datagrip](imgs/pycharm-datagrip.png)

上图是下午开发后端时候记录的，不同的是底部多了一些横线，那是我在用DataGrip软件连接后端数据库执行sql查询语句时候看结果，在底部显示了。

![reading-pdf](imgs/reading-pdf.png)

上图是我阅读一本pdf的技术书《程序员的修炼之道》，我没有想到我在阅读的时候屏幕竟然会不自觉的划出这么多横线，远远超出我的想象。

![playing-minecraft](imgs/playing-minecraft.png)

上图是我打开Minecraft随便跑了5分钟的轨迹，实际上，在mc里，鼠标是不停的被吸附在中心点的。只有在打开箱子或者背包之类的时候，鼠标才不被吸附。

![playing-game](imgs/playing-game.png)

上图是我在玩一个策略游戏《土地抢夺者》，一个需要不停的点击建筑，派遣部队攻城的小游戏。

![playing-genshin](imgs/playing-genshin.jpg)

上图是ZTY在玩《原神》，可以看到鼠标也有被吸附在中间的特征，右下角则是过剧情时点对话的轨迹。

![movie-cut](imgs/movie-cut.png)

上图是我在用Pr进行视频剪辑，可以看到鼠标大多数基本都在时间轴附近移动，能明显看到两个横线，上面的横线是由于调整时间轴上的当前位置，下面的横线是裁剪和移动视频片段导致的。（这张图片非常早，当时程序还没实现记录鼠标点击位置的功能）

## 未来可能的计划

定时开启和关闭记录，定时自动保存，开机起启动。

增加分类训练模块，预测轨迹可能性。

## 代码架构

2024年3月4日起，不再是一个《两百行的python小脚本》了，开始拆文件了。

目前按照从上到下拆成三层：

```
组件层：components
业务层：service
工具层：utils
```

通常来说上可以调下，下不能~~上吊~~调上。同层之间可以相互调用。
