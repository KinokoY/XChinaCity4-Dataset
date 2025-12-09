# XChinaCity4 Dataset

<!-- 徽章区域 -->
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Dataset Status](https://img.shields.io/badge/Dataset-Sample%20Only-yellow)](https://github.com/yourusername/reponame)

<!-- 导航栏：使用 GitHub 原生锚点 -->
[English](#-overview) | [中文](#-项目概览)

---

## 🌟 Overview

**XChinaCity4** is a comprehensive multimodal benchmark dataset tailored for **Social Media Popularity Prediction (SMPP)**. Unlike existing datasets (e.g., SMPD, TPIC) that rely on static, isolated posts, XChinaCity4 focuses on contemporary social media content with rich streaming media and inter-post relationships.

The dataset comprises **10,872 posts** collected from the official X (formerly Twitter) accounts of four major Chinese cities—**Beijing, Shanghai, Hangzhou, and Shenzhen**—spanning from January 1, 2023, to June 1, 2025. It encompasses text, images, videos, and metadata, providing a solid foundation for researching content recommendation, information dissemination, and city branding.

### 🏙️ Data Sources
Data was collected via X's advanced search from the following official verified accounts:
- **@VisitBeijingcn** (Beijing)
- **@Meetinshanghai** (Shanghai)
- **@Hangzhoufeel** (Hangzhou)
- **@szdaily1** (Shenzhen)

## 📥 Data Access & Download

> ⚠️ **Note:** Currently, this repository hosts **sample data** for preview purposes. 
>
> The **full dataset** (including all JSON metadata and the complete archive of media files) will be released publicly upon the acceptance of our associated research paper.

### Sample Media Download
For the provided sample entries, you can download the associated media files (images/videos) here:

- **Google Drive**: [Upload later]
- **Baidu Netdisk**: [https://pan.baidu.com/s/1HxvKhHkv7H38Wf8gMVSWFg] (Password: `0721`)

*The folder structure in the cloud storage mirrors the `post ID` found in `media_data.json`.*

## 🛠️ Data Construction

### Pre-processing
To ensure high quality for SMPP tasks, the raw data (15,847 posts) underwent a rigorous cleaning procedure:
1. **Privacy & Artifact Removal**: URLs and third-party user mentions were removed.
2. **Quality Filtering**: Reply tweets, retweets, and posts that were **shorter than 10 words** or contained **no media attachments** were filtered out.
3. **Normalization**: Emojis were removed to mitigate encoding inconsistencies.
4. **Retention**: The final dataset represents approximately **71%** of the initially collected data.

### Popularity Definition
Following established SMPP research methods, we define post popularity based on engagement metrics (views, likes, retweets, comments) accumulated two weeks after publication. 

The raw metrics are aggregated and log-transformed to a discrete scale ranging from **1 to 15** to mitigate skewness and ensure compatibility with existing datasets.

## 📊 Descriptive Statistics

Summary of the processed XChinaCity4 dataset:

| Field | VisitBeijingcn | Meetinshanghai | Hangzhoufeel | Szdaily1 |
| :--- | :---: | :---: | :---: | :---: |
| **Number of Posts** | 1,445 | 2,882 | 4,424 | 2,121 |
| **Number of Images** | 3,400 | 6,618 | 10,072 | 3,622 |
| **Number of Videos** | 365 | 684 | 904 | 439 |
| **Avg. Tweet Length (Words)** | 35.6 | 44.1 | 47.2 | 80.9 |
| **Avg. Tweet Length (Tokens)** | 56.7 | 84.5 | 79.8 | 124.3 |
| **Avg. Views** | 49,867.1 | 6,104.9 | 15,963.8 | 619.9 |
| **Avg. Likes** | 247.8 | 25.7 | 100.7 | 7.4 |
| **Avg. Replies** | 3.3 | 0.2 | 1.1 | 0.4 |
| **Avg. Retweets** | 16.5 | 1.8 | 9.9 | 1.2 |

## 📝 Citation

If you find this dataset useful, please consider citing our work. 
*(Note: Full citation details will be updated upon publication.)*

```bibtex
@article{SmpGraphRAG_2025,
  title={SmpGraphRAG: Improving Knowledge Graph Retrieval-Augmented Generation for Multimodal Social Media Popularity Prediction},
  author={Wang, Zitong and Peng, Yan and Liu, Chun and Wang, Jie},
  journal={Under Review},
  year={2025},
  note={Dataset available at: https://github.com/KinokoY/XChinaCity4-Dataset}
}
```

---

## 🌟 项目概览

**XChinaCity4** 是一个专为**社交媒体流行度预测 (SMPP)** 任务定制的综合多模态基准数据集。与现有的依赖静态、孤立帖子的数据集（如 SMPD, TPIC）不同，XChinaCity4 聚焦于包含丰富流媒体信息和帖子间潜在关联的现代社交媒体内容。

该数据集包含 **10,872 条推文**，采集自北京、上海、杭州、深圳四个中国主要城市的官方 X（原 Twitter）账号，时间跨度为 2023年1月1日至2025年6月1日。数据涵盖了文本、图像、视频及元数据，为内容推荐、信息传播分析及城市品牌研究提供了坚实的数据基础。

### 🏙️ 数据来源
数据通过 X 平台的高级搜索功能采集自以下官方认证账号：
- **@VisitBeijingcn** (北京)
- **@Meetinshanghai** (上海)
- **@Hangzhoufeel** (杭州)
- **@szdaily1** (深圳)

## 📥 数据获取与下载

> ⚠️ **注意：** 本仓库目前仅托管**示例数据 (Sample Data)** 以供预览。
>
> **完整数据集**（包含所有清洗后的 JSON 元数据及完整的媒体文件归档）将在我们的相关研究论文被正式录用后公开。

### 示例媒体文件下载
对于仓库中提供的示例数据，您可以从以下链接下载对应的媒体文件（图片/视频）：

- **Google Drive**: [Upload later]
- **百度网盘**: [https://pan.baidu.com/s/1HxvKhHkv7H38Wf8gMVSWFg] (提取码: `0721`)

*云存储中的文件夹结构与 `media_data.json` 中的 `post ID` 一一对应。*

## 🛠️ 数据构建

### 数据预处理
为了确保 SMPP 任务的数据质量，我们对原始采集的 15,847 条推文进行了严格的多步骤清洗：
1. **隐私与噪声去除**：移除了文本中的 URL 和第三方用户提及（Mentions）。
2. **质量过滤**：过滤掉了回复贴、转推贴，以及**单词数少于10个**或**不包含任何媒体附件**的帖子。
3. **标准化**：移除了 Emoji 表情符号以减少编码不一致的影响。
4. **数据留存**：最终数据集保留了约 **71%** 的原始数据。

### 流行度定义
遵循 SMPP 领域的研究惯例，我们将帖子的流行度定义为发布两周后积累的互动指标（浏览量、点赞数、转推数、评论数）的聚合。

为了缓解长尾分布导致的偏斜并确保与现有数据集的兼容性，我们对原始指标进行了对数转换，并将其映射到 **1-15** 的离散区间内。

## 📊 描述性统计

XChinaCity4 数据集统计摘要如下：

| 字段 | VisitBeijingcn | Meetinshanghai | Hangzhoufeel | Szdaily1 |
| :--- | :---: | :---: | :---: | :---: |
| **帖子数量** | 1,445 | 2,882 | 4,424 | 2,121 |
| **图片数量** | 3,400 | 6,618 | 10,072 | 3,622 |
| **视频数量** | 365 | 684 | 904 | 439 |
| **平均推文长度 (单词)** | 35.6 | 44.1 | 47.2 | 80.9 |
| **平均推文长度 (Tokens)** | 56.7 | 84.5 | 79.8 | 124.3 |
| **平均浏览量** | 49,867.1 | 6,104.9 | 15,963.8 | 619.9 |
| **平均点赞数** | 247.8 | 25.7 | 100.7 | 7.4 |
| **平均回复数** | 3.3 | 0.2 | 1.1 | 0.4 |
| **平均转发数** | 16.5 | 1.8 | 9.9 | 1.2 |

## 📝 引用

如果您觉得本数据集对您的研究有帮助，请考虑引用我们的工作。
*(注：完整引用信息将在论文发表后更新)*

```bibtex
@article{SmpGraphRAG_2025,
  title={SmpGraphRAG: Improving Knowledge Graph Retrieval-Augmented Generation for Multimodal Social Media Popularity Prediction},
  author={Wang, Zitong and Peng, Yan and Liu, Chun and Wang, Jie},
  journal={Under Review},
  year={2025},
  note={Dataset available at: https://github.com/KinokoY/XChinaCity4-Dataset}
}
```
