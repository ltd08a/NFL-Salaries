# NFL-Salaries
### Introduction
This project takes a closer look into salary cap percentges by position and how these correlate to team success. The data spans from the 2011 to 2023 seasons. By examining the relationship between cap hit percentages and winning this project will show not only which positions are the highest paid, but which of those investments is actually paying off. 
### Data Sources
The team statistical data is from a Kaggle dataset called 'NFL Team Data 2003-2023'. Nick Cantalupa is the author of this dataset. It contains various team stats, including year, team, win/loss percentage, and various other data points. This file was renamed as 'team_stats_2003_2023.xlsx'.    
The dataset containing salary cap data is called 'nfl_team_cap_data.xlsx'. This dataset was pulled from spotrac.com and formatted into a pandas DataFrame to use in the analysis. It was then exported into an excel (.xlsx) file.   
To determine which teams made the playoffs, data was gathered wikipedia.org. Once the data was brought into the environment it was exported into a csv file called 'nfl_playoff_teams.csv'. It shows every team that made the playoffs by year. 
### Objective
The objective here is to determine which areas of investment within the organization have provided the greatest returns and losses.   
### Methodology
This analysis was done using the Python language within a Jupyter notebook environment. 
## Gathering Data:
To start, salary cap data was pulled from spotrac.com using the BeautifulSoup and requests libraries. Once the data was returned it was formatted into a pandas DataFrame, then exported as an excel (.xlsx) file.   
Next, I downloaded the team statistical dataset from kaggle.com.   
Originally, the data was entered manually to determine which teams had made the playoffs. Upon inspection in the analysis an error was found. Because of this, data was pulled from wikipedia.com to confirm correctness and fix issues. This was done using the BeautifulSoup and requests libraries. Once this data was gathered it was converted into a pandas DataFrame and exported into a csv file. 
## Inspecting and Cleaning
To inspect and clean the data I focused on one dataset at a time. I started with the team stats data. First, I had to select only the data from 2011 - 2023, as that is the range I have pay data for. After that, unneccessary columns were dropped and others were converted to proper data types for analysis. I then inspected each column of the dataset indivisually to ensure data integrity and accuracy. A custom function was created to convert team names to a desired format. Here is where I ran into the issue of incorrect playoff teams. This issue was resolved as described above in the _Gathering Data_ section. A function was also created to discover any missing or mismathced values.   
Next the salary cap data was looked at. 
One column was dropped, and the DataFrame was formatted. Each column is checked individually. I did find a few rows with a missing age value. I reseached this and was able to get the proper value in place. 
### Analysis
The salary cap data is grouped by year and position to find the average cap hit percentage for each position by year. A function is created to depict this. The plots are split into different categories of offense, defense, special teams, offensive line, backfield, pass catchers, defensive line, linebackers, and secondary.   
Next, the merge, groupby, and pivot_table built-in functions are used to discover the correlation of positional cap hit percentage and win/loss record from the regular season. These correlations are plotted out in a bar chart. 
### Results
## Position by Position Breakdown:
# Offense:
Quarterback:   
Runningback:   
Fullback:   
Wide Receiver:   
Tight End:   
Left Tackle:   
Right Tackle:   
Tackle:   
Guard:   
Center:   
# Defense:
Defensive End:   
Defensive Tackle:   
Outside Linebacker:   
Inside Linebacker:   
Linebacker:   
Cornerback:   
Free Safety:   
Strong Safety:   
Safety:   
# Special Teams:
Kicker:   
Punter:   
Long Snapper:   
