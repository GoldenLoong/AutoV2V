本软件的主要功能是节约算例，适用范围为用stable diffusion转绘视频。大家可以理解为独立版的V2V。


你先拿到一个视频，然后把视频放入 video 文件夹，改名为 1.MP4 。

接着运行 1-start.py ，这是整合了以下这些功能（你可以跳过1和2）：

    1.拆分视频为帧；
    
    2.转换帧为蒙版；
    
    3.裁切蒙版（可选不同尺寸），并生成 坐标文件；
    
    4.利用坐标文件裁切帧；
    
    5.抽取关键帧，默认为每2张抽取1张。
    

再就是打标、图生图，请自行处理，并将生成图放进文件夹 3Datu\ready。

最后是运行下列功能：

    1.根据图生图重置小蒙版；
    
    2.把蒙版塞进大蒙版，重置大蒙版；
    
    3.依据坐标文件和大蒙版，把图生图塞进原图或背景（可选）

    
好，我要说的基本说完，你要想用，请先看使用说明，这里简要说一下配置：

    1.python3.11（官方下载地址：https://www.python.org/downloads/），需要环境变量（最简单的方法：安装最开始时，勾选“Add python.exe to PATH”）
    
    2.安装以下 python 组件：
    
```
      pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
      pip install opencv-python
      pip install tqdm
      pip install pillow
      pip install torch
      pip install numpy
      pip install torchvision
      pip install multiprocessing
```
    3.安装CUDA12.1（官方下载地址：https://developer.nvidia.com/cuda-12-1-1-download-archive）

    4.安装pytorch-nightly：
```
        pip3 install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu121
```

    5.安装ffmpeg（官方下载地址：https://github.com/BtbN/FFmpeg-Builds/releases），并配置环境变量。（随便给一个教程：https://www.bilibili.com/video/BV1xf4y1Z7pV）
    
就这样吧，最后，下载这些有困难的可以用我的网盘（https://www.123pan.com/s/Ev5eVv-G4z63.html 访问密码：8888），在文件夹（
AutoV2V>这个软件必备的东西），无需客户端。
    
