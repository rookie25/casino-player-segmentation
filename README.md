# Casino Player Segmentation Analysis

A data-driven player segmentation project using RFM (Recency, Frequency, Monetary) analysis and K-means clustering to identify distinct player groups and develop targeted marketing strategies for casino operators.

---

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Results & Deliverables](#results--deliverables)
- [Business Recommendations](#business-recommendations)
- [Future Enhancements](#future-enhancements)

---

## 🎯 Project Overview

This project analyzes **4,222 online casino players** over a 2-year period to segment them into meaningful behavioral groups. By applying unsupervised machine learning techniques and business analytics, the project identifies 5 distinct player segments and provides actionable marketing strategies tailored to each group.

**Key Objective:** Maximize player lifetime value (LTV) and marketing ROI through data-driven segmentation and personalized engagement strategies.

---

## 💼 Business Problem

Casino operators face several challenges:
- **Resource Allocation:** Where should marketing budgets be invested for maximum ROI?
- **Player Retention:** How to identify and retain high-value players?
- **Churn Prevention:** Which players are at risk of becoming inactive?
- **Conversion Optimization:** How to convert casual players into regulars?

**Solution:** Segment players based on their betting behavior and develop targeted strategies for each segment.

---

## 📊 Dataset

**Source:** Harvard Dataverse - Online Casino Dataset  
**Size:** 4,222 players  
**Time Period:** February 2005 - February 2007 (2 years)  
**Features:** 20 variables including:

### Key Variables:
- **Pclstdate:** Last active date (Recency indicator)
- **Pcsumday:** Total active days (Frequency indicator)
- **Pcsumstk:** Total stakes wagered (Monetary indicator)
- **Pcsumbet:** Total number of bets placed
- **Pcnet:** Net winnings/losses
- **Pcab:** Average bet size

### Data Quality:
- ✅ No missing values
- ✅ Complete records for all 4,222 players
- ✅ Clean dataset ready for analysis

---

## 🔬 Methodology

### Phase 1: Data Exploration & Cleaning
1. **Data Loading:** Imported raw data with proper encoding (ISO-8859-1)
2. **Exploratory Analysis:** 
   - Examined data distributions
   - Identified outliers (VIP high rollers)
   - Analyzed betting patterns
3. **Data Validation:** Verified data quality and completeness

### Phase 2: RFM Analysis
**RFM Framework:**
- **R (Recency):** Days since last bet (0-752 days)
- **F (Frequency):** Total active days (4-524 days)
- **M (Monetary):** Total stakes wagered ($0.12 - $3.4M)

**Normalization:**
- Scaled all RFM scores to 0-100 range
- Inverted Recency (higher score = more recent activity)
- Ensured equal weighting in clustering algorithm

### Phase 3: K-Means Clustering
1. **Elbow Method:** Tested K=2 through K=8 clusters
2. **Optimal K Selection:** Identified K=5 as optimal
3. **Cluster Assignment:** Segmented all 4,222 players
4. **Validation:** Analyzed cluster characteristics and separation

### Phase 4: Business Strategy Development
1. **Segment Profiling:** Analyzed behavioral patterns per segment
2. **Segment Naming:** Assigned descriptive business names
3. **Strategy Development:** Created targeted marketing approaches
4. **Budget Allocation:** Distributed $1M annual budget across segments
5. **ROI Projection:** Calculated expected returns (3x overall ROI)
6. **Implementation Roadmap:** Developed 90-day action plan

---

## 🎯 Key Findings

### 5 Player Segments Identified:

#### 1. VIP High Rollers ⭐ (Critical Segment)
- **Size:** 123 players (2.9%)
- **Average LTV:** $299,979
- **Characteristics:** Very recent activity, high frequency, high spending
- **RFM Scores:** R=94.5, F=36.3, M=8.7
- **Revenue Contribution:** Disproportionately high (premium segment)
- **Strategy:** Maximum investment - VIP retention program

#### 2. New Casual Players (Growth Opportunity)
- **Size:** 1,298 players (30.7%) - Largest segment
- **Average LTV:** $24,906
- **Characteristics:** Very recent activity, low frequency, low spending
- **RFM Scores:** R=92.7, F=5.0, M=0.7
- **Strategy:** Conversion focus - Onboarding and engagement programs

#### 3. Recent Low Spenders
- **Size:** 960 players (22.7%)
- **Average LTV:** $19,848
- **Characteristics:** Recent activity, very low frequency, minimal spending
- **RFM Scores:** R=68.0, F=3.7, M=0.6
- **Strategy:** Engagement boost - Frequency-building campaigns

#### 4. Inactive Casual
- **Size:** 893 players (21.2%)
- **Average LTV:** $17,747
- **Characteristics:** Medium recency, low frequency, low spending
- **RFM Scores:** R=39.6, F=2.9, M=0.5
- **Strategy:** Win-back campaigns with targeted offers

#### 5. Low Value Dormant
- **Size:** 948 players (22.5%)
- **Average LTV:** $11,170
- **Characteristics:** No recent activity, minimal frequency, low spending
- **RFM Scores:** R=9.8, F=1.9, M=0.3
- **Strategy:** Minimal investment - Automated re-engagement only

---

## 🛠️ Technologies Used

### Programming & Libraries:
```python
- Python 3.11
- pandas (Data manipulation)
- numpy (Numerical computing)
- scikit-learn (Machine learning - K-means clustering)
- matplotlib (Data visualization)
- seaborn (Statistical visualizations)
```

### Analysis Techniques:
- RFM Analysis
- K-Means Clustering
- Elbow Method (Cluster optimization)
- Data normalization (MinMaxScaler)
- Statistical profiling

---

## 📁 Project Structure

```
Casino-Player-Segmentation/
│
├── data/
│   ├── raw/
│   │   ├── AnalyticDataSet_VirtualCasinoTXT.txt    # Original dataset
│   │   └── AnalyticDataSet_VirtualCasinoTXT.csv    # Converted CSV
│   └── processed/
│       ├── casino_data_cleaned.csv                 # Cleaned data
│       ├── casino_data_segmented.csv               # With RFM scores
│       ├── casino_data_final_with_strategies.csv   # Complete analysis
│       └── segment_strategy_summary.csv            # Executive summary
│
├── code/
│   └── Analysis.ipynb                              # Main analysis notebook
│
├── reports/
│   ├── initial_exploration.png                     # Data distribution charts
│   ├── elbow_method.png                           # Cluster optimization
│   └── segment_analysis.png                        # Comprehensive visualizations
│
└── README.md                                        # Project documentation
```

---

## 🚀 Installation & Setup

### Prerequisites:
```bash
Python 3.8+
Jupyter Notebook
```

### Step 1: Clone Repository
```bash
git clone https://github.com/yourusername/casino-player-segmentation.git
cd casino-player-segmentation
```

### Step 2: Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Step 3: Run Analysis
```bash
jupyter notebook code/Analysis.ipynb
```

### Step 4: Execute Cells
Run all cells sequentially to reproduce the analysis.

---

## 📈 Results & Deliverables

### Quantitative Results:
- **Segments Created:** 5 distinct player groups
- **Players Analyzed:** 4,222
- **Data Coverage:** 2-year period (730 days)
- **Revenue Range:** $0.12 to $3,439,061 per player
- **Frequency Range:** 4 to 524 active days
- **Recency Range:** 0 to 752 days since last bet

### Visualizations Created:
1. **Data Distribution Charts:** Histograms and boxplots of key metrics
2. **Elbow Method Plot:** Optimal cluster selection visualization
3. **Segment Analysis Dashboard:** 6-panel comprehensive view
   - RFM scores by segment (bar chart)
   - Player distribution (pie chart)
   - Revenue contribution (pie chart)
   - Average player value (horizontal bar)
   - Recency vs Frequency scatter plot
   - Segment size vs revenue comparison

### Strategic Deliverables:
- ✅ Segment profiles with clear business names
- ✅ Targeted marketing strategies (5 detailed plans)
- ✅ Budget allocation recommendations ($1M distribution)
- ✅ ROI projections (3x overall return expected)
- ✅ 90-day implementation roadmap
- ✅ Success metrics and KPIs

---

## 💡 Business Recommendations

### Marketing Budget Allocation (Annual $1M):

| Segment | Budget | % | Per Player | Expected ROI | Strategy Focus |
|---------|--------|---|------------|--------------|----------------|
| VIP High Rollers | $400,000 | 40% | $3,252 | 5x | Retention & VIP experience |
| New Casual Players | $250,000 | 25% | $193 | 3x | Conversion & onboarding |
| Recent Low Spenders | $200,000 | 20% | $208 | 2.5x | Engagement & frequency |
| Inactive Casual | $100,000 | 10% | $112 | 1.5x | Win-back campaigns |
| Low Value Dormant | $50,000 | 5% | $53 | 1.2x | Automated re-engagement |

### Expected Overall ROI:
- **Total Investment:** $1,000,000
- **Expected Return:** $3,000,000
- **Net Profit:** $2,000,000
- **ROI:** 200% (3x return)

### 90-Day Implementation Plan:

#### Phase 1 (Days 1-30): Foundation & Quick Wins
- Launch VIP program with dedicated account managers
- Set up CRM segmentation and automation
- Deploy initial engagement campaigns
- **Quick Win:** Dormant player reactivation (5-10% expected)

#### Phase 2 (Days 31-60): Optimization & Scale
- Roll out frequency-building programs
- Launch win-back campaigns for inactive players
- Identify "rising stars" for VIP pipeline
- Analyze first 45 days and optimize budget

#### Phase 3 (Days 61-90): Advanced Tactics
- Implement churn prediction model
- Launch cross-segment referral programs
- Expand automation (80% of campaigns)
- Conduct quarterly business review

### Success Metrics (KPIs):
- **VIP Retention Rate:** Target 95%+ (vs baseline)
- **New Player Conversion:** Target 20% to regular players
- **Marketing ROI:** Target 3x return on investment
- **Revenue Growth:** Target 15-20% increase
- **Player LTV Increase:** Target 25% improvement

---

## 🔮 Future Enhancements

### Potential Extensions:

1. **Predictive Analytics:**
   - Churn prediction models
   - Lifetime value forecasting
   - Next-best-action recommendations

2. **Advanced Segmentation:**
   - Game preference clustering
   - Time-based behavior analysis
   - Cohort analysis (acquisition cohorts)

3. **Real-Time Monitoring:**
   - Live dashboard for segment tracking
   - Automated alerts for at-risk VIPs
   - Dynamic segment assignment

4. **A/B Testing Framework:**
   - Test marketing messages by segment
   - Optimize bonus structures
   - Personalization experiments

5. **Integration:**
   - CRM system integration
   - Marketing automation platform
   - Real-time recommendation engine

---

## 📊 Sample Insights

### Key Business Insights:

**1. The Pareto Principle in Action:**
- Top 2.9% of players (VIP High Rollers) drive disproportionate revenue
- Critical to retain these 123 players at all costs
- VIP churn has massive revenue impact

**2. Growth Opportunity:**
- 30.7% of players are new/casual (1,298 players)
- Currently low value but high conversion potential
- Proper nurturing could significantly increase LTV

**3. Resource Optimization:**
- 43.7% of players (dormant + inactive casual) contribute minimal value
- Should receive minimal marketing investment
- Focus resources on high-potential segments

**4. Personalization is Key:**
- One-size-fits-all approach wastes resources
- Each segment requires different messaging and offers
- Targeted strategies yield 3x better ROI

---

## 👥 Author

**Visha**  
Data Analyst | Business Intelligence | Marketing Analytics

---

## 📝 License

This project is available for educational and portfolio purposes.

---

## 🙏 Acknowledgments

- Dataset: Harvard Dataverse - Online Casino Player Behavior
- Methodology: RFM Analysis framework adapted for gaming industry
- Inspiration: Customer segmentation best practices from e-commerce and gaming sectors

---

## 📧 Contact

For questions, suggestions, or collaboration opportunities:
- Email: [your.email@example.com]
- LinkedIn: [Your LinkedIn Profile]
- GitHub: [Your GitHub Profile]

---

**Project Status:** ✅ Complete & Ready for Presentation  
**Last Updated:** January 2025  
**Version:** 1.0

---

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- **Data Analysis:** Exploratory analysis, statistical profiling
- **Machine Learning:** K-means clustering, model optimization
- **Business Strategy:** RFM analysis, segmentation strategy
- **Data Visualization:** Creating actionable insights from data
- **Technical Writing:** Documenting analysis for stakeholders
- **ROI Analysis:** Quantifying business impact of recommendations

---

*This README provides a comprehensive overview of the Casino Player Segmentation project. For detailed technical implementation, refer to the Jupyter notebook in the code/ directory.*
