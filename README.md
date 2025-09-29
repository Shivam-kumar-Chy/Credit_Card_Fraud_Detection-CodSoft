Credit Card Fraud Detection App built with Streamlit, FastAPI and Docker
Language Framework Framework Framework hosted Docker build reposize

An end-to-end Machine Learning Project carried out by Group 3 Zummit Africa AI/ML Team to detect fraudulent credit card transactions. Built with FastAPI, Streamlit and Docker.

Contributors
NNEJI IFEANYI DANIEL
IFEZUE TOONNAEMEKA HILARY
SOMTOCHUKWU OGUCHIENTI
KACHUKWU OKOH
You can check out the article on Medium describing in detail how this project was carried out.

https://medium.com/mlearning-ai/credit-card-fraud-detection-2527ca04c3de

Problem Statement
Credit card fraud is an inclusive term for fraud committed using a payment card, such as a credit card or debit card. The purpose may be to obtain goods or services or to make payment to another account, which is controlled by a criminal.

This Streamlit App utilizes a Machine Learning model served as an API with FastAPI framework in order to detect fraudulent credit card transactions based on the following criteria: hours, type of transaction, amount, balance before and after transaction etc.

The machine learning model used for this web application was deployed as an API using the FastAPI framework and then accessed through a frontend interface with Streamlit.

The App can be viewed through this link

The API and its documentation can be viewed here or here.

Data Preparation
Publicly accessible datasets on financial services are scarce, particularly in the newly growing field of mobile money transfers. Many scholars, like us who conduct research in the field of fraud detection, value financial datasets. Because financial transactions are inherently private, there are no publicly accessible datasets, which contributes to the problem. 

A synthetic dataset generated using the simulator called PaySim was used as the dataset for building the model used in this project. PaySim uses aggregated data from the private dataset to generate a synthetic dataset that resembles the normal operation of transactions and injects malicious behaviour to later evaluate the performance of fraud detection methods.

Dataset Link

Modelling
In this project 2 different classification algorithms were tested namely:

Logistic Regression
Random Forest
The final model used for the API was the Random Forest Classifier model which had an accuracy score of 0.99 and an F1 score of 0.86.

Preview
API Demo
api

Streamlit App Demo
credit

How to run API and Streamlit App on Google Colab:
💻 Running the API on Google Colab
💻 Running the Streamlit App on Google Colab
Running on Local Machine 💻
Since we have multiple containers communcating with each other, A bridge network was created called AIservice. For testing, a docker-compose.yml file has been included so as to run both the API and Streamlit app simultaneously as docker containers. To run the API and the Streamlit app on your local machine do the following:

Clone the repository to your local machine
Install docker and docker-compose if you haven't
Open a bash/cmd in the directory and run:
docker network create AIservice
Then run this command
docker-compose up -d --build
After the above steps have been carried out you can now view the documentation of the API and also the Streamlit app.
To visit the FastAPI documentation go to http://localhost:8000 with a web browser.

To visit the Streamlit UI, visit http://localhost:8501.

Logs can be inspected via:

docker-compose logs
The docker-compose method can also be used to deploy the API and Streamlit app on Heroku(using Dockhero which is not free) or using cloud services such as Microsoft Azure, Amazon Web Services or Google Cloud Platform.

Running in a Gitpod Cloud Environment
Click the button below to start a new development environment:

Open in Gitpod

Deployment
The API and Streamlit App have both been deployed using the dockerfile on heroku and Streamlit Cloud respectively.

💻 Deploying the API
💻 Deploying the Streamlit App to Streamlit Cloud
