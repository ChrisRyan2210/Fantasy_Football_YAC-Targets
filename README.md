

## Table of Contents

- [Project Overview](#project-overview)
- [Tools Used](#tools-used)
- [Data](#data)
- [Methodology](#methodology)
- [Analysis](#analysis)
- [Results](#results)
- [Visualizations](#visualizations)

## Project Overview

I play a lot of fantasy football, most of it with money on the line. I could talk for hours on strategy in dynasty leagues, but to keep it simple, I am aiming to moneyball the hell out of my leagues. In other words, I am always trying to find undervalued players that I can trade for to give me the competitive advantage wherever possible.

This project aims to analyse NLF wide receiver (WR) stats from week 1 through week 4 of the 2024 NFL season in an attempt to find correlation between WR stats and the amount of points they score in fantasy football.

In contrast to my other similar project, this project does not focus solely on rookies fantasy scoring, but aims to be a broader look at real life NFL stats of all WR's in the NFL. With that said, I aim to answer two main questions...

  - Which real life statistics have the highest impact on fantasy scoring?
  - Can I find any over/under valued players in fantasy football so I can win some money???

## Tools Used
![Python Badge](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL Server Badge](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=Microsoft-SQL-Server&logoColor=white)
![Tableau Badge](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)
- **SQL**: For data cleaning and transforming.
- **Python**: For data/statistical analysis & visualisation (Pandas/Matplotlib/Seaborn).
- **Tableau**: For data visualisation.

## Data

- **Source**:
    - NFL Player Stats received from: (https://www.rotowire.com/)
    - Fantasy Scoring Data received from: (https://www.rotowire.com/)
- **Time period**:
    - Fantasy Data: Aug 2024 - Sep 2024

## Methodology

1. **Data Analysis**:
   - Python (VSCode)
       - Importing csv file using Pandas.

          ![image](https://github.com/user-attachments/assets/b0572cc4-8c57-40d3-bed8-b0c9d09ca000)
         
       - Quick checks on DataFrame formatting.

          ![image](https://github.com/user-attachments/assets/fdbc0197-72ac-419c-9559-34d1bdf7dadf)
         
       - Checking for null values.
         
       ![image](https://github.com/user-attachments/assets/4aab7f9d-56e5-45fd-9959-b6de66af8c4c)
     
       - Next I wanted to find any outliers. As we are only 4 weeks into the season I knew certain players would have 100% passes caught due to only being targeted a very small amount of times. So I looked for players with very high Target & Yard percentages.
         - Using Seaborn to check for outliers in Targets Per Route Run %
           
            ![image](https://github.com/user-attachments/assets/6a80d3a6-5785-4358-840b-2b60c1738074)
         
         - Using Seaborn to check for outliers in Yards Per Route Run

           ![image](https://github.com/user-attachments/assets/baa5d440-f410-47d0-9ae7-a5713a5826cf)
           
       - As there were so many outliers, I decided to check the data source and found the best way to move forward was to remove players with less than 5 targets

          ![image](https://github.com/user-attachments/assets/dce54c71-b9b3-4d81-8094-387279547422)
         
       - Finally, I wanted to filter to only Wide Receivers and call the .corr() function on the dataframe.

         ![image](https://github.com/user-attachments/assets/92cda310-a304-4ce7-b2d7-a0f552aa4a55)
         
## Visualisations

1. **Visualisation 1**

   ![image](https://github.com/user-attachments/assets/47f53efb-96b0-4129-9071-3b0e0cdf8123)

   - This dashboard shows the average point per game (PPG) scored over a players career as well as displaying the players by draft round. Furthermore, the relative size of the marks on the dashboard represent total points score.
   - The two refenence lines (WR 1) and (WR 2) represent the average points a player would need to score over their career to finish in the sought after WR 1 and WR 2 fantasy rankings.
     
2. **Visualization 2**

   ![image](https://github.com/user-attachments/assets/0552ebcb-0b99-4243-9501-a1f4cba53192)

   - It's clear to see that the SEC boasts the highest number of WR 1/WR 2 players in fantasy football, with 9 total players achieving at least a career average WR 2 finish.
   - In fact, the next best conference is the Big Ten with only 4 players scoring an average of at least a WR 2 finish over their careers.

## Results

- **Key Finding 1**: Fantasy football players should focus on players who played in the SEC. Outside of this, college conference is not a good indicator of fantasy success.
- **Key Finding 2**: As draft round increases. There is a visible drop in the average PPG. However there are exceptions in later rounds. This indicates that players drafted in earlier rounds might be given more opportunities to play whether or not they are playing well.
- **Key Finding 3**: Draft round is not a good indicator of players who score a WR 1 average over their careers. There seems to be a negative correlation between draft round and PPG, however this correlation is not strong due to the outliers in the later round.
- **Key Finding 4**: There is a strong correlation between scoring at least 10 PPG and beign drafted in the top 3 rounds.
- **Key Finding 5**: Fantasy players may benefit from takign as many "flyer" picks as possible in later rounds and stashing them as there seems to be oppotunities to get a "hit" if enough chances are taken.

## Contact

Feel free to contact me for any questions or collaborations:

- **Email**: [chrisryan@umail.ucc.ie](mailto:your-email@example.com)
- **LinkedIn**: [My LinkedIn Profile](https://www.linkedin.com/in/christopher-ryan-8229a81b9/)
