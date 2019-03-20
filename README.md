# SCNN-Deeplabv3-bisenet-icnet

无人车车道线检测挑战赛baseline分享 

详情请点击参赛链接:


http://aistudio.baidu.com/aistudio/#/competition/detail/5
赛题详细介绍可以通过链接去阅读，同时想要找数据集的也可以去下载，如果下载地址失效，可以通过最底下邮箱联系我（如果百度官方觉得数据集涉及到侵权青告知立马删除）。


本次比赛的时间为2018.12.20~2019.3.15，本次比赛主要是2018.12.20~2019.1.25期间做出的成绩，最终复赛成绩，单模型0.484。
（各位大佬莫要吐槽，本人并不是要说明自己又多厉害，其实本人菜的很，只想说明这几个模型还有很大的提升空间，本人能力有限希望大佬能帮忙改进）



本来2018年春节回去打算大干一场的，结果想太多，一回去就是搬砖和家里的各种杂事，年后回学校由于找实习和论文等各种事儿，很多有效的改进和想法只能止步于想法。
比如：
  一、车道线远近不同可以通过透视变换变成俯视图，可以提高远处的车道线的准确率
  二、模型之间的融合，每个模型对每个类别的识别效果不一样，可以做一个bagging的思想
  三、对图像预处理做对比变换。
  四、识别后可以用经典图像方法后续处理，如：腐蚀，膨胀，连通域等
  无奈，想法最后只能止步是想法，希望这些想法对做车道线的大佬有点儿帮助。

框架：paddlepaddle（爬都爬抖）
由于本次比赛是基于paddlepaddle框架的车道线分割，目前paddlepaddle的用户较少，而且paddlepaddle开源的语义分割的模型更是有限。
只能自己一步一步的采坑踩过来，其中的艰辛都是泪（paddlepaddle的机制太不完善，不过值得庆幸的是百度的issue和工程师很给力）。

本次比赛使用的主要模型有：BiseNet、SCNN、deeplabv3+、ICNet，由于时间匆忙，数据读取和制作的地方写的不太灵活动，不过其中我都写了很多注释，可以调用函数来读取数据。
主要还是看模型部分即可，数据读取和制作的方式各位大佬可以根据自己的喜好来即可。
（模型主要参照论文来复现的，模型写的很粗糙，欢迎大佬改进和吐槽）

如果能对您们有帮助是我荣幸，也大佬麻烦用您的小手按下右上角的star，谢谢各位大佬！！！


邮箱：1174548879@qq.com


想一起学习和交流技术欢迎邮件联系（看到了邮件必回复）,一起交流其学习一起进步，需要百度数据集的也请邮箱联系我，到时候百度网盘链接分享给你！