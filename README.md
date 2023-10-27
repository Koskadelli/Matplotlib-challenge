# Matplotlib-challenge Summary

This assignment has us joining a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

# Resources Used
1) Matplotlib documentation used throughout: https://matplotlib.org/stable/gallery/statistics/boxplot_demo.html
2) Began with the starter file, pymaceuticals_starter.ipynb
3) ChatGPT for select functionality (specifically the one-line aggregate functionality, certian pandas plot formatting, and help calculating the line of best fit)

# Notes
I want to specifically call attention to something I think is incorrect in the starter file. For clarity, this is also commented on in my code. 

We are asked to generate a pie chart, showing a comparison of genders of the mice used in the studies. The starter file shows the ratio to be Male: 51.0%, Female: 49.0%. I think they are using the previously generated 'clean' dataframe to pull these numbers, because the math aligns perfectly (the counts here are Male: 958, Female: 922). However, this isn't correct to use because some mice have more Timepoints recorded than others. To correctly get the true ratio of genders, you have to pull the genders only for the unique Mouse IDs, which yields a count of Male: 125, Female: 123 and thus a percentage in our pie chart of Male: 50.4%, Female: 49.6%. You can QA this against the original CSV value (once you've removed the bad data of the duplicated mouse) and see that this matches. 
