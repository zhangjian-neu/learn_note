# 常用Linux 插件及配置技巧

1. 为Firefox安装Adobe Flash Player： (**最好使用google chrome**) https://blog.csdn.net/linuxnews/article/details/51750195
2. 调节ubuntu亮度：https://blog.csdn.net/lingyunxianhe/article/details/81116157
3. 调整多屏分辨率 https://blog.csdn.net/tidyjiang/article/details/70861096

# 1  Python Checklist
1. 什么是容器？在那里存放？哪个容器不可迭代？
2. 什么是可迭代对象？
3. 什么是迭代器（iterator）？在那里存放？与可迭代对象有什么关系？
4. 可不可以自定义迭代器？如何定义？
5. 生成器与迭代器的关系？生成器的特点？优点？
以上问题答案在 http://python.jobbole.com/87805/ ，https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/001431779637539089fd627094a43a8a7c77e6102e3a811000
6. 与列表生成式相比，生成器有什么优点？如何制作生成器？
https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/0014317799226173f45ce40636141b6abc8424e12b5fb27000
7. 什么是map？什么是reduce？
https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/0014317852443934a86aa5bb5ea47fbbd5f35282b331335000
8. 解释型语言和编译型语言的异同？
https://blog.csdn.net/u014647208/article/details/78329187
9. 类变量与实例变量
https://www.cnblogs.com/crazyrunning/p/6945183.html
10. 修改Jupyter浏览器
  - 1、打开anaconda prompt
  - 2、输入jupyter notebook --generate-config
  - 3、显示出jupyter_notebook_config.py 文件所在目录。找到这个文件，用记事本打开。
  - 4、在# c.NotebookApp.browser = '''' 后加入下面语句块：
  import webbrowser
  webbrowser.register("chrome",None,webbrowser.GenericBrowser(u"C:\\ProgramFiles(x86)\\Google\\Chrome\\Application\\chrome.exe"))
  c.NotebookApp.browser = 'chrome'
  - 5、上条中红色字体应替换为本机中chrome实际安装地，查看方法为开始菜单-chrome-右键点击属性，快捷方式页签有目标，是完整路径，粘在上面即可。注意表示目录的“\”要改变为双“\”

# 2  Python的官方文档
http://www.pythondoc.com/pythontutorial3/index.html

1.  相比于C++， Python 有哪些优势？见开胃菜。
2.  交互模式中最近一个表达式的赋值是如何表达的？见python简介。
3.  索引？切片？
4.  函数名重用。4.6
5.  如何定义及调用函数参数？4.7
6.  编码风格。4.8
7.  实现高效的队列。 5.1.2
8.  元组不可改变，但元组可包含可变对象。5.3
9.  模块与包。6
10.  入输出的几种方式？json是什么及其用法？7
11.  异常涉及到的几个关键字及其用法。8
12.  Python中的别名及其特性。9.1
13.  Python作用域和命名空间。9.2
14.  类对象与对象是有区别的。9.3
15.  类变量与实例变量。9.3.5
16.  类编程的一些惯用技巧，如命名约定。9.4
17.  以一个下划线开头的类变量和以两个下划线开头的类变量有什么特殊之处。9.6


- 第9章（类）之后开始转向廖雪峰网站学习。

# 3 廖雪峰-Python3-面向对象编程
https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000

1.  面向对象编程
  - i. 面向对象编程的三大特点
  - ii. 什么是动态绑定？见‘类和实例’的结尾处。
  - iii. 私有变量？见‘访问限制’。
  - iv. 子类的实例对象和父类有什么关系？见‘继承和多态’。
  - v. 多态的“开闭”原则是什么？见‘继承和多态’。
  - vi. 静态语言与动态语言的区别。见‘继承和多态’结尾处。

2.  定制类-使用魔法函数
  - i. __str__ 与 __repr__
  - ii. __iter__与 __next__
  - iii. __getitem__
  - iv. __getattr__
  - v. __call__

# 4《流畅的Python》
使用kindle打开。阅读至26.5页。
1.  Python数据模型 的好处

# 5  Quadratic programming – interior point
- 有效集法： https://blog.csdn.net/fangqingan_java/article/details/49720497
https://blog.csdn.net/philthinker/article/details/78510361?locationNum=10&fps=1
https://wenku.baidu.com/view/ad34f36079563c1ec5da71fc.html
代码：https://blog.csdn.net/sceart/article/details/53761030

- 原对偶内点法：https://wenku.baidu.com/view/f98bda1fa8114431b90dd888.html

