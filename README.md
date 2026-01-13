# MVP-Grader

> **Objective project evaluation framework to prioritize which MVPs to build based on time, efficiency, and overall value.**

## 🎯 Purpose

This framework provides a systematic, objective methodology for evaluating project ideas and MVPs. By analyzing key success factors and market potential, you can make data-driven decisions about which projects deserve your time and resources.

## 📋 Evaluation Framework

### Core Evaluation Prompt

For each project being evaluated, use this comprehensive prompt:

```
Honest review of this app and potential to be a huge successor in its category? 

Objectively review its perks and flaws and rate all features and aspects of the app.

Provide suggestions to make it better and the best of them all and ways to market it best.

Also provide:
- ARR revenue projection if done perfectly
- Assessment: If I incorporated all of the flaws and fixed them fully, how objectively good would it be?

Save analysis in: Objective Review Analysis.md
```

### Grading Criteria

Each project will be evaluated across **7 critical dimensions**:

#### 1. ⏱️ **Time to Market**
- **Development Timeline** (1-10): How quickly can an MVP be built?
- **Complexity Score** (1-10): Technical difficulty and required expertise
- **Dependencies**: External services, APIs, infrastructure needs
- **Rating Weight**: 15%

#### 2. 🚀 **Efficiency**
- **Resource Requirements** (1-10): Development team size, skill requirements
- **Operational Overhead** (1-10): Maintenance, support, infrastructure costs
- **Scalability Potential** (1-10): Can it grow without proportional cost increases?
- **Rating Weight**: 15%

#### 3. 💎 **Overall Value**
- **Market Size** (1-10): Total addressable market (TAM)
- **Revenue Potential** (1-10): Monetization clarity and ARR projection
- **Unique Value Proposition** (1-10): Differentiation from competitors
- **Rating Weight**: 25%

#### 4. 🏆 **Market Opportunity**
- **Market Demand** (1-10): Proven need vs. speculative demand
- **Growth Trajectory** (1-10): Is the market expanding or saturating?
- **Entry Barriers** (1-10): How easy is it for competitors to enter? (Higher is better)
- **Rating Weight**: 15%

#### 5. 🛠️ **Technical Complexity**
- **Tech Stack Maturity** (1-10): Using proven vs. bleeding-edge tech
- **Integration Challenges** (1-10): Third-party dependencies and APIs
- **Infrastructure Requirements** (1-10): Cloud costs, DevOps, security
- **Rating Weight**: 10%

#### 6. 🎨 **Feature Quality**
- **Core Features** (1-10): Are essential features well-defined?
- **User Experience** (1-10): Intuitive design and flow
- **Innovation Factor** (1-10): Novel approach or incremental improvement?
- **Rating Weight**: 10%

#### 7. 📊 **Competitive Landscape**
- **Competition Level** (1-10): Crowded vs. blue ocean (Lower competition is better)
- **Differentiation** (1-10): Unique advantages over competitors
- **Market Position Potential** (1-10): Can this become category leader?
- **Rating Weight**: 10%

---

## 📈 Scoring System

### Individual Category Scores
- **1-3**: Critical flaws or major gaps
- **4-6**: Average, needs significant improvement
- **7-8**: Strong, minor improvements needed
- **9-10**: Exceptional, best-in-class

### Overall Project Score

Calculate the **weighted total score** using the rating weights above:

```
Total Score = (Time×0.15) + (Efficiency×0.15) + (Value×0.25) + 
              (Market×0.15) + (Technical×0.10) + (Features×0.10) + (Competition×0.10)
```

### Priority Classification

| Score Range | Priority | Action |
|-------------|----------|--------|
| **8.5 - 10** | 🔥 **CRITICAL** | Build immediately - exceptional opportunity |
| **7.0 - 8.4** | ⭐ **HIGH** | Strong candidate - plan development sprint |
| **5.5 - 6.9** | ⚠️ **MEDIUM** | Has potential - revisit after addressing gaps |
| **4.0 - 5.4** | ⏸️ **LOW** | Deprioritize - consider pivoting concept |
| **< 4.0** | ❌ **SHELVE** | Critical issues - not viable in current form |

---

## 📝 Project Analysis Template

For each project, create an **Objective Review Analysis.md** with this structure:

