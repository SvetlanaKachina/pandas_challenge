# pandas_challenge

In order to get to the core of our analysis, we had to, first, complete District Summary:
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.
Identify Total number of unique schools and Total students using "merge" to combine both csv files.
Then, in a new data frame we needed to calculate Total budget by summarizing all of schools' budgets.
Calculating Average math score and Average reading score, using "mean", allowed us further to receive % passing math (the percentage of students who passed math)
and % passing reading (the percentage of students who passed reading), as well as % overall passing (the percentage of students who passed math AND reading) by simple math formula.

For School Summary
In order to create a DataFrame that summarizes key metrics about each school, we started with columns that contained School name, School type, Total students, Total school budget, Per student budget, Average math score, 
Average reading score, % passing math (the percentage of students who passed math), % passing reading (the percentage of students who passed reading), % overall passing (the percentage of students who passed math AND reading).
We started with set_index, following with groupby function, following with simple math calculations.

Following with creation of DataFrame called "per_school_summary" we were able to get a table with school_name being a unique value in the first column, following with per school summary in all other columns. 

In order to obtain information about the first 5 "Highest-Performing Schools (by % Overall Passing)" we used sort_values from the information we obtained above, while having ascending at False.
Similarly, we received "Lowest-Performing Schools (by % Overall Passing)", using same sort_values, but this time with ascending being True.

Math Scores by Grade
We, at first need to pull data of (th, 10th, 11th and 12th grades for each school and then obtain an average(mean) of the math scores for each school for them, using groupby, 
following by combining received information into single DataFrame "math_scores_by_grade".

We repeat the process to obtain Reading Scores by Grade.

In order to see Score by School Spending, we use pd.cut  and astype.
At last, in order to begin our analysis, we have sorted Scores by School Size and by School Type, using labels, and groupby.


Summarizing the report, we can draw few conclusions, based on the information we received.
First of all, % Ovaerall Passing in the latest table is clearly indicating Charter Schools to be at much higher level than District. Saying that, we cannot conclude that District Schools are that much worse, because when we compare % Passing Reading , though different, but is acceptable being over 80% in both Charter and District schools. Looking further at the same table, is bringing us to the conclusion that % Passing Math affects % Overall Passing tremendously as there's almost 30% gap between Charter and District Schools. 
Clearly, District Schools don't have something that Charter schools do in Math comprehension.
If we look at the table above, we would notice that while Medium and Small sized school % Passing Math is over 93%, large Schools suffer at below 70%. One would think that large schools require larger spending per student and would be wrong, 
cause Table of Spending Ranges (Per Student) clearly shows that for schools where % Passing Math is the highest, we observe the lowest Spending Range (<%585). So, Budgeting is not the case.  
How about we look at the table of Bottom Performing Schools ( By % overall Passing)?
We observe that bottom five schools are all District schools large in size and their % Passing Math is quite low. 
Stating that, we discovered, that budgeting is not the problem; however, large schools tend to have larger classes per student and social hierarchy that might affect students performance. 
We would recommend to get information about school math size classes for all district schools to see if there's an obvious benefit in having smaller classes.