# 6  Machine Learning (Andrew NG)
https://www.coursera.org/learn/machine-learning/lecture/OVM4M/deciding-what-to-try-next

### 1  Linear Regression  video-2
1. Multivariate Linear Regression
  - 线性回归中，最小二乘与梯度下降的比较：https://www.cnblogs.com/Sinte-Beuve/p/6188145.html

### 2  Advice for Applying Machine Learning video-6
1. Evaluating a learning algorithm	video-6-01
  - 测试误差很大怎么办？  诊断一个算法有哪些好处？
  - 如何评估一个假设函数（训练出的函数）？overfitting 还是underfitting?
  - 机器学习中，模型的选择包括哪两个方面？如何估计模型泛化误差？
2. Bias vs. Variance
  - 高的bias和高的variance分别对应哪两种fit？
  - 如何使用交叉验证误差和训练误差来判断overfit和underfit?
  - 正则化可以防止过拟合吗？
  - 如何选择正则化参数？
  - 学习曲线包含哪两条？横纵坐标都表示什么？
  - 在high bias情况下，学习曲线是什么样的？
  - 在high variance情况下，学习曲线是什么样的？它们有什么区别？
  - 处理overfit 和 underfit 的措施有哪些？

### 3  Machine Learning System Design video-6
  - i. 误差分析是在分析什么？
  - ii. 如何对模型进行数值评估？
  - iii. 误差分析是不是一定会带来表现提升呢？
  - iv. Skewed class指的是什么？
  - v. 处理Skewed class时，使用什么数值指标评估模型？
  - vi. 数据到底会对模型表现有多大影响？如何评估数据是否包含了有用的信息？

### 4  Support Vector Machine video-7
1. Large Margin Classification
  - SVM的损失函数与逻辑回归（LR）的损失函数有什么不同？
  大间距分类器。努力将正负样本以最大margin分开。Margin是边界到样本的距离。
2. Kernels
  - 多项式特征是最好的吗？
  - 如何选取标记点？
  - 莫塞尔定理是什么？
  - 如何确定使用LR还是SVM？或者神经网络？

### 5  Unsupervised learning & Dimensionality reduction  video-8
1. Clustering
  - K- means算法：簇分配，簇中心移动。
  - K-means的损失函数是什么？
  - 如何初始化K-means?如何避免局部最小？
  - 如何选择类的数目K？
2. Kernels
  - 多项式特征是最好的吗？
  - 如何选取标记点？  
  - 莫塞尔定理赛
3. 降维的目的是什么？
4. PCA
  - PCA是依据什么推导出来的？Video:PCA1
  - 投影误差 Video：PCA1-1.28
  - 数据预处理Video：PCA2-1.30
  - PCA 的基本步骤是什么？Video:PCA2
  - 如何恢复使用PCA压缩后的数据？
  - 如何选择压缩后的维度k？

### 6  Anrmaly Detection & Recommender Systems  video-9
i. Density estimation
     异常检测的应用实例 Video1-6.00
     高斯分布是什么？参数如何估计？Video2
     有多个特征时，各特征不独立怎么办？Video3-2.10
ii. Building an Anomaly Detection System
     如何给training data set、cross validation data set 及test data set 分配数据？Video 1
     Anomaly detection vs. Supervised learning. Video 2
非高斯分布的数据如何处理？Video 3
已有特征不能很好区分异常数据点时，如何处理？Video 3
iii. Multivariate Gaussian Distribution
使用独立的高斯分布不能进行故障检测的例子是什么？ Video 1
多高斯分布的参数如何估计？Video 2
多高斯分布的缺点是什么？为什么会有这个缺点？Video 2-8.30
多高斯分布中，协方差矩阵不可逆的原因是什么？ Video 2-12.00     
iv. Predicting Movie Ratings
     Recommendation Systems 的一个重要的好处是什么？ Video 1-2.00
     基于内容的推荐。它的缺点是什么？Video 2
v. Collaborative Filtering
     Collaborative Filtering与“基于内容的推荐”需要的数据有什么不同？Video 1
     协同滤波中的“协同”是什么意思？Video 1-9.30
vi. Low Rank Matrix Factorization
     Low Rank Matrix Factorization与Collaborative Filtering有什么关系？Video 1-4.30
     为什么要进行mean normalization？ Video 2
