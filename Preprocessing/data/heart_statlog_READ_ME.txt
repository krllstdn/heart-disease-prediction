Heart Disease Dataset Attribute Description
S.No. Attribute Code given Unit Data type
1 age - Age in years Numeric
2 sex - Sex 1, 0 Binary
3 chest pain type - chest pain type 1,2,3,4 Nominal
4 resting bp s - resting blood pressure in mm Hg Numeric
5 cholesterol - serum cholesterol in mg/dl Numeric
6 fasting blood sugar - fasting blood sugar 1,0 > 120 mg/dl Binary
7 resting ecg - resting electrocardiogram results 0,1,2 Nominal
8 max heart rate - maximum heart rate achieved 71–202 Numeric
9 exercise angina - exercise induced angina 0,1 Binary
10 oldpeak - oldpeak =ST depression Numeric
11 ST slope - the slope of the peak exercise ST segment 0,1,2 Nominal
12 target - class 0,1 Binary

Description of Nominal Attributes
Attribute Description
Sex 1 = male, 0= female;

Chest Pain Type -- Value 1: typical angina
-- Value 2: atypical angina
-- Value 3: non-anginal pain
-- Value 4: asymptomatic

Fasting Blood sugar
(fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)

Resting electrocardiogram results
-- Value 0: normal
-- Value 1: having ST-T wave abnormality (T wave inversions
and/or ST elevation or depression of > 0.05 mV)
-- Value 2: showing probable or definite left ventricular
hypertrophy by Estes' criteria

Exercise induced angina
1 = yes; 0 = no

the slope of the peak exercise ST segment
-- Value 1: upsloping
-- Value 2: flat
-- Value 3: downsloping

class 1 = heart disease, 0 = Normal


This dataset includes 272 duplicate records, notably all data from statlog is in the original dataset. Also all locations where data was previously missing look like they were simply set to 0. User beware.
How to deal with the cholestrol column with zeroes in it?
Check outliers first, if they're too many, use the median value to replace the zeros, otherwise use the mean value.

