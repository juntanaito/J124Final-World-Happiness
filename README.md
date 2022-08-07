# Which country has the happiest people and why?
## By Junta Naito
## Sourcing
I got my data from this data set and focused on the years 2019 to 2022.
## Data Analysis
### 1) In 2022, what rank and happiness score did the countries who had the top 5 highest score for GDP per capita as their explanation for happiness receive? Top 5 lowest? 
1. In "2022" sheet, highlight the "Explained by: GDP per capita" column and drag it to the right of the "Happiness score" column.
2. Sort the "Explained by: GDP per capita" column from Z to A, arranging the data in descending order from the highest GDP per capita. 
!['Highest GDP','Highest GDP'](/1a.png)
* **As shown, Luxembourg scored the highest for GDP per capita being their explanation for happiness with 2,209, however, ranked #6 among the happiest countries with a happiness score of 7,404. Singapore, coming in second, had a sharper contrast, with a score of 2,149 in their GDP per capita while ranking #27 and a happiness score of 6,480.** 
3. Sort the "Explained by: GDP per capita" column from A to Z, arranging the data in ascending order from the lowest GDP per capita. 
!['Lowest GDP','Lowest GDP'](/1b.png)
* **As shown, the countries which ranked the lowest for GDP per capita as their explanation for their happiness, ranked lower overall in happiness, as Venezuela scored the lowest for GDP per capita being their explanation for happiness with 0, and ranked #108 among the happiest countries with a happiness score of 4,925.**
### 2) In 2021, what were the averages for the ladder score, GDP per capita, social support, healthy life expectancy, freedom to make life choices, generosity, and perceptions of corruption *by region*? Round decimal to the hundredth place. Which region had the highest average "ladder score"?
1. In the "2021" sheet, create a pivot table.
2. In the pivot table, set the row to "Regional indicator."
3. In the column, add "Ladder score", "Logged GDP per capita", "Social support", "Healthy life expectancy", "Freedom to make life choices", "Generosity", and "Perceptions of Corruption" and set each "summarize by" to "AVERAGE."
4. Highlight numbers in the data set (B2 to H12) 
5. Under the number formats with the "123" icon, change the format to "number."
!['2021 Regional Averages','2021 Regional Averages'](/2.png)
* **As shown, "North America and ANZ" ("ANZ" stands for [Australia and New Zealand](https://worldhappiness.report/ed/2022/happiness-benevolence-and-trust-during-covid-19-and-beyond/)) had the highest "ladder score" of 7.13 in 2021, which indicates respondents answers on a [Cantril ladder](https://worldhappiness.report/faq/), with 0 representing the worst possible life and 10 being the best. This region overall scored well with their average score of 10.81 for "Logged GDP per capita" being , 0.93 for "Social support", and 72.33 for "Healthy life expectancy."** 
### 3) Which countries have ranked/scored top 5 in happiness from 2019 to 2022? Do you observe any patterns?
1. In the "2019" sheet, sort the "Overall rank" column from A to Z, arranging the data in ascending order from the lowest number, or the top rankings. 
!['Top Rank/Score','Top Rank/Score'](/3a.png)
2. In the "2020" sheet, sort the "Ladder score" column from Z to A, arranging the data in descending order from the highest score.
!['Top Rank/Score','Top Rank/Score'](/3b.png)
3. In the "2021" sheet, sort the "Ladder score" column from Z to A, arranging the data in descending order from the highest score. 
!['Top Rank/Score','Top Rank/Score'](/3c.png)
4. In the "2022" sheet, sort the "RANK" column from A to Z, arranging the data in ascending order from the lowest number, or the top rankings. 
!['Top Rank/Score','Top Rank/Score'](/3d.png)
* **Finland and Denmark respectively top all four years consecutively. Iceland, Switzerland, Norway, and Netherlands are also consistently in the top 5 range as well.**
### 4) In 2022, which countries gave the highest score for each of the categories: GDP per capita, social support, healthy life expectancy, freedom to make life choices, generosity, and perceptions of corruption?
1. In the "2022" sheet, create a pivot table.
2. In the pivot table, set the "Values as" to "columns" and add "Explained by: GDP per capita", "Explained by: Social support", "Explained by: Healthy life expectancy", "Explained by: Freedom to make life choices", "Explained by: Generosity", and "Explained by: Perceptions of Corruption" and set each "summarize by" to "MAX."
3. To set up for the VLOOKUP function, go to "2022" sheet and move the "Country" column to the right of the "Explained by: Perceptions of corruption" column.
4. Go back to the pivot table sheet and use the VLOOKUP function to fill in the countries which correspond to the the highest score (maximum value) in each of the categories. In order to do this, the search key would be the maximum value for each category ("2209" or cell A2 for "MAX of Explained by: GDP per capita"), the range would be from the column which the search is being made ("Explained by: GDP per capita" or column C in this example) until the "Country" (column I), index would be the number of the "Country" column counting from the left ("7" in this example), and the "[is sorted]" would be "false."  

* **Luxembourg gave the highest score for GDP per capita, Iceland for social support, Hong Kong S.A.R. of China for healthy life expectancy, Cambodia for freedom to make life choices, Indonesia for generosity, and Singapore for perceptions of corruption?**
### 5)
1.
