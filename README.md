[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/TnJIQ-Y6)
# Data Mining and Machine Learning Group Coursework


## Group Members

1. Aadithya Sasankan - Aadithya-2002 - H00485735
2. Favour Sukat - Suki-design - H00482718
3. Mozi Kelvin Agara - Kelvin-ag - H00484800
4. Faraz Amjad - farazamjad - H00488469
5. Kai Dong - DKKai-xio - H00476368

## Initial Project Proposal


### Research objectives

Our objective is to classify wildfires based on their causes using historical data by developing and evaluating different machine learning models to determine which algorithms are most effective for this classification problem.
  
### Research questions:
1. How do different machine learning algorithms perform in predicting wildfire causes based on size, location, and date data?
2. Can clustering algorithms reveal patterns in wildfire data that enhance our understanding of the factors influencing wildfire causes?
3. Which features are most significant in predicting wildfire causes, and how does feature importance vary among different models?

### Hypotheses
1. Traditional classification algorithms (Decision Trees, Naïve Bayes, k-NN) will provide a solid baseline performance in predicting wildfire causes.
2. Neural network models will outperform traditional algorithms due to their ability to capture complex patterns in the data.
3. Clustering analysis will identify distinct groups within the data that correspond to different wildfire causes, aiding in feature selection and model performance.

### Source of Dataset

