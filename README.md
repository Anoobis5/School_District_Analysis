# School_District_Analysis

## Project Overview: the School District Analysis
The purpose of this project is to analyze the data of an entire School District. We were tasked with analyzing and organizing the data to display factors such as: school funding breakdown, the average student scores across math and reading, and their passing rate in order to gain insights that will illustrate each school's perfomance for analysis. We were also tasked to uphold state-testing standards and reconduct the analysis due to potential academic dishonesty among a group of students.

## Analysis Results

The School Board has noticed possible evidence of academic dishonesty among the ninth grade students of Thomas High School. In our original analysis, we included the full set of student for every school in the district. For our second analysis, as requested by Maria and the School Board, we omitted Thomas High School calculations from our analysis. We used .loc functions to select and replace all of the 9th grade scores to NaN. See below for both a sample and grade view of the School District DataFrame with the 9th grader's scores replaced with Nan:

![9th grader NaN sample](https://user-images.githubusercontent.com/84881187/124371770-ffaeb200-dc52-11eb-8f1b-b2ff854a2971.PNG)
![9th grader scores RnM NaN](https://user-images.githubusercontent.com/84881187/124371771-01787580-dc53-11eb-9356-f1a44a7e0ae5.PNG)




Replacing the ninth graders' math and reading scores with NaN resulted in the following changes in Thomas High School's performance relative to other schools:
  1. The overall passing percentage for the entire district fell to 64.9%
![THS_Performance_post_edit](https://user-images.githubusercontent.com/84881187/124371846-c9bdfd80-dc53-11eb-9393-be8f64951974.PNG)

  2. The overall passing percentage for Thomas High School fell to 65%
![THS Overall](https://user-images.githubusercontent.com/84881187/124372595-6040ed80-dc59-11eb-87af-5d363b0a6dc6.PNG)

 3. The Top Five Schools list still included Thomas High School, despite the omitted scores.
![top 5 schools](https://user-images.githubusercontent.com/84881187/124372024-7e0c5380-dc55-11eb-8d92-280c91c124ed.PNG)
![bottom 5 schools](https://user-images.githubusercontent.com/84881187/124372025-7f3d8080-dc55-11eb-83cf-5d42dbac95b7.PNG)

When we omitted the ninth graders' of Thomas High School scores, it resulted in the following changes:
1. The overall passing percentage of Thomas High School dropped by 0.1%
2. The average scores for math at Thomas High School decreased by 0.2%
3. The avergae scores for reading at Thomas High School decreased be 0.3%
4. The overall passing percentage for schools within the school spending range of $630-$644 (per student) decreased by 0.2%


Please see below for the Original Analysis Scores vs. the Refactored Analysis Scores for comparison:


_[Original Analysis]_
![Original District Scores](https://user-images.githubusercontent.com/84881187/124372850-97180300-dc5b-11eb-96f1-1f24e9c602be.PNG)
_[Updated Analysis]_
![updated district scores](https://user-images.githubusercontent.com/84881187/124372852-997a5d00-dc5b-11eb-949d-7be010150e28.PNG)

_[Original Spending Scores]_
![Original Spenging Scores](https://user-images.githubusercontent.com/84881187/124372929-3d640880-dc5c-11eb-8588-55a9ecad1ff6.PNG)

_[Updated Spending Scores]_
![School Spinding Scores](https://user-images.githubusercontent.com/84881187/124372903-00981180-dc5c-11eb-8563-cf0ad5ae48d8.PNG)

### School Funding, Size, and Type

In part to the fact that the changes in scores results in less than 1% shifts, School Size and School Type were not affected by the changes made to our analysis. Our analysis also found that Average Scores and Passing Percentage do not increase as spending per student increases. The top scoring schools in the district received less per strudent than the lowest performing school. This could imply that there are other variables at play than funding that decide the average student scores. 
![spending ranges per student](https://user-images.githubusercontent.com/84881187/124373359-c0d32900-dc5f-11eb-81c8-a4774b834ef8.PNG)


However, when it comes to school size, 'Large' schools (over 2,000 students) have the lowest average scores and passing percentage. There is a minimal difference in performance (1%) between 'Small' and 'Medium' schools in the district. This may indicate that factor of success/passing rate may be that students learn and perfom better in smaller, more intimate class settings. 
![School Size](https://user-images.githubusercontent.com/84881187/124373353-b3b63a00-dc5f-11eb-9b2e-29e739fd5236.PNG)

When it comes to the data between Types of schools, we see that Charter schools perform better overall than District schools in this school district (about 35% better overall). Please see below for the DataFrame excerpt of the School Type DataFrame:


![School Type](https://user-images.githubusercontent.com/84881187/124373386-f11ac780-dc5f-11eb-8fa5-5629aa2f31d6.PNG)

After Analyzing the average scores for math and reading for each grade across each school, we found that students grade levels do not affect their scores as much as other variables regarding the school that they attend. Please see below for a DataFrame except of scores be grades in both Math and Reading:



![math grades across schools](https://user-images.githubusercontent.com/84881187/124390853-767f9580-dcbb-11eb-8f29-18ce98d9a4e8.PNG)
![reading grades across schools](https://user-images.githubusercontent.com/84881187/124390857-78e1ef80-dcbb-11eb-881a-1e6c4d67f574.PNG)





## Analysis Summary

The School Board notified us of the potential academic dishonesty. Unfortunately, our data does not allows us to determine which individual students were responsible for the discrepancies with the Thomas High School overall scores. This resulted in the decision to omit the all the 9th Grade Scores from Thomas High School from the complete data set. While leaving the known false data in would create an inaccurate data set, omitting the data also limits us from having the most accuate results of the school district's performance. 

By replacing the 9th graders' scores to NaN, Thomas High School's overall passing percentage, and average reading scores declined. The reading and math scores for the whole district also saw a decrease in their averages.  Even with the 9th grade data omitted, we were still able to draw some useful conclusions to help guide the School Board's decisions for th next year. We saw that even with the omitted data dropping Thomas High School's averages, they remained in the Top 5 Schools in the district. Our analysis of the grade averages for Reading and Math across each school showed that there were minimal differences in grade scores between each grade, but there were more significant differences in grade scores between schools. We did observe a slight drop in overall performance for schools withing the  $630-$644 (per student) spending range with the omitted data. However, by analyzing the School Funding Per Student data, we were able to see that higher funding per student did not results in better grade scores. In fact, the 'Bottom 5' schools had higher average funding per student than the Top 5 schools in the district. A more notable factor that appears to affect grade scores is school size. The scores did not change despite the omitted data between school sizes, but we can see that 'Large' schools have lower average scores than both 'Small' and 'Medium' sized schools. 

Our data provides a visual representation of school perfomance across the entire school district. We were able to omit some erroneous data, and provide as accurate a depeiction of the score averages as possible. The school board will be able to use our data to make necessary changes to improve education quality and scoring within this school district. 
