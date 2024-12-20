# Is it Worth it to Fire Your Coach in the NFL?

## Group Members
- Matt Mascavage
- Nik Greb
- Owen Kim (Me)

## Google Colab Worksheet
[Link to Colab Worksheet](https://colab.research.google.com/drive/17cAjFsPaYrHx-ixhsSl-JyjIttDtKu-J)

## Research Report

#### Introduction:

We created our own custom data set (linked here) by compiling statistics collected from a number of sources. The final data set contained the following info from the 2002 - 2023 NFL season (we chose this range because the 32nd team, the Texans, were added to the League in 2002):

- Year: The season for that entry
- Coach: The head coach for that season. There will be separate entries if a coach was fired and replaced midseason, one entry for each coach
This way, the rest of the data all applies to the team’s performance under that specific coach
- Team: The team for that entry
- Games Played: The number of games played under that coach
- Wins
- Losses
- Ties
- Win Percentage: Calculated as wins/games
- Points Scored
- Points Against
- Point Differential: Points scored minus points against

Creating this data set was the bulk of the work for this project. We had to combine data from multiple sources and often had to enter the data manually (this was the case for every year where a team had multiple head coaches in a season). 
Once we had created the data set, the goal was to look at some of the different measures of a team’s performance and compare that to the changes in coaching. Some of the questions we were hoping to answer were:
Does firing a coach and hiring a new one boost the team’s performance? Is it “worth it?”
How do teams who change head coaches often compare in performance to teams that keep the same coach for a long period of time?
Naturally, there are a lot of confounding factors at work, but we’re really just trying to capture the relationship between coaching changes and team performance.

#### Data sources: (MLA citations at end of document)

https://www.pro-football-reference.com/years/2023/coaches.htm - This source was used to find head coaches for each team for a given year. For years with a midseason firing, it showed the week that the firing occurred and how many wins each coach had that season. 
https://www.pro-football-reference.com/years/2008/index.htm - For seasons with midseason firings, we used this data source to calculate “Points Scored” and “Points Against”, which were then used to find “Points Differential.” We used this data source to check game by game data for a team that had a midseason firing, manually calculating the “Points Scored” and “Points Against” from before and after the firing. 
https://www.nfl.com/stats/team-stats/ - This is the official NFL website and it had really complete (and reliable) statistics on team performance. We mostly used it to find each team’s record for all of the seasons and to catch tie scores for the “Tie” column.
Wikipedia - We used wikipedia to make the coaches column, finding all of the coaches for each team for any given year. We would search “[NFL team] head coach history” and wikipedia would provide each head coach for the given team, and also the years when they were the head coach. Midseason firings were shown by two coaches in a single year. 

#### Methods and Results:

The bulk of the time dedicated to this project went into finding the data that we wanted to analyze and creating a pristine dataset that we could then analyze through our Colab notebook. We searched for a long time at the beginning of this project looking for an importable data file containing NFL season data along with the names of the head coaches corresponding to the team and years that they coached, and could not find it. So what we decided to do instead was create our own datafile. It took a lot of time looking on the internet to find season and coach data for each team and each year from 2002 to 2023, but we feel it was worth it in the end as we did not have nearly any data cleaning and wrangling to do on the back end once we started our analysis and coding. One of the biggest challenges was determining how to handle seasons in which a team had multiple head coaches in one year. In those instances, we decided to have two rows for that season and team, one row for each head coach, with the teams record that season split up by their record under each head coach. This allowed us to look at some more specific questions such as if firing a head coach specifically in the middle of season makes a difference on team performance. Over the course of one season, the player composition of a team is largely unchanged, so in effect we are keeping more “variables” the same that could impact team performance, and attempting to single out whether a head coaching change makes a difference. The first plot we created was a preliminary scatterplot of the win percentages of NFL teams by number of head coaches they have had since 2002. 