### 1. Executive Summary
- One-paragraph overview of the project
- Category and target market
- Key value proposition

### 2. Perks & Strengths
- ✅ List all competitive advantages
- ✅ Unique features
- ✅ Market opportunities

### 3. Flaws & Gaps
- ❌ Technical limitations
- ❌ Market challenges
- ❌ Feature gaps vs. competitors
- ❌ Resource constraints

### 4. Feature Rating Matrix

| Feature | Current Score (1-10) | Importance | Gap Analysis | Recommendation |
|---------|---------------------|------------|--------------|----------------|
| Feature 1 | 7/10 | High | Missing X | Add Y |
| Feature 2 | 5/10 | Critical | Poor UX | Redesign flow |

### 5. Competitive Analysis
- Direct competitors
- Indirect competitors
- White space opportunities

### 6. Improvement Roadmap
- **Phase 1 (Critical)**: Must-fix items before launch
- **Phase 2 (High)**: Enhance market position
- **Phase 3 (Nice-to-have)**: Polish and optimization

### 7. Marketing Strategy
- **Target Audience**: Detailed persona
- **Channels**: Where to reach them
- **Messaging**: Key value propositions
- **Go-to-Market Timeline**

### 8. Financial Projections

#### ARR Revenue Model (Perfected State)

| Metric | Conservative | Realistic | Optimistic |
|--------|-------------|-----------|------------|
| **Year 1 ARR** | $X | $Y | $Z |
| **Year 2 ARR** | $X | $Y | $Z |
| **Year 3 ARR** | $X | $Y | $Z |

**Assumptions:**
- Pricing model: [subscription/usage/hybrid]
- Customer acquisition cost (CAC): $X
- Lifetime value (LTV): $Y
- Monthly growth rate: Z%

### 9. Final Assessment

> **If all flaws were perfectly addressed, objective rating: X/10**

**Reasoning:**
- What makes this exceptional?
- Remaining risks even when perfected?
- Ultimate market position potential?

### 10. Recommendation

**GO / NO-GO / PIVOT**

**Next Steps:**
1. Action item 1
2. Action item 2
3. Action item 3

---

## 🎯 How to Use This Framework

### Step 1: Document Gathering
Collect all available information about the project:
- Feature lists
- Technical specifications
- Competitor research
- Market data

### Step 2: Run Evaluation
Use the evaluation prompt to create an **Objective Review Analysis.md** for each project candidate.

### Step 3: Score & Compare
Fill out the grading criteria for all projects and calculate weighted scores.

### Step 4: Prioritize
Rank projects by total score and priority classification.

### Step 5: Execute
Focus resources on **CRITICAL** and **HIGH** priority projects first.

---

## 📁 Repository Structure

```
MVP-Grader/
├── README.md                          # This file
├── criteria thus far to ask           # Core evaluation prompt
├── projects/                          # Individual project evaluations
│   ├── project-name-1/
│   │   ├── Objective Review Analysis.md
│   │   ├── scoring-matrix.md
│   │   └── assets/
│   ├── project-name-2/
│   │   └── ...
│   └── ...
├── templates/                         # Reusable templates
│   ├── analysis-template.md
│   └── scoring-sheet.md
└── rankings/                          # Project comparisons
    └── current-rankings.md
```

---

## 🏅 Success Metrics

A project is worth pursuing if:
- ✅ Overall score ≥ 7.0
- ✅ ARR potential ≥ $100K in Year 2 (if perfected)
- ✅ Time to MVP ≤ 3 months
- ✅ Clear path to fixing all critical flaws
- ✅ Passionate founder/team fit with problem space

---

## 🔄 Continuous Improvement

This framework should evolve as you:
- Gather data from launched projects
- Refine scoring weights based on outcomes
- Add new evaluation criteria
- Update market research methodology

**Last Updated**: January 12, 2026

---

## 📚 Examples

See the `projects/` directory for real-world evaluations including:
- VibeDev (Dream Game Co-Pilot)
- SyncFit (Fitness App)
- Us App (Social Connection)

Each demonstrates the full framework in action.

---

## 🤝 Contributing

This is a living framework. As you evaluate more projects:
1. Refine scoring criteria
2. Update weights based on learnings
3. Add case studies
4. Document patterns of success/failure

---

**Built to make data-driven decisions about which ideas deserve your time.**
