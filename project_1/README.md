### Overview

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university. The SAT has two sections consisting of evidence-based reading and writing and math ([*source*](https://www.princetonreview.com/college/sat-sections/)). the ACT is four sections which are english, mathematics, reading, and science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html/)).

---

### Problem Statement

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

Standardized testing may not be a fair assessment of intelligence for students, as it has been noted that those of lower socioeconomic status tend to score lower on these exams. It would be advised that colleges adopt an optional testing policy to mitigate these unfair circumstances. Those of lower socioeconomic background are exposed to stress at greater rates than their wealthier counterparts. Additionally, students of higher socioeconomic have resources available for additional test prep. Socioeconomic status has been shown to be significantly associated with race; the relationship between SES, race, and ethnicity is extremely intertwined ([*source*](https://www.brookings.edu/blog/up-front/2020/12/01/sat-math-scores-mirror-and-maintain-racial-inequity/)). Research has shown that a person's race often affects their socioeconomic status. Low SES is also correlated with lower educational attainment. Additionally, communities are often segregated by SES, race, and ethnicity. African-Americans and Latinos also are more likely to attend high-poverty schools than Asian-Americans and Caucasians. According to the U.S. Census Bureau, African American, American Indian/Alaska Native, Hispanic, Pacific Islander and Native Hawaiian families are more likely than Caucasian and Asian families to live in poverty. Poverty within the United States also varies, with states like New Hampshire, Utah, and Maryland having the lowest rates of poverty and New Mexico, Louisiana, and Mississippi having the highest rates ([*source*](https://www.apa.org/pi/ses/resources/publications/minorities/)).

---

### Datasets

* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`demographics_2017 2018 2019.xls`](./data/demographics_data_2017_2018_2019.xls): 2017,2018,2019 SAT Scores by Race/ethnicity ([source](https://nces.ed.gov/programs/digest/d19/tables/dt19_226.10.asp/))

---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|State|object|sat_2017_final, sat_2018_final|Average SAT score (total and breakdown by section) of the state in 2017/2018 of seniors who took the exam|
|Participation|float|sat_2017_final, sat_2018_final|Percent of seniors in that state who participated in the SAT exam|
|Reading_Writing|integer|sat_2017_final, sat_2018_final|Average SAT reading/writing score in 2017/ 2018 of seniors who took the exam by state|
|Math|integer|sat_2017_final, sat_2018_final|Average SAT math score in 2017/ 2018 of seniors who took the exam by state|
|Total|integer|sat_2017_final, sat_2018_final|Average SAT total score in 2017/ 2018 of seniors who took the exam by state|
|Race/ethnicity|object|demographics_2017_final, demographics_2018_final|Average SAT score (total and breakdown by section) in 2017/2018 of seniors who took the exam by race| 
|Math|integer|demographics_2017_final, demographics_2018_final|Average SAT math score in 2017/ 2018 of seniors who took the exam by race| 
|Reading_Writing|integer|demographics_2017_final, demographics_2018_final|Average SAT reading/writing score in 2017/ 2018 of seniors who took the exam by race| 
|Total|integer|demographics_2017_final, demographics_2018_final|Average SAT total score in 2017/ 2018 of seniors who took the exam by race| 

---

### Analysis

Some trends found were that there was a negative correlation between state participation for the sat exam and the total sat score. Additionally, there were some cases where states with low participation rates also had high poverty rates, and vice versa. Participation rate and total sat score were more correlated in 2017 than in 2018. Lastly, it was shown that minorities (African Americans, Latinos, Pacific Islander, and Indian/Alaska Native) tested much lower than Whites and Asians. The gap in the score between races could shed light on the disparities that exist within the sat exam. It could also be said that a larger portion of the student population is made up of minorities, but this larger portion is the one that is falling behind. This gap was actually widened in 2018. 

---

### Conclusions/Recommendations 

States should adopt an optional standardized testing policy, as minorities tend to test lower on these exams; standardized testing is an unfair assessment for intelligence of students. Further studies would need to be done where state and county data is taken into consideration. More demographic data such as average income, state race/ethnicity demographics, and homelessness rates would help paint a more complete picture of the trends within this complex topic. 



