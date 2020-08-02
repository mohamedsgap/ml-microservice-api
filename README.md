# PROJECT: Operationalize a Machine Learning Microservice API

[![circleCI](https://circleci.com/gh/mohamedsgap/ml-microservice-api.svg?style=svg)](https://app.circleci.com/gh/mohamedsgap/ml-microservice-api)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API.

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:

- Test your project code using linting
- Complete a Dockerfile to containerize this application
- Deploy your containerized application using Docker and make a prediction
- Improve the log statements in the source code for this application
- Configure Kubernetes and create a Kubernetes cluster
- Deploy a container using Kubernetes and make a prediction
- Upload a complete Github repo with CircleCI to indicate that your code has been tested

---

### Requirements

- [Python 3](https://www.python.org/downloads/)
- [Docker](https://docs.docker.com/docker-for-mac/)
- [Kubernetes](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/)

### Setup the Environment

- Create a virtualenv and activate it
- Run `make install` to install the necessary dependencies

### Running `app.py`

    python app.py

### Linting project codes

    make lint

### Run applicaion with docker.

    ./run_docker.sh

### Upload docker image

    ./upload_docker.sh

### Configure Kubernetes to Run locally

    minikube start
    kubectl get pod

After pod status change to `Running`

    ./run_kubernetes.sh

### To test application via Docker or Kubernetes

    ./make_prediction.sh

### Files

- config.yml: CircleCI configuration file.
- Makefile: includes instructions for setup, install, test and lint.
- app.py: Python application file.
- Dockerfile: Dockerfile for build and expose.
- run_docker.sh: Shell file to run Docker, locally.
- upload_docker.sh: Shell file to upload Docker image.
- run_kubernetes.sh: Shell file to run the app with kubernetes.
- make_prediction.sh: Shell file to test flask app locally.

**This project is part of my Cloud DevOps Nanodegree on Udacity**
