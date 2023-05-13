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

### The files

The files themselves have 14 columns each. However, some of the files have bogus or
incomplete data in several columns.