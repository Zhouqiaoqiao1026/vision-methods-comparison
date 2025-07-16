# 传统计算机视觉与深度学习目标识别方法比较

## 项目简介
本项目对比了两种主流图像识别方法在机器人视觉场景下的表现：

- **传统方法**：使用 SIFT 特征、Harris 角点检测、Bag-of-Words 编码、SVM 分类器；
- **深度学习方法**：使用自定义构建的轻量级卷积神经网络（CNN），结合数据增强与超参数调优。

使用的两个公开数据集：
- CIFAR-10
- iCubWorld28（更贴近机器人视觉应用）

## 实验结果概览

| 方法 | 数据集 | 准确率 |
|------|--------|--------|
| SIFT+BoW+SVM | CIFAR-10 | 46.4% |
| CNN | CIFAR-10 | 85.1% |
| SIFT+BoW+SVM | iCubWorld28 | 61.4% |
| CNN | iCubWorld28 | 96.9% |

> CNN 显著优于传统方法，尤其在复杂环境中展现更强的泛化能力。
> - 支持传统方法中的多个关键点检测器（Harris、SIFT、ORB、FAST）对比；
- CNN 模型支持数据增强、EarlyStopping 和 ReduceLROnPlateau 策略；
- 支持 GridSearchCV 搜索 SVM 参数；
- 自动生成分类报告与混淆矩阵可视化。
