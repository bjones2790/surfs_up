# surfs_up

# Overview of analysis

W. Avy, an investor, wants more information about temperature trends before opening a surf shop in Hawaii. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if a surf and ice cream shop business would be sustainable year-round. This analysis compares average temperatures for the months of June and December to identify trends.

# Results

Results of the analysis revealed the following:

1. Average temperatures were slightly higher in June as expected as seen in the tables below. June had an average high of 74.9 degrees while December had an average high of 71 degrees. 

June Temps: 
/Users/bruce0841/Desktop/UNCC/SQL/Module_9/surfs_up/Resources/June temps.png

December Temps
/Users/bruce0841/Desktop/UNCC/SQL/Module_9/surfs_up/Resources/December Temps.png

2. Although temperatures in June were higher, the two months have a comparable standard deviation between the two, meaning there is similar variation between the mean and temperature values within each dataset.

3. Both June and December a maximum high above 80 degrees, although the year this occurred was not determined for this analysis. 

# Summary

The data revealed favorable temperatures in both June and December, indicating that year round conditions are ideal for the surf shop. This analysis is limited in the fact that it only looks at temperatures and not precipitation, however.

To improve the analysis, the developer could use the following codes to add additional precipitation data:

# Get average precipitation data for June

june_temp_prec = session.query(Measurement.tobs, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

june_temp_prec = session.query(Measurement.tobs, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

june_temp_prec_df = pd.DataFrame(june_temp_prec)

june_temp_prec_df.describe()

/Users/bruce0841/Desktop/UNCC/SQL/Module_9/surfs_up/Resources/June with Precip.png

# Get average precipitation data for December 

dec_temp = session.query(Measurement.date, Measurement.tobs, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()


/Users/bruce0841/Desktop/UNCC/SQL/Module_9/surfs_up/Resources/Dec with precip.png


 