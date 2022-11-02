---
title: "CI CD Process"
date: 2022-06-08T16:05:49+01:00
draft: false
weight: 1
description: CI CD Process
---

## Continuous Integration & Continuous Delivery

Continuous Integration and automated testing is done through a combination of writing unit tests for the development language used for the project and [Azure Devops](https://dev.azure.com/).

- Azure workflow steps are created on Azure Devops and the yaml config file is maintained on there
- Developers write unit tests
- Code changes are committed to GitHub 
- Developers create a pull request on GitHub
- Azure pipelines are triggered for changes on the development branch
- If any tests fail the code should not be merged into another branch
- The apk that is build and signed on the container on Azure Devops is distributed to the app center
