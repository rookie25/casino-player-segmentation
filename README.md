# Casino Player Segmentation Analysis

**Data-driven player segmentation using RFM analysis and K-means clustering to maximize marketing ROI and player lifetime value**

---

## 📊 Overview

This project segments **4,222 online casino players** into 5 distinct behavioral groups using RFM (Recency, Frequency, Monetary) analysis and unsupervised machine learning. The segmentation enables targeted marketing strategies, optimal budget allocation, and identifies high-value players requiring retention focus. The analysis delivers actionable business recommendations with a projected **3x marketing ROI**.

---

## 💼 Business Problem

Casino operators struggle with:
- **Inefficient marketing spend** - treating all players the same
- **VIP churn risk** - losing high-value players to competitors  
- **Low conversion rates** - failing to nurture casual players into regulars
- **Resource waste** - investing in dormant, low-value segments

**Solution:** Segment players by behavior patterns and develop targeted strategies for each group, maximizing ROI and player lifetime value.

---

## 📁 Dataset

**Source:** Harvard Dataverse - Online Casino Dataset  
**Scope:** 4,222 players tracked over 2 years (Feb 2005 - Feb 2007)  
**Variables:** 20 features including betting patterns, frequency, and monetary value

**Key Metrics:**
- **Recency:** Days since last bet (0-752 days)
- **Frequency:** Total active days (4-524 days)  
- **Monetary:** Total stakes wagered ($0.12 - $3.4M)

---

## 🔬 Methodology

**Phase 1: RFM Analysis**
- Calculated Recency, Frequency, Monetary scores for each player
- Normalized all scores to 0-100 scale for equal weighting

**Phase 2: K-Means Clustering**
- Applied Elbow Method to determine optimal clusters
- Selected K=5 as optimal segmentation
- Assigned all 4,222 players to segments

**Phase 3: Business Strategy**
- Profiled each segment behaviorally
- Developed targeted marketing strategies
- Allocated $1M annual budget across segments
- Projected ROI and created 90-day implementation roadmap

---

## 🎯 Key Findings: 5 Player Segments

### 1. **VIP High Rollers** ⭐ (Critical Priority)
- **Size:** 123 players (2.9%)
- **Avg LTV:** $299,979
- **Behavior:** Very recent activity, high frequency, massive spending
- **Strategy:** Maximum investment - VIP retention program, dedicated account managers, exclusive perks
- **Budget:** $400,000 (40%) | Expected ROI: 5x

### 2. **New Casual Players** (Growth Opportunity)  
- **Size:** 1,298 players (30.7%) - *Largest segment*
- **Avg LTV:** $24,906
- **Behavior:** Very recent activity, low frequency, minimal spending
- **Strategy:** Conversion focus - onboarding programs, deposit incentives, frequency-building campaigns
- **Budget:** $250,000 (25%) | Expected ROI: 3x

### 3. **Recent Low Spenders**
- **Size:** 960 players (22.7%)
- **Avg LTV:** $19,848  
- **Behavior:** Recent activity, very low frequency, minimal value
- **Strategy:** Engagement boost - loyalty programs, gamification, weekly promotions
- **Budget:** $200,000 (20%) | Expected ROI: 2.5x

### 4. **Inactive Casual**
- **Size:** 893 players (21.2%)
- **Avg LTV:** $17,747
- **Behavior:** Moderate recency, low frequency, low spending
- **Strategy:** Win-back campaigns - targeted offers, surveys, limited-time bonuses
- **Budget:** $100,000 (10%) | Expected ROI: 1.5x

### 5. **Low Value Dormant**  
- **Size:** 948 players (22.5%)
- **Avg LTV:** $11,170
- **Behavior:** No recent activity, minimal engagement, low value
- **Strategy:** Minimal investment - automated re-engagement emails only
- **Budget:** $50,000 (5%) | Expected ROI: 1.2x

---

## 🛠️ Technologies Used

**Python** | **pandas** | **NumPy** | **scikit-learn** (K-Means) | **matplotlib** | **seaborn** | **Jupyter Notebook**

---

## 📈 Results & Business Impact

### Deliverables Created:
✅ 5 distinct player segments with clear behavioral profiles  
✅ Segment-specific marketing strategies with detailed tactics  
✅ $1M annual budget allocation optimized by segment  
✅ 3x overall marketing ROI projection  
✅ 90-day implementation roadmap with success metrics  
✅ Comprehensive visualizations (distribution charts, segment analysis, elbow method)

