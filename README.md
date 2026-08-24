# azure-ci-pipeline
This repo is for the Cloud DevOps using Microsoft Azure course

[![Python application test with Github Actions](https://github.com/etharalrehaili/azure-ci-pipeline/actions/workflows/python-app.yml/badge.svg)](https://github.com/etharalrehaili/azure-ci-pipeline/actions/workflows/python-app.yml)

<img width="1455" height="591" alt="image" src="https://github.com/user-attachments/assets/54f9b115-d712-4feb-bc7b-c2f1a7e41cf2" />

<img width="1455" height="329" alt="image" src="https://github.com/user-attachments/assets/fb38c985-d107-472f-8a9a-841d187652bb" />


# Overview

This project sets up a CI/CD pipeline on Microsoft Azure for a Flask machine learning API that predicts Boston housing prices. GitHub Actions handles Continuous Integration (linting and testing), and Azure Pipelines handles Continuous Delivery, automatically building and deploying the app to Azure App Service on every push to `main`.

## Project Plan

<TODO: Project Plan
* A link to a Trello board for the project
* A link to a spreadsheet that includes the original and final project plan>

## Instructions

### Architectural Diagram

```
GitHub Repo --push--> GitHub Actions (lint + test)
             --push--> Azure Pipelines (build + deploy) --> Azure App Service --> Flask ML API
```

### Running the project

1. Clone the repo:
```
   git clone https://github.com/etharalrehaili/azure-ci-pipeline.git
   cd azure-ci-pipeline
```
2. Set up a virtual environment and install dependencies:
```
   python3 -m venv ~/.azure-ci-pipeline
   source ~/.azure-ci-pipeline/bin/activate
   make install
```
3. Run lint and tests:
```
   make all
```
4. The Flask ML app (`flask-sklearn/`) auto-deploys to Azure App Service via Azure Pipelines on every push to `main`. Live app:
   `https://azure-ci-pipeline-ethar.azurewebsites.net`
5. Test a live prediction:
```
   cd flask-sklearn
   ./make_predict_azure_app.sh
```

### Screenshots

* Project running on Azure App Service
* Project cloned into Azure Cloud Shell
* Passing tests from `make all`
* Output of a test run
* Successful deploy in Azure Pipelines
* Azure App Service running from Azure Pipelines automatic deployment
* Successful prediction from deployed Flask app:
```bash
  udacity@Azure:~$ ./make_predict_azure_app.sh
  Port: 443
  {"prediction":[2.431574790057212]}
```
* Output of streamed log files from deployed application

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo

https://www.youtube.com/watch?v=BSiFoYAATVg
