# Exploring-the-Rosetta-Stone-of-Human-Capital
In this assignment I will work on the working paper A Rosetta Stone of Human Capital, by Dev Patel and Justin Sandefur. 

As you may know, there are different tests that measure reading and writing skills at school among countries in the world. The problem is that not all countries use the same tests. The basic contribution of the authors was to come up with a way to facilitate conversion between test scores in different countries. In this way they have created what they call a "Rosetta Stone of Human Capital", because it allows us to compare human capital across the different countries.
In this notebook I will replicate some of their findings using python Pandas, Numpy,scipy and Statsmodels.

# First Question
### "Income and Test Results"

For the first question we will study the relationship between income and the TIMSS and PIRLS score, as in Section 4.1 and Figure 5 of the original paper.

In order to do this, except for the country scores, we will need the following file:

* ```WDI_data.csv```, which contains income data per country as given by the World Bank.

Then we will be able to investigate the relationship between logged income and TIMMS, and logged income and PIRLS. We will then give the summary table of our model and Plot the two relationships.

# Second Question
### "Years of Schooling and Test Scores"

We will explore how much years of schooling impact test scores, taking account of the per capita income, as in Section 4.1 and Figure 6 of the original paper. 
To do that, we will need to take the residuals of the models we created in The first Question; the residuals contain what cannot be explained by income, so we can use them to see how much of what cannot be explained by income can be explained by years of schooling.

# Third Question 
### "Compare New and Previous Estimates"

To see if the results of the authors make sense, we can compare their scales with other estimates of learning outcomes, as in Section 4.1 and Figure 7 of the original paper.

# Fourth Question
### "Skills Intensity"

For this question we will study the relationship between the skills of the people in each country and the value of its exports, as described in Section 4.2 of the original paper. We will do this with performing four regressions:


$$ \log(V_{ci}) \sim \mathrm{TIMSS}_{c}/1000:\mathrm{college}_i + i + c $$

$$ \log(V_{ci}) \sim \mathrm{PIRLS}_{c}/1000:\mathrm{college}_i + i + c $$

$$ \log(V_{ci}) \sim \mathrm{TIMSS}_{c}/1000:\mathrm{highschool}_i + i + c $$

$$ \log(V_{ci}) \sim \mathrm{PIRLS}_{c}/1000:\mathrm{highschool}_i + i + c $$
