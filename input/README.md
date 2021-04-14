# Data Source Description

For this project, we will use data extracted from the [National Longitudinal Survey of Youth 1997](https://www.bls.gov/nls/nlsy97.htm) (NLSY97). The NLSY97 is a nationall representative sample of Americans who were first surveyed as adolescents in 1997. The NLSY97 has done a follow-up survey of these respondents each year, which is why it is "longitudinal." The survey is conducted by the US Bureau of Labor Statistics. 

We are using a subset of this data for all respondents who were still taking part in the survey by year 2008, which ensures that they had a reasonable amount of time to complete a four-year college degree. We are also using a small extract of variables from the much larger dataset. 

From the full data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.Rmd R Markdown document. The name of the dataset in R is `NAME`. 

* **college_complete**: This variable indicates whether a respondent had completed a four-year college degree by the last wave in which data was available for that respondent. The variable is coded as a 1 if they completed a four-year degree and a 0 if they did not. This is the key dependent variable. You can interpret slopes from models for this variable as indicating change in the probability of completing a four-year degree.
* **fam_structure**: This variable records the family structure of the respondent in the 1997 wave of the survey (when they were an adolescent). I have collapsed the categories into the categories of two biological parent, biological and step parent, single parent, and other family type. This is the key independent variable.
* **gender**: The gender of the respondent, recorded as male or female. This is the key contextual variable.
* **race**: The race of the respondent. Due to sample size limitations, this is recorded in four categories of black, Latino, mixed race, and non-Black/Non-Latino.
* **hh_income**: The household income of the respondent's household in 1997 (when they were an adolescent). This is measured in 1000s of dollars. 
* **highest_parent_grade**: The highest years of education among the respondent's residential parents (which could include step-parents) and biological parents.
* **mother_age_birth**: The respondent's mother's age, when the respondent was born.
