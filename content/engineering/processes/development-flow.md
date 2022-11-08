---
title: "Development Processes"
date: 2021-08-31T18:10:57+02:00
draft: false
description: "Development processes and coding standards"
weight: 1
---

## Git

- We follow a gitflow like strategy. All changes are made in branches based off of `master`
- Branches are merged into `master` via PR
- Frontend applications are deployed to individual sandbox environments for each pull request.
- Frontend applications are automatically deployed to staging when merging to `main`
- Backend applications are deployed to a dedicated staging environment when being merged to `master`
- Backend applications are deployed to production when invoking the `release` workflow
- We use _strict_ [semantic versioning](https://semver.org/) on _all_ packages. Please learn this and implement it
  strictly
- Below version `1.0.0`, the API is considered unstable

## Commit Messages

- Use the imperative, present tense: "change" not "changed" nor "changes"
- No capitals and no fullstops (.) at the end
- When a PR is ready for merge we trigger a squash and merge which will squash all your commits into one, when doing that follow the pattern of `type/scope/ticket-number: description (#PR-number)`. i.e. `style/onboarding/PROJECT-123: change button color to red (#321)`.

## Pull Requests

- PR title must follow the pattern of `type/scope/ticket-number: description`. i.e. `style/onboarding/PROJECT-123: change button color to red`.
- Include all relevant labels on the PR (e.g. `bug`, `enhancement`, `feature`, `documentation`, `test`, `release` etc.)
- Use the available pull-request templates that are set in the repository
- Codeowners automatically request reviewers, so don't worry about manually assigning reviewers unless you need someone specific
- Use the following branch-naming format `type/ticket-number/description`, eg. `fix/PROJECT-124/broken-button` (full ticket number is required in branch name to maintain Jira integration), where types are as follows:
  - **feat**: A new feature
  - **fix**: A bug fix
  - **refactor**: A code change that neither fixes a bug nor adds a feature
  - **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
  - **test**: Adding missing tests or correcting existing tests
- When relevant, add screenshots/recordings to the pull-request
- You are responsible for getting your code into production, ask for review and follow through
- PRs require _at least_ 2 reviews, with at least 1 of them being a _senior engineer_
- Test your code in production, don't fire and forget
- When reviewing, do so thoroughly and actually test the changes
- PR feedback is criticizing the code, not the author. Don't take feedback personally, and don't hold back. Just be
  polite
- Keep PR size down. The scope should be to change one thing, we are targeting a 4 hour dev cycle, with as little code change as possible
- When merging PRs, the commits are squashed and the branches are deleted automatically
- We use [the angular standard](https://gist.github.com/brianclements/841ea7bffdb01346392c) for our defined types

## Deployment Guide

- Sandbox, staging and production branches are _always_ deployed using CI
- We use github actions as the preferred build and deployment mechanism
