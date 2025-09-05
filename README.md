# Postman API Automation Integration with Github Actions #

THis repository is a demonstration for POC for integrating postman tests with github actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The projects runs on a scheduled time with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://vishalksv.github.io/Phoenix-Inwarranty-Flow/ 
The latest report is mailed to the team members using GMAIL SMTP.

## About me ##
Hi, My name is Vishal Kumar, I have 4 years of experience in Automation testing. My skillset includes UI automation with Selenium Webdriver, Postman for API Testing.
You can connect with me over: https://www.linkedin.com/in/vishalkumarks/

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets
   
## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman Test at Github Page Link: https://vishalksv.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Repost](https://github.com/vishalksv/Phoenix-Inwarranty-Flow/blob/static-content/PostmanReport.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ Inwarranty Flow Collection Copy 2.postman_collection.json # Collection File
├─ QA.postman_environment.json # Environment File
└─ testDataCreateJob.csv # TestData File

```

## How to run the project? ##
You can run the project on your local system for that:
1. Clone the Project on local system: https://github.com/vishalksv/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman using - ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra package - ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman Command:

           newman run 'Inwarranty Flow Collection Copy 2.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testDataCreateJob.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html 
 
