# Where are the happiest countries in the world and why?
## By Junta Naito

## Story Summary and Sourcing
For my story, I will be referencing the **[2019 to 2022 data set from the World Happiness Report](https://www.kaggle.com/datasets/mathurinache/world-happiness-report)** by the Gallup World Poll (GWP).

Every year the GWP conducts a World Happiness Report where they evaluate a country's level of happiness based on survey participants' self-reported responses about their quality of life. Respondents also assess six variables (GDP per capita, social support, healthy life expectancy, freedom, generosity, and absence of corruption) to explain the nuances and reasoning behind their evaluation for their respective countries. 

For the past four years (2019 to 2022), Finland and Denmark have consecutively been ranked as the top two happiest countries respectively. While there are certainly several factors contributing to a country's overall happiness, I found some noteworthy findings through my data analysis. First, by evaluating each countries' GDP per capita rankings, I observed that while those with low rankings did have a lower happiness score overall, the countries with higher rankings did not necessarily score higher in overall happiness. For example, although Singapore had the second highest score (of 2,149) for GDP per capita, it still ranked #27 in overall happiness. In conclusion, while a basic healthy economy may be a foundational standard for happiness, it was not the most influential factor for the top happiest countries. Dr. Shun Wang, professor of the KDI School of Public Policy and Management in South Korea, noted in a [New York Times article](https://www.nytimes.com/2021/04/20/world/europe/world-happiness-report-ranking.html) how although some Eastern European countries have relatively high income levels, it still ranked pretty low in overall happiness and vice versa for South America: despite having low income levels, they scored high in overall happiness. 

When comparing Finland's 2022 data to the averages among all the countries, Finland generally had a much higher positive percent difference but most significantly in their peoples' perceptions of corruption, being 245% more than all of the countries' average. This indicates that perceptions of corruption, which is based on one's views of their country's government and businesses, can significantly influence the country's overall happiness. Lastly, I compared the levels of happiness and its variables within the top countries and the United States during 2020 (before the pandemic) and 2021 (during the pandemic), and found that only Denmark decreased in the overall happiness score, while the others (Finland, Iceland, Switzerland, and the United States) increased. This is noteworthy to explore further and evalute what other variables may have shifted before and during the pandemic. 


### Contacts for Interviews
**1. Shun Wang | Professor, KDI School of Public Policy and Management**
* **Email:** swang@kdis.ac.kr
* **Phone Number:** +82 (44) 550 - 1109
* *Dr. Wang is one of the authors of the study and provided insightful commentary on the referenced New York Times' article.*

**2. John F. Helliwell | Professor Emeritus, Vancouver School of Economics, University of British Columbia**
* **Email:** John.Helliwell@ubc.ca
* **Phone Number:** 604-822-4953
* *Helliwell is one of the editors of the report and can offer deeper insight behind the numbers in the World Happiness Report, especially around the topic of COVID-19, as referenced in the additional source "Overview: Life under COVID-19".*

### Additional Sources

**1. [New York Times' "What Makes a Happy Country?"](https://www.nytimes.com/2021/04/20/world/europe/world-happiness-report-ranking.html)**
* This article provides a journalistic perspective of the World Happiness Report and expert voices on their analysis and interpretation of the data.

**2. [World Happiness Report's "Overview: Life under COVID-19"](https://worldhappiness.report/ed/2021/overview-life-under-covid-19/)**
* This report provides an in-depth anaylsis from the authors of the study about how COVID-19 has overall impacted the happiness of countries across the world.

## Data Visualization
Below is a choropleth map of the overall happiness scores from the 2022 data. Please note that not all countries were surveyed, and therefore, included into this data.
[!['2022 Happiness Map','2022 Happiness Map'](/2022HappinessMap.png)](https://datawrapper.dwcdn.net/cHX8N/2/)

## Data Analysis Process
Please refer to my [data analysis sheet](https://docs.google.com/spreadsheets/d/1nMtKNOb6AOntjbsMRxbIf5Id55MrybIcnP_VcXPXBuw/edit?usp=sharing) for further details.

### 1) In 2022, what rank and happiness score did the countries who had the top 5 highest score for GDP per capita receive? Top 5 lowest? 
1. In "2022" sheet, highlight the "Explained by: GDP per capita" column and drag it to the right of the "Happiness score" column.
2. Sort the "Explained by: GDP per capita" column from Z to A, arranging the data in descending order from the highest GDP per capita. 
!['Highest GDP','Highest GDP'](/1a.png)
* **In 2022, Luxembourg ranked the highest for GDP per capita with a score of 2,209, however, ranked #6 among the happiest countries with a happiness score of 7,404. Singapore had a sharper contrast, coming in second for GDP per capita with a score of 2,149 while ranking #27 in overall happiness and a score of 6,480.** 
3. Sort the "Explained by: GDP per capita" column from A to Z, arranging the data in ascending order from the lowest GDP per capita. 
!['Lowest GDP','Lowest GDP'](/1b.png)
* **As shown, the countries which ranked the lowest in GDP per capita, ranked lower overall in happiness. For example, Venezuela ranked the lowest in GDP per capita with a score of 0, and ranked #108 among the happiest countries with a score of 4,925.**

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
* **Finland and Denmark were consecutively ranked the top two happiest countries respectively in all four years (2019 to 2022). Iceland, Switzerland, Norway, and Netherlands were also consistently in the top 5 range as well.**

### 4) In 2022, which countries gave the highest score for each of the categories: GDP per capita, social support, healthy life expectancy, freedom to make life choices, generosity, and perceptions of corruption?
1. In the "2022" sheet, create a pivot table.
2. In the pivot table, set the "Values as" to "columns" and add "Explained by: GDP per capita", "Explained by: Social support", "Explained by: Healthy life expectancy", "Explained by: Freedom to make life choices", "Explained by: Generosity", and "Explained by: Perceptions of Corruption" and set each "summarize by" to "MAX."
3. To set up for the VLOOKUP function, go to "2022" sheet and move the "Country" column to the right of the "Explained by: Perceptions of corruption" column.
4. Go back to the pivot table sheet and use the VLOOKUP function to fill in the countries which correspond to the the highest score (maximum value) in each of the categories. In order to do this, the search key would be the maximum value for each category ("2209" or cell A2 for "MAX of Explained by: GDP per capita"), the range would be from the column which the search is being made ("Explained by: GDP per capita" or column C in this example) until the "Country" (column I), index would be the number of the "Country" column counting from the left ("7" in this example), and the "[is sorted]" would be "false."  
!['2022 Highest Category','2022 Highest Category'](/4.png)
* **In 2022, Luxembourg gave the highest score for GDP per capita, Iceland for social support, Hong Kong S.A.R. of China for healthy life expectancy, Cambodia for freedom to make life choices, Indonesia for generosity, and Singapore for perceptions of corruption.**

### 5) What was the percentage change in the ladder score from 2020 to 2021 for Finland, Denmark, Iceland, Switzerland, and the United States?
1. In the "2021" sheet, create a pivot table.
2. In the pivot table, set the row to "Country name."
3. In the filters option, unselect all other countries except for Finland, Denmark, Iceland, Switzerland, and the United States.
4. In the values option, add "Ladder score" and summarize it by "AVERAGE."
5. In order to add in the ladder scores from 2020, use VLOOKUP in the cell directly to the right of Denmark's average ladder score. The search key would be the country name ("Denmark" for example), the range would be from the "Country name" column to the "Ladder score" column, index would be "3", and the "[is sorted]" would be "false." Then drag the formula down to apply to the other countries. Name this column "2020."
6.  In order to find the percent change, follow the "(NEW-OLD)/OLD) x 100" formula, so for the first country, Denmark, it would be "B2" or "7.62" minus "C2" or "7.65", divided by "C2". Then you can name this column "Percent change" and highlight all the values under it and format them as a percent (which takes care of the "x 100" part of the formula).
!['Percent Change','Percent Change'](/5.png)
* **From 2021 to 2020, Denmark decreased in their ladder score by 0.33% while the other countries increased, such as 0.66% by Iceland and 0.16% by the United States.**

### 6) In 2022, what is the percent difference of Finland's happiness score, GDP per capita, social support, healthy life expectancy, freedom to make life choices, generosity, and perceptions of corruption compared to the average of all the countries in each of these categories. 
1. In the "2022" sheet, highlight the number data in the "Happiness score" column and use the functions to calculate the average. 
2. To calculate the average for the rest of the categories, just drag the bottom right corner of the cell which just calculated the average for the happiness score to the right, with the last cell outputting the average for the perceptions of corruption. In the cell to the left of all the newly calculated data, type in "Averages" to label the row.
3. Copy the cells from the same seven columns and the "Finland" row and paste it below the averages. In the cell to the left of the copied Finland data, type in "Finland" to label the row.
4. Highlight these two rows of data retrieved, cut it, and paste it onto a new sheet.
5. Copy the corresponding column headers from the "2022" sheet and paste them into the new sheet.
6. In the new sheet, in the row below the Finland data, by using the "((X/Y –1) x 100)" to calculate percent differences, add a function which would divide the Finland data by the average data and then substract that by 1 (For the "happiness score" column, it would "=((B3/B2)-1)" which would result in "=((7821/5,553.58)-1)". Drag this function to the right so that it applies to the rest of categories. Label this new row "Percent Differences"
7. Highlight the "Percent Differences" row and format as percent (which takes care of the "x 100" part of the formula).
!['Percent Difference','Percent Difference'](/6.png)
* **Generally, Finland has a much higher positive percent difference in each of the categories, compared to averages of all the countries. For example, it is 40.83% more in happiness score, 42.3% in freedom to make life choices, and, most significantly, 245% in perceptions of corruption. As [Gallup World Poll noted](https://worldhappiness.report/ed/2019/changing-world-happiness/), "for corruption a higher rank means a lower perceived frequency of corruption"**
