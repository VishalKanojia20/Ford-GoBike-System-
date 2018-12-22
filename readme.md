
# Ford GoBike System Data Exploration
## by Vishal Kanojia

> I explored data set that includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area and plotted univariate, bivariate and multivariate visualizations. Based on the visualizations, I made a slide deck to show the explanatory analysis in a presentation form.

## Dataset Overview
There are 519700 rows in the dataset with 15 columns (duration_sec, start_time, end_time, start_station_id, start_station_name, start_station_latitude, start_station_longitude, end_station_id, end_station_name, end_station_latitude, end_station_longitude, bike_id, user_type, member_birth_year, member_gender). Also, I have applied a transfomation on the start_time column to extract the month of ride and store the values in month column. I have also created a new column duration_min to story durations in minutes. I created a column duration_category to categorize the duration of the ride. I created a column member_age_group to categorize the users on the basis of their age groups.

I'm most interested in figuring out what are start stations that have the most distribution of bikes in greater San Francisco Bay area and their relationships with other variables.


## Univariate Visualization
### Relationships I observed in this part of the investigation. How did the feature(s) of interest vary with other features in the dataset?

> 01. Males prefer to ride the bikes than any other gender.
> 02. Subscribers are more likely to take the bikes than the normal Customers. One reason could be that the Customer Category people are not well aware of this bike renting system or the other reason could be that the subscribers get the bikes on discount offers.
> 03. Adult people top the list when it comes to rent the bike. Whereas the Teenagers are down at the bottom. Probably, they are not allowed to ride bikes on roads by their parents.
> 04. Most people like to ride the bikes during October. One good reason for this result could be that the weather conditions are more pleasant during the 10th month (which is October).

## Bivariate Visualization
### Relationships I observed in this part of the investigation. How did the feature(s) of interest vary with other features in the dataset?

> 01. **member_age_group vs member_gender** : I plotted a clustered bar chart to see the relationship between these two variables and it turned out that both the male and female members belonging to Adult age group take the bikes more frequently as compared to males and females of the other two age groups. But female adults are still very less as compared to male adults.
>02. **Top 5 start_station vs month** : I plotter 2 plots to study the relationship properly. Firstly, I plotted a clustered bar chart and then I used FacetGrid to plot bar charts for the top 5 start stations vs the months. I concluded that Powell St BART Station is more frequently used during the 9th month(September). 
For San Francisco Caltrain, it is 10th month (October). 
For San Francisco Caltrain Station 2, it is 8th (August) and 10th (October).
For San Francisco Ferry Building, 8th (August), 9th (September) and 10th (October) months are more preferred.
For Market St at 10th St, 10th (October) month is more preferred.
>03. **start_station vs member_gender** : Since these two are categorical variables i plotted a clustered bar chart to understand the relationship between the two. I concluded that Powell St BART has more males as well as females as compared to other stations. One interesting thing that I noticed that inspite of being on 4th position among the frequently used start stations, San Francisco Ferry Building station has more number of female user than San Francisco Caltrain Station and San Francisco Caltrain Station 2.
>04. **start_station vs member_age_group** : Since these two are categorical variables i plotted a clustered bar chart to understand the relationship between the two.I noticed that San Francisco Ferry Building station has the most number of Old age group user than any other station. Whereas, Powell St BART Station has the most number of Adult age group users. 
>05. **start_station vs user_type** : For every station, the number of subscriber users are more than the normal customers. But San Francisco Ferry Building has more number of customer users than San Francisco Caltrain Station and San Francisco Caltrain Station 2.

## Multivariate Visualization
### Relationships I observed in this part of the investigation. Were there features that strengthened each other in terms of looking at your feature(s) of interest?

For this part I took only the top 5 start stations as we don't want to overcrowd the plots.
> 01. **month vs duration_min vs start_station** : I plotted scatter plot using FacetGrid. I noticed that on an average the duration for every start station was around 12-14 minutes. The maximum duration in minutes was around 1420-1430 from San Francisco Caltrain station 2 and San Francisco Ferry stations in the months of August and July respectively.
> 02. **start_station vs start_station_longitude vs start_station_latitude** : I plotted a scatter plot for this relationship. I noticed that Powell St BART Station and San Francisco Caltrain station have similar latitude and longitude. Powell St BART Station and San Francisco Caltrain station are 1st and 2nd respectively on the list of most frequently used start stations. So, this means that either this location is easily accessible to the users or users like to take the routes passing through this location because of better roads or less traffic, maybe.
>03. **start_station, member_gender and duration_min** : As I am having 2 qualitative variable and one quantitative variable, I decided to plot a clusted bar chart. I noticed that if we ignore the unspecified gender (Other), for all the top 5 start stations females are taking bikes for a longer duration. One good reason could be that the females ride bikes slowly as compared to males.

### Interesting 

> One interesting thing I noticed that in the unvariate as well as in the bivariate visualizations, the most preferred month to take bikes is 10th i.e; October. But the longest rides in terms of duration (in minutes) were taken in July and August. A reason for this fact could be that during July and August the temperature is high and riders lose more energy while riding and hence slow down their speed. So, Climatic Conditions can also play a part in this case.

## Slide Deck for Explanatory Analysis

Steps:
> 01. From the menu bar, select View > Cell Toolbar > Slideshow. You'll see a drop down appear in the upper right hand corner of each cell, from which you can assign slide element types.
> 02. For cells that you want readers to see, you'll choose the Slide, Sub-Slide, or Fragment types. Slides will form the main flow of the presentation, while sub-slides are children of slides in the main flow. 
Cells that you don't want users to see should be in the Skip. 
> 03. In addition to setting slide types, make sure that all of your code cells have been run and produce the output that you want to show. 
> 04. Use the Kernel > Restart & Run All menu option to do a clean run-through of all of your cells as a final preparatory action.
> 05. Once your notebook has been prepared, save it and shut down your notebook server.
> 06. Write the following code in your terminal: **jupyter nbconvert presentation.ipynb --to slides --template output_toggle.tpl
--post serve** and run it.
