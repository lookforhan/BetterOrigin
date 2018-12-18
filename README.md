# BetterOrigin

# 说明

原作者并没有写README.md文件，可能是这个命令对原作者太简单了吧。我fork过来后，对原有的两个文件：doc_example.m和plot_data_to_origin.m文件进行了仔细的阅读和运行发现一下问题：

1. doc_example.m文件，在19行处第一次出现filenames变量，而且上文未对该变量进行赋值，因此运行到19行处会报错。联系下文，猜测filenames应该是元胞数组(cell)，但不知道为何没有赋值是否是原作者在复制时出现错误。

2. plot_data_to_origin.m文件，整体和doc_example.m文件结构类似，但是在62行运行出现错误。origin中错误提示为："plotxy:X-Function failed to execute!
Bad argument, iy:=
[mydata]Sheet1!(1,2:3)plot:=201ogl:=[<new template:=origin name:=MyGraph>]"
