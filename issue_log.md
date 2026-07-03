# 问题记录

## Issue 01：PyTorch 下载中断

### 现象

使用 pip 安装 PyTorch CUDA 版本时，多次出现 IncompleteRead 或 Connection broken。

### 原因分析

PyTorch CUDA 版本文件较大，网络不稳定时容易中断。

### 解决方法

改用 conda 安装 PyTorch 与 pytorch-cuda=12.4，最终验证 `torch.cuda.is_available()` 为 True。

---

## Issue 02：Pillow DLL 加载失败

### 现象

导入 matplotlib / PIL 时出现 `_imaging` DLL 加载失败。

### 解决方法

重新安装 Pillow 后解决。

---

## Issue 03：conda.bat / PyCharm Conda 自动识别异常

### 现象

PyCharm Conda 自动识别环境时出现 `CondaInfoJson.getEnvs()` 相关错误。

### 当前处理方式

直接将 PyCharm 解释器设置为：

`E:\study app\python\anaconda\envs\unet_repro\python.exe`

经测试，该解释器可正常导入 PyTorch、OpenCV、Albumentations，并可使用 GPU。

### 备注

该问题影响 PyCharm 的 Conda 自动识别和包管理器显示，不影响当前项目代码运行。