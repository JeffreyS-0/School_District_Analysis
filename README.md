# School_District_Analysis

## Overview
I was hired by one of the cities school board members, Maria. Our purpose was to analyze the city school data and present the academic performance of each school based on different metrics like: school size, type of school, and budget per student. After completing the analysis, the school board notified Maria and her supervisor that the "students_complete.csv" file showed evidence of academic dishonesty within the 9th graders math and reading scores at Thomas High School. With this new found information, the analysis needed to be completed again. However, this time we needed to replace all of the math and reading scores for the 9th graders at Thomas High School with "NaN" and re-run the code to get an accurate representation of data for the city schools. 

## Results
#### District Summary
  - The district summary is the least affected by the change in data. The district covers 15 schools and 39,170 students. The 461 students that are in the 9th grade at Thomas High School account for a total of 1.177% of all the students in the district. The difference in math and reading scores across the district is negligible. See the figures below; the first dataframe is from the original code with the dataset unchanged. The second dataframe is after the 9th graders math and reading scores at Thomas High School have been removed. As you can see, the difference in math and reading scores is hardly noticeable.
![District_summary_b4_audit](https://user-images.githubusercontent.com/69607218/133905780-3f2d10d9-a1bb-41b2-9d99-49b35db15682.png)
![District_summary_after_audit](https://user-images.githubusercontent.com/69607218/133905786-0340191a-061e-40d1-8c9d-a2c7b6bf091a.png)

#### School Summary
  - The school summary shows the details of each school individually. The only data that changed was that for Thomas High School, since the 9th grade math and reading scores were nulled out from this school only. See the figures below; the first dataframe is from the original code with the dataset unchanged. The second dataframe is after the 9th graders math and reading scores at Thomas High School have been removed. 

##### Before Audit
![School_summary_b4_audit](https://user-images.githubusercontent.com/69607218/133909501-89fd4501-144d-41fd-b431-15c3e302a409.png)
##### After Audit
![School_summary_after_audit](https://user-images.githubusercontent.com/69607218/133909512-fa474c3d-4790-4a76-9ba1-7dfe5ef24400.png)
  - As you can see, the average math and average reading scores for the school didn't change much. However, the passing percentage for math, reading and overall has drastically changed because we have an entire grade of students that are being accounted for, but their grades are not. In order to have a better representation, lets remove the 461 students and their grades from the equation and re-run the dataframe.

##### After Removing the 9th graders
![School_summary_after_removing_ninth_graders](https://user-images.githubusercontent.com/69607218/133909621-05904dff-7a3e-4206-82ea-18bbbd5b7261.png)
  - As you can see, our percentages for passing math, reading and overall have gone back to what they were before doing the first audit.

#### Thomas High School's performance vs. Other Schools
  - At first, we saw that replacing all of the 9th graders scores with NaN's didn't effectively change the averages for math and reading scores, because "NaN" isn't considered a number in the computer for it to average in with the other numbers. However, the computer does know that "NaN" is not something that is greater than or equal to 70, and therefore, counts the student as failing. This is why we saw a drastic decrease in % Passing Math, % Passing Reading, % Passing Overall for Thomas High School. It wasn't until after re-coding the same dataframe with just removing the 9th graders at Thomas High School, that we saw the % Passing sections go back up to 90%+. Overall this places Thomas High School in the top 5 performing schools in the district!

![Top_5_schools](https://user-images.githubusercontent.com/69607218/133910033-47da45fc-83ec-4d39-bdb1-97d210584df6.png)

#### Math & Reading by Grade
  - The math and reading scores by grade, show you each grade level's average math and reading scores for all 15 schools in the district. By replacing the 9th graders scores with "NaN" at Thomas High School, there is nothing to compare those 461 9th graders to. You can easily compare and evaluate all of the other grades and schools to each other. However, looking at the datasets below, you can make a prediction that the average grade for the 9th graders at Thomas High for math would likely be in the high 70's to low/mid 80's range. While the average reading score is likely to be in the mid 80's.

##### Math Scores By Grade
![Math_scores_by_grade](https://user-images.githubusercontent.com/69607218/133935464-201e3189-b4ce-4463-a528-78e51e78901f.png)
##### Reading Scores By Grade 
![Reading_scores_by_grade](https://user-images.githubusercontent.com/69607218/133935484-d83619cf-9e0b-43da-81ff-9a6cd7a9a51c.png)

#### Scores By School Spending
  - When evaluating the data regarding the school spending per student. We can easily compare the students average grades and their passing percentages to the amount of money the school is spending on each child. As we analyze this data we can easily see that the schools with the worst academic track record, have the highest spending per student. 

![Scores_by_school_spending](https://user-images.githubusercontent.com/69607218/133935835-7bb6b49f-238e-45cf-b5a8-3e85e2590e6a.png)

#### Scores By School Size
  - Now, when looking at the school size in comparison to the average scores. We can see a much better correlation to population and lower grade scores. As you can see below, as the population ranges for the schools get bigger, the average grades and % passing falls. This shows that with less students, there are smaller classroom sizes and therefore more students are able to get the 1 on 1 tutoring they might need, or that there are lot less distractions within a given classroom.

![Scores_by_school_size](https://user-images.githubusercontent.com/69607218/133935999-f182fbc3-4bc7-426f-bb1e-a503d79a16fd.png)

#### Scores By School Type
  - This may come to no surprise to some. However, with our data, we can easily point out that the type of school can matter a lot on the academic education a student may receive. As we can see below, our data suggests that if you go to a Charter school, the likelihood that you will be passing both Math and Reading is significantly higher than if you were to go to a local District school. Now, this can be correlated with the School Size as well, since Charter schools are highly likely to be low populated schools in comparison to other District schools.

![Scores_by_school_type](https://user-images.githubusercontent.com/69607218/133936182-50e4df5c-488e-45a6-8029-b478c6a77c82.png)

## Summary
The District Analysis has only slightly changed from replacing the Thomas High School 9th graders, math and reading scores. As stated previously, the difference that the 9th grade students is almost negligible because the 461 students only make up 1.177% of the total student population (39,170) within the district. However, since changing their scores, we can calculate small changes as stated below.
  - Average Math Score Before Audit = 79 ---- Average Math Score After Audit = 78.9
 
  - % Passing Math Before Audit = 75 ---- % Passing Math After Audit = 74.8

  - % Passing Reading Before Audit = 86 ---- % Passing Reading After Audit = 85.7

  - % Overall Passing Before Audit = 65 ---- % Overall Passing After Audit = 64.9

