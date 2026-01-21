# Video Game Sales - Exploratory Data Analysis (EDA)

## Project Overview
This project involves a deep dive into the Video Game Sales dataset to uncover trends, patterns, and relationships between game features and global market success. The goal was to move beyond raw numbers and visualize the underlying behavior of the gaming industry.

## Dataset Description
- *Source:* VGSales.csv
- *Size:* 16,598 records
- *Key Features:* Genre, Platform, Year, and Sales across four regions (NA, EU, JP, Other).

## Analysis & Visualizations

### 1. Sales Distribution (Histograms)
- *Method:* Plotted a histogram with a Kernel Density Estimate (KDE) for `Global_Sales`.
- *Finding:* The data is highly right-skewed. The vast majority of games sell less than 1 million copies, while a few "megahits" create a long tail of extreme values.

### 2. Market Saturation (Count Plots)
- *Method:* Categorical count plot of the `Genre` column.
- *Finding:* **Action** is the most frequently produced genre, followed by **Sports**. This highlights where the highest volume of development competition exists.

### 3. Outlier Detection (Box Plots)
- *Method:* Box plots comparing `Global_Sales` across different `Genres`.
- *Finding:* While "Action" has the most titles, genres like **Platform** and **Shooter** often show higher median sales and significant "outlier" hits (games that perform exceptionally better than the average).



<img width="562" height="526" alt="image" src="https://github.com/user-attachments/assets/3b7c4212-797e-4a32-988e-d042e7873b5e" />



### 4. Regional Correlation (Heatmap)
- *Method:* Correlation matrix visualized via a heatmap.
- *Finding:* There is a near-perfect correlation (0.94) between **North American (NA) sales** and **Global sales**. Europe (EU) follows closely at 0.90. This suggests that success in Western markets is the primary driver of global ranking.



## Key Insights for Prediction
- **Regional Weight:** If building a prediction model, `NA_Sales` and `EU_Sales` are the most important features.
- **Localized Markets:** Japan (JP) shows a lower correlation with Western markets, indicating that Japanese consumer preferences are distinct and may require separate modeling.
- **Targeting Success:** Because the data is so skewed, predicting an "average" game's success is difficult; models should instead focus on identifying the characteristics of "outlier" hits.

## Tools Used
- **Python (Pandas, NumPy)**
- **Visualization:** Matplotlib, Seaborn
