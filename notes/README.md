# 课堂笔记提纲

## 内容简介

### When Can Machines Learn? [何时可以使用机器学习]

- The Learning Problem [机器学习问题]
- Learning to Answer Yes/No [二元分类]
- Types of Learning [各式机器学习问题]
- Feasibility of Learning [机器学习的可行性]

### Why Can Machines Learn? [为什么机器可以学习]

- Training versus Testing [训练与测试]
- Theory of Generalization [举一反三的一般化理论]
- The VC Dimension [VC 维度]
- Noise and Error [噪声一错误]

### How Can Machines Learn? [机器可以怎么样学习]

- Linear Regression [线性回归]
- Linear 'Soft' Classification [软性的线性分类]
- Linear Classification beyond Yes/No [二元分类以外的分类问题]
- Nonlinear Transformation [非线性转换]

### How Can Machines Learn Better? [机器可以怎么样学得更好]

- Hazard of Overfitting [过度训练的危险]
- Preventing Overfitting I: Regularization [避免过度训练一：控制调适]
- Preventing Overfitting II: Validation [避免过度训练二：自我检测]
- Three Learning Principles [三个机器学习的重要原则]

## 周次内容

- 第一周：ML简介、ML与DM/AI/Statistics的区别。
- 第二周：perceptron线性分类器。
- 第三周：从输入特征、输出空间、label状况、学习方式四方面对 ML 进行分类。
- 第四周：PAC 学习原理（尽量大的训练集D和有限的假设空间H）。
- 第五-七周：'Shatter' and VC Dimension(打散和VC维度)（无限假设空间，但可以分为有限个不同类别的空间，即 ${VC}$ Dimension有限，${D}$ 尽量大，则学到的model可以较好泛化到测试集）。
- 第八周：noise and error和weighted algorithm。
- 第九周：linear regression。
- 第十周：logistic regression。
- 第十一周：multiclass classification。
- 第十二周：nonlinear hypothesis。
- 第十三周：noise and overfitting。
- 第十四周：regularization。
- 第十五周：cross validation and model selection。
- 第十六周：机器学习基石方法建议及课程总结。

## 一些解释

### VC

${VC}$ 维（Vapnik-Chervonenkis Dimension）的概念是为了研究学习过程一致收敛的速度和推广性，由统计学理论定义的有关函数集学习性能的一个重要指标。
传统的定义是：对一个指示函数集，如果存在 ${H}$ 个样本能够被函数集中的函数按所有可能的 ${2^H}$ 种形式分开，则称函数集能够把 ${H}$ 个样本打散；函数集的 ${VC}$ 维就是它能打散的最大样本数目 ${H}$。若对任意数目的样本都有函数能将它们打散，则函数集的 ${VC}$ 维是无穷大，有界实函数的 ${VC}$ 维可以通过用一定的阈值将它转化成指示函数来定义。

${VC}$ 维反映了函数集的学习能力，${VC}$ 维越大则学习机器越复杂（容量越大），遗憾的是，目前尚没有通用的关于任意函数集 ${VC}$ 维计算的理论，只对一些特殊的函数集知道其 ${VC}$ 维。例如在 ${N}$ 维空间中线形分类器和线性实函数的 ${VC}$ 维是 ${N+1}$。

### shatter

所谓 shatter（打散），说人话就是：有 ${N}$ 个样本点，每个样本点可以表示 ${2}$ 种可能的情况（比如是否上大学、是否吃了午饭），那么总共有 ${2^{N}}$ 中不同的组合，【每一种组合】就可以被看成【这 ${N}$ 个样本点的一种 shatter】。

### VC Dimension

所谓（某个模型的）VC Dimension，说人话就是：如果一个模型（或函数）能够将 ${N}$ 个样本点的【所有组合的】shatter 全部分辨出来，而不能分辨出 ${N+1}$ 个样本点的【所有组合的】shatter，那么称，这个模型（或函数）的 ${VC}$ Dimension是 ${N}$ 。用英语解释是 **"effective binary degrees of freedom"** ，往往可以近似看作这个模型（或函数）的参数的数量。

### closed-form solution

所谓 closed-form solution：比如正规方程求解 ${w}$ ，${w = (X^TX)^{-1}X^T Y}$ ，这种能够用一个等式直接求解的方式称为 closed-form。

## 参考

1. [台湾大学林轩田老师机器学习基石：内容简介](http://blog.csdn.net/mmc2015/article/details/50689626)