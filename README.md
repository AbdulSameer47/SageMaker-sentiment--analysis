# Deep Learning Udacity Nanodegree - SageMaker Deployment Project


This is the final solution of the project 'Sagemaker Deployment' which consists in deploying a Sentiment Analysis model using RNN in the Amazon AWS SageMaker tool. The notebook and Python files provided here result in a simple web app which interacts with a deployed recurrent neural network performing sentiment analysis on movie reviews.

In the final architecture AWS API Gateway and AWS Lambda functions is used as well. The application architecture diagram is:

![Web app Diagram](./Web&#32;App&#32;Diagram.svg) 

You can find the original code without solutions in the original [Udacity SageMaker Deployment repository](https://github.com/udacity/sagemaker-deployment).

 This project assumes some familiarity with SageMaker, the IMDB Sentiment Analysis using XGBoost mini-project (which can be found in the original repository) should provide enough background.


## Setup instructions
Please see the [original README](https://github.com/udacity/sagemaker-deployment/tree/master/README.md) in the root directory for instructions on setting up a SageMaker notebook and downloading the project files (as well as the other notebooks). For the solutions only clone this repository:

```
cd SageMaker
git clone https://github.com/hjlopes/sagemaker-sentiment-analysis
exit
```
Instructions
Some template code has already been provided for you, and you will need to implement additional functionality to successfully complete this notebook. You will not need to modify the included code beyond what is requested. Sections that begin with 'TODO' in the header indicate that you need to complete or implement some portion within them. Instructions will be provided for each section and the specifics of the implementation are marked in the code block with a # TODO: ... comment. Please be sure to read the instructions carefully!

In addition to implementing code, there will be questions for you to answer which relate to the task and your implementation. Each section where you will answer a question is preceded by a 'Question:' header. Carefully read each question and provide your answer below the 'Answer:' header by editing the Markdown cell.

Note: Code and Markdown cells can be executed using the Shift+Enter keyboard shortcut. In addition, a cell can be edited by typically clicking it (double-click for Markdown cells) or by pressing Enter while it is highlighted.

# General Outline
Recall the general outline for SageMaker projects using a notebook instance.

## Download or otherwise retrieve the data.
Process / Prepare the data.
Upload the processed data to S3.
Train a chosen model.
Test the trained model (typically using a batch transform job).
Deploy the trained model.
Use the deployed model.
For this project, you will be following the steps in the general outline with some modifications.

First, you will not be testing the model in its own step. You will still be testing the model, however, you will do it by deploying your model and then using the deployed model by sending the test data to it. One of the reasons for doing this is so that you can make sure that your deployed model is working correctly before moving forward.

In addition, you will deploy and use your trained model a second time. In the second iteration you will customize the way that your trained model is deployed by including some of your own code. In addition, your newly deployed model will be used in the sentiment analysis web app.

## Step 1: Downloading the data
As in the XGBoost in SageMaker notebook, we will be using the IMDb dataset


 
