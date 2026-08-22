---
title: GazeMamba：面向斜视亚型分类的跨注视状态空间建模
published: 2026-08-22
description: 'GazeMamba: Inter-Gaze State-Space Modeling for Strabismus Subtype Classification'
image: '/assets/images/papers/gazemamba-framework.png'
tags: [GazeMamba, 斜视亚型分类, Mamba, 状态空间模型, 九眼位, 眼科AI]
category: '论文'
draft: false
lang: ''
---

## 论文信息

- **标题**：GazeMamba: Inter-Gaze State-Space Modeling for Strabismus Subtype Classification
- **作者**：**Yifan Wang**, Yankewei Xiao, Yuxiang Ma, Li Luo, Jinming Guo, Kunliang Qiu, Jiafan Zhuang, Ce Zheng, Zhun Fan
- **单位**：电子科技大学（深圳）高等研究院、兰州大学、汕头大学·香港中文大学联合汕头国际眼科中心、上海交通大学医学院附属新华医院、深圳环水区域研究院等
- **方向**：斜视亚型分类、九眼位序列建模、状态空间模型、医学图像处理

## 摘要

![GazeMamba 跨注视状态空间建模总体框架（Figure 2）](/assets/images/papers/gazemamba-framework.png)

九个诊断眼位包含不同眼外肌配置下的眼位信息，斜视亚型的关键证据不仅来自单个眼位的外观，也来自不同注视方向之间眼位偏斜的变化。传统静态图像分类通常将九眼位照片视为一张组合图像或一组独立观察，难以显式保留检查采集过程中的跨眼位依赖关系。

本文提出 **GazeMamba**，一种按照真实采集顺序建模九眼位状态转换的斜视亚型分类框架。模型首先通过共享视觉编码器将九个眼位裁剪图转换为语义特征，再按照临床采集轨迹 **5 → 2 → 3 → 6 → 9 → 8 → 7 → 4 → 1** 排列为序列，随后使用两个残差 Mamba 模块进行跨注视状态空间建模，最终由偏斜类型与 A/V 型模式两个诊断头共同完成分类。

研究建立了一个包含 **1,716 张九眼位照片、6 类斜视亚型**的临床标注基准，并在固定独立测试协议下比较静态、无序聚合、顺序感知及结构化建模方法。GazeMamba 达到 **67.25% 准确率和 63.88% 加权 F1**；相较使用相同眼位特征的无序均值池化，准确率和加权 F1 分别提高 **5.26** 和 **9.21** 个百分点。实验表明，显式建模眼位之间的方向性变化能够为细粒度斜视亚型识别提供更可靠的判别信息。

## 资源

- [论文 PDF](/assets/papers/GazeMamba.pdf)
