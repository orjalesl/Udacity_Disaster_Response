# Disaster Response Pipeline Project

## Table of contents

- [Background](#background)
- [Installation](#installation)
- [Intstructions](#instructions)
- [Files](#files)


## Background

Natural disasters require immediate action to attend victims in need; the issue being that first-responder teams are fluded with communications and typically do not have the necessary resources to cover all requests. This project was motivated to create a tool to:
1. Identify messages that require a first-responder team dispatch
2. Classify input messages into specific disaster categories

## Installation
  The libraries used in this project are all native to Anaconda enviroment. The following libraries were used for the project:
```bash
# libraries for data
import pandas as pd
from sqlalchemy import create_engine
  
# libraries for NLP
import re
import nltk
from nltk.corpus import stopwords
from nltk.stem.wordnet import WordNetLemmatizer
from nltk.tokenize import word_tokenize
from sklearn.feature_extraction.text import CountVectorizer, TfidfTransformer

# libraries for Modeling
from sklearn.pipeline import Pipeline
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.multioutput import MultiOutputClassifier
from sklearn.model_selection import GridSearchCV

# library for scoring
from sklearn.metrics import classification_report
```

## Instructions
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Go to `app` directory: `cd app`

3. Run web app: `python run.py`

4. Click the `PREVIEW` button to open the homepage

## Files
There are 2 files used in the project:
1. 'disaster_messages.csv' - comprised of messages used to train the model
2. 'disaster_categories.csv' - comprised of the disaster categories used to label the messages and used as the target variables.


