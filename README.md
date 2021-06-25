# Dr.-Semmelweis-Discovery-of-Handwashing---DataCamp
This is Dr. Ignaz Semmelweis, a Hungarian physician born in 1818 and active at the Vienna General Hospital. If Dr. Semmelweis looks troubled it's probably because he's thinking about childbed fever: A deadly disease affecting women that just have given birth. He is thinking about it because in the early 1840s at the Vienna General Hospital as many as 10% of the women giving birth die from it. He is thinking about it because he knows the cause of childbed fever: It's the contaminated hands of the doctors delivering the babies. And they won't listen to him and wash their hands!

In this notebook, we're going to reanalyze the data that made Semmelweis discover the importance of handwashing. Let's start by looking at the data that made Semmelweis realize that something was wrong with the procedures at Vienna General Hospital.
Load in the dataset with the yearly number of deaths.

Import the pandas, aliasing it as pd.
Read in datasets/yearly_deaths_by_clinic.csv and assign it to the variable yearly.
Print out yearly.
Calculate the yearly proportion of deaths.

Calculate the proportion of deaths per number of births and store the result in a new column named proportion_deaths.
Extract the rows from Clinic 1 into clinic_1 and the rows from Clinic 2 into clinic_2.
Print out clinic_1.
Plot the yearly proportion of deaths for both clinics.

Plot proportion_deaths by year for the two clinics in a single plot. Use the DataFrame .plot() method.
Label the plotted lines using the label argument to .plot().
Change the y-axis label to "Proportion deaths" using the ylabel parameter in your second call of .plot().
Save the Axes object returned by the plot method into the variable ax.
Load in the dataset with the monthly number of deaths for Clinic 1.

Read in datasets/monthly_deaths.csv and assign it to the variable monthly. Make sure to tell read_csv to parse the date column as a date.
Calculate the proportion of deaths per number of births and store the result in the new column monthly["proportion_deaths"].
Print out the first rows in monthly using the .head() method.
Plot the monthly proportion of deaths for Clinic 1.

Plot proportion_deaths by date for the monthly date using the DataFrame .plot() method.
Change the y-axis label to "Proportion deaths"
Save the Axes object returned by the .plot() method into the variable ax.
Make a plot that highlights the effect of handwashing. The code to define handwashing_start is already provided to you using pandas' to_datetime() function.

Split monthly into before_washing (the rows in monthly before handwashing_start) and after_washing (the rows in monthly at and after handwashing_start).
Using the same approach you used in Task 3, plot proportion_deaths in before_washing and after_washing into the same plot. Again, use the DataFrame .plot() method twice, saving the Axes object returned by the first call of .plot() into the variable ax.
Label the plotted lines using the label argument to .plot().
Change the y-axis label to "Proportion deaths" in your second call of .plot().
Calculate the average reduction in proportion of deaths due to handwashing.

Select the column proportion_deaths in before_washing and assign it to before_proportion.
Do the same for proportion_deaths in after_washing and assign it to after_proportion.
Calculate the difference in mean monthly proportion of deaths as mean after_proportion minus mean before_proportion.
Make a bootstrap analysis of the difference in mean monthly proportion of deaths.

Within your for loop:
boot_before and boot_after should be sampled with replacement from before_proportion and after_proportion.
The difference in means should be appended to boot_mean_diff.
Calculate a 95% confidence_interval as the 2.5% and 97.5% quantiles of boot_mean_diff.
Given the data Semmelweis collected, is it True or False that doctors should wash their hands?

Note: You may experience problems with the formatting of data types. 
Some data types change when importing CSV data. 
Pay attention to this. Press ".info()" after each operation.
