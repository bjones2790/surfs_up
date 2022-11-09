# surfs_up

# Overview of analysis

W. Avy, an investor, wants more information about temperature trends before opening a surf shop in Hawaii. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if a surf and ice cream shop business would be sustainable year-round. This analysis compares average temperatures for the months of June and December to identify trends.

# Results

Results of the analysis revealed the following:

1. Average temperatures were slightly higher in June as expected as seen in the tables below. June had an average high of 74.9 degrees while December had an average high of 71 degrees. 

June Temps:![June temps](https://user-images.githubusercontent.com/112994018/200960404-e6b879c2-9a8b-4e1b-b89a-93b2e7efacdd.png)


December Temps: ![December Temps](https://user-images.githubusercontent.com/112994018/200960424-675a314f-0859-49c0-9b88-8f01f4d6debe.png)


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

![June with Precip](https://user-images.githubusercontent.com/112994018/200960516-144cc3d1-2a64-4238-b0db-77d4f1b53fe6.png)

# Get average precipitation data for December 

dec_temp = session.query(Measurement.date, Measurement.tobs, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
dec_temp_prec = session.query(Measurement.tobs, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
dec_temp_prec_df = pd.DataFrame(dec_temp_prec)
dec_temp_prec_df.describe()

![December Temps](https://user-images.githubusercontent.com/112994018/200960546-83f34384-855b-410e-900a-0655e82b3c70.png)



 