### 7  Large Scale Machine Learning  video-10
i. Gradient Descent with Large Datasets
原有的梯度下降算法（Bath Gradient Descent）有什么缺点？Video 2
为什么SGD开始时要打乱training set 中的数据顺序。Video 2-7.30
SGD的基本步骤。Video 2-9.20
比较Mini-Batch GD与SGD。Video 3-5.00
如何观察SGD是否已经正确学习？Video 4
ii. Online Learning
举例Online Learning。
什么是CTR？
iii. Map-Reduce （映射-简化） and Data Parallelism
为什么要用这种方法？
主要的思想是什么？
如何判断是否应该使用Map-reduce？Video-8.30
能否在一台计算机上实现Map-reduce？与多台计算机相比，有什么好处吗？Video-11.00
### 8  Application Example: Photo OCR （Optical Character Recognition） video-11
i. Photo OCR pipeline Video 1-3.00
ii. 获得一个比较有效机器学习系统的方法是什么？ Video 3-0.00
iii. Artificial Data Synthesis是用来干什么的？Video 3-0.15
    两种合成方式。Video 3-0.50
    调试机器学习时的两个需要思考的问题：学习曲线和获取数据的时间。
    机器学习系统的方法是什么？ Video 3-0.00
iv. Ceiling Analysis (上限分析)
   为什么要进行上限分析？Video 4-0.00

# 7  Deep Learning (Andrew NG)
书籍： http://www.deeplearningbook.org/
1   查看心得体会网址
i. 学习对应的笔记
                心得体会：
https://blog.csdn.net/koala_tree/article/details/79913655
https://www.sohu.com/a/164569342_505915
      最后尝试学习coursa上面的课程，学习Tensorflow。

# 8  Deep Learning - MIT Book
http://www.deeplearningbook.org/
1.  Machine Learning Basics - P96
i. Learn的三要素 P51
ii. Design matrix的构成P104
iii. Machine learning 与Optimization的区别P108
iv. 模型的表达能力与有效能力P111
v. 非参数化模型的代表P113
vi. 极大似然估计 P129
     什么是模型分布与经验分布？P130
vii. 贝叶斯估计与极大似然估计的区别？P134
     https://blog.csdn.net/u011508640/article/details/72815981
     什么是MAP估计？P137
viii. 核与映射的关系？几何上，核表示的是什么？ P140
ix. 无监督学习的任务是什么？P144
     在机器学习中，representation 指的是什么？P144
     将PCA视为无监督学习方法。P145
x. 为什么会研究Deep Learning？ P152
xi. Mainfold流形。P157
    传统的方法依赖于“局部持续（平滑正则）”假设，样本数量必须多于局部区域数量，如决策树、KNN及核技术。这个条件在有高维特征时很难保证。深度学习依赖流形假设客服该问题，也就是数据之间是由流形连接在一起的。
2.  Deep Feedforward Networks - P164
i. 深度前馈网络的三个名称是什么？P164
ii. Feedforward Neural Networks 与Recurrent Neural Networks的区别？P164
iii. 模型的深度？P165
iv. 为了拟合非线性函数，Deep Learning 如何处理非线性转换？P165
v. Example: Learning XOR P167
    线性模型为什么不能拟合XOR？P168、P169
    为什么不能使用线性函数作为隐层激励函数？P168
    Relu函数的数学表达是什么？P171 它有哪些好处？P170
vi. Gradient-Based Learning P172
    如何初始化Feedforward Neural Networks。P173
    极大似然估计的一个好处？P175
    训练神经网络时，对损失函数的梯度有什么要求？P175
    损失函数可能是一个泛函（函数的函数），其对应的优化问题需要使用变分求解。P176
    为什么cross-entropy损失函数比均方差函数和平均绝对误差函数更流行？P177
    隐层和输出层各在网络中扮演什么角色？P177
    线性函数作为输出层，主要应用于哪种任务？P178
    sigmod函数作为输出层，主要应用于哪种任务？P178
    Sigmod为什么会有效？P180 为什么此时极大似然是有效的？P180
    Softmax函数作为输出层，主要应用于哪种任务？P180
    Softmax 函数如何避免饱和？P182
    Softmax函数中的soft指的是什么？P183

# 9 机器学习技法 (林轩田)
        https://www.bilibili.com/video/av12469267/

关注于“特征转换”，主要有三个内容：SVM，AdaBoost和Deep Learning。包括RF、GBDT等等。
1  Support Vector Machine video-7
i. SVM的知识点：https://www.cnblogs.com/bentuwuying/p/6444516.html
     什么是概
2  Boosting-Adaboosting, GBDT, Xgboost
i. 三者比较:
     https://www.cnblogs.com/willnote/p/6801496.html
     什么是
3  Random Forest
i. 概念上RF与GBDT的对比
     https://www.cnblogs.com/willnote/p/6801496.html
     什么是

# 10  Tensorflow
        很好的总结资料： https://www.cnblogs.com/mq0036/p/8595608.html
