---
title: "CI CD"
date: 2022-06-09T08:57:43+02:00
draft: false
description: "Automated Testing, Continuous Integration and Continuous Delivery"
weight: 4
---

## Automated Testing

![Image alt](/imgs/pocs/ci-cd/Automated-Testing.png)

Automated testing is done through a combination of writing unit tests for the development language used for the project and GitHub action.

### Steps for automated testing:

- GitHub workflow file is created
- Developers write unit tests
- Code changes are committed to GitHub
- Developers create a pull request on GitHub
- GitHub Actions executes the workflow file
- If any tests fail the code cannot be merged into another branch
- The automated tests have a percentage requirement of 75% that needs to be met otherwise merging is blocked

## CI-CD

![Image alt](/imgs/pocs/ci-cd/CI-CD.png)
Continuous development and integration steps:

- CI/CD is executed through GitHub actions and tracked through Jira
- Stories and tasks are created which specify the product requirements
- Developers pick up tasks they have capacity for and create code branches for those tasks
- The branch created is pushed to GitHub
- A pull request with a branch reference to the Jira ticket is created
- Automated tests are run on the pull request
- Other developers review the code created in the pull request
- The branch is merged into the main branch
- The main branch is deployed to a staging environment
- On a schedule the code is deployed to a sandbox environment
