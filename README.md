# Advanced Data Analysis of flights

This Github repository contains code for analyzing flight delay data from the years 2009 to 2018 using **Spark** . The main goal of this project is to provide insights into flight delays, allowing users to query information based on specific variables.

The initial step involved merging the "flights" dataframe with the "holidays" dataframe to include all relevant information. Additional columns were created to classify the date as a weekday/weekend, holiday/non-holiday, and specific day of the week.

To measure average arrival delay, four statistics were computed using the ARR_DELAY variable, which is more useful to users than the DEP_DELAY variable. These statistics were computed over a window of 7, 30, or 365 days or based on carrier, with each average value being computed excluding cancelled flights.

The final dataframe, "finalDF," was created by merging all of the relevant information and sorting it in ascending order of delays.

Furthermore, a classification model was built and evaluated based on whether the departure delay was less than 10 minutes or greater than or equal to 10 minutes, and flights were classified as SHORT or LONG delays.

The code was run with the 2018 year dataset and can be run on Google Colab or other environments. The flights dataset used in this project was obtained from the Bureau of Transportation Statistics, and it includes information on domestic flights within the United States.

To query information, users can specify the origin and destination airports and the carrier they wish to travel with.

Drive folder with data: https://drive.google.com/drive/folders/1XW2vvXh2flZS03fW28FRXLH2C4CaFUVR?usp=sharing
