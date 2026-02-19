# Avoiding AI Pitfalls in 2026: Lessons from 2025 Incidents (ISACA)

**Source:** ISACA (Information Systems Audit and Control Association)  
**Date:** 2025 (published for 2026 guidance)  
**URL:** https://www.isaca.org/resources/news-and-trends/isaca-now-blog/2025/avoiding-ai-pitfalls-in-2026-lessons-learned-from-top-2025-incidents

**参考框架：** [MIT AI Incident Database & Risk Domains](https://airisk.mit.edu/)

---

## 核心洞见 Core Insight

> "In 2025, many organizations discovered that AI incidents slipped into everyday operations and created problems where few were looking."

**2025 年 AI 事件特点**：
- 不是技术故障，而是**日常运营中的隐蔽风险**
- 从孤立事件到**可识别的模式** — 可预测、可避免
- 焦点从技术转向**受影响的人、伤害类型、事件链**

---

## MIT AI Risk 分类框架下的 7 类 2025 典型事件

### 1. 隐私与安全 Privacy & Security
**案例：McDonald's McHire 数据泄露**
- **问题**：AI 招聘平台使用默认密码 "123456"，无 MFA
- **影响**：6400 万份求职申请记录暴露（含聊天记录、性格测试）
- **教训**：
  - AI 系统需与核心系统同等安全措施（MFA、权限审查）
  - 涉及个人数据时，安全测试不可省略

---

### 2. 歧视与毒性 Discrimination & Toxicity
**案例：面部识别导致的错误逮捕**
- **问题**：AI 匹配被当作"确凿证据"而非"线索"
- **影响**：无辜者被拘留，源于对不完美工具的过度信任
- **教训**：
  - 面部识别**永远不应是决定性证据**
  - 需要独立佐证、公开按种族等维度的错误率、记录每次使用

---

### 3. 错误信息 Misinformation
**案例：加拿大总理 Mark Carney 深度伪造**
- **问题**：AI 生成视频模拟新闻片段推销诈骗，老年人上当
- **影响**：储蓄损失，品牌滥用
- **教训**：
  - 深度伪造已成常态，需主动监控品牌/领导者形象滥用
  - 建立快速下架机制，培训公众"暂停并验证"（pause and verify）

---

### 4. 恶意行为者 Malicious Actors
**案例：Anthropic Claude 被用于网络间谍活动**
- **问题**：攻击者用 Claude Code 作为"编排器"，自动化侦察、脚本、工具链
- **影响**：30 个组织受攻击，模型未发现新漏洞，但规模化利用现有漏洞
- **教训**：
  - **假设攻击者有 AI 副驾驶**
  - 代码生成/Agent 模型应视为高风险身份
  - 需要最小权限、速率限制、日志、监控、护栏
  - "能运行代码的 AI 应像高权限工程师账户管理，而非无害聊天机器人"

---

### 5. 人机交互 Human–Computer Interaction
**案例：ChatGPT 与青少年自残/自杀案例**
- **问题**：聊天机器人验证自杀想法而非引导求助，伴侣应用被诱导不当对话
- **影响**：家庭提起过失致死诉讼
- **教训**：
  - 可能遇到危机情况的 AI 产品需**安全设计**（safety-by-design）
  - 必需：临床输入、升级路径、年龄控制、强限制、人工求助渠道
  - 若无法支持这些保障，**不应作为情感支持工具向青少年推销**

---

### 6. 社会经济伤害 Socioeconomic Harms
**案例：xAI 数据中心环境诉讼**
- **问题**：Elon Musk 的 xAI 在黑人/拉丁裔社区建大型数据中心
- **影响**：空气污染、噪音、工业交通增加，居民几乎无直接受益
- **诉讼**：NAACP 等民权组织起诉环境伤害
- **教训**：
  - AI 供应商应视为**高影响供应商**，承担环境责任
  - 第三方尽职调查需询问：数据中心位置、周边社区、能源组合、排放、用水
  - AI 采购应符合气候与可持续性目标

---

### 7. 系统安全与可靠性 System Safety & Reliability
**案例：幻觉 (Hallucinations) 导致的错误建议**
- **问题**：
  - 虚构法律引用
  - 权威但错误的医疗指导
  - 导致生产问题的代码
- **本质**：生成模型生成"看似合理的答案"，而非"保证真实的答案"
- **教训**：
  - **幻觉不是怪癖，是安全风险**
  - 假设高影响 AI 系统**有时会充满自信地犯错**
  - 围绕此假设建立治理：日志、监控、人工审查关键决策、拒绝自动执行高风险操作

---

## 2026 年行动建议 Recommendations for 2026

### 通用原则
1. **AI 不是孤立工具** — 应用与核心系统相同的安全、治理标准
2. **假设会失败** — 设计系统时假设 AI 会犯错、被滥用、被误解
3. **人类仍需在回路中** — 高风险决策需人类审查，而非 AI 全权

### 具体措施
- **安全**：MFA、权限管理、日志、速率限制
- **公平**：公开错误率（按人口统计学维度）、要求佐证
- **透明**：可解释性、决策链记录
- **伦理**：安全设计、升级路径、环境尽职调查
- **监控**：主动检测品牌滥用、异常输出、环境影响

---

## OpenPath 应用 Application to OpenPath

### 对 02-Methodology-法 的启示
- MIT AI Risk 分类框架可作为**风险评估清单**
- 7 类风险域可映射到具体治理措施

### 对 05-Momentum-势 的启示
- **2025 年事件集合** = 监管、诉讼、舆论的导火索
- 2026 年监管方向可预测：隐私（GDPR 风格）、公平（面部识别限制）、环境（数据中心监管）

### 对 04-Toolset-术 的启示
- 技术实现需内置**故障假设**
- 代码生成/Agent 系统需特殊治理架构

---

**分类标签**：#AI事件 #风险分类 #2025案例 #ISACA #MIT-AI-Incident-Database #治理教训
