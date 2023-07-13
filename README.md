# Premier_League_Predictions_2324
Python program that simulates the results of the 23/24 Premier League season 10 times using Poisson regression and random scores based on 22/23 xG for home and away teams, a final table using the mean of the 10 simulations is then the final output with the teams sorted by points ascending.

The code first imports the following libraries:


statsmodels.api

statsmodels.formula.api

pandas

matplotlib.pyplot

numpy

seaborn

scipy.stats


The code then reads the CSV file Pl_2223 xG.csv into a Pandas DataFrame. You will need to save on your machine and alter the code on line 51. The CSV file contains the expected goals (xG) for each team in each match of the Premier League season. You could make the assumption that xGa (expected goals against) is also used as part of the modle but this isn't explicit in the code.

The relegated teams have been removed and replaced with promoted teams from the Championship, again there has been some assumptions over the xGa used for the newly promoted teams.

The code then creates two Poisson regression models, one for the home team and one for the away team. The Poisson regression models are used to predict the number of goals scored by each team in each match.

The code then uses the Poisson regression models to predict the number of goals scored by each team in each match. The predicted goals are then used to generate random scores for each match taking into consideration the formula for expected goals.

The code then creates a dictionary to store the results of each match. The dictionary is keyed by the team name and the values are the number of points that the team has received. i.e. 3 points for a win, 1 for a draw and 0 for a loss.

The code then iterates the above 9 more times, therefore providing 10 seasons of simulated scores and results.

20 teams
38 matchweeks

38*10= 380 games a season

380*10 seasons = 3,800 simulated games

Once all 10 seasons has been simulated an out is provided of each season.

The code then produces a mean of the 10 seasons for each team to provide a measure of central tendency of a probability distribution along median and mode. The code then sorts the teams by points in descending order.

The code finally prints the Premier League table.
