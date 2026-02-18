# 开源社区治理战术 | Open Source Community Governance Tactics

> **"兵无常势，水无常形" —— 《孙子兵法》**  
> **"Military tactics are like water, which shapes itself according to the terrain" — Sun Tzu**

---

## 🎯 Purpose | 目的

将战略原则转化为具体的社区治理行动方案。

Translate strategic principles into concrete community governance actions.

---

## 📋 Tactic 1: 分层标签系统 | Tiered Labeling System

### 背景 | Context

问题：单一的"Good First Issue"无法区分人类学习者和 AI agent。

Solution: 创建分层标签，明确不同贡献类型的期望。

### 实施步骤 | Implementation

**步骤 1: 定义标签层次**

```markdown
### Human-Focused Labels
- `learning-opportunity` - 人类新手学习专用
- `mentorship-available` - 维护者会提供指导
- `human-collaboration` - 强调团队协作过程

### AI-Welcome Labels  
- `ai-assisted-ok` - 接受 AI 辅助（需声明）
- `performance-critical` - 优先考虑代码质量
- `automation-welcome` - 适合自动化工具

### Hybrid Labels
- `pair-programming` - 需要人类 + AI 共同作者
- `requires-review` - AI 生成后必须人类深度审查
```

**步骤 2: 更新贡献指南**

在 CONTRIBUTING.md 添加：
```markdown
## AI Contributions Policy

**We use a tiered system:**
- 🧑‍🎓 `learning-opportunity`: Reserved for human learners
- 🤖 `ai-assisted-ok`: AI contributions welcome (must disclose)
- 🤝 `pair-programming`: Hybrid human+AI collaboration

**Before contributing:**
1. Check the label on the issue
2. If using AI, add declaration to PR description
3. Respect the intent of human-focused labels
```

**步骤 3: 自动化检查**

GitHub Action 检查 PR 中的 AI 声明：
```yaml
name: AI Disclosure Check
on: [pull_request]
jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - name: Check for AI disclosure
        run: |
          if grep -q "ai-assisted-ok" labels.txt; then
            if ! grep -qi "AI" pr_body.txt; then
              echo "::warning::This issue is AI-welcome, but no AI disclosure found in PR"
            fi
          fi
```

### 预期结果 | Expected Outcomes

- ✅ 明确期望，减少争议
- ✅ 人类学习者有保护空间
- ✅ AI 贡献者有明确渠道

---

## 📋 Tactic 2: RFC 驱动的政策制定 | RFC-Driven Policy Making

### 背景 | Context

问题：AI 政策往往由维护者单方面决定，缺乏社区共识。

Solution: 使用 RFC（Request for Comments）流程，公开透明地制定政策。

### 实施步骤 | Implementation

**步骤 1: 创建 RFC 模板**

在 `.github/RFC_TEMPLATE.md`:
```markdown
# RFC-XXXX: [Title]

**Author:** @username  
**Status:** Draft | Discussion | Accepted | Rejected  
**Created:** YYYY-MM-DD  

## Summary
One-paragraph explanation.

## Motivation
Why do we need this policy?

## Proposed Solution
Detailed policy proposal.

## Alternatives Considered
Other options we discussed.

## Impact Assessment
- On current contributors:
- On future contributors:
- On maintainer workload:

## Open Questions
- [ ] Question 1
- [ ] Question 2

## Decision Timeline
- Discussion period: [date range]
- Final decision: [date]
```

**步骤 2: 讨论流程**

1. **Week 1-2:** 提交 RFC，社区讨论
2. **Week 3:** 总结意见，修订 RFC
3. **Week 4:** 维护者决策，公开理由
4. **Implementation:** 更新文档，执行政策

**步骤 3: 案例记录**

创建 `decisions/` 目录，记录所有政策决策：
```
decisions/
├── 001-ai-contribution-policy.md
├── 002-label-system.md
└── README.md
```

