---
title: "CI CD Process"
date: 2022-06-08T16:05:49+01:00
draft: false
weight: 1
description: Setup guides for the POS device
---

## Continuous Integration & Continuous Delivery

Continuous Integration and automated testing is done through a combination of writing unit tests, code style analysis & ui tests for the development language used for the project and [Azure Devops](https://dev.azure.com/).

- Azure workflow steps are created on Azure Devops and the yaml config file is maintained on there
- Developers write unit tests
- Code changes are committed to GitHub 
- Developers create a pull request on GitHub
- The following Azure pipelines are triggered for changes on the development branch
  - **Code Style** which runs a Sonar linting code analysis (required workflow)
    - the Sonar linting account to view the linting reports for this project can be accessed using the **iciuser@devrevention.onmicrosoft.com** azure account credentials can be acquired through the designated team LastPass account
  - **Unit Test, Build APK & Distribution** (required workflow)
  - **UI test** (required workflow)
- If any tests fail the code should not be merged into another branch
- The apk that is build and signed on the container on Azure Devops is distributed to the app center
