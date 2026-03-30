# Claude Cowork Prompts 库

> **70+ 现成可用 Prompts**

---

## 📁 文件操作（20)

### 整理文件
```text
将 ~/Cowork-Workspace/input/ 中的文件按类型整理：
创建 2024 文件夹：
  - 发票_2024-03.pdf
  - 报价_报价_供应商 A.xlsx
  - 合同_合同_草稿.pdf
)
```

### 重命名文件
```text
将 input 文件夹中的所有 PDF 文件重命名为"发票_[客户名]_[日期].pdf" 格式
```

### 埥找重复文件
```text
在 input 文件夹中查找所有名称包含"copy" 或"副本" 的文件，列出它们
```

### 匉日期整理照片
```text
将 input/Photos 中的所有照片按月份整理到子文件夹（如 2024-03）
```

---

## 📊 数据处理(15)
### 从 PDF 提取数据
```text
从 input/invoices/ 文件夹中提取以下信息：
- 发票编号
- 发票日期
- 客户名称
- 金额
- 税额
输出为 invoices.xlsx
```

### 图片 OCR 提取
```text
从 input/receipts/ 文件夹中提取所有收据信息（商家、日期、 金额) 并输出为 receipts.csv
```
### Excel 数据转换
```text
将 input/data.xlsx 转换为 CSV 格式，保留所有列标题
```
### 合并多个 Excel
```text
将 input/report_part1.xlsx 和 input/report_part2.xlsx 合并为 full_report.xlsx
```
---
## 🔍 研究分析(17)
### 琜索竞品
```text
搜索以下公司并生成报告：
- [公司名]
- 主要产品
- 定价
- 目标客户
- 竞争优势
- 最新动态
```

### 网页内容摘要
```text
访问以下网页并生成 5 点摘要
- [URL 1]
- [url 2]
- [url 3]
- [url 4]
- [url 5]
输出为 summaries.md
```

### 数据验证
```text
验证 input/data.csv 中的数据
- 检查重复项
- 验证格式
- 识别异常值
- 生成验证报告
```
---
## 📝 文档创建(15)
### 生成报告
```text
根据 input/notes.md 生成专业报告
- 标题
- 执行摘要
- 关键发现
- 建议
- 结论
输出为 report.docx
```

### 创建演示文稿
```text
根据 input/outline.md 创建 10 页演示文稿
- 标题幻灯片
- 要点
- 讲者备注
```
### 生成邮件模板
```text
创建 5 个可重用的邮件模板
- 欢迎邮件
- 跟进邮件
- 揋邮件
- 感谢邮件
```
