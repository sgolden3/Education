# How does State along with Socioeconomic variables impact Average ACT scores?

> This project aims to evaluate how the location of a student and different socio-economic features impact standardize testing scores for students in high school.

---

## Project Overview

Provide a short and concise overview of the project. Mention the problem it solves, the data used, and the key outcomes or findings.

- **Objective:** To assess how diferent socioeconomic facotrs impact ACT scores
- **Domain:** Education
- **Key Techniques:** Regressions, Linear Modelin

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

- **Source:** [Link to the data source(s)](https://nces.ed.gov/programs/digest/d21/tables/dt21_226.60.asp) 
- **Description:** The dataset contains ACT scores for 2017 and 2021 for each state
- **License:** There are none for this project.

---

## Analysis

Cleaned education data was utilized. The primary data set is the EdGap data set from EdGap.org and the secondary data set comes from the National Center for Education Statistics. These tow data sets have already been cleaned and merged into “df”. The ACT score data by state was also from the National Center for Education Statistics. The ACT score by state date was imported, formatted and tidyed. The ACT by state scores and the “df” date frame were merged by an inner join on state to keep data from matching states. Composite ACT data from year 2017 and 2021 were carried over to states in the education dataset. A correlation matrix of the predictor variables was created. Single input models of linear regressions were conducted for median income and state. From analysis of the correlation matrix, a reduced model was created to reflect the variables that are the strongest predictors. A residual plot was created to reflect the new reduced model. Finally, numerical variables were scaled and assessed.

---

## Results

The first pairplot shows a clear linear relationship between the state an ACT score was taken and the average score. Some states will impact the ACT more than others. In the reduced model, all states have a p value that is less than or equal to 0.01, showing a great statistical significance between the state a student took their exam and their ACT score. Percent lunch is shown to have the greatest impact on a student’s ACT score, with the strongest coefficient of the all (-7). The high R squared values shows that all the reduced predictor variables together created a statistical significance.


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
