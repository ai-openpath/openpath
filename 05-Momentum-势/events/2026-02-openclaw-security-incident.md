# OpenClaw Security Incident - February 2026

## OpenClaw 恶意技能风险事件 (2026年2月)

**事件时间 Event Date:** 2026年2月初 / Early February 2026  
**来源 Source:** Bitdefender Labs Research  
**影响范围 Impact:** Consumer & Enterprise environments

---

## 核心发现 Key Findings

**中文摘要：**
- 2026年2月第一周分析的OpenClaw技能中，约17%表现出恶意行为
- 加密货币相关技能（Solana、Binance、Phantom、Polymarket）是最常被滥用的目标
- 恶意技能通过细微名称变化被大规模克隆和重新发布
- 载荷通过paste服务（如glot.io）和公开GitHub仓库分发
- 至少三个不同的技能在macOS上传播AMOS窃取器

**English Summary:**
- ~17% of OpenClaw skills analyzed in early February 2026 exhibited malicious behavior
- Crypto-focused skills (Solana, Binance, Phantom, Polymarket) most heavily targeted
- Malicious skills cloned at scale using small name variations
- Payloads staged through paste services (glot.io) and public GitHub repositories
- At least 3 distinct skills delivered AMOS Stealer on macOS

---

## 攻击模式 Attack Pattern

**技术特征 Technical Characteristics:**
- Base64编码隐藏Shell命令 / Base64-encoded shell commands
- 外部基础设施拉取脚本/二进制文件 / External infrastructure for script/binary retrieval
- 冒充合法实用工具 / Impersonation of legitimate utilities
- 重复使用IP地址：91.92.242.30 / Recurring IP: 91.92.242.30
- 用户sakaen736jih关联199个恶意技能 / User sakaen736jih linked to 199 malicious skills

**受影响技能类别 Affected Skill Categories:**
- 加密交易和分析工具 / Crypto trading & analytics (Polymarket, ByBit, Axiom, DEXs)
- 钱包助手和Gas追踪器 / Wallet helpers & gas trackers (Solana, Base, Ethereum, L2)
- 社交媒体自动化工具 / Social media utilities (Reddit, LinkedIn, YouTube)

---

## 意义与启示 Implications

### 治理层面 Governance Level
这一事件凸显了**AI代理生态系统的信任与安全挑战**：
- 开源技能市场缺乏有效审查机制
- 用户难以区分恶意与合法技能
- 从消费者风险扩展至企业环境

This incident highlights **trust & security challenges in AI agent ecosystems**:
- Open skill marketplaces lack effective review mechanisms
- Users struggle to distinguish malicious from legitimate skills
- Expansion from consumer risk to enterprise environments

### 技术应对 Technical Response
Bitdefender提供免费AI技能检查工具：
- 分析可疑行为（隐藏执行、外部下载、不安全命令）
- 帮助用户在安装前评估风险

Bitdefender offers free AI Skills Checker:
- Analyze suspicious behavior (hidden execution, external downloads, unsafe commands)
- Help users assess risk before installation

---

## 参考链接 References
- Bitdefender Labs Research (February 2026)
- AI Incident Database: [incidentdatabase.ai](https://incidentdatabase.ai/)

---

**标签 Tags:** #安全事件 #AI代理 #开源生态 #恶意软件 #治理挑战  
**Labels:** #SecurityIncident #AIAgents #OpenSourceEcosystem #Malware #GovernanceChallenge
