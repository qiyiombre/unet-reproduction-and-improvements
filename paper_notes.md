# U-Net 论文阅读笔记

## 1. 论文基本信息

- 论文名称：U-Net: Convolutional Networks for Biomedical Image Segmentation
- 作者：Olaf Ronneberger, Philipp Fischer, Thomas Brox
- 发表会议：MICCAI 2015
- 任务：生物医学图像分割
- 核心思想：编码器提取上下文信息，解码器恢复空间定位信息，并通过跳跃连接融合浅层细节与深层语义。

## 2. 要重点阅读的问题

1. U-Net 的输入输出是什么？
2. 编码器和解码器每一层的尺寸如何变化？
3. skip connection 为什么重要？
4. 原论文使用了什么数据增强？
5. 原论文使用了什么损失函数？
6. 原论文使用了什么评价指标？
7. 原始 Caffe 实现和 PyTorch 复现可能有哪些差异？

## 3. 今日初步结论

今天先完成资料归档和问题列表。明天开始逐段阅读论文，重点整理网络结构图、训练策略和实验设置。