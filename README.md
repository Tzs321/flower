<<<<<<< HEAD
# flower
基于花朵分类的一个模型
=======
# 花卉图像分类系统（基于 ResNet34 迁移学习）

> 使用 PyTorch 实现的花卉种类识别模型，在 Oxford 102 Flowers 数据集上达到 **91.6% 验证准确率**。

## 目录结构
.
├── model.py               # ResNet34 模型定义
├── train.py               # 训练脚本
├── predict.py             # 预测脚本
├── resNet34.pth           # 训练好的模型权重（83MB）
├── class_indices.json     # 类别索引映射
├── results.jpg            # 训练损失与准确率曲线
└── prediction_result1.jpg # 预测结果示例1
└── prediction_result2.jpg # 预测结果示例2
└── prediction_result3.jpg # 预测结果示例3

## 项目亮点

- 基于 **ResNet34 预训练模型**，利用迁移学习提升小样本分类性能
- 完整训练流程：数据加载 → 模型微调 → 验证 → 保存最佳权重
- 支持单张图片预测，可识别 5 类常见花卉：
  - Daisy（雏菊）
  - Dandelion（蒲公英）
  - Roses（玫瑰）
  - Sunflowers（向日葵）
  - Tulips（郁金香）
- 提供训练曲线与预测结果可视化

## 环境依赖

```bash
pip install -r requirements.txt

## 使用方法
1.Anaconda PowerShell Prompt 训练模型：python train.py
2.预测单张图片：python predict.py --img-path your_flower.jpg #your_flower.jpg改成自己图片的路径

