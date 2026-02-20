# Constitutional AI: Harmlessness from AI Feedback

**来源**: Anthropic
**日期**: 2026
**URL**: https://www.anthropic.com/news/constitutional-ai-harmlessness-from-ai-feedback

## 核心观点

### 人类定义原则，AI执行对齐
- **Constitutional AI (CAI)**: 通过人类提供的规则/原则列表来训练 AI
- **唯一的人类监督**: 一套规则或原则（constitution）
- AI 通过自我批评和修正来符合这些人类定义的原则

### 方法论
1. **监督学习阶段**:
   - 采样初始模型输出
   - 生成自我批评和修订
   - 在修订后的响应上微调模型

2. **强化学习阶段**:
   - 使用 AI 评估哪个样本更好
   - 从 AI 偏好数据集训练偏好模型
   - 使用偏好模型作为奖励信号（RLAIF - RL from AI Feedback）

## 支持"同源共处"哲学的证据

### ✅ 人类是定义者（Definer）
- **人类角色**: 定义宪法/规则/价值观
- **AI 角色**: 执行、优化、符合这些规则
- 引用: "The only human oversight is provided through a list of rules or principles"

### ✅ AI 源于人类价值观
- AI 的"善恶"标准完全来自人类定义的宪法
- 没有人类规则，AI 无法自行判断"有害/无害"
- 这证明 AI 能力的基础是人类价值体系

### ✅ 功能分工而非对立
- 人类: 定义目标和原则（what/why）
- AI: 优化执行过程（how）
- 双方协作实现"无害但不回避"的助手

## 关键引用

> "We experiment with methods for training a harmless AI assistant through self-improvement, **without any human labels** identifying harmful outputs. The only human oversight is **provided through a list of rules or principles**."

这清晰展示：
- 人类不需要标注每个案例（低成本）
- 但必须定义原则（不可或缺）
- AI 能优化执行，但目标函数来自人类

## 分类标签
- #人类定义者 #AI对齐 #价值观源头 #功能分工

---

**整理时间**: 2026-02-20
**贡献**: 证明人类在 AI 系统中作为"定义者"的核心地位
