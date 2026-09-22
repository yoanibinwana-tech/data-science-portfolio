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






