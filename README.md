# Capstone
1. Executive Summary
2. Objectives
3. Causal Question
4. Data
5. Variables
6. This repository

## 1. Executive Summary
Although much research has been done to predict the effects and outcomes of dismissal, only some researchers have tried to quantify the causes behind CEO dismissal. Previous literature suggests that firm performance, economic trends, company size, industry type, stock price, and public sentiment all have some impact on involuntary CEO dismissal. However, these variables' effects on CEO dismissal are often understudied and data is unavailable. Having noticed this gap in the modern management consulting and finance landscape, I built on the Gentry et al. 2021 CEO Dismissal dataset to compile and gather financial information for the S&P 500 companies. Thus, this project aims to contribute to understanding factors leading to CEO dismissal, utilizing a custom panel dataset.
#### 2. Objectives: 
The primary goal of this project is to build and publish a dataset combining quarterly financial information, CEO dismissal outcomes, industry data, and economic trends for S&P 500 companies. This facilitates observational studies to explore factors contributing to involuntary CEO dismissal. The secondary objective involves conceptualizing CEO dismissal under a broader economic analysis, defining financial indicators, and showcasing a successful observational panel data study. The reader of this study should expect to develop a solid understanding of a causal study, the steps to design it, the difference between causation and correlation, and how to interpret logistic regression results (Cunningham, 2021). 
#### 3. Causal Question: 
What is the effect of earnings per share on involuntary CEO dismissal in the given S&P 500 company per quarter?
### 5. Data 
This research develops a data set that includes the information from Gentry et al. merged with the financial performance metrics covering S&P 500 companies from 2008 until the third quarter of 2023 and the FED treasury yield and recession data set to account for macroeconomic cycles and fluctuations. Thus, this research combines these three data sets, resulting in a longitudinal panel data set that covers the available financial metrics within the S&P 500 companies and involuntary CEO dismissal over the past decade. A descriptive statistics table of variables in the data set is provided in the research PDF file in Table 1 under the Products/ folder in this repository.
### 4. Variables

| Treatment Variable | Outcome variable |
| ------------- | ------------- |
| 1 = Quarterly EPS < Previous Year's Yearly Moving Average  | 1 = Involuntary CEO Dismissal  |
| 0 = Quarterly EPS < Previous Year's Yearly Moving Average  | 0 = No Dismissal  |

|  | Confounding Variables |
| ------------- | ------------- |
|  1. | Net Income  |
|  2. | Quarterly Adjusted Close Price |
|  3. | Operating Income | 
|  4. | Quarterly Interest Rate |
|  5. | Recession Year |
1. Net income: discrete variable measuring what a business makes after taxes, deductions, and other expenses are taken out.
2. Quarterly Adjusted Close Price: discrete variable factoring in anything affecting the stock price after the market closes. The quarterly adjusted close price is the moving average of the daily adjusted close price over the fiscal quarter. Although the price is a continuous variable, the variable is discrete in the sense of a data point (price has a decimal point. See Nasdaq reference). 
3. Operating income: discrete variable measuring the amount of revenue left after deducting the operational direct and indirect costs from sales revenue. 
4. Quarterly Interest Rate: discrete variable measuring the amount set by the FED that banks charge borrowers and is a percentage of the principal. It is also the amount earned from deposit accounts. Interest rate is often used as a proxy for the health/state of the economy since it reflects the potential effects of inflation, the level of risk in an investment, and the real value of the investment.
5. Recession Year: Dummy binary variable accounting for a special year taking the value 1 when the recession happened in the US and taking the value 0 when not. 

### 6. This Repository
Navigating this repository is quite easy since it is divided into 4 main folders. Folders 2-4 are the most relevant while folder 1 contains archived code snippets. The code folder contains two subfolders clean and raw. Subfolder "Clean" contains clean and polished code while "Raw" contains unpolished and general code, but it is still relevant since some variables in the "Clean" folder are originally created from notebooks within the "Raw" folder. The "Data" folder contains all the relevant datasets and the "Products" folder contains the final write-up, executive summary, and all the relevant data sets. 
