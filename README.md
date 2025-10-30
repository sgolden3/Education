# How does State along with Socioeconomic variables impact Average ACT scores?

> This project aims to evaluate how the location of a student and different socio-economic features impact standardize testing scores for students in high school.

---

## Project Overview

This project assesses how location and different socioeconomic variables impact average ACT scores across the U.S. Different socioeconomic variables are assumed to impact a student’s performance on their assessments. Data from the EdGap and the National Center for Education Statistics were joined with state ACT data also from the National Center of Education Statistics to analyze the impact of different predictor variables. Exploratory analysis included creating a pair plot of the numerical data. Modeling methods including linear regressions and residual plots were used to assess the statistical significance of the impact of different variables. Results showed that percent lunch was the predictor variable that had the greatest impact on ACT score, while a student’s location in general did not have a statistically significant impact on their ACT score.

- **Objective:** To assess how diferent socioeconomic facotrs impact ACT scores
- **Domain:** Education
- **Key Techniques:** Regressions, Linear Modeling

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** (https://nces.ed.gov/programs/digest/d21/tables/dt21_226.60.asp) 
- **Description:** The dataset contains ACT scores for 2017 and 2021 for each state
- **License:** There are none for this project.

---

## Analysis

The primary data set is the EdGap data set from EdGap.org and the secondary data set (ACT composite scores) comes from the National Center for Education Statistics. The data set was cleaned by dropping unnecessary rows and columns that were not the state, year or composite score. The EdGap data set was revised to have state names labelled fully instead of abbreviations, and an additional “years” column was created to keep similar formatting. These two data sets were merged by an inner join on state and year into “merged_df” to keep only state data that is included in both datasets. Composite ACT data from year 2017 and 2021 were carried over to states in the education dataset. A correlation matrix of the predictor variables was created for numerical values. Single input models of linear regressions were conducted for median income. A multiple linear regression was created including state data. From analysis of the correlation matrix, a reduced model was created to reflect the variables that are the strongest predictors. A residual plot was created to reflect the new reduced model. Finally, numerical variables were scaled and assessed.

---

## Results

As shown by the variation in different colored points, the first pair plot shows a clear linear relationship between the state an ACT score was taken in and different socioeconomic variables. This clear linear relationship encourages a deeper dive into the impacts of different predictor variables.
It is important to note that in the multiple regression analysis, the state of reference is Delaware. In this model, only New York has a p-value less than 0.05, showing a statistical significance between the comparison of ACT test scores taken in New York vs. Delaware. The high R squared value (0.708) shows that all the predictor variables together created a statistical significance.
Percent lunch is shown to have the greatest impact on a student’s ACT score, with the strongest coefficient of the all (-7). The high R squared value (0.679) shows that all the reduced predictor variables together created a statistical significance. The p values for states all display as 0.00, hinting at possible error with integrated categorical variables into the analysis.
The residual model is derived from the model that was used in the second computational results. It displays most points somewhat along the dotted red line, with a few outliers showing a weak negative relationship. Since the relationship appears weak, it shows that there is most likely not another quadratic or additional relationship between the variables that is not being accounted for. 



---

## Authors

- Sydney Golden - [@yourhandle](https://github.com/sgolden3)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Tools/libraries used
- Tutorials or papers referenced
- Inspiration or collaborators
