# Deliverable 3: Analysis 
## 1. Overview of Project
Performing analysis and visualizing data on how different Kickstarter campaigns under the theater category fared in relation to their launch dates and their fundraising goals.  

## 2. Analysis and Challenges
Analysis was performed through filtering, formatting, and creating visuals from a database that encompasses all Kickstarter campaigns to propose a conclusion to a bussiness query. Database was formatted and filtered acording to the required elements that best display the fundraising goals and launch dates. Analysis was focused on parent category, years, goal, and outcomes based on %. Data was visualized in two figures below.

Figure 1.0: Theater Outcomes by Launch Date provides a visual comparison of how theater Kickstarter campaigns did in relation to their launch dates. The results below was achieved through filtering data in a pivot table to Theater, Years (in months) and outcomes as the column. 
![Theater Outcomes by Launch Date](https://github.com/just-yen/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

Figure 2.0: Outcomes vs Goals displays a visual representation and breakdown of how theater Kickstarter campaigns in relation to their fundraising goals. The visual representation was created through breaking down goal categories and using a =countifs function in the database to populate the categories. 
![Outcomes vs Goals](https://github.com/just-yen/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

Challenges faced was optimizing methods to populate data correctly and efficiently. The results acheived in figure 2.0 would have been time consuming to populate the categories. Especially since the formula would have to be manually adjusted for each category. To create a more efficient method, the following formula was used: *=COUNTIFS(Kickstarter!$F:$F,"=Successful",Kickstarter!$D:$D,">='&Value($B2),Kickstarter!$D:$D,"<="$Value($C2))*. A text to column method was used to break down the Goal categories which populated under Columns B and C. This allowed the formula to convert the category range into a value. With the $ in front of range criteria this allowed the forumla to be easily replicated throughout the whole table. 

## 3. Results 
#### Conclusion: Theater Outcomes by Launch Date (Figure 1.0)
a) There is more successful theater outcomes launches then failed outcomes overall and per month.

b) The months between May and August have the greatest amount of total theater based Kickstarter campaigns. 

#### Conclusion: Outcomes based on Goals (Figure 2.0)
a) Most successful outcomes are based in the Less than 1000 category. 

b) There is an above 50% successful outcome rate in two categories. Less than 1000 and 1000 to 4999. 

### Limitations 
The dataset provides a good overview and provides easy to understand numbers. However, with respect to a client querying of "how different campaigns fared in relation to their launch dates and their funding goals" the analysis does not provide the full picture. For an example, within the theater category itself there are endless amounts of genres. There is a possibility of misinterpretation of data since there may be the possibility that the most successful outcomes are more frequently correlated to a musical genre or comedy. Without understanding the full picture, it could lead to a costly business decision as the assumption that the project will be most likely funded if the goal is less than $1000 and it is launched outside of the May - Aug period. However, without the full picture and a expanded data set the results may be the opposite of what the initial assumption was. Another limitation could be extended to the lack of statistical inference the data set itself. There were no outlier calculations completed to test any trends at risk of being skewed significantly. 

A possible table and graph that can be added is a more in-depth breakdown of Theater Outcomes by Launch Date and Outcomes based on Goals. For an example, the dataset used contained launch years from the 1900 to 2017. It may be useful to either eliminate any data points that extend beyond 10 years or less. Factors such as currency value has changed and therefore does not accurately reflect the current monetary value. This could cause misinterpretation of data. Alternatively, a breakdown of the year specifically can be displayed in the table as well. This will help inform the audience of the full picture and not misguide them based on one graph or table. 
