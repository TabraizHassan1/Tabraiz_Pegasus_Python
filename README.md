# Pegasus_Python - sprint 1 by tabraiz hassan
CDK Toolkit is used to synthesize an AWS CloudFormation template and the created new app is deployed to AWS account 

## Setup

Download and install Visual Studio Code

Download and install python 

Download, install and configure AWS CLI V2

Git clone from the shared link


### Create project directory

Create empty directories in your system:

```
$ mkdir Tabraiz && cd Tabraiz
$ mkdir sprint1 && cd sprint1
```
### cdk init

We will use cdk init to create a new Python CDK project:
```
$ cdk init sample-app --language python
```
### Activating the Virtualenv

To activate our virtualenv:
```
$ source .venv/bin/activate
```

Now that the virtual environment is activated, we install the required python modules:
```
$ python -m pip install -r requirements.txt
```

### NVM and NPM installation

We will install nvm and nmp:
```
$ nvm install v16.3.0 && nvm use v16.3.0 && nvm alias default v16.3.0
```
Then for npm cdk:
```
$ npm install -g aws-cdk
```

The '.venv' contains python virtual envirnment information. The 'app.py' in the project folder is the 'main' for the sample application. It is the entry point for the app. The code in this file loads and instantiates an instance of class "tabraizSprint1Stack" located in the folder sprint1/sprint1_stack.py. The 'sprint1_stack.py' is a custom CDK stack construct that is to be used in our CDK application. It is the main stack. 


### Lamda 

We create a resource folder in sprint1 in which we create a file 'hw_labda.py'. In this new file, we create a simple 'lambda_handler()' function to print hello world. We add an import 'aws_lambda as _lambda' in the beginning of 'sprint1_stack.py' file and create a lambda function 'create_lambda()' and make changes to the code accordingly. 

### Cdk synth and deploy

After successfully creating, lambda construct we need to synthesize and deploy it to the cloud. AWS CDK apps are effectively only a definition of our infrastructure using code. When CDK apps are executed, they produce or synthesizevan AWS CloudFormation template for each stack defined in our application. 

To synthesize a CDK app, we use:
```
$ cdk synth
```

After this command is run, we can see the cloud formation template and we can find our lambda in the file 'tabraizSprint1Stack.template.json'. 

We then deploy using:
```
$ cdk deploy
```

After deploying, we can check our cloud formation,s3 bucket, lambda, etc in our aws account and also test our lambda function.
