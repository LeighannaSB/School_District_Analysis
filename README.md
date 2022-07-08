# School District Analysis

### Reconfiguring district wide testing results to account for academic dishonesty

## Overview

The local schoolboard found evidence of academic dishonesty in the reported 9th grade math and reading testing scores for one of the local schools, Thomas High Schoo. In order to adhere to the state testing standards, the compromised 9th grade scores had to be removed from the district wide data report and the report re-analyzed. In this report we will show how the compromised scores were removed, the data re-analyzed, and how the results were changed by removing the dishonest scores.

## Process and Results

The testing data was pulled from a CSV and was used to create a data frame with all the student info. Then the loc method was used to replace all of the math and reading test scores from Thomas High School 9th graders with NaN as shown below.
![image](https://user-images.githubusercontent.com/107161421/177902907-d97f1397-e9da-4221-a604-8234a967f926.png)
![image](https://user-images.githubusercontent.com/107161421/177903026-33226d48-b7ee-48ef-a118-d5bbae23b29d.png)
![image](https://user-images.githubusercontent.com/107161421/177903118-b0dd3413-5986-422b-a57e-1defe73b01f9.png)

The total student count was adjusted to remove the Thomas High 9th graders and the passing percentages were recalculated using the new student count. This new information was then used to create an updated district summary dataframe. 
![image](https://user-images.githubusercontent.com/107161421/177903674-27bd1366-d717-456b-aac2-511cbe4d83a4.png)
![image](https://user-images.githubusercontent.com/107161421/177903813-8cd7aa23-a162-4c79-bc56-ce5626d848ef.png)

A data frame was created to show the school type, student count, budget (total and per student), and test results for each school in the district:
![image](https://user-images.githubusercontent.com/107161421/177904377-c44f1df9-1864-482e-8980-51b949900030.png)

The results for Thomas High in the above data frame needed to be reworked to account for the removal of the 9th grade students. In order to complete this task a new student count for Thomas was calculated using only the 10th-12th grade students. This count was then used to recalculate the correct passing percentages for Thomas High.
![image](https://user-images.githubusercontent.com/107161421/177904883-bebf8270-5b36-4506-a5e8-e419af8cb4d4.png)
![image](https://user-images.githubusercontent.com/107161421/177904986-5d9df408-9ca6-449a-b05f-7018c606ad41.png)
![image](https://user-images.githubusercontent.com/107161421/177905059-7e72a9fc-b32a-414a-b521-548bda6a215c.png)
![image](https://user-images.githubusercontent.com/107161421/177905121-bb57762b-87bb-4695-acd2-868be7af8057.png)

The loc method was then used to update the Thomas High results in the School Summary data frame:
![image](https://user-images.githubusercontent.com/107161421/177905238-7378e36a-ce51-44c3-8a4e-5e9a399bd23a.png)

## Results

Updating the scores for Thomas High resulted in several changes in the district wide results:
* The school's percentage of students passing Math went up to 93.19 from 66.91
* The school's percentage of students passing reading went up to 97.02 from 69.66
* The school's percentage of students passing overall went up to 90.63 from 65.08
* Thomas High moved from the bottom of the district wide ranking to the 2nd highest overall passing position
![image](https://user-images.githubusercontent.com/107161421/177906240-7c78fb25-1585-495f-8071-2ac0a866a2d0.png)

The schools size and spend per student were also calculated and compared to their test results as shown below:
![image](https://user-images.githubusercontent.com/107161421/177906807-4ccd3f76-21b1-4b34-9b25-e7e93b6dd7e8.png)
![image](https://user-images.githubusercontent.com/107161421/177906862-9b5f4aed-ffb6-4ee0-82db-486ded67e7af.png)
![image](https://user-images.githubusercontent.com/107161421/177906896-4812ab11-8533-4d5f-9bb4-6622097221f3.png)

The district schools were also broken out by their school type to compare the test results:
![image](https://user-images.githubusercontent.com/107161421/177907010-279d6af7-bc75-4f93-8040-cad457c44f28.png)

