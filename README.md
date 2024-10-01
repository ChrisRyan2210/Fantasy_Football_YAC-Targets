

## Table of Contents

- [Project Overview](#project-overview)
- [Tools Used](#tools-used)
- [Data](#data)
- [Methodology](#methodology)
- [Analysis](#analysis)
- [Results](#results)
- [Visualisations](#visualisations)

## Project Overview

I play a lot of fantasy football, most of it with money on the line. I could talk for hours on strategy in dynasty leagues, but to keep it simple, I am aiming to moneyball the hell out of my leagues. In other words, I am always trying to find undervalued players that I can trade for to give me the competitive advantage wherever possible.

This project aims to analyse NFL wide receiver (WR) stats from week 1 through week 4 of the 2024 NFL season in an attempt to find correlation between WR stats and the amount of points they score in fantasy football.

In contrast to my other similar project, this project does not focus solely on rookies fantasy scoring, but aims to be a broader look at real life NFL stats of all WR's in the NFL. With that said, I aim to answer two main questions...

  - Which real life statistics have the highest impact on fantasy scoring?
  - Can I find any over/under valued players in fantasy football so I can win some money???

## Tools Used
![Python Badge](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL Server Badge](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=Microsoft-SQL-Server&logoColor=white)
![Tableau Badge](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)
- **SQL**: For data cleaning and transforming.
- **Python**: For data/statistical analysis & visualisation (Pandas/Matplotlib/Numpy/Seaborn).
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
           
       - As there were so many outliers, I decided to check the data source and found the best way to move forward was to remove players with less than 5 targets which allowed me to keep true anomolies/outliers in the dataset.

          ![image](https://github.com/user-attachments/assets/dce54c71-b9b3-4d81-8094-387279547422)
         
       - Finally, I wanted to filter to only Wide Receivers and call the .corr() function on the dataframe.

         ![image](https://github.com/user-attachments/assets/92cda310-a304-4ce7-b2d7-a0f552aa4a55)
         
## Visualisations

1. **Visualisation 1**

   - I wanted to avoid using the stats that directly scored points in fantasy football, Yards & Receptions, as these have been heavily analysed in the past. So using the correlation results from above, I decided to focus on Yards After the Catch (YAC) & Team Target % 

    ![image](https://github.com/user-attachments/assets/b9fbb582-644e-436a-b00d-d7bfd5efb02b)

   - This scatter plot shows a positive correlation between YAC & Fantasy Points Scored (Pts)
     
2. **Visualization 2**

   ![image](https://github.com/user-attachments/assets/b8266b68-3030-4bfc-b898-128bbf9b3736)

   - Similarly, thiss scatter plot shows a strong positive correlation between Team Target % & Fantasy Points Scored (Pts)
  

## Results

- With the info from above, I was happy to move ahead with my final visualisation, plotting YAC against Team Target % to see which players have performed best in these stats through Week 4 of the season.

  ![image](https://github.com/user-attachments/assets/d1b56cd9-c699-409b-85ca-9a4d27f96b9e)

- **Key Finding 1**: Highly valued but low performing fantasy players such as Jamaar Chase and Jaxon Smith-Njigba might be possible sells if I can get similar production back + draft captital.
- **Key Finding 2**: I should look to buy for players with high YAC but low target % that are sitting behind an aging WR 1 such as Rome Odunze, Jameson Williams & Jaylen Waddle.
- **Key Finding 3**: Khalil Shakir & Rashee Rice are both heavily undervalued for their current performance.

## Contact

Feel free to contact me for any questions or collaborations:

- **Email**: [chrisryan@umail.ucc.ie](mailto:your-email@example.com)
- **LinkedIn**: [My LinkedIn Profile](https://www.linkedin.com/in/christopher-ryan-8229a81b9/)
