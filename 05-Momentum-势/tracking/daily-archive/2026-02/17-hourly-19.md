# 2026-02-17 19:00 Hourly Scan | 每小时扫描

> 时间：19:00 (Asia/Shanghai)  
> 来源：HN + arXiv

---

## 05-Momentum-势 | AI透明度争议

### Anthropic隐藏Claude行为遭开发者反对
- **来源**: The Register (2026-02-16)
- **URL**: https://www.theregister.com/2026/02/16/anthropic_claude_ai_edits/
- **分类**: 05-Momentum → AI透明度争议
- **价值**: ⭐⭐⭐⭐ 透明度治理的现实案例

**事件概要**:
- Anthropic更新Claude Code v2.1.20，隐藏文件名（默认折叠输出）
- 开发者强烈反对：需要看到文件名以便安全审计、节省token、早期捕获错误
- Boris Cherny（Claude Code负责人）称目的是"简化UI"，开发者可用详细模式
- 反馈："这不是简化，是愚蠢地删除有价值信息"
- 核心问题：**AI工具如果隐藏行为，错误更可能漏过**

**关键引用**:
> "I'm a Claude user who has been burned lately by how opaque the system has become. Right now Claude cannot be trusted to get things right without constant oversight and frequent correction... If I cannot follow the reasoning, the session just burns through my token quota."

**对OpenPath的启示**:
- 透明度不是"nice to have"，是**用户信任和效率的核心**
- AI自主性 ≠ 黑箱化，反而需要更强的可观测性
- 案例可用于 `02-Methodology/references/案例库/Anthropic-透明度争议.md`

---

## 02-Methodology-法 | Agent评估标准

### SkillsBench: Agent技能跨任务效果基准测试
- **来源**: arXiv (2026-02-13)
- **URL**: https://arxiv.org/abs/2602.12670
- **分类**: 02-Methodology → 评估框架
- **价值**: ⭐⭐⭐⭐ Agent技能评估标准

**研究摘要**:
- 86个任务 × 11个领域，测试三种条件：无技能、精选技能、自生成技能
- **精选技能平均提升16.2个百分点**，但领域差异大（软件工程+4.5pp，医疗+51.9pp）
- **自生成技能平均无效**：模型无法可靠生成它们能受益的程序性知识
- **聚焦技能（2-3模块）优于全面文档**
- **小模型+技能可匹配无技能大模型**

**核心洞察**:
1. 技能不是万能的（16/84任务负增益）
2. 模型"消费知识"能力 ≠ "生成知识"能力（类似人类学习）
3. 结构化技能 > 通用文档

**对OpenPath的启示**:
- Agent能力需要**结构化外部知识（技能）** + **强评估标准**
- 与Q2（碳基智能）的联系：人类专业知识仍需手工编码为技能，AI无法自生成
- 可补充到 `02-Methodology/references/案例库/SkillsBench-评估框架.md`

---

## 元信息

- 搜索方式：HN前端页面 + arXiv直接抓取
- 结果归档：
  - 05-Momentum（透明度）：1条
  - 02-Methodology（评估）：1条
- 下次建议：继续搜索政策/哲学类内容补充01-道、02-法

---

**"透明度是信任的前提 | Transparency is the foundation of trust"**
