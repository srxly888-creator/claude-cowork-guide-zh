# Claude Cowork 插件指南

> **11 个官方插件 + 最佳实践**

---

## 插件概览

| 插件 | 功能 | 连接器 |
|------|------|--------|
| **Productivity** | 任务管理 + 日常更新 | Slack, Notion, Asana, Linear, Jira, Microsoft 365 |
| **Sales** | 客户研究 + 弼叫准备 | Slack, HubSpot, Close, Clay, ZoomInfo, Notion |
| **Marketing** | 内容创建 + 品牌声调 | Slack, Canva, Figma, HubSpot| Ahrefs |
| **finance** | 财务报表 + 对账 | Snowflake, Databricks | BigQuery | Slack |
| **legal** | 合同审查 + 合规 | Slack, Box, Egnyte | Jira, Microsoft 365 |
| **customer-support** | 工单处理 + 知识库 | Slack, Intercom, HubSpot | Guru | Jira |
| **product-management** | 需求 + 路线图 | Slack, Linear, Asana| Figma | Amplitude |
| **data** | SQL + 数据分析 | Snowflake, BigQuery | Hex | Amplitude | Jira |
| **enterprise-search** | 企业搜索 | Slack, Notion, Guru | Jira | Asana |
| **bio-research** | 生物医药研究 | PubMed, BioRender | ChEMBL |
| **design** | 设计审查 + 品牌一致性 | Slack, Figma | Canva | Ahrefs |

---

## 安装插件

### 方法 1: 从 Claude Desktop 安装
1. 打开 Claude Desktop
2. 点击左侧边栏的 **Customize**
3. 点击 **Browse Plugins**
4. 找到想要的插件
5. 点击 **Install**

### 方法 2: 从命令行安装（Claude Code)
```bash
# 添加市场
claude plugin marketplace add anthropics/knowledge-work-plugins

# 安装特定插件
claude plugin install sales@knowledge-work-plugins
```

---

## 最佳实践

### 1. 先安装 Productivity 插件
无论你的角色，，Productivity 插件都提供了
- 任务管理
- 每日更新
- 个人上下文管理

### 2. 根据角色选择插件
| 角色 | 推荐插件 |
|------|---------|
| 销售 | sales + marketing |
| 产品经理 | product-management + design |
| 财务 | finance + data |
| 客服 | customer-support |
| 工程师 | engineering |
| 设计 | design |
| 法务 | legal |

### 3. 自定义插件
安装 `cowork-plugin-management` 插件来创建自己的插件。

---

## 使用技巧
### 斜杠命令
安装插件后，输入 `/` 查看可用命令
```text
/sales:call-prep
/product-management:write-spec
/finance:reconciliation
```

### 抿能触发
技能会根据上下文自动触发，无需手动调用。

### 连接器
编辑 `.mcp.json` 连接你的工具。
