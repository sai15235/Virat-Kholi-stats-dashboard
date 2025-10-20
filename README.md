# 🏏 Virat Kohli Career Performance Dashboard | Power BI

### 📊 Interactive Cricket Analytics Dashboard built in Power BI

This project visualizes **Virat Kohli’s batting performance** across his international matches.  
It highlights insights such as his **total runs, consistency, top scores, and performance trends** against various opponents and venues.

---

## 📁 Dataset Overview

**File:** `Source.csv`  

| Column | Description |
|:--------|:-------------|
| `index` | Match sequence number |
| `runs` | Runs scored in the match |
| `opponent` | Opponent team |
| `ground` | Stadium / venue |
| `date` | Date of the match |
| `match` | Match format (e.g., ODI) |
| `Match_No` | Sequential match number |
| `total` | Running total of runs |

---

## ⚙️ Power BI DAX Measures

| Measure Name | DAX Formula | Purpose |
|:--------------|:-------------|:---------|
| **Total Runs** | `SUM(Source[runs])` | Total runs scored by Virat |
| **Total Matches** | `COUNTROWS(Source)` | Number of matches played |
| **Average Runs** | `DIVIDE(SUM(Source[runs]), COUNTROWS(Source))` | Average runs per match |
| **Highest Score** | `MAX(Source[runs])` | Highest individual score |
| **Cumulative Runs** | *(below)* | Running total of runs |
```DAX
Cumulative Runs =
CALCULATE(
    SUM(Source[runs]),
    FILTER(
        ALLSELECTED(Source),
        Source[Match_No] <= MAX(Source[Match_No])
    )
)


📈 Key Insights

⚡ Peak Consistency: Post-2012, Kohli maintained an average of 50+ across formats.

🏟️ Favorite Opponents: Exceptional records against Sri Lanka and Australia.

🌏 Strong Grounds: Notable performances in Colombo, Adelaide, and Kolkata.

📅 Performance Trend: Clear upward trajectory in average runs per match over time.

🛠️ Tools & Technologies

Power BI Desktop – Data Modeling & Visualization

DAX – Custom Measures for Insights

Power Query (M) – Data Transformation

Author

👤 Sai Kiran Reddy
📧 saikiranr717@gmail.com

🔗 LinkedIn :https://www.linkedin.com/in/saikiran-reddy-2b6842298
