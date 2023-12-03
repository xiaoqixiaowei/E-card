<img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20231202233913.jpg" alt="微信图片_20231202233913" style="zoom: 15%;" />

## [SJTU-E-card]电院NFC卡片

> 本项目主要是Jason(我)和Benjamin做的一个SJTU的纪念品，复刻基本没有难度 :blush:（可能需要一些焊接设备）
>
> 个人比较崇拜香农和稚晖君，所以对一些比较有意思的东西都会感兴趣，平时大部分时间还是在学术（主攻通信算法）上。刚刚进学校，有很多课，有些课程比较无聊，打发时间就做了这个东西。
>
> 设想一下，在参加学术会议时，短短的Presentation可能还不足以给学术大牛留下印象。在后续和同行交流的过程中，赠送别人一张具有交大特色的NFC卡片，另外在卡片的内部存上自己实验室或者个人主页，是不是会让别人对自己的印象变深呢？
>
> ---
>
> 卡片接触时NFC设备时LED会闪烁，总共分为两版：
>
> - 使用nt3h1101w0fhkh芯片：只能实现NFC名片功能，不能当作门卡使用
> - 使用CUID芯片：门卡和一般NFC名片功能都可以实现
>
> 如果有对 **元器件如何摆放为地图** 的样式好奇的朋友，后文会详细描述如何拓展到其他地区或者地形NFC卡片的制作一般化方法，可能是原创方法hhh :sunglasses:
>
> 后文还讲述了试验过的外壳方案，后面还有一版亚克力的外壳模型还在制作中。。。
>
> ---
>
> 最后的最后，电院是个大家庭，我还绘制了一个包含电气学院的卡片（这栋楼不在电院群楼太可惜了 :pensive:）

#### 项目文件说明：

<img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231202230845209.png" alt="image-20231202230845209" style="zoom:15%;" />

​	**Hardware:** 立创EDA专业版文件，可以自行查看修改

​	**Gerber:** 这里保存了打板所需要的文件（注意我都没有加客编，要选择不加客编；或者无所谓的话加上客编也可以），如果不想修改的话 **可以直接嘉立创下单**；里面还有相关元件的购买链接（里面还有绳子的选型图，我试验了很多种方案，可供参考）

​	**3D-Model:** 可以根据这个pcb设计外壳

#### 手机APP配置NFC名片

##### 软件基本使用

这一部分主要说明如何进行NFC名片配置，以及实现一些其他有趣的功能

