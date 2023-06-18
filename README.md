# StrataScratch Solution [for the free questions]

## Getting started by Easy questions at first [you can access them by filetering the difficulty level of the question and choosing only Easy ones]
--------------------------------------------------------------------------------------------------------------------------------------------------
#### 1. Write a query that calculates the difference between the highest salaries found in the marketing and engineering departments. Output just the absolute difference in salaries.

#### Dataset:
![image](https://github.com/ZiadAhmed10/StrataScratchSolution/assets/121814714/ac47c855-8fef-4a9e-9209-2147bd194ade)
![image](https://github.com/ZiadAhmed10/StrataScratchSolution/assets/121814714/af1042af-afcb-4df9-9e31-84b71ed1fb54)

### Solution:

SELECT ABS ((Select MAX(salary)
FROM db_employee e
INNER JOIN db_dept d
ON e.department_id = d.id
AND department = 'marketing') - (SELECT MAX(salary)
FROM db_employee e
INNER JOIN db_dept d
ON e.department_id = d.id
AND d.department = 'engineering')
) AS Salries_differnce;

#### Output:
![image](https://github.com/ZiadAhmed10/StrataScratchSolution/assets/121814714/bd22aaa7-d902-44bd-8cc3-6a25dabfe065)

