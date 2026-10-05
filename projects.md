# Projects
This section documents my data science projects, research questions, and data stories I create throughout the semesters.
---
## Project 1

**Portfolio project one:**
- Research Question: What are statistical distributions (offensive rating, usage rate, and points per game) that determine if a player is a Division 1 basketball player, and how is it different in top-tier programs compared to lower-tier D1 programs?
- Source: https://collegebasketballdata.com/ A Clean, structured CBB data via API and prebuilt packs.
- Unit of Analysis: Each row represents one player-season
- Features: Points per game (PPG), Offensive rating and usage rate, Field goal percentage (FG%), Three-point percentage (3PT%), Player position
- Size: D1 season including roughly 350+ teams and 4,000–5,000 rostered players
- Missing Values: Vertical leap, Wingspan

**Conceptualized/operationalized Variables:**
- Offensive Rating(Conceptualized): A player's overall scoring efficiency estimating a player's true skill at generating points (Oliver, 2004).
- Offensive Rating(Operationalized): Points produced per 100 individual possessions used, calculated from field goals, free throws, assists, and turnovers (Oliver, 2004).

- Usage Rate(Conceptualized): How often a possession "runs through" them via a shot, free throw trip, or turnover (Oliver, 2004).
- Usage Rate(Operationalized): The percentage of a team's total possessions used by a given player while on the floor (Oliver, 2004).

- Points Per Game(Conceptualized): Raw scoring output
- Points Per Game(Operationalized): Total points scored across the season divided by games played

**Data Cleaning and Preparation:**
Loading & Inspecting the Data
<img width="1711" height="750" alt="image" src="https://github.com/user-attachments/assets/6ec91c72-6a58-4f27-a001-b8c7ff4eb4bf" />

**Visualizations:**
Player Statistics: Points Scored vs Games Played
<img width="768" height="650" alt="image" src="https://github.com/user-attachments/assets/049430e1-ca15-444b-af13-5dc0a40b9743" />

Player Statistics: Offensive Rating vs Games Played
<img width="767" height="636" alt="image" src="https://github.com/user-attachments/assets/38b96f06-a793-4e8e-aff6-3bea06dd47fb" />

Distribution of Offensive Rating Across D1 Players: Offensive Rating vs Numbers of Players
<img width="792" height="655" alt="image" src="https://github.com/user-attachments/assets/8337d5ea-f895-46ba-94e2-7e84934a91dc" />

**Ethics and Limitations:**
Dataset: This dataset shows only the people who have made it onto a D1 roster. It addresses top tier D1 players from lower tier D1 players but it cannot show D1 players from high school or non D1 players. There is some important context missing. Some teams game schedule is comparably weaker than other teams' schedules. There's also no context to injury or leave during the season. Some stats may be inflated due to playing fewer amount of games compared to others. In certain teams, bias can take effect as well due to programs' concentration on roles. One program may favor using their PG more than another program so things like the usage rate can be thrown off due to that as well. 

**References:**

## Project 2

**Portfolio project two:**
- Research Question: How does incorporating rolling 7-day averages of rainfall improve the accuracy of predicting weekly precipitation compared to using raw daily data?
- Source: NCEI NOAA GOV (National Center For Environmental Information, National Oceanic and Atmospheric Administration) https://www.ncei.noaa.gov/
- Task: Regression
- Target Variable: The total precipitation over the seven days following the forecast day
- Unit of Analysis: A forecast day paired with the total rainfall of the seven days that follow it.
- Features: The features include raw daily rainfall in the previous 28 days, a four 7-day rolling average from 7, 14, and 21 days before, and lastly seasonality features.
- Size: The size of the dataset included 5,418 daily records of forecast.
- Missing Values: There was 0 missing days out of the days recorded.

**Background:**
This is important because predicting rainfall helps agricultural productivity and our food security. It's also important we have rainfall to ensure that we don't fall into a drought. Machine learning has been used to help predict rainfall from all kinds of atmospheric measurements. For example, in a study multivariate linear regression, random forest, and XGBoost was compared for daily rainfall amount, Liyew and Melese (2021). They used MAE and RMSE to judge the models. Another study related to this used lagged values of precipitation, temperature, and insolation to capture rainfall patterns. 

**References:**
Breiman, L. (2001). Random forests. Machine Learning, 45(1), 5–32. https://doi.org/10.1023/A:1010933404324 

Liyew, C. M., & Melese, H. A. (2021). Machine learning techniques to predict daily rainfall amount. Journal of Big Data, 8, Article 153. https://doi.org/10.1186/s40537-021-00545-4 

Menne, M. J., Durre, I., Vose, R. S., Gleason, B. E., & Houston, T. G. (2012). An overview of the Global Historical Climatology Network-Daily database. Journal of Atmospheric and Oceanic Technology, 29(7), 897–910. https://doi.org/10.1175/JTECH-D-11-00103.1 

**Data Cleaning:**
The data contained many different informations about wind, snow, and other flags that trigger the prediction of weather but my research question focused on only precipitation so I kept the daily precipitation column and left out the rest.

**Visualizations (Linear Regression):**
<img width="1336" height="540" alt="image" src="https://github.com/user-attachments/assets/da244c2f-e825-44aa-bcb7-2a9c387aa6a8" />
This image represents the Predicted vs the actual next week rainfall. As you can see, these two panels look nearly identical.

<img width="682" height="538" alt="image" src="https://github.com/user-attachments/assets/03ddaf54-1cd0-4a62-a34e-5b93238cbb83" />
This image represents the Mean Absolute Error comparison between both graphs. The lower, the better. Each bar is one model and they are both about 0.78. This means the rolling averages did not reduce the error compared with the raw daily values.

**Visualizations (Random Forest):**
<img width="1331" height="536" alt="image" src="https://github.com/user-attachments/assets/6cfae2e8-6675-4aca-b699-b2401f7d486b" />
This image represents the Predicted vs the actual next week rainfall. The rolling panel is more scattered than the raw panel. The random forest is more spread out than the linear regression plots, giving a wider range of predictions.

<img width="802" height="611" alt="image" src="https://github.com/user-attachments/assets/09d91fbf-014b-480f-90e3-72909087a1c0" />
This image represents the Mean Absolute Error comparison for all five models. The lower, the better. Here, the random forest: rolling 7-day (0.76) is the lowest. This means the linear regression rolling averages made no difference but the random forest rolling averages gave the best score of any model.

<img width="1328" height="607" alt="image" src="https://github.com/user-attachments/assets/faf3fffc-90cb-423a-973e-cc4d63a6fe2b" />
This image represents one of the trees in the random forest. 

Overall, the models show that incorporating rolling 7-day averages of rainfall does not improve the accuracy of predicting weekly precipitation compared to using raw daily data. 


