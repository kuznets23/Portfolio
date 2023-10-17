## Conduct a cohort (vintage) analysis of a bank's overdue debt using raw data (Test task from one of the largest Russian banks).

### Task No. 1: Make a summary table to create a vintage for debt of 90+ days.
#### Conclusions of Task No. 1:
- a table with cohort analysis is ready: we have 12 cohorts broken down by month for 2019, with information on the amount of disbursements in each cohort, the number of loan agreements and information on overdue 90+ days broken down by the life time of each cohort.
  
### Task No. 2: Using Python, you need to write a function that receives vintage as input: pandas.DataFrame and returns vintage with overdue debt as a percentage of the Issued Amount.
- the created function `overdue_perc()` works correctly.
- the result of the function is a vintage with a % of overdue debt of 90+ from the amount issued for each cohort.
- for clarity, a `heatmap` is built on the result of the function
- the resulting schedule can be presented to management.