1. 安装
     https://blog.csdn.net/Aiolia86/article/details/80342240?utm_source=blogxgwz1
     https://blog.csdn.net/m0_37924639/article/details/78785699
2. tf中的参数初始化方法
https://blog.csdn.net/dcrmg/article/details/80034075
3. tf.variable() tf.get_varible() 区别？
https://blog.csdn.net/u012223913/article/details/78533910?locationNum=8&fps=1

# 11   线性代数的本质（The essence of linear algebra）
参考https://www.bilibili.com/video/av5987715/?spm_id_from=trigger_reload
1. 向量是什么？video-01
i. 三种向量的理解。
ii. 线性代数中向量的起点？物理中向量的起点？ 02:31
iii. 向量和点的表达的区别，方括号还是圆括号？3:45
iv. 向量的基本运算。04:40
2. 线性组合、张成的空间与基 video-02
i. 什么是“向量的线性组合”？03:00
ii. 什么是向量张成的空间（span）？04:00
iii. 三维坐标系下，两个不共线向量张成的空间？06:30
iv. 向量空间的某一个基的严格定义。09:00
3. 矩阵与线性变换 video-03
i. “变换”与“函数”的区别？01:00
ii. 线性变换的两条性质。02:40 线性变换到底是什么？09:40
iii. 矩阵向量乘法是什么？10:13
4. 矩阵乘法与线性变换复合 video-04
i. 矩阵和向量乘法代表什么？01:40
ii. 线性变换复合与矩阵乘法的关系？两个矩阵相乘是什么？03:25
iii. 矩阵乘法有交换率吗？为什么？ 07:30
5. 行列式 video-05
i. 行列式的几何意义？02:25
ii. 行列式为负表示什么？04:35
6. 逆矩阵、列空间与零空间 video-06
i. 逆矩阵与单位矩阵？05:10
ii. 什么是列空间？ 08:50
iii. 列空间与秩的关系？09：20
iv. 零空间（核）？10：20
7. 点积与对偶性 video-07
i. 点积的几何解释？01:30
ii. 点积次序的影响？02:35
iii. 点积的计算方法和投影是如何联系在一起的？03:55， 7:20
iv. 对偶性。12:00
8. 叉积的标准介绍 video-08-1
i. 叉积数值大小的几何意义？01:00
ii. 叉积正负的定义？01:40
iii. 叉积与行列式。02:35
iv. 三维空间中的叉积是什么？05 :00
9. 以线性变换的眼光看叉积 video-08-2
i. 如何将叉积理解为线性变换。03:15。 目的是为了理解叉积计算过程与几何含义之间的关系。
ii. 叉积运算过程说明了什么？08:00
iii. 叉积的几何解释。09:15
10. 基变换 video-9
i.  如何看待线性代数中的坐标？00:10
ii. 坐标系的一种定义。01:10
iii. 如何转化坐标系？04:10
iv. 线性变换与基变换08:50
——如何将线性变换转换为某一坐标系下的相同的变换？
——如何看待P-1AP?
11. 特征值与特征向量 video-10
i. 研究特征值有什么用？04:00
ii. 没有特征值的矩阵。11:00
iii. 特征基。对角矩阵的特征向量和特征值。13:00
iv. 从特征基的角度看原来的线性变换，该变换是什么？15:00
12. 抽象向量空间 video-11
i. 向量的两种理解。00:30
从函数的角度，有没有更深层次的理解呢？02:14
广义的向量的理解。11:20，14:00
ii.  矩阵描述多项式求导。06:00
iii. 一些线性代数的概念与函数的概念。11:15
iv. 定义向量空间的8条公理。它们背后的两条运算是什么？12:40

# 12 关系数据库
https://baike.baidu.com/item/%E5%85%B3%E7%B3%BB%E6%95%B0%E6%8D%AE%E5%BA%93/1237340?fr=aladdin
1  数据库
i. 略

# 13  git
git 的参考廖学锋网站。
1. 使用git管理word
https://www.cnblogs.com/yezuhui/p/6853271.html

- 修改仓库名称 https://blog.csdn.net/zht741322694/article/details/79508574

