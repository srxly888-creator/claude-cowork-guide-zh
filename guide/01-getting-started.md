# Claude Cowork 入门指南

> 10 分钟快速上手

---

## 什么是 Cowork？

**Cowork** 是 Claude 桌面应用中的自主执行模式。与普通的 Chat 模式不同：

| Chat 模式 | Cowork 模式 |
|-----------|-------------|
| 问答式对话 | 任务委托式 |
| 只能建议 | 直接执行 |
| 无法访问文件 | 读/写/创建文件 |
| 单步操作 | 多步骤自主执行 |

**核心能力**：
- 📁 文件操作（读取、创建、编辑、移动、重命名）
- 🔍 网络搜索（自动搜索并整理信息）
- 📊 数据处理（Excel、PDF、图片分析）
- 🔄 自动化工作流（定时任务、批量处理）
- 🔌 工具集成（Slack、Gmail、Google Calendar 等）

---

## 第一步：启用 Cowork

### 1. 下载 Claude Desktop
```
https://claude.ai/download
```

### 2. 登录付费账户
- Pro ($20/月)
- Max 5x ($100/月)
- Max 20x ($200/月)

### 3. 启用 Cowork
```
设置 → 功能 → 启用 Cowork
```

### 4. 授予文件夹权限
**重要**：创建专用文件夹，不要授予整个 Documents 访问权限！

```bash
mkdir -p ~/Cowork-Workspace/{input,output,context}
```

---

## 全局指令设置

**位置**：设置 → Cowork → 全局指令（编辑）

**推荐模板**（复制粘贴）：

```
我是 [姓名]，[职位] 在 [公司]。我专注于 [领域]。

开始任何任务前：
- 先阅读相关上下文文件
- 执行前先问澄清问题
- 展示简要计划并等待我的批准

输出偏好：
- 最终交付物默认格式：.docx
- 草稿默认格式：.md
- 直接简洁，无填充语言
- 每个交付物应可直接使用

安全规则：
- 未经明确确认绝不删除文件
- 绝不修改指定输出文件夹之外的文件
- 在基于假设行动前明确标记假设
```

---

## 文件夹结构设置

### 推荐结构
```
~/Cowork-Workspace/
├── 00_Context/           # 持久化上下文
│   ├── about-me.md       # 关于我
│   ├── brand-voice.md    # 品牌声调
│   └── working-preferences.md  # 工作偏好
├── projects/             # 活跃项目
│   ├── client-a/
│   └── client-b/
└── outputs/              # 输出目录
```

### 上下文文件模板

#### about-me.md
```markdown
# 关于我

## 角色与职责
- [姓名、职位、公司]
- [日常工作内容]
- [关键利益相关者]
- [成功标准]

## 领域背景
- [行业/领域细节]
- [关键术语或框架]
- [工作流程中的工具和平台]

## 示例工作
[粘贴 1-2 个你满意的输出示例]
```

#### brand-voice.md
```markdown
# 沟通风格

## 语调
- [例如：直接简洁。必要时技术化。]
- [你自然使用的短语]
- [听起来不对的短语]

## 写作示例
[粘贴 2-3 个你的实际写作示例]

## 反模式
- [例如：永远不要把 "leverage" 当动词用]
- [例如：不要以 "希望这封邮件找到你" 开头]
```

#### working-preferences.md
```markdown
# 我希望 Claude 如何工作

## 流程
- 开始非平凡任务前总是问澄清问题
- 执行前展示你的计划
- 保存输出为 [.docx / .xlsx / .md — 你的偏好]

## 输出风格
- [简短 vs 详细输出]
- [首选格式约定]
- [文件命名约定]

## 守卫规则
- 未经明确确认绝不删除文件
- 绝不修改指定输出文件夹之外的文件
- 在基于假设行动前明确标记假设
```

---

## 第一个工作流

### 示例 1：文件整理
```
将 ~/Cowork-Workspace/input/ 中的文件按类型整理：
- 图片 → images/
- 文档 → documents/
- 表格 → spreadsheets/
- 其他 → others/
```

### 示例 2：发票生成
```
根据 ~/Cowork-Workspace/input/order.xlsx 生成专业发票：
- 使用公司模板
- 保存为 PDF
- 输出到 ~/Cowork-Workspace/output/
```

### 示例 3：会议准备
```
为明天的客户会议准备简报：
- 搜索公司背景信息
- 整理关键联系人
- 准备讨论要点
- 输出为 ~/Cowork-Workspace/output/meeting-brief.md
```

---

## 计划模式（关键！）

**一行代码防止 90% 错误**：

> "执行前展示简要计划。等待我的批准。"

**为什么重要**：
- 没有：Claude 立即开始工作，可能误解一个词就错误整理文件
- 有：Claude 先展示计划，你有 30 秒审查窗口

---

## 安装插件

### 如何安装
1. 点击 Claude Desktop 左侧边栏的 **Customize**
2. 点击 **Browse Plugins**
3. 选择插件点击 **Install**

或访问：https://claude.com/plugins

### 推荐首发插件
1. **Productivity** - 任务管理 + 日常更新
2. **Memory** - 两层上下文系统
3. 根据你的职位选择一个专业插件

---

## 连接工具

### 可用连接器
| 类别 | 工具 |
|------|------|
| 沟通 | Slack, Gmail, Microsoft Teams |
| 项目管理 | Notion, Asana, Linear, Jira, Monday, ClickUp |
| 文档 | Google Drive, Microsoft 365 |
| 设计 | Figma, Canva |
| 数据 | Snowflake, BigQuery, Amplitude |
| CRM | HubSpot, Salesforce |

### 连接步骤
1. 设置 → Connectors → 添加连接器
2. 授权 Claude 访问
3. 在 Cowork 中直接使用

---

## 下一步

1. ✅ 完成文件夹设置
2. ✅ 设置全局指令
3. ✅ 创建上下文文件
4. ✅ 安装第一个插件
5. ✅ 连接第一个工具
6. ✅ 运行第一个工作流

**推荐阅读**：
- [完整能力指南](02-capabilities.md)
- [安全最佳实践](03-security.md)
- [工作流库](../workflows/)
