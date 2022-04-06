找一个自己的键盘样式（如果自定义的比较多，就自己修改一下）

准备每一层按键，都复制出来raw

http://www.keyboard-layout-editor.com/

粘贴到这里，每一层

https://tkg.io/#

刷进去就可以了，不会的的可以参考

https://tieba.baidu.com/p/3990207294

注意，以下内容有一个非常容易忽视的：装驱动一定要装成功，有人没装好驱动找我半天，我以为是芯片不对，结果……



上方链接防吞备份：

一．准备工具

1. 对应列表上的键盘PCB一张
2. 代码一份http://www.enjoyclick.org/keyboard-layout-editor/
3. 制作eep http://www.enjoyclick.org/tkg/
4. tkg-toolkit-master工具包一个https://github.com/kairyu/tkg-toolkit

二．代码制作

！！！！！标准标记（各种刻标记）

刷配列必须使用标准标记也就是代表着每个按键的代码如果不懂请到以下网站查看：http://www.kaiserver.com/tkg/#help

代码制作：

首先打开做代码的网页http://www.enjoyclick.org/keyboard-layout-editor/

页面的简单介绍：

三．制作eep文件

打开http://www.enjoyclick.org/tkg/

五．开始刷固件（重点）

到最重要的一步了

PCB接上电脑。按一下PCB背后的按钮，按下的时候，GH60键盘的状态灯会全部灭掉。


然后装驱动：

插好pcb后，点：开始-设备和打印机（win7）.会发现有下图中出现GH60.

打开桌面上下载好的tkg-toolkit-master打开/windows/tool.会发现有一个文件zadig_2.1.2，右键，以管理员身份运行。

注意了此时会出现两种情况，

第一种情况：

A1：你原来装过驱动，会出现下图

此时，点击options.选择listall。然后出现下图

然后点击replace Driver,这个过程 的时间有点长，请耐心等，大概5分钟的样子。

第二种情况：

A2：原来没有安过驱动，那么打开zadig之后应该如下图所示，atm32u4dfu默认被选中，其余步骤相同。

注：如果没有变成WinUSB ,那么必须重做，请把各种杀毒软件关闭，然后重启电脑重新按上面的步骤做。

3、打开tkg-toolkit-master,按一下pcb后面的小黑圆圈按钮

运行setup后选择你对应的键盘

4.把刚才制作的eep拖到reflash.bat上出现小黑屋

6、小黑屋关闭后，试试键盘，一般都是成功的。