# 14  ubuntu系统
### 1.  Thinkpad480s – 安装win10、ubuntu双系统
vii. 自带win10。
viii. 查看UEFI还是BIOS？
http://www.xitongtiandi.net/wenzhang/win7/2015-05-11/1482.html
ix. 安装双系统笔记
https://blog.csdn.net/davidhopper/article/details/78884196
x. 下载ubuntu镜像
去清华大学镜像网站，复制下载链接地址，然后使用迅雷下载。
### 2.  LibreOffice
vii. LibreOffice 插入公式
https://blog.csdn.net/matrixvirus/article/details/52420134
### 3.  Anaconda
i. 下载：清华的开源软件镜像站https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/
ii. 安装教程：https://blog.csdn.net/u012318074/article/details/77074665
iii. 使用： https://blog.csdn.net/horcham/article/details/57075388
iv. spyder的端错误：https://blog.csdn.net/xiaoshen0121/article/details/81291432
v. Linux 下给Spyder创建桌面快捷方式： https://blog.csdn.net/wu_lian_nan/article/details/76170121
### 4.  gcc
- gcc安装教程如下：
https://blog.csdn.net/anneqiqi/article/details/51725658
- 写程序大体步骤为：
  1. 用编辑器编写源代码，如.c文件。
  2. 用编译器编译代码生成目标文件，如.o。
  3. 用链接器连接目标代码生成可执行文件，如.exe。

如果源文件太多，一个一个编译时就会特别麻烦，于是人们想到，为什么不设计一种类似批处理的程序，来批处理编译源文件呢，于是就有了make工具，它是一个自动化编译工具，你可以使用一条命令实现完全编译。但是你需要编写一个规则文件，make依据它来批处理编译，这个文件就是makefile，所以编写makefile文件也是一个程序员所必备的技能。

对于一个大工程，编写makefile实在是件复杂的事，于是人们又想，为什么不设计一个工具，读入所有源文件之后，自动生成makefile呢，于是就出现了cmake工具，它能够输出各种各样的makefile或者project文件,从而帮助程序员减轻负担。但是随之而来也就是编写cmakelist文件，它是cmake所依据的规则。所以在编程的世界里没有捷径可走，还是要脚踏实地的。

原文件－－camkelist ---cmake ---makefile ---make ---生成可执行文件

### 5.  opencv
i. opencv安装教程如下：
https://blog.csdn.net/GreenHandCGL/article/details/81452362
ii. opencv使用：
https://www.cnblogs.com/neo-T/p/6430583.html
### 6.  vim
i. 安装：
https://blog.csdn.net/zht741322694/article/details/78959338
ii. 使用
https://www.cnblogs.com/everyday0error/p/5316363.html
iii. 常用快捷键
             https://linux.cn/article-8143-1.html
iv. vim卡死的原因
使用vim时，如果你不小心按了 Ctrl + s后，你会发现不能输入任何东西了，像死掉了一般，其实vim并没有死掉，这时vim只是停止向终端输出而已，要想退出这种状态，只需按Ctrl + q 即可恢复正常。

### 7.  root密码
i. 设置及修改
https://blog.csdn.net/u013063153/article/details/53303045
### 8. sudo执行命令时提示找不到该命令
i. https://blog.csdn.net/Cryhelyxx/article/details/53384004
### 9.  安装子书阅读器calibre
https://calibre-ebook.com/download_linux
### 10.  linux常见命令
i. 教程如下：
  https://blog.csdn.net/ljianhui/article/details/11100625
https://www.cnblogs.com/lz2lhy/p/6843634.html
### 11.  Jupter notebook使用方法
i. 使用
https://www.linuxidc.com/Linux/2017-03/142295.htm
### 12.  浏览器
i. 推荐使用chrome，安装方法如下：
https://jingyan.baidu.com/article/335530da98061b19cb41c31d.html
尽量不要使用firefox，它使用老版的flash，可能不能支持一些视频网站，如bilibili。
ii. 解决无法播放cousera的问题
https://www.cnblogs.com/shuaishuai-it/p/6722725.html
### 13.  拯救黑屏

https://blog.csdn.net/u012348774/article/details/81042843

### 14.  使用nvidia显卡
默认情况下，系统使用的是Intel集成显卡，若要切换显卡，需要以下步骤：
  1. 关闭Device Guard，至Disable。
  2. 关闭 Boot Security，至Disable。
  3. 在应用程序的NVIDIA X Server Settings中，进入PEIME Profiles选项，设置显卡优先级。
  4. 使用以下两条命令更新显卡：
  ubuntu-drivers devices
  sudo ubuntu-drivers autoinstall
15  tex
https://blog.csdn.net/qq_41814939/article/details/82288145

### 15  机器学习的资料
1. 前阿里资深工程师的总结
http://www.huaxiaozhuan.com

### 16  Shell
1  什么是shell？
https://blog.csdn.net/weixin_41122339/article/details/81078900
i. chmod命令
https://blog.csdn.net/SprintfWater/article/details/8220185
ii.
