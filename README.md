# ds_BVN-Sravan-Kumar

#what we have to do:
The assignment aims to analyze how Bitcoin market sentiment affects trader performance using two datasets,  one containing daily sentiment labels and the other with historical trading data. The objective is to explore correlations, perform statistical and pattern analysis, and derive insights that can guide smarter and emotion-aware trading strategies.

##  What We Have Done (Steps Breakdown)

###  1. Data Cleaning and Preparation
- Cleaned column names and formats
- Converted timestamps to standard datetime
- Extracted date fields
- Merged both datasets on common `date` field

###  2. Exploratory Data Analysis (EDA)
- Trader activity over time
- Distribution of PnL across sentiment categories
- Trade volume vs sentiment
- Number of trades by sentiment

###  3. Statistical Analysis
- **ANOVA on PnL:** Significant differences in average PnL between different sentiment groups
- **ANOVA on Trade Volume (`size_usd`)**: Tested impact of sentiment on trading volume
- Tested whether behavior significantly changes during extreme emotions (like *Extreme Fear*)

###  4. Pattern Recognition / ML (Optional Step)
- Built a Logistic Regression model to predict trade direction (`long` or `short`) using:
  - sentiment classification
  - leverage
  - size in USD
- Achieved decent classification performance, showing sentiment’s impact on trader actions


##  Final Insights & Strategy Recommendations

###  Key Insights
- **Trader PnL is influenced by sentiment:**  
  During *Extreme Fear*, traders showed relatively lower PnL than during *Neutral* or *Greed* states.
  
- **Volume spikes during emotional extremes:**  
  Trade volumes were unusually high during *Extreme Greed* and *Extreme Fear*, suggesting panic buying/selling.

- **Neutral sentiment days show better discipline:**  
  Consistent performance and average PnL were better during *Neutral* sentiment phases.

- **Sentiment correlates with trade direction:**  
  Most `long` positions were taken during *Greed*, while more `shorts` occurred during *Fear* or *Extreme Fear*.

###  Recommendations
- **Avoid trading emotionally:** During *Extreme Fear* or *Greed*, traders tend to make irrational decisions.
- **Use sentiment as a signal, not a driver:** While sentiment informs volatility, it's better to use it as a cautionary signal, not a standalone strategy.
- **Monitor volume during sentiment shifts:** Unusual volume activity on sentiment transitions can be a useful market signal.
- **Consider ML-based risk assessment:** Using market sentiment in predictive models could help control risk and identify trade direction.

---

##  CSV Files

Due to GitHub's 25MB file upload limit, you can download the full data files from Google Drive:

- [Download historical_df.csv]([https://drive.google.com/file/d/YOUR_HISTORICAL_FILE_ID/view?usp=sharing](https://drive.google.com/file/d/1VlepTJe4OJCjXiXCO8pyQepRE7RyXyhO/view?usp=drive_link))
- [Download fear_greed_df.csv]([https://drive.google.com/file/d/YOUR_SENTIMENT_FILE_ID/view?usp=sharing](https://drive.google.com/file/d/1gFGkgLtcPe0Kkq-oZvLG_s_u5117OeWX/view?usp=drive_link))
- [Download merged_df.csv]([https://drive.google.com/file/d/YOUR_MERGED_FILE_ID/view?usp=sharing](https://drive.google.com/file/d/1eNoIeXfutLXWED_yvy5iUHGXlXn--tDo/view?usp=drive_link))
