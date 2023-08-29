#### train.py 参数介绍

--model：指定模型结构文件，都存放在config文件夹下了，默认的是替换了FPN以及预测头的模型结构

--data：指定存放数据读取路径文件，指定的txt文件里面存放的是图片的读取路径，同样存放在config文件夹下了，默认的是使用两批Union数据以及Sun数据

--pretrained_weights：指定预训练文件，默认的是之前训练100epoch得到的最好模型

--output：指定输出文件夹，用于保存网络训练过程中产生的模型，日志等文件

--description：指定实验配置，主要是用来区分每次实验，程序会在--output指定的文件夹下创建每个实验的子文件夹

#### 实验操作

目前完整的数据只在.3和.98服务器上有备份，如果在这两台服务器上实验，在配置好上述参数之后直接运行train.py即可；如果在其他服务器上可能需要先把把数据拷贝过去

#### 验证和可视化

如果需要验证模型在指定数据集上的指标，可以运行test.py文件，参数设置和train.py类似

如果需要将模型预测结果可视化，可以运行detect.py文件。需要注意的是，可视化程序的数据读取是按照文件夹进行读取的，所以在运行前可能需要先将希望可视化的图片存放到一个文件夹下再修改 --images参数

# modified