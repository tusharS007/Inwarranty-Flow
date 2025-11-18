# Postman API AUtomation Integration with Github Actions #

This repository is a POC for integrating postman test with github actions. The tests are written in Postmna and they are executed with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger every push to the main branch. You can also execute peoject manually using workflow_dispatch. The projects run on scheduled time with the help of the cron job.

The html report is archieved and kept in artifact section for team to download it. Along with that they can view the report directly from the github page https://tushars007.github.io/Inwarranty-Flow/
The latest reports is made to the team members using GMAIL SMTP.

## About Me ##
Hi, I’m Tushar Shelar. I have 4.5+ years of experience in QA, including over 2 years in Automation Testing. My skill set includes UI automation using Selenium WebDriver and API testing with Rest Assured and Postman. 
I also have hands-on experience with SQL and a strong background in functional testing.

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets


## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. GMAIL SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 Instance for Self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://tushars007.github.io/Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/tusharS007/Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json #Collection File
├─ QA.postman_environment.json #Environment file
└─ testdata.csv #Test Datafile

```

## How to run the project ##
You can run the project on your local system for that:
1. Clone the project on local system: ```https://github.com/tusharS007/Inwarranty-Flow.git```
2. Install Nodejs and NPM from:``` https://nodejs.org/en```
3. Install Newman using: ``` npm install -g newman```
4. Install Newman-reporter-htmlextra:``` npm install -g newman-reporter-htmlextra```
5. Run the Neman Command:
```
              newman run 'Inwarranty-flow Collection_CLI.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
```


