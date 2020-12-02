### Project 1: Standardized Test Analysis

### Problem Statement

The SAT (Scholastic Aptitude Test) and the ACT (American College Testing) are standardized tests used by many colleges and universities in the United States in their admissions process. The two tests are largely equivalent: both are available to students in all US states and neither is considered prefered by the ultimate consumers of the test results: the schools' admissions committies.

This project attempts to validate the need for two separate standardized aptitude tests used for college admissions in the USA. By examining the popularity and results of both SAT and ACT across all states, as well as the acceptance requirements of top academic institutions in the country that involve these tests, the analysis:

1. Assesses feasibility of converging onto one standard (either only SAT or only ACT);

2. Evaluates if one of the tests can be generally considered easier than the other;

3. Determines if either the SAT or the ACT is better for “elite school”* candidates.

*For the purpose of this project, “elite schools” are defined as those which are both popular among students (high # of applicants) and selective (low acceptance rate) 

### Executive Summary

The notebook reads in the 2017-2019 SAT and ACT datasets with information about participation and average scores, by state, as well as the dataset of 405 US colleges and universities, with information about number of applications, acceptance rates, and SAT / ACT scores for accepted students (see data dictionary below).

Because the SAT and the ACT use different score ranges, in order to allow for direct comparison of the scores, results of both tests are normalized to a 0-1 range using a min-max function. On this normalized scale, 0 represents the worst possible result and 1 - best possible result, for both tests.

The Exploratory Data Analysis examines participation and results for both tests, and creates data frames used further  for visualizations, observations, and recommendations.

The Visualization, Observations, and Recommendations section centers on the three key objectives listed in the Problem Statement.

### Data Dictionary

|**Feature**|**Type**|**Dataset**|**Description**|
|:---|:---|:---|:---|
|state|string|sat_all.csv|Name of US state where SAT is administered|
|participation|float|sat_all.csv|Percentage of eligible students who take the SAT in each state|
|total|int|sat_all.csv|Average total (composite) SAT score of students in each state|
|total_norm|float|sat_all.csv|Average total (composite) SAT score of students in each state, normalized using min-max method|
|year|int|sat_all.csv|The year (2017/2018/2019) covered in listed dataset|
|state|string|act_all.csv|Name of US state where ACT is administered|
|participation|float|act_all.csv|Percentage of eligible students who take the ACT in each state|
|total|float|act_all.csv|Average total (composite) ACT score of students in each state|
|total_norm|float|act_all.csv|Average total (composite) ACT score of students in each state, normalized using min-max method|
|year|int|act_all.csv|The year (2017/2018/2019) covered in listed dataset|
|school|string|sat_act_by_college_mod.csv|Name of a U.S. college|
|number_of_applicants|integer|sat_act_by_college_mod.csv|The number of students applying to the college in a year|
|accept_rate|float|sat_act_by_college_mod.csv|Percentage of applicants accepted to the college|
|sat_norm_25th|float|sat_act_by_college_mod.csv|Lower bound of interquartile range of normalized SAT scores for students accepted to school|
|sat_norm_75th|float|sat_act_by_college_mod.csv|Upper bound of interquartile range of normalized SAT scores for students accepted to school|
|act_norm_25th|float|sat_act_by_college_mod.csv|Lower bound of interquartile range of normalized ACT scores for students accepted to school|
|act_norm_75th|float|sat_act_by_college_mod.csv|Upper bound of interquartile range of normalized ACT scores for students accepted to school|


### Key Observations, Conclusions and Recommendations

#### Feasibility of converging onto one standard (SAT or ACT):

While both the ACT and the SAT are available to students in all 51 states, some states seem to overwhelmingly "prefer" one over the other. There are 24 states where one of the tests (SAT or ACT) is more popular than the other by more than 70 pct point and 15 states where one of the tests (SAT for one and ACT for the remaining 14) is more popular than the other by more than 90 pct points. However, although the 14 states could feasibly switch to the ACT, this would not drive much benefit. 
Standardization across all states does not currently appear feasible.

#### Comparative difficulty levels of the SAT and the ACT:

Based on analysis of the distribution of state averages, it does not appear as though overall test results skew towards either SAT or ACT, making it impossible to conclude that one is generally easier than the other. Of 51 states, 27 reported better SAT results, 24 - better ACT results. An overlay of both test results' histograms additionally supports the conclusion that neither the ACT nor the SAT can generally be considered "easier".

#### Relative advantage of the SAT / ACT in terms of "elite school" admissions:

To get accepted into one of 28 colleges and universities which are both most popular with high school students (largest volumes of applications) and most selective (lowest acceptance rates), students should aim for at least  87.9% or 31.6 points on the ACT, or at least 82.1% (1405.7 points) on the SAT. Based on the assumption of normal distribution, the probabity of a test-taker achieving the required ACT minimum is 2.6% - lower by 0.9% (or 26%!) than the probability of achieving the minimum SAT score.

### Next Steps

Additional analysis:
As noted above, the conclusion that the SAT is "better" for candidates to top schools relies on the assumption of normal distribution for both tests. Further research might validate this assumption or determine the more appropriate distribution shape.


---
