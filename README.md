# CO2-emissions
# CO2-emissions
For this project we started with discussions on emissions as two of the three teammates work in relations to regulations & have newly assigned projects with CO2 & Emissions standards.
First, we were reviewing carbon footprint of some of the materials used to make leather seats vs. vegan leather which is made with synthetic polymers but could not find datasets that had enough information. We then found regulations of CO2 Emissions in Europe which are set to have a target of 93.6g/km until 2029 (15% reduction compared to the 2021 baseline), 49.5g/km from 2030 to 2034 (55% reduction) and 0g/km from 2035 (100% reduction). 
In these European Environmental Agency Guidelines: https://www.eea.europa.eu/en/analysis/indicators/co2-performance-of-new-passenger#:~:text=To%20help%20achieve%20the%20EU's,2035%20(100%25%20reduction). 

We then researched databases and found this one from the Environmental Agency which includes raw data for emissions / CO2 usage & also fuel usage for petrol & diesel vehicles in Europe model years 2018 to 2023. While we were reviewing the data and the dashboard we decided to also look at the average price of the vehicles in the dataset, curious if price would correlate to emissions standards. 
The Dataset with European car prices can be found in this dataset
https://www.kaggle.com/code/dronax/car-prices-dataset.
Once we had both datasets we came up with these two problem statements we will try to solve:
1.	How likely “Real World – CO2 Emissions (g/KM) will be to the WLTP (World harmonized Light Vehicle Test Procedure) Standard in Europe for vehicles model year 2018 to 2023.
a.	Identify the Price Point (vehicle make & model) at which a vehicle’s CO2 Emissions (g/KM) is most beneficial for the environment by reviewing how price point of vehicle drives/influences CO2 Emissions.
For these vehicle Makes:
1.	Audi AG 2978
2.	Peugeot 11817 
3.	Bentley 70 
4.	BMW AG 10876 
5.	Ferrari 58
6.	Fiat 15126
7.	Ford Werke GMBH 84828
8.	Hyundai Czech 1592
9.	Jaguar Land Rover Limited 4918
10.	Kia Slovakia 1391
11.	Mazda 1950
12.	Mercedes-Benz AG 29995
13.	Nissan Auto 6872
14.	Porsche 2192
15.	Renault 28846
16.	Rolls Royce 20
17.	Seat 2934
18.	Suzuki2231
  Because the Co2 Dataset was too large we eliminated some of the columns in excel before uploading it into the code. For our analysis we did what we had done in previous projects and first listed the visualizations & steps or code that made sense before we opened VS Code or Google Collab to start adding code. We chose the following visualizations in our initial plan:
1.	Import panda libraries and dependencies
2.	Preprocess xls file
3.	Import, read, and write data frame
4.	Remove columns and rename columns
5.	The CO2 data and Car Price Data cleaned by sorting and dropping empty rows (fill null values etc).
6.	Merge CO2 data and Car Price Data (on Brand)
7.	Visualizations
1.	Scatterplot -Al
2.	Boxplot - Ebeni
3.	Pairplot
4.	Heatmap
5.	Correlation & bar chart
6.	Histogram
8.	Test/Train/Split Data
9.	Normalization Factor for standardizing the data (NN – Day 3 activity 2 – preprocessing) in respect to the target ~ 95 g C02 /km (cars) and 147 g C02 /km (vans)
10.	 Fit the Model and compare several models for accuracy
11.	 Prediction Model (18 -Neural Networks Day 2 activities 5 & 7) – Printing the top 3 numbers. Day 2 ex.7 – Predicting objectivity (making predictions) 
12.	 Evaluations:   (NN- Day 3 Activity 6 ) generate recommendations for price and C02 -> generate a code.  Addresses 2nd part
Once we began working on the datasets we realized that the comparison of Car Prices from our second dataset would not be an accurate comparison to the Co2 numbers as they are for different years and the difference is too far apart for an accurate comparison. Where as the dataset for Car prices included model years from the 70’s through the 90’s, the Co2 dataset was for cars in model year 2021. Because of this discrepancy we decided to research the average car price per make in 2021 and adding that to our dataset using a for loop, and not merge the two datasets. Instead each serves as an individual reference point. 
With that decision made we began adding the code to our VS File and ran the first set of corrections on 7/29. To add the code we relied on previous homework & class asingments and we also had the need for a line of code that we had not reviewed in class before, which was to make the text in our datasets lower case so that they wouldn’t cause syntax errors, that line of code was: 
df = df.applymap(lambda x: x.lower() if isinstance(x, str) else x)

20.	Toyota 6338
21.	Volkswagen 21296
22.	Volvo 8988


