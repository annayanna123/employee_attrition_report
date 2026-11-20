# Results and Discussion

## Data and Dashboard Summary

This report summarizes employee attrition patterns in the Power BI dashboard using the project source file `data_source/hr-attrition.csv`. The source contains **480 employee records**, of which **140** have an exit date and are classified as attrition exits. The overall attrition rate is therefore **29.17%**.

Headcount and attrition in this report are calculated as follows:

- **Headcount:** 480 employees
- **Exits:** 140 employees
- **Attrition Rate:** Exits / Headcount = 29.17%

## Results

### Attrition by Department

| Department | Headcount | Exits | Attrition Rate |
|---|---:|---:|---:|
| Customer Service | 160 | 60 | 37.50% |
| Sales | 70 | 23 | 32.86% |
| Technical Support | 110 | 38 | 34.55% |
| IT | 45 | 8 | 17.78% |
| Training | 30 | 5 | 16.67% |
| HR | 30 | 4 | 13.33% |
| Finance | 35 | 2 | 5.71% |

Customer Service has the highest attrition rate at **37.50%** and also the largest number of exits (**60**). It is followed by Technical Support at **34.55%** and Sales at **32.86%**. Finance has the lowest attrition rate at **5.71%**.

### Attrition by Salary Band

| Salary Band | Headcount | Exits | Attrition Rate |
|---|---:|---:|---:|
| Below 22k | 86 | 26 | 30.23% |
| 22k to 32k | 142 | 52 | 36.62% |
| 32k to 45k | 204 | 56 | 27.45% |
| 45k and up | 47 | 6 | 12.77% |

The **22k to 32k** band has the highest attrition rate at **36.62%**. The **45k and up** band has the lowest attrition rate at **12.77%**. The 32k to 45k band contains the largest number of employees (**204**) and exits (**56**).

The dashboard transformation leaves an exact monthly salary of 45k outside all displayed salary bands because its rule checks values below 45k and above 45k but not a value equal to 45k. One employee has this exact salary and is represented as a blank salary band.

### Attrition by Age Range

| Age Range | Headcount | Exits | Attrition Rate |
|---|---:|---:|---:|
| Young Adults | 120 | 41 | 34.17% |
| Adults | 206 | 58 | 28.16% |
| Middle-aged Adults | 154 | 41 | 26.62% |

Young adults have the highest attrition rate at **34.17%**, compared with **28.16%** for adults and **26.62%** for middle-aged adults. There are no records in the source data for the Senior Adults category.

### Attrition by Overtime Status

| Overtime Status | Headcount | Exits | Attrition Rate |
|---|---:|---:|---:|
| No | 267 | 76 | 28.46% |
| Yes | 213 | 64 | 30.05% |

Employees who work regular overtime have a slightly higher attrition rate (**30.05%**) than employees who do not work regular overtime (**28.46%**). The difference is **1.59 percentage points**.

### Attrition by Gender

| Gender | Headcount | Exits | Attrition Rate |
|---|---:|---:|---:|
| Female | 224 | 70 | 31.25% |
| Male | 256 | 70 | 27.34% |

Female employees have a higher attrition rate at **31.25%**, while male employees have a rate of **27.34%**. Both groups had **70** exits, but the higher rate for female employees is due to their smaller headcount.

### Attrition by Job Satisfaction

| Job Satisfaction | Headcount | Exits | Attrition Rate |
|---|---:|---:|---:|
| 1 | 130 | 50 | 38.46% |
| 2 | 125 | 51 | 40.80% |
| 3 | 111 | 19 | 17.12% |
| 4 | 114 | 20 | 17.54% |

Employees with satisfaction ratings of **1 or 2** have substantially higher attrition rates than those with ratings of **3 or 4**. The highest rate is in satisfaction level 2 at **40.80%**, followed by level 1 at **38.46%**. In contrast, satisfaction levels 3 and 4 have attrition rates of **17.12%** and **17.54%**, respectively.

When the satisfaction levels are combined, ratings 1-2 represent **255 employees** with **101 exits** (**39.61%**), while ratings 3-4 represent **225 employees** with **39 exits** (**17.33%**).

### Attrition by Job Role

| Job Role | Headcount | Exits | Attrition Rate |
|---|---:|---:|---:|
| CSR II | 49 | 22 | 44.90% |
| TSR II | 30 | 12 | 40.00% |
| Team Lead | 91 | 31 | 34.07% |
| Account Executive | 36 | 12 | 33.33% |
| CSR I | 57 | 19 | 33.33% |
| TSR I | 43 | 14 | 32.56% |
| Account Associate | 34 | 11 | 32.35% |
| Developer | 14 | 4 | 28.57% |
| QA Analyst | 12 | 2 | 16.67% |
| Trainer | 18 | 3 | 16.67% |
| Recruiter | 13 | 2 | 15.38% |
| Systems Analyst | 17 | 3 | 17.65% |
| HR Associate | 17 | 2 | 11.76% |
| Network Engineer | 14 | 1 | 7.14% |
| Accountant | 16 | 1 | 6.25% |
| Payroll Analyst | 19 | 1 | 5.26% |

CSR II has the highest job-role attrition rate at **44.90%**, followed by TSR II at **40.00%** and Team Lead at **34.07%**. The lowest rate is for Payroll Analyst at **5.26%**.

## Discussion

The dashboard indicates that attrition is not evenly distributed across the workforce. Customer Service is the highest-risk department by attrition rate, while Finance has the lowest rate. Because Customer Service also has 160 employees, improvements in this department could produce the largest reduction in exits.

The salary pattern suggests that lower-to-mid salary bands experience more attrition: employees earning 22k to 32k have the highest displayed salary-band attrition rate. Employees in the 45k and up band retain staff at a much higher rate. However, salary may reflect differences in job role, seniority, department, and tenure, so these results alone do not establish that pay caused employees to leave.

Job satisfaction shows the clearest contrast. Employees reporting satisfaction levels 1 or 2 have an attrition rate of **39.61%**, versus **17.33%** for employees reporting levels 3 or 4. This pattern supports prioritizing employee engagement, workload, management, compensation, recognition, and career-development reviews, especially for low-satisfaction groups.

The age comparison shows higher attrition among young adults than among adults or middle-aged adults. Regular overtime is associated with only a small increase in attrition, and the overtime result should not be interpreted as a major retention driver on its own. Similarly, female employees have a higher attrition rate in this dataset, but this difference requires context from role, department, pay, tenure, and workload before any organizational conclusion is drawn.

The job-role view identifies CSR II and TSR II as roles with particularly high attrition. Targeted retention interviews and workload or support reviews could help determine whether their exits are associated with scheduling, overtime, compensation, advancement opportunities, or management practices.

## Recommendations

1. Prioritize a retention review for Customer Service, Technical Support, and Sales, with the strongest focus on Customer Service.
2. Conduct exit interviews or stay interviews for CSR II and TSR II employees to identify role-specific causes.
3. Review compensation progression and career opportunities for the 22k to 32k salary band.
4. Investigate the needs of employees reporting job satisfaction levels 1 or 2 through targeted surveys and manager check-ins.
5. Use overtime patterns as a monitoring indicator rather than a standalone explanation, and examine workload together with department and role.
6. Monitor attrition by department, salary, age, overtime, gender, satisfaction, and job role using consistent filters and refresh cycles.

## Limitations

- This analysis is descriptive and does not establish causation.
- Attrition is determined by whether an employee has an exit date in the source data.
- Employee tenure and the reason for exit are not available in the displayed fields.
- No statistical significance testing or control for confounding variables was performed.

