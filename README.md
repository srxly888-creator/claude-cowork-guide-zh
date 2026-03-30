# Claude Cowork 中文完全指南

> **从入门到精通** | 整合官方文档 + 社区最佳实践
> **版本**: 1.0.0 | **更新**: 2026-03-30

---

<p align="center">
  <strong>🔥 Claude 桌面应用完全指南 🔥</strong>
</p>

<p align="center">
  <a href="https://github.com/anthropics/knowledge-work-plugins"><img src="https://img.shields.io/badge/官方插件-11+-blue" alt="官方插件"/></a>
  <a href="#工作流"><img src="https://img.shields.io/badge/工作流-43+-green" alt="工作流"/></a>
  <a href="#prompts-库"><img src="https://img.shields.io/badge/Prompts-70+-purple" alt="Prompts"/></a>
</p>

---

## 📚 这是什么？

**Claude Cowork** 是 Anthropic 推出的桌面 AI 助手，内置三大功能：
- **Chat** - 智能对话
- **Coworker** - 自主执行任务（读取/写入文件、自动化工作流）
- **Code** - 代码助手

**本指南整合了：**
1. 🔥 [FlorianBruniaux/claude-cowork-guide](https://github.com/FlorianBruniaux/claude-cowork-guide) - 43 工作流 + 70 Prompts
2. 🔥 [JJenglert1/getting-started-with-claude-cowork](https://github.com/JJenglert1/getting-started-with-claude-cowork) - 10 个入门技巧
3. 🔥 [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins) - 11 个官方插件

---

## ⚡ 快速开始

### 1. 启用 Cowork
设置 → 功能 → 启用 Cowork → 授予文件夹访问权限

### 2. 第一个工作流
```bash
mkdir -p ~/Cowork-Workspace/{input,output}
# 将文件放入 input/，然后：
```
> "将 ~/Cowork-Workspace/input/ 中的文件按类型整理"

### 3. 进阶学习
- 📋 [速查表](reference/cheatsheet.md) - 打印备用
- 📖 [完整指南](guide/01-getting-started.md) - 10 分钟

<details>
<summary><strong>前提条件</strong></summary>

- **订阅**: Pro ($20/月) 或 Max ($100-200/月)
- **平台**: macOS 和 Windows
- **应用**: Claude Desktop（最新版本）

</details>

---

## 📋 目录

### 入门指南
| 文档 | 内容 | 时间 |
|------|------|------|
| [概述](guide/00-overview.md) | Cowork 能做什么 | 5 分钟 |
| [入门](guide/01-getting-started.md) | 安装 + 第一个工作流 | 10 分钟 |
| [能力](guide/02-capabilities.md) | 什么能用 / 什么不能 | 8 分钟 |
| [安全](guide/03-security.md) | 最佳实践 | 12 分钟 |
| [故障排除](guide/04-troubleshooting.md) | 常见问题 | 8 分钟 |

### 核心概念
- [什么是 Cowork](guide/00-overview.md#什么是-cowork)
- [全局指令](guide/01-getting-started.md#全局指令)
- [计划模式](guide/01-getting-started.md#计划模式)
- [文件夹作用域](guide/01-getting-started.md#文件夹作用域)

### 插件系统
| 插件 | 用途 | 连接器 |
|------|------|--------|
| **Productivity** | 任务管理 + 日常更新 | Slack, Notion, Asana, Linear, Jira |
| **Sales** | 客户研究 + 销售准备 | HubSpot, Close, Clay, ZoomInfo |
| **Marketing** | 内容创作 + 品牌声调 | Canva, Figma, HubSpot, Ahrefs |
| **Finance** | 财务报表 + 审计 | Snowflake, Databricks, BigQuery |
| **Data** | SQL + 数据分析 | Snowflake, BigQuery, Hex, Amplitude |
| **Legal** | 合同审查 + 合规 | Box, Egnyte, Jira, Microsoft 365 |
| **Customer Support** | 工单 + 知识库 | Intercom, HubSpot, Guru, Jira |
| **Product Management** | 需求 + 路线图 | Linear, Asana, Figma, Amplitude |
| **Enterprise Search** | 企业搜索 | Slack, Notion, Guru, Jira |
| **Bio Research** | 生物医药研究 | PubMed, BioRender, ChEMBL |
| **Plugin Management** | 创建/定制插件 | — |

### 工作流（43+）
- [管理类](workflows/administrative.md) - 发票、报价、付款提醒
- [销售营销类](workflows/sales-marketing.md) - 客户研究、竞争分析
- [运营类](workflows/operations.md) - 项目规划、库存跟踪
- [沟通类](workflows/communication.md) - 社交媒体、邮件模板
- [组织类](workflows/organization.md) - 文件整理、费用追踪

### Prompts 库（70+）
| 集合 | 数量 | 示例 |
|------|------|------|
| [文件操作](prompts/file-ops.md) | 20 | 整理、重命名、去重 |
| [文档创建](prompts/document-creation.md) | 15 | 报告、摘要、Excel |
| [数据提取](prompts/data-extraction.md) | 15 | PDF、OCR、图片 |
| [研究分析](prompts/research.md) | 17 | 网页搜索、信息综合 |

---

## 🔑 黄金法则

1. **始终审查计划** - Cowork 提议，你决定
2. **专用文件夹** - 永远不要授予 Documents/Desktop 访问权限
3. **不要存储凭证** - 密码和 API Key 放在别处
4. **验证来源** - 下载的文件可能包含恶意提示
5. **断开 VPN** - 问题 #1，会破坏虚拟机网络
6. **删除前备份** - 没有撤销功能

---

## 📁 推荐文件夹结构

```
~/Cowork-Workspace/
├── 00_Context/           # 持久化上下文文件
│   ├── about-me.md
│   ├── brand-voice.md
│   └── working-preferences.md
├── projects/             # 活跃项目
│   ├── client-a/
│   └── client-b/
└── outputs/              # Claude 输出目录
```

---

## 🚀 病毒式 X 起始 Prompt

**一键设置完整工作区**（复制粘贴）：

```text
你将帮助我设置 Claude Cowork 工作区，让每个会话都从完整上下文开始。
我们将构建一个"大脑"，让你从第一条消息就有用。

工作方式：你将分阶段采访我。问我问题，然后根据我的回答构建文件。
不要着急。不要假设。构建前先问。

阶段 0：插件和连接
推荐安装 Productivity 插件（任务管理+日常更新）和 Memory 插件。
询问我每天使用哪些工具，帮我连接：Slack、Gmail、Google Calendar、Notion。
连接的工具越多，系统越有用。

阶段 1：关于我
采访我创建 about-me.md 文件。询问我的工作、背景、内容频道、
专业价值观和定位。创建文件，展示给我，获得批准后继续。

阶段 2：品牌声调
分析我已创建的内容。如果没有，采访我关于我想如何发声、
我使用的短语、我永远不会使用的短语、我欣赏的创作者语调、
以及我的语调如何随上下文变化。创建 brand-voice.md 文件。

阶段 3：工作偏好
采访我关于我希望你每天帮助什么、我希望你如何沟通、
我最大的工作流程痛点、输出格式偏好和安全规则。
创建 working-preferences.md 文件。

阶段 4：内容策略（如适用）
如果我创建内容，采访我关于平台、目标受众、主题、
发布频率和内容格式。为每个平台，询问我是否有现有技能文件。
如果没有，提供创建。创建 content-strategy.md 文件。

阶段 5：团队和联系人（如适用）
如果我与团队合作，询问关键人员、角色和沟通偏好。
检查连接工具中的团队数据。创建 team-members.md 文件。

阶段 6：活跃项目
采访我关于当前项目、目标、里程碑和截止日期。
在 Current Projects 文件夹中创建单独的项目文件。

阶段 7：记忆系统
用我们构建的所有内容的热缓存更新 CLAUDE.md。
创建 memory/ 目录，包含人员、项目和上下文的子文件夹。
添加 glossary.md 用于首字母缩写和内部术语。

阶段 8：技能文件
审查所有内容。对于任何需要特定重复输出的领域，
提供创建专用技能文件，包含格式、声调规则、示例和质量检查清单。

规则：一次采访我一个阶段。保存前展示每个文件。
如果不确定，就问。在要求我重复之前，使用我现有的文件和连接的工具。
保持文件简洁。文件名：小写、连字符、.md 格式。
将所有内容保存到我的工作区文件夹。

从阶段 0 开始。
```

---

## 📊 学习路径

### 初学者（第一周）
1. [概述](guide/00-overview.md) - Cowork 能做什么
2. [入门](guide/01-getting-started.md) - 安装和第一个工作流
3. [文件整理](workflows/organization.md) - 实践示例
4. [Prompts 库](prompts/file-ops.md) - 20 个现成 Prompts
5. [速查表](reference/cheatsheet.md) - 打印备用

### 决策者（概览）
1. [内容](#📋-目录) - 能力和资源
2. [黄金法则](#🔑-黄金法则) - 核心原则
3. [安全](guide/03-security.md) - 最佳实践

### 高级用户（深入）
1. [完整能力](guide/02-capabilities.md) - 功能矩阵
2. [所有工作流](workflows/) - 43 个分步指南
3. [故障排除](guide/04-troubleshooting.md) - 问题解决
4. [高级 Prompts](prompts/research.md) - 研究和综合

---

## 🛡️ 安全须知

| 隐私设置 | 数据保留 | 模型训练 |
|----------|----------|----------|
| 默认 | 5 年 | 是 |
| 退出 | 30 天 | 否 |
| 企业 | 0 | 否 |

**操作**: [禁用训练](https://claude.ai/settings/data-privacy-controls)

---

## 🔗 资源链接

### 官方资源
- **Claude 下载**: https://claude.ai/download
- **官方插件市场**: https://claude.com/plugins
- **Anthropic 文档**: https://docs.anthropic.com
- **Anthropic Academy**: https://anthropic.skilljar.com/

### 源仓库
- [FlorianBruniaux/claude-cowork-guide](https://github.com/FlorianBruniaux/claude-cowork-guide)
- [JJenglert1/getting-started-with-claude-cowork](https://github.com/JJenglert1/getting-started-with-claude-cowork)
- [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins)

---

## 📄 许可证

本仓库整合了以下开源项目：
- claude-cowork-guide: CC BY-SA 4.0
- knowledge-work-plugins: MIT License

---

**版本** 1.0.0 | 2026-03-30 | 中文翻译版
