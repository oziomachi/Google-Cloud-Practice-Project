#LAB: Google Cloud Fundamentals: Getting Started with App Engine

##Objectives:

In this lab, you learn how to perform the following tasks:

-Initialize App Engine.

-Preview an App Engine application running locally in Cloud Shell.

-Deploy an App Engine application, so that others can reach it.

-Disable an App Engine application, when you no longer want it to be visible.

##Stages:

1.Initialize App Engine:

-Initialize App Engine app with a project and choose its region:

    gcloud app create --project=$DEVSHELL_PROJECT_ID --region=us-central

-Clone the source code repository for a sample application in the hello_world directory:

    git clone https://github.com/GoogleCloudPlatform/python-docs-samples

-Navigate to the source directory:

    cd python-docs-samples/appengine/standard_python3/hello_world

2.Run Hello World application locally:

-Download and update the packages list:

sudo apt-get update

-Set up a python virtual environment in which the application will run:

sudo apt-get install virtualenv -y

-If prompted [Y/n], press Y and then Enter

virtualenv -p python3 venv

-Activate the virtual environment

source venv/bin/activate

-Navigate to the project directory and install dependencies

pip install -r requirements.txt

-To run the application:

python main.py

3.Deploy and run Hello World on App Engine:

-Navigate to the source directory:

cd ~/python-docs-samples/appengine/standard_python3/hello_world

-Deploy your Hello World application:

gcloud app deploy

-If prompted enter y

-Launch your browser to view the app:

gcloud app browse

4.Disable the application:

gcloud app versions stop 20200910t135648

Note: Auto-scaling has to be disabled
