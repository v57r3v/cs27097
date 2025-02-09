java cHomework Assignment 2
This homework asks you to calculate seasonally unadjusted and seasonally adjusted time series
of monthly unemployment-to-employment (UE) rate, employment-to-unemployment (EU) rate,
and employment-to-employment (EE) rate using the CPS. UE rate is the fraction of employed
individuals ﬁnding a job in a month. EU rate is the fraction of employed individuals becoming
unemployed in a month. Finally, EE rate is the fraction of employed individuals changing jobs in
a month.
1. List of variables to download: empstat, age, empsame only from CPS basic monthly ﬁles.
Note that you will also download (preselected) weights, cps id, and year and month of each
observation.
2. I ask you to calculate the above rates for each month between January 1976 and December
2021 by following the instructions below.
(a) Drop individuals whose age below 16 and who are in military as we did in class.
(b) Deﬁne an employed dummy employed such that a person is considered to be employed
(i.e., employed dummy is equal to 1) if the person is at work or has a job but not at
work last week. The employed dummy is 0 (i.e., the person is unemployed) if the person
is unemployed, unemployed experienced worker, or unemployed new worker. You should
use empstat variable to deﬁne this dummy given these descriptions.
(c) Sort the data by year_month and cpsidp, the latter of which is a unique ID of an
individual in the dataset. In the CPS, the same individual can be observed in diﬀerent
time periods. Speciﬁcally, an individual is in the sample for 4 consecutive months, leaves
the sample during the following 8 months, and then returns for another 4 consecutive
months. Note that this describes the situation when the person stays in the survey. Most
of the time, the person may leave and not come back to the survey. Nevertheless, the
same person is observed potentially in consequtive months. For this reason, you need to
declare the dataset as a panel. Hint: This can be done using xtset command and make
sure that you follow individuals not households. To do this, you need to combine cpsid
and pernum variables to identify individuals (separately from households) OR directly
use cpsidp variable directly that is preselected and downloaded in the dataset already.
(d) Deﬁne an EU dummy which is equal to 1 if a person is unemployed this month (employed
dummy is 0) but employed last month. This dummy is 0 if the person is employed both
1this month and last month. Hint: Whe代 写program、c/c++，Java
代做程序编程语言n looking at the employment status in the last
month, you can consider using L1.employed command.
(e) Similarly, deﬁne a UE dummy which is equal to 1 if a person is employed this month
(employed dummy is 1) but unemployed last month. This dummy is 0 if the person is
unemployed both this month and last month. Again, take advantage of operator L1.
(f) Finally, deﬁne an EE dummy which is equal to 1 if a person is employed and changed
employer this month. The latter can be understood using empsame variable.
(g) Calculate monthly EU, UE, and EE rates over time. Note that EE rate can be calculated
starting February 1994 given that empsame variable becomes available starting that
month. Hint: Think about using collapse command.
(h) Then, also calculate the seasonally adjusted EU, UE, and EE rates.
(i) As I did in class, your code should have a switch at the top for calculating non-seasonally
adjusted and seasonally adjusted rates and should output these rates to the same excel
with two diﬀerent columns (side by side).
(j) Create a report (.pdf document) where you include 3 ﬁgures to plot EU rate, UE rate,
and EE rate over time. In each ﬁgure, please plot both non-seasonally adjusted and
seasonally adjusted rates (so each ﬁgure will have 2 lines). Carefully label each axis and
use diﬀerent colors for two lines within the same ﬁgure. In this report, please provide
answers to the following questions.
i. How did seasonally-adjusted EU, UE, and EE rates change over time?
ii. How do recoveries of seasonally-adjusted EU, UE, and EE rates diﬀer between the
recovery from the Great Recession vs the Covid Recession? Compare and comment.
Hint: At what year EU, UE, and EE rates return to their pre-Great Recession level
(2007 December) after the Great Recession? At what year these rates reutn to their
pre-Covid Recession (2019 December) after the Covid recession?
iii. If you think there are diﬀerences, why do you think these diﬀerences could have
happened? Provide intuitive explanations.
Outcomes to submit
1. .do ﬁle that runs your code. Please name it as “name_surname_hw2.do”. This .do ﬁle should
use the data ﬁle you downloaded and create the excel ﬁle discussed above.
2. .pdf ﬁle that has three ﬁgures discussed in 2j) above and answers the questions in 2j) above.
Please name it as “name_surname_hw2.pdf”
3. Please submit these two ﬁles to Canvas under Assignment 2 before 3.00 pm CST on February
12.
2

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
