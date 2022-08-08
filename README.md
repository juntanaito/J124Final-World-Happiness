# Which country has the happiest people and why?
## By Junta Naito
## Sourcing
I got my data from this data set and focused on the years 2019 to 2022.

## Story Summary and Sourcing
NYT - "Dr. Wang said some results were surprising: Parts of Eastern Europe ranked relatively low on the list, despite having relatively good income levels, while in South America, the reverse was true: Happiness levels tended to be high, given relatively low income levels."

NYT - explains more about why Fins may be happier
"The country’s public school system, which rarely tests children, is among the best in the world. College is free. There is a good universal health care system and child care is affordable. And Finland has been one of the least affected European countries by the pandemic, which experts attribute to the high trust in government and little resistance to following restrictions."

## Data Visualization
!['2022 Happiness Map','2022 Happiness Map'](/2022HappinessMap.png)

## Data Analysis Process

### 1) In 2022, what rank and happiness score did the countries who had the top 5 highest score for GDP per capita as their explanation for happiness receive? Top 5 lowest? 
1. In "2022" sheet, highlight the "Explained by: GDP per capita" column and drag it to the right of the "Happiness score" column.
2. Sort the "Explained by: GDP per capita" column from Z to A, arranging the data in descending order from the highest GDP per capita. 
!['Highest GDP','Highest GDP'](/1a.png)
* **In 2022, Luxembourg scored the highest for GDP per capita being their explanation for happiness with 2,209, however, ranked #6 among the happiest countries with a happiness score of 7,404. Singapore, coming in second, had a sharper contrast, with a score of 2,149 in their GDP per capita while ranking #27 and a happiness score of 6,480.** 
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
* **In 2021, "North America and ANZ" ("ANZ" stands for [Australia and New Zealand](https://worldhappiness.report/ed/2022/happiness-benevolence-and-trust-during-covid-19-and-beyond/)) had the highest "ladder score" of 7.13 in 2021, which indicates respondents answers on a [Cantril ladder](https://worldhappiness.report/faq/), with 0 representing the worst possible life and 10 being the best. This region overall scored well with their average score of 10.81 for "Logged GDP per capita", 0.93 for "Social support", and 72.33 for "Healthy life expectancy."** 

### 3) Which countries have ranked/scored top 5 in happiness from 2019 to 2022? Do you observe any patterns?
1. In the "2019" sheet, sort the "Overall rank" column from A to Z, arranging the data in ascending order from the lowest number, or the top rankings. 
!['Top Rank/Score','Top Rank/Score'](/3a.png)
2. In the "2020" sheet, sort the "Ladder score" column from Z to A, arranging the data in descending order from the highest score.
!['Top Rank/Score','Top Rank/Score'](/3b.png)
3. In the "2021" sheet, sort the "Ladder score" column from Z to A, arranging the data in descending order from the highest score. 
!['Top Rank/Score','Top Rank/Score'](/3c.png)
4. In the "2022" sheet, sort the "RANK" column from A to Z, arranging the data in ascending order from the lowest number, or the top rankings. 
!['Top Rank/Score','Top Rank/Score'](/3d.png)
* **Finland and Denmark respectively ranked the top two happiest countries in all four years (2019 to 2022) consecutively. Iceland, Switzerland, Norway, and Netherlands are also consistently in the top 5 range as well.**

### 4) In 2022, which countries gave the highest score for each of the categories: GDP per capita, social support, healthy life expectancy, freedom to make life choices, generosity, and perceptions of corruption?
1. In the "2022" sheet, create a pivot table.
2. In the pivot table, set the "Values as" to "columns" and add "Explained by: GDP per capita", "Explained by: Social support", "Explained by: Healthy life expectancy", "Explained by: Freedom to make life choices", "Explained by: Generosity", and "Explained by: Perceptions of Corruption" and set each "summarize by" to "MAX."
3. To set up for the VLOOKUP function, go to "2022" sheet and move the "Country" column to the right of the "Explained by: Perceptions of corruption" column.
4. Go back to the pivot table sheet and use the VLOOKUP function to fill in the countries which correspond to the the highest score (maximum value) in each of the categories. In order to do this, the search key would be the maximum value for each category ("2209" or cell A2 for "MAX of Explained by: GDP per capita"), the range would be from the column which the search is being made ("Explained by: GDP per capita" or column C in this example) until the "Country" (column I), index would be the number of the "Country" column counting from the left ("7" in this example), and the "[is sorted]" would be "false."  
!['2022 Highest Category','2022 Highest Category'](/4.png)
* **In 2022, Luxembourg gave the highest score for GDP per capita, Iceland for social support, Hong Kong S.A.R. of China for healthy life expectancy, Cambodia for freedom to make life choices, Indonesia for generosity, and Singapore for perceptions of corruption.**

### 5) What was the percentage change in the ladder score from 2021 to 2022 for Finland, Denmark, Iceland, Switzerland, and the United States?
1. In the "2022" sheet, create a pivot table.
2. In the pivot table, set the row to "Country name."
3. In the filters option, unselect all other countries except for Finland, Denmark, Iceland, Switzerland, and the United States.
4. In the values option, add "Ladder score" and summarize it by "AVERAGE."
5. In order to add in the ladder scores from 2020, use VLOOKUP in the cell directly to the right of Denmark's average ladder score. The search key would be the country name ("Denmark" for example), the range would be from the "Country name" column to the "Ladder score" column, index would be "3", and the "[is sorted]" would be "false." Then drag the formula down to apply to the other countries. Name this column "2020."
6.  In order to find the percent change, follow the "(NEW-OLD)/OLD) x 100" formula, so for first country Denmark, it would be "B2" or "7.62" minus "C2" or "7.65", divided by "C2". Then you can name this column "Percent change" and highlight all the values under it and format them as a percent.
!['Percent Change','Percent Change'](/5.png)
* **From 2021 to 2020, Denmark decreased in their ladder score by 0.33% while the other countries increased such as 0.66% by Iceland and 0.16% by the United States.**

### 6) In 2022, what is the percent difference of Finland's happiness score, GDP per capita, social support, healthy life expectancy, freedom to make life choices, generosity, and perceptions of corruption compared to the average of all the countries in each of these categories. 
1. In the "2022" sheet, highlight the number data for "Happiness score" and use the functions to calculate the average. 
2. To calculate the average for the rest of the categories, just drag the bottom right corner of the cell which just calculated the average for the happiness score to the right, with the last cell outputting the average for the perceptions of corruption. In the cell to the left of the newly calculated data, type in "Averages" to label the row.
3. Copy the same seven columns from the "Finland" row and paste it below the averages. In the cell to the left of the copied Finland data, type in "Finland" to label the row.
4. Highlight these two rows of data retrieved, copy it, and paste it onto a new sheet.
5. Copy the corresponding column headers and paste them into the new sheet.
6. In the new sheet, in the row below the Finland data, add a function which would divide the Finland data by the average data and then substract that by 1 (For the "happiness score" column, it would "=((B3/B2)-1)" which would result in "=((7821/5,553.58)-1)". Drag this function to the right so that it applies to the rest of categories. Label this new row "Percent Differences"
7. Highlight the "Percent Differences" row and format as percent.
!['Percent Difference','Percent Difference'](/6.png)
* **Generally, Finland has a much higher positive percent difference in each of the categories, compared to averages of all the countries. For example, it is 40.83% higher in happiness score, 42.3% in freedom to make life choices, and, most significantly, 245% in perceptions of corruption. As [Gallup World Poll noted](https://worldhappiness.report/ed/2019/changing-world-happiness/), "for corruption a higher rank means a lower perceived frequency of corruption"**

