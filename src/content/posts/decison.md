---
title: DECIS：基于双证据校正验证的可解释斜视诊断决策
published: 2026-07-20
description: 'DECIS: Dual-Evidence Corrective Verification for Interpretable Strabismus Diagnostic Decision-Making'
image: '/assets/images/papers/decis-framework.png'
tags: [DECIS, 斜视诊断, 可解释AI, 多智能体, 因果推理, 眼科AI]
category: '论文'
draft: false
lang: ''
---

## 论文信息

- **标题**：DECIS: Dual-Evidence Corrective Verification for Interpretable Strabismus Diagnostic Decision-Making
- **发表**：arXiv:2606.09249 (2026.07.20)
- **作者**：Xikai Tang, **Yifan Wang**, Jiafan Zhuang, Li Luo, Jinming Guo, Xiaoling Xie, Jiacheng Liu, Peiwei Wei, Lihao Zhong, Xiaoli Kang, Jie Cen, Guangqiang Yin, Kunliang Qiu, Ce Zheng, Zhun Fan
- **单位**：电子科技大学（深圳）高等研究院 等

## 摘要

![DECIS 双证据校正验证框架](/assets/images/papers/decis-framework.png)

DECIS 提出了一种面向**斜视亚型诊断**的双证据校正验证框架。传统深度学习方法将诊断视为黑盒预测，缺乏可解释的推理过程；近来出现的大视觉-语言模型虽然能同时理解图像并生成报告，但在此类证据敏感且依赖规则的医学场景中极易产生幻觉。

DECIS 将端到端生成转化为结构化的诊断流程：**候选假设生成 → 双证据约束上下文 → 证据驱动的校正验证 → 报告生成**。具体而言：

- **DECC（Dual-Evidence Constrained Context）**：联合组织来自九个注视方位照片的视觉证据与循证临床诊断规则，构建约束上下文，使推理有据可依。
- **EBCV（Evidence-Based Corrective Verification）**：验证当前诊断假设是否被视觉证据、热力图线索及循证临床规则支持；检测到不一致时触发假设修正，确保输出与证据一致。

在细粒度斜视诊断基准上，DECIS 将加权 F1 从 **72.0% 提升至 91.3%**，同时显著改善了生成报告的临床可靠性（一致性、对齐度与完整性）。结果表明 DECIS 为构建准确、循证、临床可解释的斜视诊断系统提供了有效解决方案。

## 资源

- [论文：arXiv:2606.09249](https://arxiv.org/abs/2606.09249)
