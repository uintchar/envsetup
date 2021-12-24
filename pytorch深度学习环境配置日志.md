- [1. Linux(Ubuntu)](#1-linuxubuntu)
  - [1.1. 安装 cuda](#11-安装-cuda)
  - [1.2. 安装 cudnn](#12-安装-cudnn)
  - [1.3. 安装 anaconda](#13-安装-anaconda)
- [2. Windows 10](#2-windows-10)
  - [2.1. 安装CUDA 10.2](#21-安装cuda-102)
  - [2.2. 安装 cudnn](#22-安装-cudnn)
  - [2.3. 安装 anaconda](#23-安装-anaconda)
- [3. nvidia-smi与nvcc](#3-nvidia-smi与nvcc)

# 1. Linux(Ubuntu)

## 1.1. 安装 cuda

## 1.2. 安装 cudnn

## 1.3. 安装 anaconda

# 2. Windows 10

## 2.1. 安装CUDA 10.2

首先需要查看本机显卡支持的 CUDA 版本，桌面右键-NVIDIA控制面板-帮助-系统信息-组件

![NVIDIA控制面板-帮助-系统信息-组件](./figures/NVIDIA控制面板-帮助-系统信息-组件.png)

可以看到最高支持到 CUDA 10.2，下面安装 CUDA 10.2，CUDA 的下载页面：https://developer.nvidia.com/cuda-toolkit-archive

![选择下载CUDA10.2](./figures/选择下载CUDA10.2_1.png)
![选择下载CUDA10.2_1](./figures/选择下载CUDA10.2_2.png)

下载 CUDA 10.2 完成后，按照安装指示一路安装，可以自定义安装路径。安装完成后，可能需要配置相关的系统环境变量。可以通过在 Windows PowerShell 中验证是否安装成功，输入 `nvcc -V` 查看是否正常输出，或者运行其给的示例程序 `D:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.2\extras\demo_suite\bandwidthTest.exe` 查看是否正常运行

![nvcc-V](figures/nvcc-V.png)
![bandwidthTest](figures/bandwidthTest.png)


## 2.2. 安装 cudnn

## 2.3. 安装 anaconda

# 3. nvidia-smi与nvcc