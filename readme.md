# 程序说明 

(**注: 本程序仅供编程学习使用, 不对实际投资构成建议**)



## 海龟交易法

​		海龟交易策略是一套非常完整的趋势跟随型的自动化交易策略。这个复杂的策略在入场条件、仓位控制、资金管理、止损止盈等各个环节，都进行了详细的设计。它的基本思想是通过近20天内的沪深300指数波动情况以及当天的股价来判断未来涨跌的趋势，当当天股价高于一个界限时，认为未来股价存在上涨的趋势，立即进行买入。而当已经有持仓时，如果股价有继续上涨的趋势，则继续加仓；如果股价跌破一个下界，则减少持仓量。



## 程序使用说明

​	使用前，请在安装Python3.6或以上版本，并安装部分第三方库，包括PyQt5、qtawesome、matplotlib、numpy库。

​	**运行程序前，请将电脑分辨率调成1920×1080，并将电脑日期的显示格式调成如“2021-06-01”的形式。**

​	进入程序后，在“参数设置”一栏中选择需要调整的参数（其中期初资金必须主动设置，其余参数如果不主动设置将视为默认值），在“图像显示”一栏中选择需要显示的图像，单击界面最下方的“测试/重测”按钮可以进行测试/重新测试。所生成的测试结果将自动保存至程序所在的文件夹下。单击“删除当前结果”按钮可以删除所生成的测试结果。在“帮助”一栏中，可查看相关专业名词的含义，提供反馈建议或通过邮箱与开发者联系。单击界面最下方的“退出”按钮可退出程序。(界面详细操作请参考界面设计部分)



## **界面设计**

​	界面分为左右两部分: 左边为垂直布局，分为三个板块：参数设置、图像显示和帮助。

1、参数设置板块下是可变参数的设置和更改。

​	（1）设置期初资金按钮的图标为人民币符号。点击该按钮后弹出小窗口，小窗口为网格布局，设置有标签提示语“请输入您的期初资金（整数万元）”、整数输入框、OK和Cancel按钮。

​	（2）设置交易开始时间的图标为计时沙漏的初始状态。点击该按钮后弹出小窗口，小窗口为网格布局，设置有三个标签提示语“请输入您的交易开始时间”、“时间格式示例：2011-03-01”、“时间范围为2011-03-01至2021-04-01”，以及文本输入框、OK和Cancel按钮。

​	（3）设置交易结束时间的图标为计时沙漏的终止状态。点击该按钮后弹出小窗口，小窗口为网格布局，设置有三个标签提示语“请输入您的交易结束时间”、“时间格式示例：2020-04-01”、“时间范围为2011-03-01至2021-04-01”，以及文本输入框、OK和Cancel按钮。

​	（4）修改唐奇安通道的图标为箭头走势图。点击该按钮后弹出小窗口，小窗口为网格布局，设置有标签提示语“唐奇安通道修改为：”、显示滑动块数值的数字显示框、范围为5~50的整数滑动块、OK和Cancel按钮。整数滑动块默认数值为20.

​	（5）修改ATR的图标为圆圈打勾图。点击该按钮后弹出小窗口，小窗口为网格布局，设置有标签提示语“ATR修改为：”、显示滑动块数值的数字显示框、范围为5~50的整数滑动块、OK和Cancel按钮。整数滑动块默认数值为20.

​	（6）修改手续费的图标为饼状图。点击该按钮后弹出小窗口，小窗口为网格布局，设置有标签提示语“修改手续费为（单位：万分之一）：”、整数输入框、OK和Cancel按钮。整数输入框默认数值为1.

​	（7）修改投资系数的图标为阶梯箭头图。点击该按钮后弹出小窗口，小窗口为网格布局，设置有标签提示语“修改投资系数为（单位：百分之一）：”、整数输入框、OK和Cancel按钮。整数输入框默认数值为1.

点击OK，相应参数会传入程序，同时小窗口关闭；点击Cancel，输入或设置的值清空，小窗口仍然保留。如果未输入相应数值，点击OK，无反应。

2、图像显示板块下是可选图像的勾选，包括策略收益、沪深300、仓位图。

3、帮助板块：

（1）专业名词含义查询的图标为问号。点击该按钮后弹出小窗口，小窗口为水平布局，设置有标签提示语“请选择专业名词”和下拉框。下拉框中可选：唐奇安通道、ATR、投资系数，基准收益率，年化收益率。选中后在标签处会显示其含义。

（2）反馈建议的图标为消息。点击该按钮后弹出小窗口，小窗口为网格布局，设置有标签提示语“您的反馈与建议”、文本输入框、OK和Cancel按钮。点击Cancel，输入的文本内容清空，小窗口仍然保留；点击OK，反馈与建议会传入程序存放，同时小窗口关闭，弹出新的感谢小窗口“感谢您的反馈与建议！基于您的反馈与建议，我们会努力做得更好！”，点击OK可关闭感谢小窗口。

（3）联系我们的图标为邮件。点击该按钮后弹出小窗口，小窗口为水平布局，设置有标签提示语“欢迎您来信联系我们！”以及三位开发者的邮箱，点击“网易邮箱”标签会通过电脑浏览器打开网易邮箱主页，点击“QQ邮箱”标签会通过电脑浏览器打开QQ邮箱主页，便于用户写邮件给开发者。

左边为网格布局，分为三个板块：数据显示、图像显示和操作。

1、数据显示板块显示期初资金、总资产、累计盈亏、可交易天数、年化收益率、开始时间、结束时间、胜率在下方相应文本框（文本框不可点击）。

2、图像显示板块分为上下两个部分：

（1）上半部分相对较大，是策略收益图和/或沪深300图（显示具体情况由左边勾选确定）；

（2）下半部分相对较小，是仓位图。

（3）既不勾选策略收益图，也不勾选沪深300图，上半部分显示原背景图；不勾选仓位图，下半部分显示原背景图。

3、操作板块：

（1）测试/重测的图标为蓝色圆环状箭头；

（2）删除当前结果图标为灰色文件图；

（3）退出图标为红色叉。



## Requirements

​	QtAwesome >= 1.0.1

​	pyqt >=5.9.2

​	numpy>=1.19.2

​	matplotlib>= 3.3.2



## **备注**

**如果在程序使用之中遇到恶行bug或者其他问题, 可以随时通过邮件联系我们或者在GitHub上提交issue, 我们会尽快回复您的困惑.**