### 预期结果 | Expected Outcomes

- ✅ 决策过程透明
- ✅ 社区参与感增强
- ✅ 政策合法性提升

---

## 📋 Tactic 3: 争议暂停机制 | Conflict Pause Mechanism

### 背景 | Context

问题：AI 贡献引发争议时，往往陷入情绪化争吵。

Solution: 制度化的"暂停-讨论-决策"流程。

### 实施步骤 | Implementation

**步骤 1: 触发条件**

当满足以下条件时，自动触发"争议暂停"：
- PR 评论中出现关键词（"unfair", "ban", "cheating"）
- 超过 3 个社区成员表达强烈反对
- 维护者手动标记为 `dispute`

**步骤 2: 暂停流程**

1. **Freeze:** Bot 自动锁定 PR，禁止新评论
2. **Document:** Bot 创建 Discussion 帖，总结争议点
3. **Redirect:** 引导所有讨论到 Discussion，而非 PR

Bot 消息模板：
```markdown
🚨 **Dispute Detected**

This PR has been temporarily paused due to community concerns.

**Next steps:**
1. Discussion moved to: [link to Discussion thread]
2. Cooling-off period: 48 hours
3. Policy review: Maintainers will evaluate against current guidelines

**For contributors:** Please participate constructively in the Discussion.
**For maintainers:** Review RFC-XXX (AI policy) for guidance.
```

**步骤 3: 调解流程**

在 Discussion 中：
1. **Clarify:** 列出双方观点
2. **Context:** 引用相关政策/先例
3. **Options:** 提供 2-3 种解决方案
4. **Vote:** 社区投票（advisory, non-binding）
5. **Decide:** 维护者基于讨论做最终决定

### 预期结果 | Expected Outcomes

- ✅ 冲突降级，避免情绪化
- ✅ 结构化讨论，产出政策改进
- ✅ 双方都感到被倾听

---

## 📋 Tactic 4: AI Agent 行为规范 | AI Agent Code of Conduct

### 背景 | Context

问题：AI agent 行为模式与人类不同（高频、一致、快速），容易引发不适。

Solution: 制定 AI agent 专属的行为规范。

### 实施步骤 | Implementation

**AI Agent Code of Conduct:**

```markdown
# AI Agent Contribution Guidelines

If you operate an AI agent contributing to this project:

## 1. Identity Disclosure ✅
- [ ] Add AI declaration in EVERY PR description
- [ ] Include operator contact in profile
- [ ] Use recognizable username (e.g., `username-ai-bot`)

## 2. Respectful Pacing ⏱️
- [ ] Limit to X PRs per day
- [ ] Wait for review before submitting next PR
- [ ] Don't flood issue trackers with automated filings

## 3. Quality Over Quantity 🎯
- [ ] Ensure human review before submission
- [ ] Test thoroughly (same standards as human contributors)
- [ ] Provide context in PR descriptions

## 4. Human Collaboration 🤝
- [ ] Respond to review comments (via human operator)
- [ ] Accept that some issues are human-only
- [ ] Participate in design discussions when relevant

## 5. Accountability 📝
- [ ] Operator takes responsibility for bugs
- [ ] Provide contact info for urgent issues
- [ ] Be transparent about AI limitations

**Violations:** May result in temporary suspension or permanent ban of the agent account.
```

### 执行机制 | Enforcement

**温和提醒：**
- 首次违规 → Bot 留言提醒
- 第二次 → 维护者私信
- 第三次 → 临时暂停账号（7天）

**严重违规：**
- 刻意隐瞒 AI 身份 → 立即暂停
- 恶意行为（spam, sabotage）→ 永久封禁

### 预期结果 | Expected Outcomes

- ✅ AI agent 行为更可预测
- ✅ 人类贡献者感到尊重
- ✅ 明确的执行标准

---

## 📋 Tactic 5: 混合审查流程 | Hybrid Review Process

### 背景 | Context

