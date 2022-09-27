# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Overview

The SAT is a standardized test that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). 

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on the SAT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

### Problem Statement

The use of the SAT score as one of the criteria for colleges and universities admission should be abolished as the SAT score is not a fair measure of a student's true potential or ability.

There are various uncontrollable limiting factors that influence the SAT score, and one of them that is the highest level of parental education.

From this project, we will discover that the higher level the parental education, the higher the students' SAT score.

We would like to explore the acceptance rate into a university based on the parental education by using the below guided questions.

**1) whether a student is likely to be accepted into colleges/universities base on the parents' highest education level**

**2) what type of insitutes are the students likely to be accepted to?**

**3) if a student is accepted, which school will he/she likely be accepted to?**

**4) how likely are students be accepted when they scored above the 25th percentile of the acceptance score?**

---

### Datasets

* [`sat_act_by_college.csv`](./data/sat_act_by_college.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges ([source](https://www.compassprep.com/college-profiles/))
* [`sat_student_profile.xls`](./data/sat_student_profile.xls): SAT, by sex, race/ethnicity, first language learned, and highest level of parental education: Selected years, 2017 through 2021 ([source](https://nces.ed.gov/programs/digest/d21/tables/dt21_226.10.asp))
* [`acceptance_rates_2020_2021.xls`](./data/acceptance_rates_2020_2021.xls): SAT and ACT scores for degree-granting postsecondary institutions with first-year undergraduates, by control and level of institution: 2020-21 ([source](https://nces.ed.gov/programs/digest/d21/tables/dt21_305.40.asp))

---
### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**school**|*string*|sat_acc|The universities| 
|**class_year**|*string*|sat_acc|The year of the class of enrollment|
|**no_of_applicants**|*float*|sat_acc|Number of students who applied to the university|
|**accept_rate**|*float*|sat_acc|Percentage of students who applied to the university and got accepted|
|**total_25**|*float*|sat_acc|Total SAT scores of the enrollees at 25th percentile|
|**total_75**|*float*|sat_acc|Total SAT scores of the enrollees at 75th percentile|
|**parent_edu**|*string*|sat_parent_edu|The highest level of education of the students' parents|
|**no_of_student**|*float*|sat_parent_edu|Number of students with that level of parental education|
|**percent_student**|*float*|sat_parent_edu|Percentage of students with that level of parental education|
|**total**|*float*|sat_parent_edu|Average Total SAT Score of the students|
|**ebrw**|*float*|sat_parent_edu|Average Evidence-Based Reading and Writing SAT Score of the students|
|**math**|*float*|sat_parent_edu|Average Math SAT Score of the students|
|**institutes**|*string*|acc_rate_t|The type of institutes|
|**ebrw_25**|*string*|acc_rate_t|Average Acceptance Evidence-Based Reading and Writing SAT Score at 25th percentile|
|**ebrw_75**|*string*|acc_rate_t|Average Acceptance Evidence-Based Reading and Writing SAT Score at 75th percentile|
|**math_25**|*string*|acc_rate_t|Average Acceptance Math SAT Score at 25th percentile|
|**math_75**|*string*|acc_rate_t|Average Acceptance Math SAT Score at 75th percentile|
|**total_25**|*string*|acc_rate_t|Average Acceptance Total SAT Score at 25th percentile|
|**total_75**|*string*|acc_rate_t|Average Acceptance Total SAT Score at 75th percentile|

---

### Summary 

We first look at the type institute students are likely able to be accepted based on the highest level of parental education.
We concluded that students whose parents' highest education is lower than Associate's degree did not score enough to meet the acceptance scores of any school.

For students whose parents' highest education is Associate's degree or higher, we then look at the percentage of sampled universities students are likely to be accepted.

Finally, using the acceptance rate at the universities, we tried to populate the likelihood students are able to be accpeted into a university.

---

### Conclusions
- The higher the level of parental education, the higher the students' SAT scores.

-  Students whose parents' highest education is lower than Associate's degree did not score enough to meet the acceptance scores of any school.

- Students whose parents' highest education is Associate's degree scored barely enough to meet the acceptance scores of public schools.

- Students whose parents' highest education is Bachelor's degree or Graduate degree scored well above the 25th percentile of acceptance scores of all schools.

- Of the sampled 381 universities:

  - Students whose parents' highest education is Associate's degree are able to enter 9.71% of the universities
  - Students whose parents' highest education is Bachelor's degree are able to enter 39.11% of the universities
  - Students whose parents' highest education is Graduate degree are able to enter 61.42% of the universities


The acceptance rate at the universities are not 100%.

To find out the probability of students getting accepted into a university based on their parental education,
we use the below:

|Percentage of universities students likely to be accepted| * |mean acceptance rate of the universities|
|---|---|---|

That works out to the following:

- Students whose parents' highest education is Associate's degree has a 7.26% probability to be accepted into a university
- Students whose parents' highest education is Bachelor's degree has a 28.00% probability to be accepted into a university
- Students whose parents' highest education is Graduate degree has a 42.75% probability to be accepted into a university

In conclusion, the higher the level of parental education, the higher the students' SAT score and therefore the more likely to be accepted in to a university.


### Recommendations
Given that it is unlikely for students whose parents' highest education is lower than Associate's degree to be accepted into a university, the SAT is not an accurate measurement of students' abilities and talents.
Universities should remove SAT scores as one of the admission criteria.
If SAT is going to stay, more help and resources should be rendered to students whose parents have lower level of education.