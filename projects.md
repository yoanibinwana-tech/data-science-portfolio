# Projects
This section documents my data science projects, research questions, and data stories I create throughout the semesters.
---
## Project 1

Portfolio project one:
- Research Question: What are statistical distributions (offensive rating, usage rate, and points per game) that determine if a player is a Division 1 basketball player, and how is it different in top-tier programs compared to lower-tier D1 programs?
- Source: https://collegebasketballdata.com/ A Clean, structured CBB data via API and prebuilt packs.
- Unit of Analysis: Each row represents one player-season
- Features: Points per game (PPG), Offensive rating and usage rate, Field goal percentage (FG%), Three-point percentage (3PT%), Player position
- Size: D1 season including roughly 350+ teams and 4,000–5,000 rostered players
- Missing Values: Vertical leap, Wingspan

Conceptualized/operationalized Variables:
- Offensive Rating(Conceptualized): A player's overall scoring efficiency estimating a player's true skill at generating points (Oliver, 2004).
- Offensive Rating(Operationalized): Points produced per 100 individual possessions used, calculated from field goals, free throws, assists, and turnovers (Oliver, 2004).

- Usage Rate(Conceptualized): How often a possession "runs through" them via a shot, free throw trip, or turnover (Oliver, 2004).
- Usage Rate(Operationalized): The percentage of a team's total possessions used by a given player while on the floor (Oliver, 2004).

- Points Per Game(Conceptualized): Raw scoring output
- Points Per Game(Operationalized): Total points scored across the season divided by games played

Data Cleaning and Preparation:
<img width="1711" height="750" alt="image" src="https://github.com/user-attachments/assets/6ec91c72-6a58-4f27-a001-b8c7ff4eb4bf" />

Visualizations

