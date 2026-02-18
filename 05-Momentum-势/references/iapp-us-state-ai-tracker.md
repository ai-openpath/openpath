# IAPP US State AI Governance Legislation Tracker

**Source:** [IAPP (International Association of Privacy Professionals)](https://iapp.org/resources/article/us-state-ai-governance-legislation-tracker)  
**Type:** Living Resource (continuously updated)  
**Focus:** Cross-sectoral AI governance bills (private sector)  
**Archived:** 2026-02-18

---

## Purpose

**Why this matters for OpenPath:**
- **Real-time monitoring** of state-level AI regulations (before federal preemption kicks in)
- **Early warning system** for emerging governance patterns
- **Data source** for 05-Momentum timeline updates

---

## Key Insights (as of Feb 2026)

### Regulatory Patterns by State

**Leading states (most active):**
1. **California** — Focus on algorithmic accountability, bias audits
2. **New York** — Employment AI, automated decision systems
3. **Illinois** — Biometric privacy (BIPA expanded to AI)
4. **Colorado** — Consumer protection, algorithmic transparency

**Trends:**
- **Employment AI** (hiring, firing, promotion) most regulated sector
- **Biometric data** (face recognition, emotion detection) second priority
- **Transparency requirements** (impact assessments, public disclosures) common theme

### Federal Preemption Impact (Dec 2025 Order)

**Tracker now includes:**
- ⚠️ **Conflict markers** for state laws potentially preempted by federal "truthfulness mandate"
- Example: California bill requiring "context-sensitive outputs" may conflict with federal "no alteration" rule

---

## Connection to OpenPath Framework

### 02-Methodology: Governance Case Studies

**Use tracker to identify:**
- **Best practices** (Colorado's stakeholder input model)
- **Failures** (Texas bill that died due to industry lobbying)
- **Conflicts** (state innovation vs. federal uniformity)

### 05-Momentum: Timeline Building

**Monthly review cadence:**
1. Check tracker for new bills
2. Categorize by sector (employment, healthcare, criminal justice, consumer)
3. Assess alignment with OpenPath principles
4. Update 势-Momentum with key developments

---

## Strategic Use Cases

### For OpenPath Advocacy

**Scenario 1: Supporting Good Bills**
> "Colorado's HB 24-1387 requires AI impact assessments — exactly what OpenPath advocates for in 02-Methodology. Here's how to adapt it to your state..."

**Scenario 2: Opposing Bad Bills**
> "Texas SB 123 exempts 'proprietary algorithms' from transparency — this undermines carbon-based oversight. Here's why..."

### For Academic Research

**Data mining opportunities:**
- Track **which AI risks** states prioritize (bias? safety? privacy?)
- Analyze **lobbying patterns** (which industries resist which rules?)
- Compare **enforcement mechanisms** (fines? audits? certifications?)

---

## Monitoring Workflow

**Weekly check (automated reminder):**
1. Visit IAPP tracker
2. Filter by "Updated in last 7 days"
3. Scan for:
   - New bills introduced
   - Existing bills passed/failed
   - Amendments to active laws

**Document significant updates in:**
- `05-Momentum/势/policy-timeline.md`
- `memory/YYYY-MM-DD.md` (daily notes)
- Flag major changes for `MEMORY.md` (long-term memory)

---

## Cross-Reference with Other Trackers

**Combine IAPP data with:**
- **AI Now Institute** — Research-focused policy analysis
- **Future of Privacy Forum** — Industry perspective
- **Electronic Frontier Foundation** — Civil liberties focus

**Why?** No single source is neutral — triangulate across perspectives.

---

## Example Entry Format (for 05-Momentum)

```markdown
### California AB 1008 - Algorithmic Accountability Act
**Status:** Passed Assembly, pending Senate (2026-02-10)  
**Key provision:** Requires impact assessments for "high-risk" AI systems  
**OpenPath alignment:** ✅ Supports transparent governance  
**Risk:** ⚠️ Definition of "high-risk" may exclude critical systems  
**Source:** [IAPP Tracker](link)
```

---

## Integration with Cron Job

**Current hourly job can:**
1. Scrape IAPP tracker for updates
2. Auto-generate summaries for new bills
3. Flag conflicts with federal policy
4. Commit to `05-Momentum/势/references/`

**Future enhancement:** RSS feed parser + Telegram alerts for major developments.

---

**Tags:** #state-policy #ai-regulation #tracking-tool #iapp #momentum-source
