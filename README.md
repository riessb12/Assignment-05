# Assignment-05  

This is our fifth assignment for BIOL390 in the summer of 2020. The purpose of this project is to give you some practice importing and cleaning COVID-19 data for analysis.

## Data URL
You will be using COVID-19 data from the Harvard Dataverse for this project. The url that you need is: https://dataverse.harvard.edu/api/access/datafile/:persistentId?persistentId=doi:10.7910/DVN/L20LOT/FZLQRQ 

## Instructions  

1) Create folders for raw_data and output

2) Write a chunk that loads the needed tidyverse libraries but does not show up in any way in the final html document.

3) Write a chunk that uses wget to download the data file from the Harvard Dataverse and save is as raw_data/Countries-Deaths.tsv. This chunk should also not show up in any way in the final html and should be cached so that you do not repeatedly download the file as you reexecute your code.

4) Write a chunk that creates a tidy dataset called output/GFI_total_deaths_by_date.csv. This file should have variables named Country, Date, and Total_Deaths. You will need to use several tidy tools to restructure the data with pivot_long() and convert the four-digit codes to dates using lubridate. Filter the data so that only information from Germany, France, and Italy are present. This chuck should not display anything in the final html document.

5) Write another chunk that reates a tidy dataset called output/GFI_daily_deaths_by_date.csv. This file should have variables named Country, Date, and Daily_Deaths. You can start from the previous data and use the lag() function to calculate the daily death rates as a difference between adjacent datapoints. Once again, this should not show up in the final html.

6) Write a chunk that uses ggplot2 to create a line graph that comparing the total deaths between the three countries over time. Color each line by country and use a line size of 1.5. Set the Y axis to be a log10 scale, and label that axis as Total COVID-19 Deaths. Please use the ggplot2 linedraw theme for your plot.

7) Write a chunk that uses ggplot2 to create a line graph that comparing the daily deaths between the three countries over time. Color each line by country and use a line size of 1.5. Label the y axis as Daily COVID-19 Deaths and set the y-axis limits to range from 0 to 1,000. Please use the ggplot2 linedraw theme for your plot.

8) Write one last chuck that groups the daily death data by country and finds the maximum number of deaths per day. Use knitr::kable() to display this as a table in your html document.

9) Using markdown, provide an introduction and conclusion section before and after the analysis that you just performed, respectively. These sections should be level 2 headings.

10) Cite your data source - another level 2 heading - using this reference. Check online to make sure that you get any formatting (e.g. italics, links, etc. correct)

Take some time and explore some of the other datasets that are available in the Harvard Dataverse collection. This is one possible source of raw data for your project. I will show you lots more later.
