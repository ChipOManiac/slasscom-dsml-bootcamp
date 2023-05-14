# Assignment report

## Objective

The initial objective on first reading appeared to be to create and train a
model to use the data-sets given. This model would then be used to look
through any other data set with the same attributes in order to determine
if a patient had the risk of heart-disease.

Apparently not. In general the assignment appeared to be, on further
reading, simply asking me to perform some standard analysis on the data to
determine correlations.

## The data-sets
Data-sets are available at: 

https://archive.ics.uci.edu/ml/datasets/Heart+Disease

The raw data consists of a large number of attributes which would make it 
difficult to determine a correlation between the attributes and heart-disease.

Fortunately for us, the data-providers have processed the data to include only
14 attributes.

The attributes are as follows:

  1. Age (in years)
  2. Sex:
     - 0:female
     - 1:male
  3. Type of chest-pain:
     - 1:typical angina
     - 2:atypical angina
     - 3:non-typical pain
     - 4:asymptomatic
  4. Blood-pressure at rest (in mm of Mercury on admission to hospital)
  5. Serum cholesterol (in mg/dl)
  6. Fasting blood-sugar that is greater than 120 mg/dl:
     - 0:false
     - 1:true
  7. Electro-cardiograph results at rest:
     - 0:normal
     - 1:having ST-T wave abnormality
     - 2:showing probable or definite left ventricular hypertrophy by Estes' criteria
  8. Maximum heart rate achieved
  9. Existence of exercise induced angina:
     - 0:false
     - 1:true
  10. ST depression induced by exercise relative to rest
  11. Slope of the peak exercise ST segment:
     - 1:upsloping
     - 2:flat
     - 3:downsloping
  12. Number of major vessels coloured by flouroscopy (between 0-3)
  13. "thal" (unknown attribute):
     - 3:normal
     - 6:fixed
     - 7:reversable defect
  14. Diagnosis of heart-disease (angiographic disease status):
     - 0:diameter narrowing of <50% (diameter is sufficiently large)
     - 1:diameter narrowing of >50% (diameter is sufficiently small)

## Log

We started by defining the columns headings in a variable. We then used this
variable when loading the first data-set (Cleveland) into a data-frame called
'df1_raw', which we checked dimensions on and did a head of the data.

Next, we started to assign data-types to each of the columns, assigning the
data-types one-by-one. Unfortunately, some assignments didn't happen. 
Examination showed that there were columns where missing information was 
denoted with a '?', which were preventing setting data-types to numeric values.

These rows of missing data were removed for each data-type assignment, until
the complete assignment of data-types to columns were complete.

Next, we attempted to load in data from the other three data-sets. However,
it seems that all of the rows were missing at least one column of data,
resulting in all the data sets having to be discarded.

A quick view of the 'reprocessed.hungarian.data' determined, that the missing
values were simply replaced with '-9', which made the data still incomplete.

The last part was in visually representing the data, for which we used the
plot() function implicit to Pandas data-frames to create histograms.

Since the required label is 'Diagnosis' we grouped the rows by that and plotted
graphs for each of the columns.

We made two graphs for each column, one for histograms, one for scatterplots.

## Question: Logistics Regression Model

Question:

"Do you think whether you can use logistics regression model to 
predict the heart disease. Explain."

Answer: 

Yes. In this data-set, the dependent variable is binary, and the
independent variables are either binary or continious.

## Histograms

![Diagnosis by Age](../graphs/01-hist-diagnosis-by-age.png "Diagnosis by Age")
![Diagnosis by Sex](../graphs/02-hist-diagnosis-by-age.png "Diagnosis by Age")
![Diagnosis by Chest Pain Area](../graphs/03-hist-diagnosis-by-chestpaintype.png "Diagnosis by Chest Pain Area")
![Diagnosis by Blood Pressure](../graphs/04-hist-diagnosis-by-bloodpressure.png "Diagnosis by Blood Pressure")
![Diagnosis by Fasting Blood Sugar Greater than 120](../graphs/05-hist-diagnosis-by-fastingbloodsugar.png "Diagnosis by Fasting Blood Sugar Greater than 120")
![Diagnosis by ECG At Rest](../graphs/06-hist-diagnosis-by-ecgatrest.png 'Diagnosis by ECG At Rest')
![Diagnosis by Max. Heart Rate](../graphs/07-hist-diagnosis-by-maxheartrate.png 'Diagnosis by Max. Heart Rate')
![Diagnosis by Diagnosis by Prescense of Exercise Induced Angina](../graphs/08-hist-diagnosis-by-hasexerciseinducedangina.png 'Diagnosis by Prescense of Exercise Induced Angina')
![Diagnosis by ST Depression](../graphs/09-hist-diagnosis-by-stdepression.png 'Diagnosis by ST Depression')
![Diagnosis by ST Slope](../graphs/10-hist-diagnosis-by-stslope.png 'Diagnosis by ST Slope')
![Diagnosis by Major Vessel Count in Flouroscopy](../graphs/11-hist-diagnosis-by-vesselsinflouroscopy.png 'Diagnosis by Major Vessel Count in Flouroscopy')
![Diagnosis by Thal](../graphs/12-hist-diagnosis-by-thal.png 'Diagnosis by Thal')

## References

  - [https://stackoverflow.com/questions/33303644/pandas-data-frame-find-all-rows-with-particular-column-value]
  - [https://stackoverflow.com/questions/1841565/valueerror-invalid-literal-for-int-with-base-10]
  - [https://stackoverflow.com/questions/23307301/replacing-column-values-in-a-pandas-dataframe]
  - [https://stackoverflow.com/questions/59204445/how-to-do-i-groupby-count-and-then-plot-a-bar-chart-in-pandas]
  - [https://stackoverflow.com/questions/50582168/pandas-get-all-columns-that-have-constant-value]
  - [https://pandas.pydata.org]
  - [https://towardsdatascience.com/discovering-patterns-in-data-with-exploratory-data-analysis-fd07ce1c5efa]
  - [https://www.kaggle.com/code/robikscube/introduction-to-exploratory-data-analysis/notebook]
  - [https://www.youtube.com/watch?v=xi0vhXFPegw]
  - [https://en.wikipedia.org/wiki/Logistic_regression]