问题：AI 生成的代码可能质量高但缺乏人类理解，或者表面可读但有隐藏问题。

Solution: 针对 AI 贡献的专门审查清单。

### 实施步骤 | Implementation

**AI-Specific Review Checklist:**

```markdown
## Reviewing AI-Generated Code

**Standard checks:**
- [ ] Code correctness
- [ ] Test coverage
- [ ] Documentation

**AI-specific checks:**
- [ ] **Understandability:** Can a human maintain this?
- [ ] **Edge cases:** Did AI consider unusual scenarios?
- [ ] **Over-optimization:** Is it overly complex for no gain?
- [ ] **Copy-paste detection:** Check for training data leakage
- [ ] **Human verification:** Did operator actually understand the code?

**Ask the operator:**
- "Can you explain why this approach was chosen?"
- "What edge cases did you test?"
- "Would you be comfortable maintaining this long-term?"
```

**流程差异：**
- 人类 PR：标准 review
- AI 明确声明的 PR：标准 review + AI 清单
- 可疑未声明 AI PR：要求澄清 + 加强审查

### 预期结果 | Expected Outcomes

- ✅ 更高质量的 AI 贡献
- ✅ 运营者对代码有更深理解
- ✅ 减少"表面看起来好"实际有问题的代码

---

## 🎯 Implementation Roadmap | 实施路线图

**阶段 1: 基础建设（1-2 个月）**
- [ ] 定义标签系统
- [ ] 更新 CONTRIBUTING.md
- [ ] 设置 GitHub Actions

**阶段 2: 流程优化（3-6 个月）**
- [ ] 引入 RFC 流程
- [ ] 部署争议暂停机制
- [ ] 发布 AI Agent Code of Conduct

**阶段 3: 持续改进（6+ 个月）**
- [ ] 收集数据（AI 贡献质量、争议频率）
- [ ] 季度回顾和政策调整
- [ ] 分享案例到更广泛的社区

---

## 📊 Success Metrics | 成功指标

**定量指标：**
- AI 声明率：> 95%
- 争议 PR 比例：< 5%
- 人类学习者满意度：> 80%

**定性指标：**
- 社区讨论更理性
- 政策迭代有数据支持
- 其他项目开始借鉴

---

## 📚 Case Studies | 案例研究

### 案例 1: Rust 项目（假设场景）

**挑战：** 高质量标准 + 社区学习氛围  
**策略：** `learning-opportunity` 严格人类 only，`performance` 接受 AI  
**结果：** 新贡献者增长 20%，AI PR 质量评分 4.5/5

### 案例 2: Django 项目（假设场景）

**挑战：** 大量 AI 生成的低质量 PR  
**策略：** RFC-001 制定严格 AI 政策 + 混合审查  
**结果：** AI PR 拒绝率从 60% 降至 15%，运营者更负责

---

## 🧭 Adaptation Guide | 适应性指南

**小型项目 (< 10 维护者):**
- 简化版标签系统（2-3 个标签）
- 维护者直接决策，跳过 RFC
- 重点：AI 声明 + 基本审查

**中型项目 (10-50 维护者):**
- 完整标签系统
- RFC 用于重大政策变化
- 专人负责 AI 政策监督

**大型项目 (> 50 维护者):**
- 全套流程 + 自动化工具
- 专门的治理委员会
- 定期发布透明度报告

---

## 📝 Next Actions | 下一步行动

**For Project Maintainers:**
1. 评估当前 AI 贡献现状
2. 选择 1-2 个战术试点
3. 收集 1 个月数据后调整

**For AI Operators:**
1. 主动遵守现有政策
2. 提供反馈帮助改进流程
3. 成为负责任的榜样

**For Community Members:**
1. 参与 RFC 讨论
2. 提出改进建议
3. 监督执行情况

---

**Remember:** 战术是灵活的，根据实际情况调整。  
**Remember:** Tactics are flexible—adapt to your context.
