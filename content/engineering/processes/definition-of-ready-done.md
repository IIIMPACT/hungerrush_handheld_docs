---
title: "Definition of Ready/Done"
date: 2021-08-31T18:11:15+02:00
draft: false
description: "Definition of Ready and Done for each stage in the workflow"
weight: 2
---

At each stage of a task or story's progression we have a set of criteria that must be met before the task or story can be moved to the next stage. This is known as the Definition of Ready (DoR) and Definition of Done (DoD).

#### [Miro Board design reference](https://miro.com/app/board/o9J_lQZaYIk=/)

## Selected for development (DoR)

- We have designs
- We have assets
- Are there integration points available
- Do we have API keys
- Do we have API documentation
- Are the requirements clear
- Do we have Acceptance Criteria

## Development (DoD)

- PR is open and well detailed
- It satisfies all the Acceptance Criteria (AC)
- It passes all the checks (tests, coverage, linting, etc.)
- It has > 70% coverage
- Documentation is up-to-date
- Ticket updated with review and QA testing instructions

## Code review (DoD)

- Reviewer has pulled and read through the changes
- Reviewer has executed the changes locally
- At least 2 people (project team dependent) has reviewed and approved the PR

## Releasing (DoD)

- Changes are available in staging/production and accessible by the QA team

## Validating (DoD)

- Changes have been checked against AC
- Changes have been checked against design
- Changes have been checked and evidenced in appropriate environment(s)
