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


