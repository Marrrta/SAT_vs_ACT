### Project 1: Standardized Test Analysis

### Problem Statement

The SAT (Scholastic Aptitude Test) and the ACT (American College Testing) are standardized tests used by many colleges and universities in the United States in their admissions process. The two tests are largely equivalent: both are available to students in all US states and neither is considered prefered by the ultimate consumers of the test results: the schools' admissions committies.

This project attempts to validate the need for two separate standardized aptitude tests used for college admissions in the USA. By examining the popularity and results of both SAT and ACT across all states, as well as the acceptance requirements of top academic institutions in the country that involve these tests, the analysis:

1. Evaluates the reasons for both tests to be maintained;

2. Sizes the opportunity to switch to either only SAT or ACT, either US-wide or for select states;

3. Assesses the differences in distribution of results to determine whether the (inconsistent) claims that one of the tests is "easier" than the other are justified;

4. Provides insight for high school students as they choose between SAT and ACT in order to get accepted to their prefered college.


### Summary

...


### Data Dictionary

|**Feature**|**Type**|**Dataset**|**Description**|
|:---|:---|:---|:---|
|state|string|sat_all.csv|Name of US state where SAT is administered|
|participation|float|sat_all.csv|Percentage of eligible students who take the SAT in each state|
|total_sat|int|sat_all.csv|Average total (composite) SAT score of students in each state|
|total_norm_sat|float|sat_all.csv|Average total (composite) SAT score of students in each state, normalized using min-max method|
|year|int|sat_all.csv|The year (2017/2018/2019) covered in listed dataset|
|state|string|act_all.csv|Name of US state where ACT is administered|
|participation|float|act_all.csv|Percentage of eligible students who take the ACT in each state|
|total_act|float|act_all.csv|Average total (composite) ACT score of students in each state|
|total_norm_act|float|act_all.csv|Average total (composite) ACT score of students in each state, normalized using min-max method|
|year|int|act_all.csv|The year (2017/2018/2019) covered in listed dataset|
|school|string|sat_act_by_college_mod.csv|Name of a U.S. college|
|number_of_applicants|integer|sat_act_by_college_mod.csv|The number of students applying to the college in a year|
|accept_rate|float|sat_act_by_college_mod.csv|Percentage of applicants accepted to the college|
|sat_norm_25th|float|sat_act_by_college_mod.csv|Lower bound of interquartile range of normalized SAT scores for students accepted to school|
|sat_norm_75th|float|sat_act_by_college_mod.csv|Upper bound of interquartile range of normalized SAT scores for students accepted to school|
|act_norm_25th|float|sat_act_by_college_mod.csv|Lower bound of interquartile range of normalized ACT scores for students accepted to school|
|act_norm_75th|float|sat_act_by_college_mod.csv|Upper bound of interquartile range of normalized ACT scores for students accepted to school|


### Key Observations

...

### Conclusions and Recommendations

...

---

### Next Steps

Additional ...:
- ...


---
