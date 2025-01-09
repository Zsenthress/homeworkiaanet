此IAAnet代码基于开源的IAAnet做了部分修改工作：
更改了其数据装载部分，train、test等文件。

在跑此代码之前：
需要安装深度学习环境，可按照此教程：https://blog.csdn.net/up_and_down__/article/details/125739528?fromshare=blogdetail&sharetype=blogdetail&sharerId=125739528&sharerefer=PC&sharesource=m0_74250200&sharefrom=from_link

说明：
train.py用来训练网络模型，test.py用来测试，detect.py用来预测照片、也可用来做可视化
训练的结果保存在result.docx文档中，网络参数模型在outputs中，其中best.pt为训练过程中最好的模型。原开源代码也提供了自己的模型，在iaanet.pt中。

（一）训练模型：
1、训练集为dataset中的训练集部分
2、验证集可自行设置，为保证可信度，本文将val验证集设置为train数据集的20%，即训练集的前2000张照片。

（二）测试模型：
test.py中以F1score为衡量指标。测试集可选dataset中的MDvsFA(99张)或者SIRST（427张）。
