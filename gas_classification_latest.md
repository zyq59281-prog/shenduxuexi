# 气体分类识别（Electronic Nose / Gas Sensor）最新模型与数据整理（截至 2026-05-07）

> 说明：以下优先收录近两年（2024–2026）可验证来源（论文主页/期刊/预印本）中的模型，并附带可用数据集入口。

## 1) 最新模型（按时间倒序）

| 年份 | 模型/方法 | 任务 | 主要结果（论文报告） | 来源 |
|---|---|---|---|---|
| 2025/2026 | **SNM-Net**（Spherical Normalization + Mahalanobis Distance，可配Transformer） | 开集气体识别（open-set gas recognition） | 在 Vergara 数据上 AUROC 报告 0.9977，未知气体检测率 99.57%（TPR@5%FPR） | ArXiv: https://arxiv.org/abs/2512.22792 |
| 2025 | **TCN + Channel Attention**（Open-Set Gas Classification） | 开闭集统一识别 | 在 UCI 公共数据上优于基线方法（文中描述） | IEEE/索引页: https://colab.ws/articles/10.1109%2Fippr66507.2025.11198442 |
| 2025 | **PTQ-CNN**（Post-Training Quantization + CNN） | 气体分类 + 浓度回归 | 分类准确率 99.89%，并做轻量化压缩 | ScienceDirect: https://www.sciencedirect.com/science/article/pii/S0924424725001888 |
| 2025 | **ExAIRFC-GSDC**（可解释随机森林框架） | 泄漏检测与分类 | 面向 LPG/CNG/Methane/Propane 等场景的解释型分类 | Springer: https://link.springer.com/article/10.1007/s44196-025-00742-6 |
| 2024 | **AMDS-PFFA**（无监督注意力多源域适配） | 传感器漂移补偿下的气体识别 | 在 UCI 漂移数据与自建长期漂移数据验证 | ArXiv: https://arxiv.org/abs/2409.13167 |

---

## 2) 可用数据集（优先公开、可复现）

| 数据集 | 简介 | 适用任务 | 链接 |
|---|---|---|---|
| **UCI Gas Sensor Array Drift Dataset** | 16 个化学传感器，长期漂移、多批次采样 | 闭集分类、漂移补偿、域适配 | https://archive.ics.uci.edu/dataset/224/gas |
| **UCI Gas Sensor Array Drift Dataset at Different Concentrations** | 在 Drift 基础上增加浓度标签 | 分类 + 浓度估计、多任务学习 | https://archive.ics.uci.edu/dataset/270/gas%2Bsensor%2Barray%2Bdrift%2Bdataset%2Bat%2Bdifferent%2Bconcentrations |
| **SMELLNET (2025)** | 大规模真实世界气味识别数据（便携化学/气体传感器） | 多类别真实场景气味/气体模式识别 | https://arxiv.org/abs/2506.00239 |
| **MultimodalGasData** | 多模态气体检测与分类数据（Data Descriptor） | 多模态融合分类、鲁棒性研究 | https://www.mdpi.com/2306-5729/7/8/112 |

---

## 3) GitHub 落地建议（可直接执行）

1. 在仓库中新增 `gas_classification_latest.md`（本文件）。
2. 再新增一个 `resources/` 目录，按如下结构管理：
   - `resources/papers.csv`：模型名称、年份、任务、链接、是否开源代码
   - `resources/datasets.csv`：数据集名称、链接、许可、规模、标签类型
3. 若需要，我可以继续补一版“**只包含有公开代码仓库**”的清单（筛选出带 GitHub 实现的模型）。

---

## 4) 检索关键词（便于后续增量更新）

- `open-set gas recognition 2025`
- `electronic nose drift compensation arxiv 2024 2025`
- `gas sensor array classification benchmark dataset`
- `PTQ-CNN gas classification`

