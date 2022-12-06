# Disaster Response Pipeline Project

## Table of contents

- [Background](#background)
- [Installation](#installation)
- [Intstructions](#instructions)
- [Files](#files)


## Background

Airbnb has certainly made an impact on today's hospitality industry. In 2022, Airbnb has recorded 6 million listings in over 100,000 cities world wide, which has left many people wondering, "should I get in on the action?"

## Installation
  The libraries used in this project are all native to Anaconda enviroment. The following libraries were used for the project:
```bash
  import pandas as pd
  import numpy as np
  import matplotlib.pyplot as plt
```

## Instructions
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Go to `app` directory: `cd app`

3. Run your web app: `python run.py`

4. Click the `PREVIEW` button to open the homepage

## Files
 
  The file used in this analysis was retrieved from Kaggle - https://www.kaggle.com/datasets/airbnb/boston.
  The 'listings.csv' data set consists of 2016 Airbnb listings in the Boston Area. There were a total of 3585 unique obersvations and 95 variables.
  
## Summary of Results
1. I observed that there was **no clear relationship** between **price per nights and utilization rate** in the Boston Airbnb listings within the data set 
2. I determined the neighborhoods with the **highest potential revenue** by combining **prices per night * 365 * utilization rates**
3. Finally, I determined the neighborhoods with the **quickest returns on investment** given their yearly revenue potential and the median house prices per neighborhood


