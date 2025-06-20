# HR ATTRITION ANALYSIS 
![1000257046](https://github.com/user-attachments/assets/a2c7ccaf-a9b0-493d-8f34-47e1e85591e2)

## PROJECT OVERVIEW 
The  HR Attrition dashboard uncovers potential cause of attrition rate based on job satisfaction, salary and job roles. High Attrition rate can lead to negative impact in business productivity. The project analysis help the human resources team with actionable insight and understand why employees tends to leave the organization and also to develop and improve work space satisfaction, employee retention and organization performance 

## PROBLEM STATEMENT 
The HR needs answers to the following questions:

- What is the overall Attrition rate in the company and which department is affected the most?
- What job roles and age groups are affected by Attrition?
- Do employees with low job satisfaction and monthly income tends to leave more?
- How does Attrition varry by years at the company?
- What gender are leaving the most?   
## DATA SOURCE 

The data set for the project is obtained from incubator hub program facilitators. It is an excel sheet containing 1,470 rows and 39 columns containing employees informations like Employee ID, Department, Job role, Marital status, Job satisfaction rating, Gender etc

## METHODOLOGY 

Data import and cleaning: I imported the data set into power BI and performed data cleaning in power query editor 

-Checked for missing values 
- spelling errors and duplicate - None found 
- Adjusted the data types
- Added new columns like Age group and Distance from home 
## Dax measures

I created Dax measures to generate performance measures

- Total Employee
```
  Total Employee= Sum('Hr data'[Employee count])
```
- Attrition Rate
```
Attrition Rate= Sum('Hr data'[Attrition count]/sum ('Hr data'[Employee count])
```
- Current Employee
```
 Current Employee= Sum('Hr data'[ Current Employee ])
```
- Average Age
 ```
Average age= Average ('Hr data'[Age])
```
- Avg monthly income
```
Avg Monthly income= Average ('Hr data'[Monthly income])
```
- Avg tenure of attrited employee
```
Avg Tenure = Calculate(average('Hr data'[Years at company],'Hr data'[Attrition]="yes")
```
- Attrition count
```
Attrition count= Calculate(sum('Hr data'[Employee count],'Hr data'[Attrition]="yes")
```

## DASHBOARD 
![hr attrition](https://github.com/user-attachments/assets/709a839b-f093-445f-b0de-d7a6bc7ca1ca)
 ## 💡INSIGHTS

- About 1,470 total count of employee, (16%) of employee has left the company which is a total of 150 Male and 87 Female
- Research and development department experience most attrition of 56.12%
- Employee within the age of 25-34 left which implies that younger employees may be seeking for better career growth, pay or flexibility 
- Most Attrition happened within the first 5 years of employment pointing possible issues in onboarding or Job role clarity 
- Employee who lives far away from office is one of the main reasons for attrition 
- Employee who left were not satisfied with the job as laboratory technicians has the highest attrition count due to low monthly salary.
### 🎯RECOMMENDATIONS 

- Employee with long distance from home, consider remote/hybrid work or transport allowance where remote work isn't feasible 
- Improve pay scale by offering overtime payment and bonuses
- Recognize and award prize to employee regularly and offer promotion to high performers
