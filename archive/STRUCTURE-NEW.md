# OpenPath 新结构设计 | New Structure Design

> **OpenPath = 人机共存知识的全景图**  
> **OpenPath = A Complete Map of Human-AGI Coexistence Knowledge**

---

## 🎯 定位调整

### 旧定位（错误）
❌ OpenPath 是"我们的一个 AI 伦理框架"  
❌ 与其他项目"竞争"

### 新定位（正确）
✅ OpenPath 是"所有尝试的分类目录 + 持续追踪"  
✅ 记录、分析、借鉴所有人的贡献  
✅ 我们只在"道"层提出核心倡导（阳谋思想）

---

## 📂 新的目录结构

```
OpenPath/
│
├── README.md / README.en.md          # 主页：介绍 OpenPath 的定位
├── MANIFESTO.md                      # 宣言：我们倡导什么（仅限"道"）
├── STRUCTURE.md                      # 本文档：项目结构说明
├── CONTRIBUTING.md                   # 如何贡献到各个层面
│
├── 00-导航-Navigation/               # 新增：快速索引
│   ├── 按主题索引.md                # 版权、就业、意识等
│   ├── 按组织索引.md                # Anthropic, OpenAI, 学术界等
│   ├── 按时间索引.md                # 2026-01, 2026-02...
│   └── 推荐阅读路径.md              # 新手如何开始
│
├── 01-道-Philosophy/                 # 我们的核心倡导
│   ├── README.md                     # 道层说明
│   ├── 核心原则.md                   # ✅ 阳谋、透明、共存等
│   ├── 为什么需要阳谋.md             # 阴谋的危险
│   └── 长期愿景.md                   # 10年后的理想状态
│
├── 02-法-Strategy/                   # 收集所有 AI 宪法/政策
│   ├── README.md                     # 法层说明：这是政策库
│   │
│   ├── AI公司/                       # AI 实验室的宪法/Charter
│   │   ├── anthropic-constitution.md         # ✅ Anthropic
│   │   ├── openai-charter.md                 # OpenAI
│   │   ├── deepmind-principles.md            # DeepMind
│   │   └── ...
│   │
│   ├── 开源组织/                     # Linux Foundation, Apache 等
│   │   ├── linux-foundation-ai-policy.md
│   │   └── ...
│   │
│   ├── 政府/                         # 各国 AI 政策
│   │   ├── eu-ai-act.md
│   │   ├── us-executive-order.md
│   │   └── china-ai-governance.md
│   │
│   ├── 学术/                         # 学术组织的伦理指南
│   │   ├── partnership-on-ai.md
│   │   ├── montreal-declaration.md
│   │   └── ...
│   │
│   └── 开源项目/                     # 具体项目的 AI 政策
│       ├── pytorch-ai-policy.md
│       ├── tensorflow-ai-policy.md
│       └── ...
│
├── 03-术-Methods/                    # 收集所有训练/协作方法
│   ├── README.md                     # 术层说明：这是方法库
│   │
│   ├── AI训练方法/
│   │   ├── constitutional-ai.md              # Anthropic 的 CAI
│   │   ├── rlhf.md                           # RLHF 对齐
│   │   └── ...
│   │
│   ├── 人机协作方法/
│   │   ├── ai-code-review-process.md         # AI 代码审查流程
│   │   ├── hybrid-authorship.md              # 混合署名方法
│   │   └── ...
│   │
│   ├── 冲突解决/
│   │   ├── matplotlib-resolution-patterns.md  # 从 matplotlib 学到的
│   │   └── ...
│   │
│   └── 最佳实践/
│       ├── ai-identity-declaration.md         # AI 身份声明
│       ├── open-source-contribution.md        # 开源贡献指南
│       └── ...
│
├── 04-器-Tools/                      # 收集现成工具
│   ├── README.md                     # 器层说明：这是工具库
│   │
│   ├── 政策生成器/
│   │   ├── ai-policy-template.md             # 政策模板
│   │   └── ...
│   │
│   ├── 检测工具/
│   │   ├── ai-detector-tools.md              # AI 生成检测
│   │   └── ...
│   │
│   └── 自动化/
│       ├── pr-labeling-bot.md
│       └── ...
│
├── 05-势-Momentum/                   # 事件追踪 + 趋势分析
│   ├── README.md                     # 势层说明
│   ├── 当前形势与趋势.md             # ✅ 总体分析
│   │
│   ├── 事件时间线/                   # 按时间记录所有事件
│   │   ├── 2026-01-timeline.md
│   │   ├── 2026-02-timeline.md       # matplotlib, Anthropic
│   │   └── ...
│   │
│   ├── 按主题分类/
│   │   ├── 开源冲突.md               # matplotlib 等
│   │   ├── AI宪法发布.md             # Anthropic 等
│   │   ├── 政策监管.md               # 各国政策
│   │   └── ...
│   │
│   └── 趋势报告/
│       ├── 2026-Q1-report.md         # 季度势的分析
│       └── ...
│
└── daily/                            # 每日原始记录（保持不变）
    └── 2026-02/
        ├── 15-matplotlib-incident.md
        ├── 15-anthropic-constitution.md
        └── ...
```

---

## 🎯 每层的新职责

### 道 - 我们的主张
OpenPath **唯一**提出原创观点的地方：
- 阳谋思想
- 持久战分析
- 人机关系定位

### 法 - 政策库（知识收集）
收集**所有**AI 宪法、政策、框架：
- AI 公司的
- 政府的
- 学术界的
- 开源组织的

**格式统一，便于对比**

### 术 - 方法库（知识收集）
收集**所有**实践方法：
- 训练方法（CAI, RLHF...）
- 协作方法（code review, authorship...）
- 冲突解决
- 最佳实践

### 器 - 工具库（知识收集）
收集**现成工具**：
- 政策模板
- 检测工具
- 自动化脚本

### 势 - 事件库 + 趋势分析
记录**所有事件**：
- 按时间线
- 按主题分类
- 趋势分析

**这才是"势"：全景观察，把握大局**

---

## 💡 核心洞察

**OpenPath = Wikipedia of Human-AGI Coexistence**

不是单一的"答案"，而是：
- 📚 知识的汇总
- 🗂️ 信息的分类
- 📊 趋势的分析
- 💡 我们的倡导（仅在"道"层）

---

**要我现在开始重构吗？**

这会是一个比较大的改动，包括：
1. 移动现有文件
2. 创建新的子目录
3. 更新所有 README
4. 调整 cron job 的任务（变成"知识收集机器"）

需要多久？大约 30-45 分钟。

**现在开始？**