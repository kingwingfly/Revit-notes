# Revit笔记

**Written by Louis翔	Powered by B站 @BIMer北冥_今年不答疑**

主要操作为正体字，强调为**粗体**或<u>划线</u>，技巧为*斜体*。

笔记采用Markdown语法编辑，故文档的浏览需要在联网环境下进行；可在左侧查看大纲，笔者使用的Revit版本为2022 。

## 零、族库的安装

某些破解版本或离线安装的Revit没有完整的样板或者族库，这会导致绘制某些结构时报错，故须安装基本族库。

### 查看有无基本族库：

#### 法一：直接查看文件

1. 打开显示隐藏文件选项

![image-20220510000256641](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510000256641.png)

2. 打开该隐藏路径：C:\Program Data\Autodesk\RVT 20XX

![image-20220510000702665](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510000702665.png)

3. 查看Libraries\Chinese

![image-20220510000754470](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510000754470.png)

#### 法二：Revit内查看

按如下操作

![image-20220510002413238](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510002413238.png)

若发现为明显缺失，则需打开[Autodesk官网](https://knowledge.autodesk.com/zh-hans/download)，并注册，下载对应版本的补丁包。

### 补丁包的下载安装

选择版本

![image-20220510001002870](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510001002870.png)

点击进入“内容”下载详情页

![image-20220510001116265](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510001116265.png)

下载补丁安装器

![image-20220510001303085](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510001303085.png)

关闭Revit，以管理员权限运行补丁安装器

![image-20220510010127888](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510010127888.png)

点击安装

![image-20220510010206784](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510010206784.png)

完成安装

![image-20220510010325049](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510010325049.png)

可以看到，族库文件夹的内容完备了。

![image-20220510010400991](https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220510010400991.png)

## 一、基本操作

### 1.1 布局小技巧

1. 属性放左边，项目浏览器放右边。

<img src="https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/20220509171647.png" style="zoom: 35%;" />

2. 视图-平铺视图，展示多窗口。

<img src="https://notesoflouis.oss-cn-chengdu.aliyuncs.com/imgs/image-20220509171839952.png" alt="image-20220509171839952" style="zoom:35%;" />

### 1.2 图元的选择

1. 点选：Ctrl多选，Shift减选

2. 框选：与CAD相同

3. 对于多段线（端点相连的多条线），将鼠标悬于其中一段，按下Tab键，即可选择整条多段线。

4. 过滤器：

   <center>
       <img src="C:\Users\83625\AppData\Roaming\Typora\typora-user-images\image-20220508234326445.png" alt="image-20220508234326445" style="zoom: 35%;" />
       <img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508234420742.png" alt="image-20220508234420742" style="zoom: 65%;" />
   </center>
   
   

### 1.3 直接绘图模式与草图模式

1. 可以用ESC退出，则为直接绘图模式，如画墙或线时。
2. 如下无法使用ESC退出的为草图模式。需点击完成或取消后才能退出。如楼板、屋顶。

![image-20220508195311081](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508195311081.png)

### 1.4 属性栏

1. 点击空白处，则为当前窗口的属性。
2. 点击图元后，才显示图元的属性。

### 1.5 族的相关术语

例如，结构柱：柱1：600X600

族类别：结构柱

族：柱1

族类型：600X600

*理解：族类别 是用来分类的。譬如，“人类”这一 族类别 中，“族”可以理解为个体，“族类型”可以理解为人种。同一种 族类别 包含多种 族类型。而 图元 就是构成族的最小单位，即细胞*

### 1.6 可以在项目浏览器中查看族

### 1.7 载入族的不同方式

1. 不同专业的样板默认自带的族不同
2. 法一：插入-载入族

![image-20220508201026913](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508201026913.png)

​			法二：专业选项卡-构件-放置构件-载入族（只能载入对应专业的族）

​			法三：修改选项中载入

![image-20220508201500470](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508201500470.png)

### 1.8 类型参数与实例参数

类型参数：修改后，会使相同族类型的所有族全都变化的参数

实例参数：只对一个族或图元起作用的参数

<a href='#back1'>回到刚才</a>*（这里是后面会引用到，所以放个回引）*

### 1.9 复制族类型单独修改某个族

<img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508221807766.png" style="zoom:50%;" />

### 1.10 撤销与重做

Ctrl+Z 撤销

Ctrl+Shift+Z 重做

### 1.11 视角旋转

鼠标中键平移视角，按住Shift+鼠标中键旋转视角。

### 1.12 三维视图的展示

此底部两项设置可以修改三维视图的展示样式。如图所示为精细与着色。

![image-20220510202154044](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510202154044.png)

### 1.13 材质修改

在材质管理器中（进入方法在后面），将AEC材质库的材质点击拖入项目材质才可以应用。

![image-20220511200756483](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511200756483.png)

## 二、实操

新建建筑样板。

### 2.1 标高与轴网的创建

关于在Revit中对标高与轴网的理解：

标高与轴网均是特殊的族类别，是在对应位置的一个平面。

![image-20220510004310822](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510004310822.png)

![image-20220510004453654](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510004453654.png)

<u>建议一定要先画标高再画轴网。</u>

[2.1.5 先画标高的原因](#2.1.5 先画标高的原因)

#### 2.1.1 标高

1. 在项目浏览器中打开某个立面

<center>
    <img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/20220508231334.png" alt="image-20220508205318740" style="zoom: 50%;" />
    <br/>
    立面中标高名称与项目管理器中平面的名称具有关联性
</center>

2. 双击即可修改标高（单位：m）与标头

3. 绘制方法：**（推荐法三）**

   法一：点击 建筑/结构选项卡-标高，在对应高度横画一条线即可。

   **快捷键为LL**

    法二：复制

   **快捷键为CO或CC**；操作与CAD相同

![image-20220508211153335](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508211153335.png)

​			法三：阵列

​			**快捷键为AR**；

​			选中，AR，输入间距，输入数量。*Tip，需要n个标高，则数量输入n+1*

​			**通过“解组”，将族类型从“阵列组”修改为“上标头”**（或者在阵列时就取消勾选“成组并关联”）

<img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/20220508231724.png" alt="修改阵列标高族类型" style="zoom: 50%;" />

解组后，可以选择标高检查一下，若还有“阵列组”，则选中解组。此外，标高一的族类型是与其他标高不同的。

4. 复制与阵列的方法生成的标高可能不会出现在项目浏览器-楼层平面内，故须**在视图-平面视图-对应平面手动添加楼层平面**。

![image-20220508213505913](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/20220508231855.png)

![](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/20220508232151.png)

5. 在<u>类型属性</u>中的修改会应用到同一族类型的所有族中（如颜色、形状、标注位置等）<a href='#1.8 类型参数与实例参数' name='back1'>类型参数与实例参数</a>

​	![image-20220508215520747](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/20220508233324.png)

---

*【关于标高的其他小知识：】*

*（对于标高的理解：是在该高度上的一个平面。标高是一种特殊的族类别，如族标高一为$\pm {0}$标高族类型）*

*Tip：可以移动标高的断点对齐标高，对齐后，会产生一把蓝色的锁，使对齐的端点同步变化。*

![image-20220508210644881](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508210644881.png)

*Tip：有时，标高离得过近导致数字重叠，则需要弯头*

<center>
    <img src='https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508214134673.png' style='zoom:0.5'/>
    <br>效果如下：<br/>
    <img src='https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508214333097.png' style='zoom:0.5'/>
</center>

*Tip：若要单独修改某一层标高的样式，需要复制一个新的族类型单独给它。*

<img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508221807766.png" alt="image-20220508221807766" style="zoom: 67%;" />

*Tip：*关于标高旁边小小的3D符号

<img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508222109897.png" style="zoom: 50%;" />

可以发现，点击后“3D”会变为“2D”。例如，在3D下，修改南立面标高线长度，西立面的标高线长度也会变化；在2D下，修改南立面标高线长度，西立面的标高线长度则不会变化。

可以理解为将标高这一矩形平面等比例扩大（3D）与水平拉伸（2D）。

【End 小知识】

#### 2.1.2 轴网

1. 轴网在标高1平面中进行绘制
2. 使用建筑/结构选项卡-轴网（或快捷命令GR）绘制一条轴线
3. 使用与标高相同的方法复制（CC/CO）或者阵列**并解组**（AR）

（一通百通）

双侧标注在类型属性中。

弧形轴线绘制方法：与CAD相同。

![image-20220508224418679](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508224418679.png)

折线轴线绘制方法：使用多段网格。操作上与CAD中PL命令同。（点击后会进入草图模式）

![image-20220508224720076](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508224720076.png)

---

以下为扩展知识。不想看请直接[2.2](#2.2 结构选项卡命令详解)

#### 2.1.3 对扩散型圆弧轴线阵列的方法—— 模型线

说明：直接阵列圆弧轴线仅是将轴线向上平移，并不能形成类似“涟漪”一样的扩散形状。故须采用模型线。此方法对于折线轴线也适用。

1. 建筑选项卡-模型线

![模型线](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508225336434.png)

2. 绘制半圆弧，绘制完成后ESC，GR（轴网命令）使用拾取线拾取圆弧并偏移。

![image-20220508230101136](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508230101136.png)

#### 2.1.4 轴网的影响范围

因为对标高一的轴线进行拉伸，其他标高层不会变化。

若只想让2F与3F的轴线与1F同步变化，其他楼层不变，则需在平面中修改影响范围。

![image-20220508233612181](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508233612181.png)

勾选想要修改的标高平面，即可在选中的图中同步修改轴线。

![image-20220508233833219](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220508233833219.png)

#### 2.1.5 先画标高的原因

若先画标高，则画好轴网后，如果需要增设标高，则可能出现以下情况：立面图中的最高标高高过了轴线。



<center>
    <img src='https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/asdafafsgseau.jpg'style='zoom:0.5'/>
</center>

会导致过高标高对应的平面图没有轴网。你可以说：那我在立面里调高轴线超过标高鸭。可若轴网是弧形的，则在立面中是看不到的，就凉凉啦。

[回到2.1](#2.1 标高与轴网的创建)

### 2.2 结构选项卡命令详解

#### 2.2.1 独立基础

1. 自标高的高度偏移
2. 按轴生成
3. 按柱生成

独立基础可以复制族类型单独编辑。

*Tip：当前窗口属性-视图范围可以调整平面图中展示的图元、投影面的位置*

#### 2.2.2 条形基础

1. 点击命令，点击墙即可
2. 修改-选择多个，可以批量放置条形基础

条形基础具有保护层厚度、材质、尺寸等的参数。

*Tip：材质设置。可以在材质浏览器中新建材质*

#### 2.2.3 筏板基础

草图模式

1. 必须封闭

2. 多种绘制形式：

   绘图区多边形

   拾取墙体（在“绘制”的右下角）

   拾取支座（结构墙、结构梁）

3. 类型属性-结构中修改厚度

筏板基础也具有自标高的高度偏移。

属性中勾选“结构”后才可以进行配筋等操作。

*Tip：倒角命令TR，与CAD中F命令效果相同，可以用于封闭*

*Tip：在结构-钢筋-钢筋保护层设置中添加新的保护层类型，用于各种基础的材料属性设置*

#### 2.2.4 梁

1. 默认绘制的梁的上顶面标高为当前平面标高

   在标高2画的梁实际为第一层楼的梁

2. “在轴网上放置”需要支座（柱、承重墙等）

3. Y轴对正与CAD中ML的对齐方式相同。左中右由绘制方向决定。Z轴对正体现在立面图中。

4. Z轴偏移值调整梁的标高

5. 起点、终点标高偏移用于绘制坡屋顶的梁。*Tip：起点、终点标高偏移设置为同一值后可以达到与Z轴偏移相同的效果*

此外，还有材料、结构用途等参数。

*Tip：画梁时勾选“链”可以连续绘制*

*Tip：不同材质的钢梁连接时会有起点连接缩进，钢梁的修改面板中还有专属的“连接端切割”，用于还原实际的钢梁连接情况*

*Tip：结构-梁系统可以批量等距创建梁。草图模式中，先修改间距、材质等，再画闭合梁范围，再在框附近点选梁方向，确定完成即可。点击梁系统的边框，删除梁系统即可只保存画好的梁。*

#### 2.2.5 楼板

与筏板相似。

属性中有”结构“选项，勾选与否决定其所属专业。

楼板开洞：

法一：草图模式中画轮廓（布尔运算）

![image-20220510003044666](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510003044666.png)

法二：结构-洞口-竖井

![image-20220510003231005](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510003231005.png)

画完后点击完成即可

![image-20220510003416596](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510003416596.png)

效果如下：

![image-20220510003544855](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510003544855.png)

#### 2.2.6 楼板坡度

介绍三种方法。

法一：

选中已经画好的楼板-编辑边界，进入草图模式。若还没画好楼板，则参照2.2.5中方法进入草图模式。

![image-20220510004659685](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510004659685.png)

框选边界作为倾斜的轴。

![image-20220510005016749](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510005016749.png)

勾选自定义坡度

![image-20220510005920456](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510005920456.png)

效果如下：

![image-20220510005938268](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510005938268.png)

注：同一楼板只能设置一处坡度。

法二：

在绘制楼板时绘制坡度箭头，并设置尾高

![image-20220510190958540](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510190958540.png)

也可以通过属性栏选择坡度模式

![image-20220510191320949](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510191320949.png)

法三：

绘制楼板后，选中楼板-修改子图元

![image-20220510192221889](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510192221889.png)

点击断点，设置偏移量即可。

![image-20220510192349388](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510192349388.png)

可通过修改子图元-重设形状还原

也可以通过修改子图元，选择边进行偏移。

*Tip：法三绘制出的坡的属性参数中不包含坡度。但是该方法对于设置地漏、设置较复杂坡度等的适用度高*

#### 2.2.7 结构柱

在平面视图中，选择结构选项卡-柱

![image-20220510193643787](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510193643787.png)

载入族，选择混凝土柱

![image-20220510193813934](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510193813934.png)

下图中“高度”是向上立柱，“深度”是向下埋柱

![image-20220510193922203](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510193922203.png)

未连接，则需手动输入柱高度；标高，则高度自动对齐所选标高。

![image-20220510194045897](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510194045897.png)

可以在类型属性中修改材质、尺寸、保护层等。单独修改需要复制族类型。

也可以像独立基础一样，选择按轴网放置，或者在建筑柱处放置。

*Tip：绘制柱时，对准轴网交点，按空格一次旋转45度，没对准轴网交点，按空格一次旋转90度*

#### 2.2.8 墙体

墙体与柱很像，各种参数的表意也很准确。

勾选“链”可以连续绘制。

各种偏移也与前面类似。设置为“未连接”时，有未连接高度参数；“对齐标高\*”时，有顶部偏移参数。

勾选“房间边界”后才能作为往后“房间绘制”时的参数。

结构的勾选与否决定其所属专业。也可以设置结构用途。

可以在类型属性中复制族类型后，在结构中更详细地设置墙的做法。

##### 叠层墙与复合墙的设置

叠层墙：两种不同类型的墙体构成的墙。如图就能很好展示叠层墙的特点。

<img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510202444395.png" alt="image-20220510202444395" style="zoom:50%;" />

复合墙：

<img src="https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220510202731000.png" alt="image-20220510202731000" style="zoom:50%;" />

##### 叠层墙的自定义：

逻辑：叠层墙是由其他墙体上下叠合成的。

1. 绘制一叠层墙，打开编辑类型-结构
2. 设置偏移可以更改叠合的方式。
3. 也可以修改构成叠层墙的墙的种类。
4. 在族管理器中，修改组成叠层墙的复合墙族类型的参数，叠层墙也会随之发生改变。

自己摸索吧，挺简单的。

##### 复合墙：

复合墙较复杂。详见[B站此课程](https://www.bilibili.com/video/BV1Hb411p7Av?p=11&share_medium=iphone&share_plat=ios&share_source=QQ&share_tag=s_i&timestamp=1652189356&unique_k=CH0RHyw)

#### 2.2.9 钢筋

### 2.3 建筑选项卡命令详解

#### 2.3.1 幕墙

#### 2.3.2屋顶

#### 2.3.3 门、窗绘制与视图范围调整

#### 2.3.4 场地、地形调整

#### 2.3.5 楼梯、坡道

#### 2.3.6 明细表、图纸的创建及调整

#### 2.3.7 房间标记及颜色修改

### 2.4 系统选项卡命令详解

略

### 2.5 族

#### 2.5.1 族的界面

##### 1.  新建族

选择公制常规模型，一般选择“公制常规模型”。

![image-20220511173732828](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511173732828.png)

##### 2. 界面

2.1 宏观

![image-20220511174052698](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511174052698.png)

2.2 族类别与族参数按钮的位置

![image-20220511174149506](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511174149506.png)

![image-20220511174603217](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511174603217.png)

2.3 族类型按钮的位置

![image-20220511174837803](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511174837803.png)

因为一个族类别往往包含多个族类型，所以可以在此处新建族类型

![image-20220511175306871](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511175306871.png)

2.4 其它

![image-20220511175444799](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511175444799.png)

#### 2.5.2 认识族、基本操作

##### 1. 例一（族的绘制、载入到项目、可见性设置）

绘制一长方体：

选择拉伸命令，进入草图模式

![image-20220511175727456](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511175727456.png)

绘制矩形并完成

![image-20220511175802647](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511175802647.png)

效果如下

![image-20220511175850566](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511175850566.png)

载入到项目：

操作如下，会报错。

![image-20220511190320542](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511190320542.png)

则需新建项目或者打开一个项目，以下为新建一个项目

![image-20220511190429811](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511190429811.png)

![image-20220511190510764](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511190510764.png)

切换回到族中

![image-20220511190607731](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511190607731.png)

再点击“载入到项目”时就不会提示没有项目了。

![image-20220511190706127](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511190706127.png)

效果如下：

![image-20220511191033032](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511191033032.png)

修改载入到项目时的指针所在位置：

![image-20220511191211547](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511191211547.png)

这样修改后，放置时，指针就在族的形心了。

![image-20220511191316829](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511191316829.png)

之后可在项目浏览器中通过拖拽的方式载入自己绘制的族：

![image-20220511191515899](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511191515899.png)

可见性设置的位置：

![image-20220511191729950](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511191729950.png)

效果简单易懂形象

![image-20220511191803423](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511191803423.png)

其中，详细程度与项目视图中的以下设置对应：

![image-20220511192028056](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511192028056.png)

##### 2. 例二（体量族——一种特殊的族）

新建概念体量

![image-20220511192256848](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511192256848.png)

操作选项卡中没有同族一样的命令：

![image-20220511192355176](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511192355176.png)

取而代之的是模型、参照、平面。

体量模型是线面体构成的。

#### 2.5.3 族的常用命令

> 关键在于理解“路径”与“轮廓”。

##### 1. 拉伸

新建公制常规模型

见[2.5.2](#2.5.2 认识族、基本操作)的例一，注意：轮廓必须闭合

选中图元后，通过六个箭头可以对模型进行六个方向的推拉。此箭头名为“操作柄”。

![image-20220511193208798](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511193208798.png)

拉伸起点与拉伸终点，自己悟。拉伸起点与拉伸终点由创建体时所在的视图决定（参照标高中绘制创建的即以其为拉伸起点，立面图中创建的即以该立面为拉伸起点）

![image-20220511193449035](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511193449035.png)

也可以在其他视图中绘制，效果如下：

![image-20220511193845278](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511193845278.png)

也可以修改材质

![image-20220511194448872](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511194448872.png)

效果如下：

![image-20220511200930681](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511200930681.png)

这里可以设置空心、实心

![image-20220511201018607](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511201018607.png)

也可以在创建的时候就设置

![image-20220511201044118](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511201044118.png)

空心的图元与实心图元相较会缺少很多属性。

##### 2. 融合

拉伸是一种特殊的融合，是上下面相同的一种融合。

选择融合：

![image-20220511201357545](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511201357545.png)

编辑底部：

![image-20220511201524784](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511201524784.png)

编辑顶部：

![image-20220511201544207](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511201544207.png)

![image-20220511201604293](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511201604293.png)

点击完成，效果如下：

![image-20220511201702775](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511201702775.png)

两个轮廓沿着一条线段（这条线段垂直于创建图元所在视图平面）连接

可以通过操作柄修改高度（图略）

可以通过第一端点、第二端点修改标高：

![image-20220511202023963](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511202023963.png)

可以 修改材质、空/实心

选中后，还可以通过编辑修改高度之外的形状：

![image-20220511202248144](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511202248144.png)

##### 3. 旋转

常用于创建球体或圆锥

进入旋转草图模式：

![image-20220511202406218](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511202406218.png)

绘制一半圆（封闭）：

![image-20220511202458389](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511202458389.png)

绘制旋转轴：

![image-20220511202546688](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511202546688.png)

点击完成，效果如下：

![image-20220511202643085](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511202643085.png)

![image-20220511203032540](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511203032540.png)

可以设置旋转的角度

![image-20220511203226629](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511203226629.png)

效果如下：

![image-20220511203320330](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511203320330.png)

##### 4. 放样

有点复杂[见视频](https://www.bilibili.com/video/BV1Hb411p7Av?p=25&t=602.6)

先路径后轮廓

效果如下：

![image-20220511204532956](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511204532956.png)

##### 5. 放样融合

即两个轮廓沿着一条路径融合

放样是一种特殊的放样融合（两个轮廓相同）

操作详见视频，链接同上

效果如下：

![image-20220511205021047](https://cdn.jsdelivr.net/gh/kingwingshit/Louis/img/image-20220511205021047.png)

#### 2.5.4 五大参数类型

[视频](https://www.bilibili.com/video/BV1Hb411p7Av?p=26)

#### 2.3.5 体量

[体量简介](#2. 例二（体量族——一种特殊的族）)

我摆烂了

[视频](https://www.bilibili.com/video/BV1Hb411p7Av?p=27)

### 2.6 CAD图纸处理与导入项目信息设置

### 2.7 结构案例模型绘制