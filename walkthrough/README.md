# Walkthrough

## Setup

Authenticate your local environment with AWS so AWS_ACCESS_KEY and AWS_SECRET_ACCESS__KEY are in the environment

Clone the repo and run the deploy command to setup the lambda function

```
git clone https://github.com/TheTechCompany/zeplin-html-to-pdf

cd zeplin-html-to-pdf

REGION=aws-region FUNCTION=html2pdf yarn deploy
```

Create an API Gateway in AWS with a route pointing to the newly created lambda function and then configure CORS for your intended application.


## Invocation

The invocation url can be used to test by providing an appropriate html blob to the query like e.g. http://$url?html=<html></html>

Data is return as base64 in a json blob this can then be rendered or downloaded as needed

```
{
    data: "base64pdf"
}

```

