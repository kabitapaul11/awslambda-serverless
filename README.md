# awslambda-serverless
AWS lambda to build server-less Data Engineering pipeline
Steps:
- Launch Cloud9 console
- Create Cloud9 environment
- Create a github repo
- Clone your git repo to your cloud9 instance
- Go to AWS resources create lambda function select python environment. Choose a role (admin).
- create the lambda with named "producer" serverless wizard. Copy the code of populate_sqs.py in git repo and paste here in producer/lambda_function.py
- Go to dyanamodb and create table "fang" with company names.
- Go to SQS and create a queue. Then copy the queue url and replace it in producer/lambda_function.py
- cd into lambda and install packages on level up if not already installed.
    pip3 install boto3 --target ../
    pip3 install python-json-logger --target ../
- Right click on lambda function and deploy it.
- Go to Lambda console, you should be able to see the function running.
- Add a cloud watch trigger.
- Check the SQS service.
