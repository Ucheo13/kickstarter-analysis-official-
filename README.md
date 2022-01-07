# kickstarter-analysis 

## Overview
Louise’s play Fever was near its fundraising goal in a relatively short amount of time. She wanted to compare her play to other campaigns focusing on their launch dates and their funding goals. The purpose of this analysis is to help Louise organize this information into visuals that are easily comprehended using the Kickstarter dataset.

## Analysis and Challenges
To get the outcomes based on launch date I had to perform my analysis using a pivot table with certain titles placed specifically. Date Created Conversion was attached to the rows, outcomes attached to the columns, categories and years placed as filters, and count of outcomes in sum of values. This allowed me to filter based on theatre and create a line graph showing the number of successes, failures, and cancellations in each month.
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/96452277/148588993-f83fad0f-00d2-4470-95a5-fb272fcbe2d9.png)

In order to get the outcomes based on goals I had to find how many successes, failures, and cancellations there were for each goal range for the ‘plays’ category. To perform this analysis I needed to use the COUNTIFS() function to accurately count the amounts needed for each section. An example of code used for the goal range of 35000 to 39999 is =COUNTIFS(Kickstarter!$D:$D,"<=39999",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,">=35000",Kickstarter!$R:$R,"plays"). This looks for the number of successes with the goal range specified. Each condition must be true for the count to increase. Is the goal under or equal 39999, is the outcome successful, is the goal over or equal 35000, and is the subcategory plays? After deciphering how many successes and failures there were I calculated the percentages simply by summing the total projects in the goal range and using that number to divide the number of successes, failures, and cancellations separately. Using the goals column and the three percentage columns I created the line graph that you see below.
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/96452277/148589067-52754fdc-5c6f-4cb4-9b92-8f51f7afc2b4.png)

I did not encounter much of a challenge, but there are certainly challenges that could have been met. For example, when using the COUNTIFS() function there are little details that you need to pay close attention to in order to ensure the results come out the way you need them to. Whether it is the dollar signs on the rows or the equal or greater/less signs where you need them to be, these details could be looked over. 

## Results
One conclusion that is very clear in the outcomes based on launch date is that there is a peak in successful outcomes in the early summertime, starting from May and ending in August. But the number of successes may be deceiving from the fact that there are more total data points during these months. With more total data points there is not much of a surprise that the total number of successes is higher than the rest of the months. But there is also the fact that failures do not differ too much in comparison to successes throughout the seasons. The peak proportion should potentially be similar if the number of successes were only based on quantity of data points and not the true performance during the summer. Another conclusion is that no matter the season there are not many canceled performances. The number stays nearly consistent from January to December.

One observation in the line graph is that the percentage successful and the percentage failed is a mirror image of one another. This is no surprise because the percentage cancelled remains zero throughout the entire graph. Where percentage successful is higher at a goal of less than 1000 and around goals from 35000 to 44999. But at 45000 to 49999 the graph shows 100% percentage failed. There is no where else that touches 100%. I can conclude that it is harder to reach higher goal numbers. 

One limitation of this dataset is that not all the currencies are the same. Yet we are treating the Outcomes Based on Goals as if all the currencies are equivalent. Even with a small difference in the currencies it effects the true accuracy of our results. Another graph that could have possibly been used is a stacked bar graph. This would also portray the same message, but a line graph is the optimal graph for such data. This data shows how outcomes were over time and over an increased goal. Using a line graph makes it very easy to see the trend over time which is why it is the preferred method to use. 

