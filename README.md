# Data Science Immersive Bootcamp Project
## Heart Disease
## 1. Introduction 

Health care analytics is analysis activities that can be undertaken as a result of data collected from healthcare; claims and cost data, 
pharmaceutical and research and development (R&D) data.


###   Dataset information

Heart disease  is a class of diseases that involve the heart or blood vessels. Cardiovascular diseases are the leading cause of death globally. 
This database contains 14 attributes

1-age: The person's age in years

2-sex: The person's sex (1 = male, 0 = female)

3-cp: The chest pain experienced (Value 1: typical angina, Value 2: atypical angina, Value 3: non-anginal pain, Value 4: asymptomatic)

4-trestbps: The person's resting blood pressure (mm Hg on admission to the hospital)

5-chol: The person's cholesterol measurement in mg/dl

6-fbs: The person's fasting blood sugar (> 120 mg/dl, 1 = true; 0 = false)

7-restecg: Resting electrocardiographic measurement (0 = normal, 1 = having ST-T wave abnormality, 2 = showing probable or definite left ventricular hypertrophy by Estes' criteria)

8-thalach: The person's maximum heart rate achieved

9-exang: Exercise induced angina (1 = yes; 0 = no)

10-oldpeak: ST depression induced by exercise relative to rest ('ST' relates to positions on the ECG plot. See more here)

11-slope: the slope of the peak exercise ST segment (Value 1: upsloping, Value 2: flat, Value 3: downsloping)

12-ca: The number of major vessels (0-3)

13-thal: A blood disorder called thalassemia (3 = normal; 6 = fixed defect; 7 = reversable defect)

14-target: Heart disease (1 = Have disease , 0 = Haven't disease)

## 2. Tools 
### 1- Python 
Python provide great functionality to deal with mathematics, statistics and scientific function. It provides great libraries to deals with data science application.

![python-logo-C50EED1930-seeklogo com](https://user-images.githubusercontent.com/58987879/100966349-b9b73180-353d-11eb-9927-d6ebc30fd91e.png)

### 2- Power BI 
Power BI is a business analytics service by Microsoft. It aims to provide interactive visualizations and business intelligence capabilities
with an interface simple enough for end users to create their own reports and dashboards.

![images-2](https://user-images.githubusercontent.com/58987879/100966336-b1f78d00-353d-11eb-9898-e7965a4a38ff.png)



## 2. Data Preparation

```python
import os
import csv 
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

```python
path= "c:/Users/AlmousaRazan/Documents/python"

data= pd.read_csv(path+'/heart.csv')

```

```python

print(data.head())

```
<img width="702" alt="Screen Shot 2020-12-02 at 7 29 13 PM" src="https://user-images.githubusercontent.com/58987879/100929216-58b93a80-34f8-11eb-89ce-060fe6352d63.png">

#### Calculate Corrlation 


```python
corr = data.corr()
fig = plt.figure()
ax = fig.add_subplot(111)
cax = ax.matshow(corr,cmap='coolwarm', vmin=-1, vmax=1)
fig.colorbar(cax)
ticks = np.arange(0,len(data.columns),1)
ax.set_xticks(ticks)
plt.xticks(rotation=90)
ax.set_yticks(ticks)
ax.set_xticklabels(data.columns)
ax.set_yticklabels(data.columns)
plt.show()
```
<img width="941" alt="Screen Shot 2020-12-02 at 7 24 49 PM" src="https://user-images.githubusercontent.com/58987879/100900655-1b42b600-34d4-11eb-8fa3-18232ab033e1.png">

```python
minAge=min(heart.age)
maxAge=max(heart.age)
meanAge=heart.age.mean()
print('Min Age :',minAge)
print('Max Age :',maxAge)
print('Mean Age :',meanAge)
```
<img width="712" alt="Screen Shot 2020-12-02 at 7 32 04 PM" src="https://user-images.githubusercontent.com/58987879/100929312-7d151700-34f8-11eb-964a-fef759810127.png">

## 3. Visualization
### Dashboard

![project Dec 2](https://user-images.githubusercontent.com/58987879/100929383-9ddd6c80-34f8-11eb-84cd-c462f31c3b68.jpg)
