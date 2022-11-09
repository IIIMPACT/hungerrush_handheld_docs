---
title: "Pre-Git Commit linting"
date: 2022-11-08T20:19:49+01:00
draft: false
weight: 4
description: General info about setting up the linting tool
---

## Introduction
This setup uses husky and lint-staged to clean C# and XML-based codes.

## Setup for new members
1. navigate to root directory where we have the .SLN file and .git folder

2. run **npm install**


## Fresh setup

### Pre-requisites
- **1. Install node on your computer** ->, and make sure it’s available in your terminal by running node -v

- **2. Install dotnet cli** -> and make sure it’s available by running dotnet -v

- **3. Then, install dotnet format** -> : dotnet tool install -g dotnet-format which helps format C# code in dotnet projects


### Procedure

The steps below work for projects where the solution (.SLN) file is in the same directory as the hidden .git folder. You will have to make some changes to make it work for other folder structure

1. You need to add a package.json file in the root folder of your repository, which you can do using by opening the repository in the command linenpm init --yes. This allows you to run npm commands

2. Add a .editorconfig file in your root folder and add put in the code from here and save it. This file performs a lot of functions and for us it contains all the formatting rules you want to enforce.

3. We’ll install Husky to our project which does the magic here, using npx husky-init && npm install. You’ll notice several temp files getting installed, but it will also add items to your package.json file and a new file .husky/pre-commit which is a “pre-commit hook” that gets called when you try to commit something (either by tapping a button in a Git client or through the terminal). If the command isn’t successful, it will stop a commit and show an error

4. Then installlint-staged using this within the project directory npm install lint-staged --save-dev

5. Inside your .husky/pre-commit, replace npm test with npx lint-staged --relative so that relative file paths will be used

6. Then add this to your package.json file (I place mine below scripts): “lint-staged”: {“*.cs”: “dotnet format --include”}. This command is invoked by lint-staged against all files with a .cssuffix in your commit, and this is what the changes will look like in the commit


### How to test
1. To test this in action, you can try to add an incorrect extra line break and commit the file and you should see the entire file get auto-corrected inside the commit.

2. After your code commit is pushed and your co-workers pull the latest changes, they just need to run an npm install in the root directory and the pre-commit magic should work on their computer as well at the time of any commit.