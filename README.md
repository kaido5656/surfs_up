# surfs_up
Demonstrating SQLite and flask application


### Purpose
  The purpose of this analyis was to assist and demonstrate various data to W.Avy and other board members to ensure financial backing to start and open several Surfing and ice creams shops in Oahu. The analysis was done using SQLite in jupyter notebook and presented using flask. W.Avy asked to see specific weather data pertinent to Oahu to determine whether or not the decision to open surf shops there had merit. After demonstrating to W.Avy the precipatation, temperature and most active weather station on Oahu, I was tasked further with retrieving weather data for the months of June and December to further solidify W.Avy's interest in investing in this future venture.

### Results 
  1. The main difference coding during this analysis was the asking month either being June or December. Seeing as W.Avy was ony asking for all the Temperatures for those months, the code ending up being very similar for each query. That being be the case I was able to mildy refactor the code for the next query using the extract function to recieve all the applicable data for their respective month.
##### The main code block retieving temp data
```
results = session.query(Measurement.date, Measurement.tobs).filter(extract('month',Measurement.date) == ??).all()
```
  2. Another observation from the analysis was that each there were more readings for the months of June(1,700) than there were for the months of December(1,517) across the 7 years worth amount of data. This seemed important to make note of going forward to present the data.
  3. The data summary using the describe function on each dataframe yielded various findings. I was able to determine that just about every data entry including mean, min, the quartiles, and max were all moderately higher for the months of June. The standard deviation was higher for the months of December.

### Summary
  Upon completion of the analysis for the mnths of JUne and Decemeber, I was able to find and present my weather findings to W.Avy an dother board members by mildy refactoring the code for each month. The data yielded more readings for the month of June and higher reading for June as well. Additional query recommendations that I would suggest would to add the precipitation data for each month and seperate the months by year to accurately compare one another. I would also suggest plotting the data to easier present the analysis findings. 
