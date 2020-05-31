# Team 21: Predicting NBA Scores 

Final project for the Boot Camp 2020 runned by the Erdos Institute.



## Table of contents
* [Susquehanna International Group (SIG)](#Susquehanna-International-Group-(SIG))
* [Data](#Data)
* [Model](#model)
* [Contact](#contact)
* [Team Members](#Team-Members)


## Susquehanna International Group (SIG) - Sports Analytics Group Problem

We aim to build classifiers on totals for NBA games. More formally, we construct a model that takes in inputs {team A, team B, and any other relevant conditions}, and outputs the following: for all reasonable values of X, what is the probability that the combined final score of both teams is at least X?

## Data

The `final_nba_data.csv` is the main dataset containing the target and features. The `Constructing NBA Dataset.ipynb` shows how we cleaned and obtained the final dataset. `referees.csv`,`rivalries.csv`, and `distance_between_cities.csv` were imported to get the final dataset. 

- *Target*
 - Combined score (TOT_PTS)
- *Features* (past scores are also: logged, squared, and cubed) 
 - Number of days between games (DAYS_BTWN_GAMES_x, DAYS_BTWN_GAMES_y)
 - Number of wins in last 10 games (WINS_10GAMES_x, WINS_10GAMES_y)
 - Wins thus far in the season (WINS_UPTOGAME_x, WINS_UPTOGAME_y)
 - Combined points in previous matchup (pre_PTS)
 - Distance traveled (distance_miles)
 - Rivalry (rivalry)
 - Avg. points/team in last 2,3 and 4 games (AVGPOINTS_2GAMES_x,...AVGPOINTS_4GAMES_y)
  - Past scores are also logged, squared, and cubed


## Model 

- `ridge_lasso_enet` fits ridge regression, lasso regression, and eleastic net models. 
- `random_forest.ipynb` fits random forests on the past month of games before the game of interest. 
- `pr_score_less_than_x.ipynb` calculates the probability that a combined final score is at least X. 



## Team Members

- Soohyun Cho (cho.885@osu.edu) 
- Miguel Garza Casado (garzacasado.1@osu.edu)
- Daniel Kent (kent.249@.osu.edu) 