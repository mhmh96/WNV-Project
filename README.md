Executive Summary

0. Guide to the notebooks:

There are two sequential notebooks containing initial EDA and documenting feature engineering.  These are 01_Data_Setup and 02_Additional_Data_Setup.  03_Models documents predictive modeling on the data, and 04_Measurement_locations generates a map of standing water, spray site, and testing site locations in Chicago (based on mapping code supplied).

1. Division of Labor

Kiros and David worked on the notebook.  Harsha worked on developing the presentation.

2. Data Setup

Determined which species of mosquito are most common, and which are most likely to carry WNV.  Made dummies to reflect whether trap data corresponded to one of the chief carrier mosquitos, and whether trap data collected from a particular street.  Obtained total pricipation data, and average temperature data for the 14 days prior to the date of each trap measurement.  Obtained distance to the nearest site where standing water was reported to the city of Chicago and to the nearest site where pesticides were sprayed (for the years in which data were available: 2011 and 2013).

3. Additioanl Data Setup

Obtained the average day length for the 7 days prior to the date of trap measurement.  Obtained wind data for the 20 days prior to the date of measuremeent.  Added latitude, longitude data (although only longitude data used for modeling).

4. Modeling

Notebook contains some EDA, to describe the relationship between the day length, weather, and longitude features and WNV classification status.  Day length was the feature that varied the most dramatically between the two classes.  Generated models (Random Forest, SVC, and Logistic Regression).  Generated Kaggle submission.

5. Kaggle Score is reported in 05_Kaggle Score.png.  Best AUC_ROC score was .665, generated using logistic regression.  The primary features relied on by the logistic regression were day length, day length squared, the particular mosquito found in the trap, and recent temperature, the longitude (i.e., distance to Lake Michigan), wind in the recent past, and whether the trap was from certain streets that were "hot spots" for WNV.