- US Wildfire Dataset
  - Source: [US Forest Service Research Data Archive](https://www.fs.usda.gov/rds/archive/catalog/RDS-2013-0009.6)
  - License: [Open Access](https://www.fs.usda.gov/rds/archive/dataUseInfo)

### About Dataset
#### Some Key Features
- Fires,LOCAL_INCIDENT_ID,Number or code that uniquely identifies an incident for a particular local fire management organization within a particular calendar year.
- Fires,DISCOVERY_TIME,Time of day that the fire was discovered or confirmed to exist.
- Fires,NWCG_CAUSE_CLASSIFICATION,"Broad classification of the reason the fire occurred (Human, Natural, Missing data/not specified/undetermined)."
- Fires,NWCG_GENERAL_CAUSE,"Event or circumstance that started a fire or set the stage for its occurrence (Arson/incendiarism, Debris and open burning, Equipment and vehicle use, Firearms and explosives use, Fireworks, Misuse of fire by a minor, Natural, Power generation/transmission/distribution, Railroad operations and maintenance, Recreation and ceremony, Smoking, Other causes, Missing data/not specified/undetermined)."
- Fires,NWCG_CAUSE_AGE_CATEGORY,"If cause attributed to children (ages 0-12) or adolescents (13-17), the value for this data element is set to Minor; otherwise null."
- Fires,CONT_DATE,"Date on which the fire was declared contained or otherwise controlled (mm/dd/yyyy where mm=month, dd=day, and yyyy=year)."
Fires,CONT_DOY,Day of year on which the fire was declared contained or otherwise controlled.
Fires,CONT_TIME,"Time of day that the fire was declared contained or otherwise controlled (hhmm where hh=hour, mm=minutes)."
- Fires,FIRE_SIZE,The estimate of acres within the final perimeter of the fire.
- Fires,LATITUDE,Latitude (NAD83) for point location of the fire (decimal degrees).
- Fires,LONGITUDE,Longitude (NAD83) for point location of the fire (decimal degrees).
- Fires,STATE,"Two-letter alphabetic code for the state in which the fire burned (or originated), based on the nominal designation in the fire report (not from a spatial overlay)." 

- Example
- FOD_ID: 1
- FIRE-SIZE:0.10
- LATITUDE: 40.036944
- LONGITUDE:-121.005833
- STATE: CA

### Milestones

1. M1: Complete data cleaning and EDA (Week 5)
2. M2: Finish clustering analysis and baseline model implementation (Week 6)
3. M3: Complete neural network models and evaluations (Week 8)
4. M4: Finalize report and presentation materials (Week 10)


## Installing the project

> Follow these steps to set up and run the project:
1. Listing all dependencies and tools required:-
```bash
# Python>=3.10
# !pip install -qy 
# pandas==2.2.3 
# numpy==1.26.4 
# seaborn==0.13.2
# matplotlib==3.9.2 
# scikit-learn==1.5.2
# sqlite3==3.39.5
# imblearn==0.12.4
# tensorflow==2.16.2
# catboost==1.2.7
```
2. Clone the repository:
- git clone https://github.com/dmml-heriot-watt-2024-25/group-coursework-bots-ahead.git

## Data Preparation Pipeline

> Features:
1. Data Loading: Reads raw data from the specified directory in CSV format.
2. Data Cleaning: Removes duplicates, fills missing values , and standardizes column names.
3. Data Preprocessing: Scales numeric features, encodes categorical variables.
4. Visualization: Visualizing the features, clusters, decision trees, and confusion matrix.

> How to run the pipeline:
```bash python run_pipeline.py --input_dir data/wildfire2.csv --output_dir data/processed ```
> Confirm that the processed files are  reated in the output directory:
ls data/processed
Expected output files: train.csv, val.csv, test.csv
Verifying the invocation is identical by checking the output using MD5 Checksum:
```bash md5sum data/processed/train.csv ``` 
Debug errors using verbose logs:
```bash python run_pipeline.py --input_dir data/wildfire2.csv --output_dir data/processed --verbose ```


## Coursework Requirements

### R2. Data Analysis and Exploration
Comprehensive data preprocessing and cleaning to ensure data quality. Exploratory data analysis (EDA) to gain insights into the datasets. Visualization techniques to present data patterns and trends. Feature selection and evaluation should be included. (https://github.com/dmml-heriot-watt-2024-25/group-coursework-bots-ahead/blob/17e87e0c7de1534029809cd974447306dfd31d4b/notebooks/01_data_exploration.ipynb)
### R3. Clustering
Implement an appropriate clustering algorithm to show aspects of the data with similar characteristics. Evaluate the performance of clustering algorithms. Interpret the results and discuss their implications.(https://github.com/dmml-heriot-watt-2024-25/group-coursework-bots-ahead/blob/67e4db5474ce16cd3beffba8e79f428a44fe3aa4/notebooks/02_K-Means_Clustering.ipynb)
### R4.	Baseline Training and Evaluation Experiments
Apply at least three (3) machine learning algorithms to build predictive models, including Decision Trees and two more such as Naïve Bayes, Linear Models, Perceptron and k-Nearest Neighbours. Note your task can be either classification and/or regression, depending on the topic and dataset(s) you choose. Evaluate and compare the models in terms of appropriate metrics for the respective tasks, e.g., accuracy, precision, recall, F-1 or error measures (like RMSE). In the case of Decision Trees discuss their practical applications in the context of the selected datasets/topic. 
(https://github.com/dmml-heriot-watt-2024-25/group-coursework-bots-ahead/blob/67e4db5474ce16cd3beffba8e79f428a44fe3aa4/notebooks/03_DecisionTree.ipynb) 
(https://github.com/dmml-heriot-watt-2024-25/group-coursework-bots-ahead/blob/67e4db5474ce16cd3beffba8e79f428a44fe3aa4/notebooks/04_k-NearestNeighbor.ipynb) 
(https://github.com/dmml-heriot-watt-2024-25/group-coursework-bots-ahead/blob/67e4db5474ce16cd3beffba8e79f428a44fe3aa4/notebooks/05_Naive_Bayes.ipynb)
### R5. Neural Networks
Implement neural network models, such as Multi-Layer Perceptrons (MLPs) and Convolutional Neural Networks (CNN), for tasks such as classification or regression. Train and fine-tune the neural network models. Assess the performance of neural network models and compare them with other techniques.
(https://github.com/dmml-heriot-watt-2024-25/group-coursework-bots-ahead/blob/67e4db5474ce16cd3beffba8e79f428a44fe3aa4/notebooks/06_NeuralNetwork_CNN.ipynb)

## Documentation

Weekly updates are kept in the `documentation/` directory.
