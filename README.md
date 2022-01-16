# Udagram

This application is provided to you as an alternative starter project if you do not wish to host your own code done in the previous courses of this nanodegree. The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.

You will find the result of hours after hours of trying to figure out how this stuff works at:

- http://udagram-salzteig.s3-website-us-east-1.amazonaws.com/ (frontend in S3 bucket)
- http://udagram-env.eba-6ztdwjmr.us-east-1.elasticbeanstalk.com/ (backend via Elastic Beanstalk)

## CircleCI build status
[![otacke](https://circleci.com/gh/otacke/udacity-dev-ops-capstone-project.svg?style=svg)](https://github.com/otacke/udacity-dev-ops-capstone-project)

## Getting Started
There's a starter project at https://github.com/udacity/nd0067-c4-deployment-process-project-starter that
I adjusted: Added calls to scripts in package.json files, added `.env` file (see below), added scripts to
run test/deployment, added circleci configuration added docs, ...

The `.env` file needs to go into the `udagram-api` folder. It should look like
this:

```
POSTGRES_PORT=<postgres db port, e.g. 5432>
POSTGRES_DB=<postgres db name>
POSTGRES_USERNAME=<postgres db user name>
POSTGRES_PASSWORD=<postgres db password>
POSTGRES_HOST=<postgres db host, e.g. aws rds endpoint>
AWS_BUCKET=<name of s3 bucket for image storing>
URL=<backend address, e.g. elastic beanstalk endpoint>
AWS_REGION=<default aws region, e.g. us-east-1>
AWS_PROFILE=<aws profile>
AWS_ACCESS_KEY=<aws iam access key id>
AWS_SECRET=<aws iam secret access key>
JWT_SECRET=<some jwt secret>
```

## Rubric
### Preparing source code infrastructure for deployment
#### Write code that demonstrates parameterized environment variables
- [x] No environment variables that change from the development environment and production should be present in the source code.
- [x] A central configuration file is used in order to set the environment variables and make them available to the code.
- [x] No authentication strings are hard-coded in the source code.

No environment variable or authentication string was put into the source code. I had to make changes, but they refer to the `.env` file.

#### Write a project-level package.json file and organize it properly
- [x] A project-level package.json file should contain scripts for running: Tests, Builds
- [x] Any new dependencies should be located in the devDependencies section of the package.json.

The [file is in the root directory of the repository](https://github.com/otacke/udacity-dev-ops-capstone-project/blob/master/package.json) and no devDependencies were added.

#### Configure the needed infrastructure for a web application
- [ ] Screenshots of the AWS console indicate that the following services are properly set up, i.e. healthy and accessible: AWS RDS for the database, AWS ElasticBeanstalk (or alternatives like lambda) for the API, AWS s3 for web hosting
- [x] The app is accessible via the link provided.

**TODO:** Screenshots. Links: [frontend in S3 bucket](http://udagram-salzteig.s3-website-us-east-1.amazonaws.com/), [backend via Elastic Beanstalk](http://udagram-env.eba-6ztdwjmr.us-east-1.elasticbeanstalk.com/)

### Configuring Continuous Integration Pipeline with Github
#### Trigger a successful pipeline on each push to the main branch
- [ ] A screenshot of the last build shows that the student’s CircleCi account is authorized to access his/her repo on Github and is detecting changes each time he/she is pushing to the main branch.
- [x] Optionally, a build status badge is present in the README.md, indicating the current state of the main branch build.

**TODO:** Screenshot. Build status: [![otacke](https://circleci.com/gh/otacke/udacity-dev-ops-capstone-project.svg?style=svg)](https://github.com/otacke/udacity-dev-ops-capstone-project)

#### Write a proper pipeline file using the config.yml format used by CircleCi
- [x] The submission includes a config.yml that ensures the build occurs in a logical sequence. Comments help explain the flow of the pipeline and are straight to the point.
- [x] The pipeline file uses correct syntax and can be executed by CircleCi.

There's a [CircleCI configuration](https://github.com/otacke/udacity-dev-ops-capstone-project/blob/master/.circleci/config.yml) and it obviously can be executed given that there's a (passing) build status.

#### Configure secrets via the Continuous Integration software
- [ ] All the secrets found in the application are configured inside CircleCi and passed to the production application. A screenshot of the configuration screen is present to show where secrets were added.

**TODO:** Screenshot

### Documenting Deployment Process
#### Write code that demonstrates a well-organized docs folder
- [ ] A documentation folder should include separate pages on different topics that cannot be discovered by just quickly glancing at code: Infrastructure description, App dependencies, Pipeline process

**TODO**

#### Prepare an architecture diagram to document the deployment flow
- [ ] The submission contains a simple diagram giving a high-level overview of the infrastructure and another diagram showing the overview of the pipeline. The diagram Includes the different AWS services used for hosting the following: DB, API, Front-End
- [ ] A representation of the communication between the services is present in the diagram (ex: arrows between services).

**TODO**

## License

[License](LICENSE.txt)
