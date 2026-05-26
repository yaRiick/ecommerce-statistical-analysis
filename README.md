# E-commerce Data Analysis: A/B Testing & Traffic Performance

## 🎯 Project Overview
This project focuses on analyzing user purchasing behavior and evaluating the effectiveness of marketing acquisition channels for an e-commerce platform. By applying statistical hypothesis testing, the analysis uncovers actionable business insights regarding user registration value, Average Order Value (AOV), and traffic quality to optimize marketing spend and improve checkout conversion funnels.

## 💡 Key Business Insights
* **The "Guest" Paradox (Registration vs. Revenue):** Contrary to traditional marketing assumptions, unregistered (guest) users generate the absolute majority of total daily revenue. Furthermore, they exhibit a **statistically significant higher Average Order Value (AOV)** ($953 vs. $891, $p = 0.034$). *Business Recommendation: Avoid forcing registration at checkout, especially for high-ticket items, to prevent friction and revenue drop.*
* **Traffic Channel Purchasing Power:** While `Organic Search` and `Paid Search` drive over 60% of all successful sessions, a Kruskal-Wallis H-test ($p < 0.05$) confirmed that user purchasing power varies significantly across channels. Not all traffic volumes translate equally into high-value baskets.
* **Geographic SEO Variations:** A Chi-Square Test of Independence proved a statistically significant difference in the share of organic traffic between Europe and the Americas, indicating unequal SEO penetration and brand visibility across continents.
* **Traffic & Revenue Synchronization:** Time-series analysis utilizing dual-axis visualizations and Spearman rank correlation dynamically mapped how daily traffic spikes directly correlate with actual revenue generation across top product categories.

## 🛠 Tech Stack & Statistical Methods
* **Data Extraction & Architecture:** SQL (Google BigQuery) utilizing complex `LEFT JOIN` operations to preserve and analyze guest (unregistered) transaction rows.
* **Data Manipulation:** Python, Pandas, NumPy.
* **Statistical Hypothesis Testing (`scipy.stats`):**
  * **Normality Assessment:** D'Agostino-Pearson omnibus test & Q-Q Plots.
  * **Non-Parametric Analysis:** Mann-Whitney U Test (for 2 groups), Kruskal-Wallis H-Test (for 5 channels).
  * **Categorical Data & Proportions:** Chi-Square Test of Independence ($\chi^2$).
  * **Correlation Analysis:** Spearman's Rank Correlation with automated $p$-value calculation and significance matrix visualization.
* **Data Visualization:** Matplotlib, Seaborn (with custom significance annotation logic).

## 📂 Repository Structure
* `Yaroslav_Matvienko_Ecommerce_Statistical_Analysis.ipynb` — The core Jupyter Notebook containing full data pipeline: authentication, SQL query, data cleaning, EDA, statistical testing, and visualizations.
* `README.md` — Project description and executive summary of key insights.

## 🚀 How to Run the Project
1. Clone this repository:
[https://github.com/yaRiick/ecommerce-statistical-analysis.git](https://github.com/yaRiick/ecommerce-statistical-analysis.git)
2. Open the .ipynb file in Google Colab or Jupyter Notebook.

3. Ensure you have access to the Google Cloud BigQuery dataset data-analytics-mate.DA or replace the client initialization block with your own data source.

4. Install required libraries:
pip install pandas numpy matplotlib seaborn scipy

5. Run all cells sequentially to execute data extraction, mathematical modeling, and visualization generation.

Author: Yaroslav Matvienko

Feel free to connect or review my other data analytics projects!
