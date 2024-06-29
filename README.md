# 深度学习期末项目——nerf重建

这个项目实现了用于3D场景表示和渲染的神经辐射场（NeRF）。

## 先决条件

确保你已安装以下依赖项：
- Python 3.7+
- PyTorch
- imageio
- tqdm
- matplotlib
- tensorboard
- numpy

你可以使用以下命令安装所需的包：
```bash
pip install -r requirements.txt

数据准备
COLMAP 数据
准备你的 COLMAP 数据如下：

确保你的 COLMAP 目录设置正确，例如：
plaintext
复制代码
C:/COLMAP/exp
确保你的 NeRF 数据目录设置正确，例如：
plaintext
复制代码
C:/COLMAP/test/data
将你的数据集放在项目中的 data 目录内。
Blender 数据
如果你使用 Blender 数据，下载并解压数据集到 data 目录中。

训练模型
要训练模型，请使用以下命令：

bash
复制代码
python run_nerf.py --config configs/config_colmap.txt
这将使用 COLMAP 数据配置启动训练过程。训练日志和检查点将保存在 logs 目录中。

测试模型
要测试模型，请使用以下命令：

bash
复制代码
python run_nerf.py --config configs/config_colmap.txt --render_test
这将使用训练好的模型渲染测试集，并将结果保存在 logs 目录中。

TensorBoard 可视化
要使用 TensorBoard 可视化训练过程，请运行：

bash
复制代码
tensorboard --logdir=C:\COLMAP\nerf-pytorch\logs\summaries\room_test --port 7001
这将在端口 7001 上启动一个 TensorBoard 服务器，你可以在其中查看训练和测试指标。
