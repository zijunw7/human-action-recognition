# YOLOv5 + SlowFast：实时行为检测

### 一个基于PyTorchVideo 的实时行为检测框架。  

#### 以下是我们所做的部分改进细节：

- 选用 YOLOv5 作为目标检测器，替代了 Faster R-CNN，速度更快、使用更便捷；
- 引入 DeepSORT 跟踪器，为不同帧中具有相同 ID 的目标分配一致的行为标签 
- 在单张 RTX 2080Ti GPU 上，推理批大小为 30 时，处理速度可达 24.2 FPS

#### 左侧为原始方法，右侧为本项目效果：

![图片1](C:\Users\15201\Documents\GitHub\human-action-recognition\demo\图片1.gif)!1763019153956](C:\Users\15201\AppData\Local\Temp\1763019153956.png)<![yolov5+slowfast](C:\Users\15201\Documents\GitHub\human-action-recognition\demo\yolov5+slowfast.gif)mg src="./demo/yolov5+slowfast.gif" width="400" />

#### Update Log:

- 2022.12.24  优化预处理流程（无需提前将视频拆帧为图像），运行更快速、代码更简洁 

## Installation

1. 克隆本仓库： 

   ```
   git clone https://github.com/zijunw7/human-action-recognitiontb/yolo_slowfast
   cd yolo_slowfast
   ```

2. （可选）创建新的 Python 环境： 

   ```
   conda create -n {your_env_name} python=3.7.11
   conda activate {your_env_name}
   ```

3. 安装依赖 

   ```
   pip install -r requirements.txt
   ```

4. 下载 DeepSORT 权重文件（ckpt.t7）

   ```
   ./deep_sort/deep_sort/deep/checkpoint/
   ```

5. 在你的视频上测试

   ```
   python yolo_slowfast.py --input {你的视频路径}
   ```


### Stargazers over time

[![Stargazers over time](https://starchart.cc/wufan-tb/yolo_slowfast.svg)](https://starchart.cc/wufan-tb/yolo_slowfast)


