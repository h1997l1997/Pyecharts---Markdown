# PYECHARS入门学习笔记

pyecharts 是一个用于生成 Echarts 图表的类库。Echarts 是百度开源的一个数据可视化 JS 库。用 Echarts 生成的图可视化效果非常棒，pyecharts 是为了与 Python 进行对接，方便在 Python 中直接使用数据生成图。
## PYECHARTS的安装
在安装PYTHON3的环境下，以管理员的身份打开CMD，输入
>pip install pyecharts

即可完成安装

## 快速入门
#### 构建第一个图表
>from pyecharts import Bar
>
>bar = Bar("我的第一个图表", "这里是副标题")  
>bar.add("服装", ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"], [5, 20, 36, 10, 75, 90])
>bar.print_echarts_options()
>bar.render()

这样你的第一个图表就出来了。可以去PY文件下面的目录找到一个叫render.html的文件，打开就能看到生成的柱形图。
在之中点击右侧的工具就可以保存到本地图片.  
![](https://github.com/h1997l1997/Pyecharts---Markdown/blob/master/Pic/zhuzhuangtu.png)

现在我们来解释一下代码中一些基础语句的作用。  
> from pyecharts import Bar
> 导入pyechatrs模块
> bar = Bar("我的第一个图表", "这里是副标题")  
> 初始化具体类型图表，这里选的柱形图
> bar.add("服装", ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"], [5, 20, 36, 10, 75, 90])
> 添加数据及配置项
> bar.render()
> 生成 .html 文件。

如果你觉得“打开html”再“下载图片”比较繁琐的话，你可以使用一个叫做 pyecharts-snapshot 的插件，来完成生成html之后生成图片的操作。
安装过程
>npm install -g phantomjs-prebuilt
> pip install pyecharts-snapshot

使用方法
>from pyecharts_snapshot.main import make_a_snapshot

调用方法
>make_a_snapshot('render.html', 'snapshot.png')
make_a_snapshot() 第一个参数为生成的 .html 文件，第二个参数为要保存的文件，可以为 png/pdf/gif

今天的内容大约就是这些，后面的内容是Pyecharts各个图表的绘画方法和在地图上实现数据可视化的方法。
