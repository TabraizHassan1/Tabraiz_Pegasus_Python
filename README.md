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

The '.venv'contains python virtual envirnment information. The 'app.py' in the project folder is the 'main' for the sample application. It is the entry point for the app. The code in this file loads an instance of class 'tabraizSprint1stack'  The 'sprint1_stack.py' is a custom CDK stack construct that is to be used in our CDK application.