### Budget Allocation & Expected ROI:

| Segment | Players | % Base | Budget | % Budget | Per Player | Expected ROI | Net Profit |
|---------|---------|--------|--------|----------|------------|--------------|------------|
| **VIP High Rollers** | 123 | 2.9% | $400,000 | 40% | $3,252 | **5.0x** | $1,600,000 |
| **New Casual Players** | 1,298 | 30.7% | $250,000 | 25% | $193 | **3.0x** | $500,000 |
| **Recent Low Spenders** | 960 | 22.7% | $200,000 | 20% | $208 | **2.5x** | $300,000 |
| **Inactive Casual** | 893 | 21.2% | $100,000 | 10% | $112 | **1.5x** | $50,000 |
| **Low Value Dormant** | 948 | 22.5% | $50,000 | 5% | $53 | **1.2x** | $10,000 |
| **TOTAL** | **4,222** | **100%** | **$1,000,000** | **100%** | **$237** | **3.0x** | **$2,000,000** |

### Key Business Insights:

**1. The Pareto Principle in Action**  
- Only 2.9% of players (123 VIPs) drive disproportionate revenue
- VIP retention is mission-critical - even 1 VIP lost = massive revenue impact
- Justifies 40% budget allocation to <3% of player base

**2. Massive Growth Opportunity**  
- 30.7% of players are new/casual with low current LTV
- Proper nurturing and conversion programs could significantly increase revenue
- 15-25% conversion rate would add substantial value

**3. Resource Optimization**  
- 43.7% of players (dormant + inactive) contribute minimal value
- Should receive only 15% of budget (automated campaigns)
- Frees resources for high-potential segments

### 90-Day Implementation Roadmap:

**Phase 1 (Days 1-30): Foundation**
- Launch VIP program with dedicated account managers
- Set up CRM segmentation and marketing automation
- Deploy initial campaigns and quick wins

**Phase 2 (Days 31-60): Optimization**  
- Roll out engagement programs for all segments
- Analyze performance and optimize budget allocation
- Identify rising stars for VIP pipeline

**Phase 3 (Days 61-90): Scale**
- Implement predictive models and automation
- Launch referral programs and social features
- Conduct quarterly business review

**Success Metrics:**
- VIP Retention: 95%+ target
- New Player Conversion: 20% to regular players
- Marketing ROI: 3x overall return
- Revenue Growth: 15-20% increase
- Player LTV: 25% improvement

---

## 📊 Visualizations

The project includes comprehensive visualizations:
- **Data distribution analysis** - Histograms and boxplots showing player behavior patterns
- **Elbow method chart** - Cluster optimization showing K=5 as optimal
- **Segment analysis dashboard** - 6-panel visualization including:
  - RFM scores comparison across segments
  - Player distribution pie chart
  - Revenue contribution breakdown
  - Average player value by segment
  - Recency vs Frequency scatter plot with segment colors
  - Segment size vs revenue comparison

All visualizations saved in `/reports/` directory.

---

## 🎯 Project Impact

This analysis transforms raw casino data into actionable business strategy:

✅ **Identifies high-value players** requiring retention focus (VIP segment)  
✅ **Optimizes marketing spend** with data-driven budget allocation  
✅ **Prevents revenue loss** through VIP churn risk identification  
✅ **Maximizes conversion** of casual players through targeted nurturing  
✅ **Eliminates waste** by minimizing investment in low-value segments  
✅ **Projects 200% ROI** ($2M net profit on $1M investment)  

**Business Value:** Provides casino operators with a clear, actionable framework to maximize player lifetime value and marketing efficiency through behavioral segmentation.

---

## 📂 Repository Structure

```
Casino-Player-Segmentation/
├── data/
│   ├── raw/                    # Original dataset
│   └── processed/              # Cleaned and segmented data
├── code/
│   └── Analysis.ipynb          # Complete analysis notebook
├── reports/
│   └── *.png                   # Visualizations
└── README.md                   # This file
```

---
## 📊 Power BI dashboard


The dashboard includes:
- KPI cards showing total players, revenue, and average LTV
- Player distribution by segment
- Revenue analysis by segment
- RFM scores with color-coded performance indicators
- Visual representation of the VIP paradox

---

*For detailed technical implementation and code, see Analysis.ipynb in the code/ directory.*
