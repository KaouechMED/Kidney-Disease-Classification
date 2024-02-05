# Kidney-Disease-Classification-MLflow-DVC


## Workflows

1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml
10. app.py

# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/KaouechMED/Kidney-Disease-Classification
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n cnncls python=3.8 -y
```

```bash
conda activate cnncls
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```

```bash
# Finally run the following command
python app.py
```








## MLflow

- [Documentation](https://mlflow.org/docs/latest/index.html)



##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/KaouechMED/Kidney-Disease-Classification.mlflow \
MLFLOW_TRACKING_USERNAME=KaouechMED \
MLFLOW_TRACKING_PASSWORD=0000000000000000000000000000000000000000 \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/KaouechMED/Kidney-Disease-Classification.mlflow

export MLFLOW_TRACKING_USERNAME=KaouechMED 

export MLFLOW_TRACKING_PASSWORD=0000000000000000000000000000000000000000

replace "export" with "set" if you are using windows command prompt

```
### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


# AZURE-CICD-Deployment-with-Github-Actions



## Run from terminal:

docker build -t kidneyapplication.azurecr.io/kidney:latest .

docker login kidneyapplication.azurecr.io

docker push kidneyapplication.azurecr.io/kidney:latest


## Deployment Steps:

1. Build the Docker image of the Source Code
2. Push the Docker image to Container Registry
3. Launch the Web App Server in Azure 
4. Pull the Docker image from the container registry to Web App server and run 