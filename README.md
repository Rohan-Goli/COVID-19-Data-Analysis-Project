COVID-19 Data Analysis Project

Overview:

This project analyzes the impact of the COVID-19 pandemic in India through various data visualizations and statistical analyses. Using Python libraries such as Pandas, NumPy, Matplotlib, Seaborn, and Plotly, the project provides insights into confirmed cases, deaths, recoveries, and vaccination statistics across different states.

Project Structure:

Data Manipulation: Utilizing Pandas for loading and manipulating datasets, ensuring the data is clean and structured for analysis.

Numerical Computation: Employing NumPy for efficient numerical operations and calculations.
Libraries Used

Pandas: For data manipulation and analysis.
NumPy: For numerical computations.
Matplotlib: For basic plotting and visualizations.
Seaborn: For advanced statistical visualizations.
Plotly: For interactive visualizations.

Installation:

To run this project, ensure you have Python installed. You can install the necessary libraries using:

pip install numpy pandas matplotlib seaborn plotly

Analysis Overview:

1. Data Loading and Cleaning

   The COVID-19 dataset is loaded, and unnecessary columns are dropped to focus on relevant information. The date column is converted to datetime format for accurate time-series analysis.

2. Statistical Analysis

   Descriptive Statistics: Summary statistics are generated using df.describe(), providing insights into the distribution of key variables.

Pivot Tables: Created to summarize total confirmed cases, deaths, and recoveries by state, allowing for easy comparison.

3. Visualizations:

   Top 10 Active Cases: A bar plot visualizing the states with the highest active COVID-19 cases.

Python code:

ax = sns.barplot(data=top_10_active_cases.iloc[:10], y="Active_Cases", x="State/UnionTerritory", linewidth=2, edgecolor='red')
Deaths Analysis: Another bar plot showing the states with the highest reported deaths.

Python code:

ax = sns.barplot(data=top_10_deaths.iloc[:12], y='Deaths', x='State/UnionTerritory', linewidth=2, edgecolor='black')

Growth Trends: A line plot depicting the growth trend of active cases in the top five affected states.

Python code:

ax = sns.lineplot(data=covid_df[covid_df['State/UnionTerritory'].isin(['Maharashtra', 'Karnataka', 'Kerala', 'Uttar Pradesh', 'Tamil Nadu'])], x='Date', y='Active_Cases', hue='State/UnionTerritory')

4. Vaccination Analysis:

   Most and Least Vaccinated States: Bar plots comparing the total vaccinations across states.

Python code:

x = sns.barplot(data=max_vac.iloc[:10], y=max_vac.Total, x=max_vac.index, linewidth=2, edgecolor='green')

Conclusion:

This project provides a comprehensive overview of the COVID-19 situation in India, showcasing the effectiveness of vaccination drives and highlighting areas of concern with rising case numbers. The visualizations help in understanding the trends and making informed decisions based on data.