`下载原始链接` [NFC 工具下载链接](https://www.52pojie.cn/thread-1541093-1-1.html)

简要说明一下这个软件能够实现的功能（这里以安卓鸿蒙手机为例，IOS系统的同理，不过功能似乎没有那么齐全）

<div align=center>  <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203131553664.png" alt="image-20231203131553664" style="zoom:15%;" /> <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203131443046.png" alt="image-20231203131443046" style="zoom: 15%;" />      </div>



下载过后，可以选择自己感兴趣的应用：触碰之后跳出自己预设的文本，跳出URL网址，触碰打开某个应用，又或者是触碰之后直接连接蓝牙设备，然后再download到卡片上

##### 举两个比较实用的例子：

使用URL功能，写上自己的个人主页，或者是写上URL Scheme（实际上就是通过网址进行应用的某个功能的直接跳转，比如直接跳转到某个歌曲进行播放），实现音乐墙的功能

一些常见的URL Scheme可以查看[快捷指令常用 URL Scheme - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/660270338)

#### 外壳方案尝试

##### 成功方案

###### 无外壳

这个其实看着还是挺不错滴，但从完整度上来讲，还是需要一个外壳 :smirk:

<img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/afcb5bda2679b378840348629d66528.jpg" alt="afcb5bda2679b378840348629d66528" style="zoom:25%;" />

###### 胶壳方案

这个算是属于包好了饺子，然后找醋的方法了

淘宝可以直接购买（有一些劣质商家，还有线头，非常可恶，后面这个算是质量还可以的），购买链接如下【淘宝】https://m.tb.cn/h.5OI7IUl?tk=q33TW4OpNmC CZ0001 「门禁卡套小长方形水滴形门卡迷你小区电梯卡保护套公交卡卡套」

**需要说明**的是，因为我是先设计的卡片，当时没有考虑胶壳，最后也是运气好，刚好找到了这个尺寸的壳子（3.5*5），所以在塞入卡片的时候可能需要用东西顶一下，而且不是很好取出来，不过测试完成之后也不太容易坏掉啦

<div align=center> <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/769e7460c06fe24727d405a076eb11d.jpg" alt="769e7460c06fe24727d405a076eb11d" width="500" height="450" /> </div>



###### 贴膜方案

贴膜方案，摸起来是磨砂质感，但是感觉不如纯色炫酷

<div align=center>   <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203123026265.png" alt="image-20231203123026265" width="440" height="300" />     <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203122549502.png" alt="image-20231203122549502" width="400" height="300" /> </div>

---

##### 失败方案

###### 滴胶方案

我自制了一个简易的模具，然后尝试一下滴胶，我是没有成功 :joy:，欢迎心灵手巧的朋友自行制作

<div align=center>  <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/7c1fecc6b96eb6c6bba721a8fe9ae3a.jpg" alt="7c1fecc6b96eb6c6bba721a8fe9ae3a" width="300" height="300" />     <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/ed469983ef8ba6367f11581665067c3.png" alt="ed469983ef8ba6367f11581665067c3" width="300" height="300" /> </div>

<div align=center> <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/2b1de033ff374579ec290269c43f8ea.jpg" alt="2b1de033ff374579ec290269c43f8ea" width="500" height="300" /></div>

###### 树脂打印方案（务必喷油；后续设计好之后也会放在项目中）

这个是初代的亚克力设计方案，下图是没有粘贴的时候的图， 但是粘贴的时候还存在一定的问题，后面另外一个朋友会改进一下

<div align=center>   <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/5a0c18eb4b6009bf24a1d71e8e86bc0.png" alt="5a0c18eb4b6009bf24a1d71e8e86bc0" width="300" height="300" />    <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203120842002.png" alt="image-20231203120842002" width="500" height="300"" /></div>

如果使用502进行粘贴，胶水会渗入到卡片上，非常丑陋。所以后面会改进一下

<div align=center><img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203125059929.png" alt="image-20231203125059929" style="zoom: 67%;" /></div>

#### 地图绘制一般化方法

* 获取地图，eg. [上海交通大学校园电子地图 (sjtu.edu.cn)](https://map.sjtu.edu.cn/)
* 截图保存

<div align=center> <img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203132415613.png" alt="image-20231203132415613" style="zoom:5%;" /></div>

* 选择导入图片

<div align=center><img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203132522105.png" alt="image-20231203132522105" style="zoom:5%;" /></div>

* 选择导入彩色图片

<div align=center><img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203132739482.png" alt="image-20231203132739482" style="zoom: 5%;" /></div>

* 调制图片的尺寸

<div align=center><img src="https://xiaoqixiaowei.oss-cn-chengdu.aliyuncs.com/img_for_typora/image-20231203132829333.png" alt="image-20231203132829333" style="zoom:5%;" /></div>

* 选择合适封装的元件即可，临摹即可

#### 总结

这个项目整体来说没有什么难度，喜欢的朋友可以自己制作改进。

我的偶像是香农和稚晖君，他俩都是能够把自己脑袋里面构思的做出来，他俩的动手能力都不弱。希望有朝一日成为他们一样的人。

#### References：

[[已成功\] 基于nfc的PCB名片 - 嘉立创EDA开源硬件平台 (oshwhub.com)](https://oshwhub.com/scarrr0725/ji-yu-nfcde-ming-pian-ji-ji-yu-a)

[基于NFC的毕业纪念卡片_nt3h1101_Mr.Idleman的博客-CSDN博客](https://blog.csdn.net/qq_42059060/article/details/117825940)
