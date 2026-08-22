---
title: EviCausal：面向跨域斜视诊断的证据增强多智能体因果学习
published: 2026-08-22
description: 'EviCausal: Evidence-enhanced Multi-Agent Causal Structure Learning for Domain-Generalizable Strabismus Diagnosis'
image: '/assets/images/papers/evicausal-framework.png'
tags: [EviCausal, 斜视诊断, 因果学习, 多智能体, 域泛化, 眼科AI]
category: '论文'
draft: false
lang: ''
---

## 论文信息

- **标题**：EviCausal: Evidence-enhanced Multi-Agent Causal Structure Learning for Domain-Generalizable Strabismus Diagnosis
- **状态**：匿名评审稿
- **方向**：跨域斜视诊断、循证变量发现、因果结构学习、多智能体协作

## 摘要

![EviCausal 证据增强多智能体因果学习框架](/assets/images/papers/evicausal-framework.png)

真实场景中的斜视筛查照片会受到设备、光照、背景、头位和图像质量等因素影响，导致模型在受控临床数据上训练后，部署到新环境时出现明显性能下降。现有因果方法通常依赖人工预定义变量与纯数据驱动的结构学习，其临床有效性和跨域可靠性仍然有限。

本文提出 **EviCausal**，一个面向域泛化斜视诊断的证据增强多智能体因果结构学习框架。框架由研究智能体、代码智能体和因果智能体协作完成，并包含两个核心机制：

- **ERVD（Evidence-Based Reasoning and Variable Discovery）**：从指南、论文与专家共识等医学证据中识别具有临床意义的概念，将其转化为可计算变量并实现为可执行代码。该机制发现了 16 个此前未被公式化的诊断变量，且均经眼科医生评估为具有临床合理性。
- **ECDR（Evidence-Based Causal Discovery and Refinement）**：学习源域数据中的初始因果结构，再结合变量语义、公式依赖、计算来源与关系级临床证据，对因果关系进行审计和修正，得到可追溯的证据增强因果图。

研究建立了由受控临床源域与独立真实世界目标域构成的跨域斜视诊断基准。在开发阶段完全不访问目标域的条件下，EviCausal 取得 **84.0% AUC、85.4% 准确率和 70.6% F1**，相较此前最佳结果分别提升 **12.4 个百分点 AUC** 和 **20.2 个百分点 F1**。

> 该版本为匿名评审稿，依照论文声明暂不公开传播原始手稿及作者信息；网页仅展示研究简介与框架概览。
