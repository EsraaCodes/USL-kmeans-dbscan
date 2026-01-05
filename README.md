# Fund Allocation for Countries in Need

## Project Overview
This project focuses on **strategic allocation of funds** by HELP International, an NGO committed to fighting poverty and providing relief to countries in need during disasters and natural calamities. Using **unsupervised learning**, countries are clustered based on socio-economic and health indicators to identify those that require immediate assistance.  

The project demonstrates how **data-driven decisions** can optimize humanitarian aid distribution.

---

## Aim
To cluster countries based on numerical features such as child mortality, health spending, trade, income, GDP, fertility, and life expectancy to prioritize fund allocation.

---

## Dataset
The dataset contains information for **167 countries** and includes the following attributes:

| Column       | Description |
|--------------|------------|
| `country`    | Name of the country |
| `child_mort` | Deaths of children under 5 per 1000 live births |
| `exports`    | Exports of goods and services (% of GDP per capita) |
| `health`     | Total health spending (% of GDP per capita) |
| `imports`    | Imports of goods and services (% of GDP per capita) |
| `income`     | Net income per person |
| `inflation`  | Annual GDP growth rate (%) |
| `life_expec` | Life expectancy at birth |
| `total_fer`  | Total fertility rate |
| `gdpp`       | GDP per capita |

Dataset source: [Kaggle](https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data)

---

## Methodology

1. **Exploratory Data Analysis (EDA)**  
   - Distribution and summary statistics for all numerical features  
   - Identification of economically backward countries based on features like high child mortality, low income, and high fertility  

2. **Feature Engineering**  
   - Grouped features into three categories: `Health`, `Trade`, `Finance`  
   - Normalized features for clustering  

3. **Data Scaling**  
   - Normalization applied to `Health`, `Trade`, and `Finance` features using MinMaxScaler  

4. **Dimensionality Reduction**  
   - PCA used to reduce feature dimensions for visualization and better cluster separation  

5. **Clustering**  
   - K-Means clustering applied to categorize countries into clusters based on socio-economic and health indicators  
   - Cluster results analyzed to identify countries in **direst need of aid**  

---

## Key Findings

- **Health Indicators**: African countries have high child mortality, low life expectancy, and high fertility rates, signaling urgent need for assistance.  
- **Trade & Economy**: Singapore, Luxembourg, Malta, and Seychelles have high exports and imports, indicating strong trade balance; African countries generally have low trade activity.  
- **Income & GDP**: Qatar, Singapore, and Luxembourg top income rankings; African countries dominate the lower end.  
- **Inflation**: High inflation observed in African countries, whereas some Asian and European countries have low or negative inflation.  

**Clusters provide actionable insights** for HELP International to strategically allocate funds to countries that need them the most.

---

## Tools & Libraries
- Python 3.12  
- pandas, numpy, matplotlib, seaborn  
- scikit-learn (KMeans, PCA, MinMaxScaler, StandardScaler)  
- plotly for interactive visualizations  

---

## Repository Structure
| File | Description |
|------|------------|
| `Fund_Allocation.ipynb` | Complete Jupyter Notebook with analysis, visualization, and clustering results |
| `country_data.csv` | Dataset of 167 countries |
| `requirements.txt` | Python dependencies |
| `README.md` | Project documentation |

---

## Future Work
- Implement **hierarchical and DBSCAN clustering** for better granularity  
- Integrate **geospatial mapping** to visualize clusters on a world map  
- Automate **fund allocation recommendations** based on cluster priority  

---

## References
1. Kaggle Dataset: [Unsupervised Learning on Country Data](https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data)  
2. Scikit-learn Documentation: [https://scikit-learn.org](https://scikit-learn.org)  
3. Plotly Python Docs: [https://plotly.com/python/](https://plotly.com/python/)  

---

> This project demonstrates a **data-driven approach to humanitarian aid** by clustering countries based on socio-economic and health indicators to prioritize funding effectively.

