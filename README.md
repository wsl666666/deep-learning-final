# 深度学习期末项目——nerf重建

这个项目实现了用于3D场景表示和渲染的神经辐射场（NeRF）。

## 环境配置

确保你已安装以下依赖项：
torch
torchvision>=0.9.1
imageio
imageio-ffmpeg
matplotlib
configargparse
tensorboard>=2.0
tqdm
opencv-python

你可以使用以下命令安装所需的包：

pip install -r requirements.txt

数据准备
room 数据

官网下载


https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1


在压缩文件里面找到room数据集保存在相应的路径下：C:\COLMAP\nerf-pytorch\data\nerf_llff_data\room





————————————————

                          
模型运行：

要运行模型，请使用以下命令：


python run_nerf.py --config configs/room.txt
这将使用 room数据配置启动训练过程。训练日志和检查点将保存在 logs 目录中。



TensorBoard 可视化
要使用 TensorBoard 可视化训练过程，请运行：


tensorboard --logdir=C:\COLMAP\nerf-pytorch\logs\summaries\room_test --port 7001
这将在端口 7001 上启动一个 TensorBoard 服务器，你可以在其中查看训练和测试指标。
