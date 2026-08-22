---
title: Keep It in Mind：以用户为中心的持续空间智能推理
published: 2026-07-13
description: 'Keep It in Mind: User-Centric Continual Spatial Intelligence Reasoning in Egocentric Video Streams (ICML 2026)'
image: '/assets/images/papers/keep-it-in-mind-framework.png'
tags: [空间智能, 自我中心视频, ICML, 多模态大语言模型, 视野感知]
category: '论文'
draft: false
lang: ''
---

## 论文信息

- **标题**：Keep It in Mind: User-Centric Continual Spatial Intelligence Reasoning in Egocentric Video Streams
- **发表**：ICML 2026（第 43 届国际机器学习大会，首尔），PMLR 306
- **作者**：Yun Wang, Junbin Xiao, Han Lyu, **Yifan Wang**, Jing Zuo, Zhanjie Zhang, Hong Huang, Dapeng Wu, Angela Yao
- **单位**：City University of Hong Kong, USTC, NUS, CUHK Shenzhen, **电子科技大学**, BUPT, Zhejiang University

## 摘要

![UCS-Bench 四类持续空间认知任务与双时间戳问答示例（Figure 2）](/assets/images/papers/keep-it-in-mind-framework.png)

人类在穿行走廊、转进房间、走出建筑物时，能持续追踪自己当前的位置以及已离开的环境相对于身体的方位——这种能力被称为**以用户为中心的持续空间智能**（User-Centric Continual Spatial Intelligence）。

本文提出了 **UCS-Bench**，一个包含 **170+ 小时第一视角视觉观测**与 **8100+ 带时间戳问题**的数据集，专门用于诊断第一人称视频流中的持续空间智能。目标问题强调三个核心能力：

- **动态空间推理**：不仅基于当前视野，更融合记忆中曾经见过的空间关系
- **长期记忆**：跨场景、跨时间地维护空间参照系
- **用户中心对齐**：回答须结合用户当前的实时位置与朝向

同时提出 **DirectMe** 框架，通过增量构建并维护结构化的空间记忆，实现相对于用户运动的物体位置追踪与回忆。实验表明 DirectMe 显著提升了主流多模态大语言模型的空间推理能力，并超越了多个空间感知与长序列视频模型。

## 资源

- [代码与数据：UCS-Bench](https://github.com/cocowy1/UCS-Bench)
