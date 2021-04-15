# End-to-end Bedrock tutorial on Google Cloud or AWS

This example demonstrates how to use Bedrock to preprocess data, train a model and create a HTTPS endpoint for serving. This example complements [Bedrock documentation](https://docs.basis-ai.com/guides/quickstart).

This example uses sample customer churn data. The code shows how to
- read data from GCS or S3 bucket
- preprocess the data and generate features
- train a LightGBM classifier model
- deploy the model as an endpoint

### Data exploration and Model prototyping
See [notebook](./doc/churn_prediction.ipynb)

## Goals
At the end of the tutorial, the user will be able to
- set up a Bedrock training pipeline
- monitor the training
- deploy a model endpoint in HTTPS
- query the endpoint
- monitor the endpoint API metrics

## Run on Bedrock
Just follow the Bedrock [quickstart guide](https://docs.basis-ai.com/guides/quickstart). We have already prepared the data on GCS so that you do not have to upload any.

## Test your endpoint
After deploying your model as an endpoint, you can test it with the query below
```
'{"State": "ME", "Area_Code": 408, "Intl_Plan": 1, "VMail_Plan": 1, "VMail_Message": 21, "CustServ_Calls": 4, "Day_Mins": 156.5, "Day_Calls": 122, "Eve_Mins": 209.2, "Eve_Calls": 125, "Night_Mins": 158.7, "Night_Calls": 81, "Intl_Mins": 11.1, "Intl_Calls": 3}'
```
