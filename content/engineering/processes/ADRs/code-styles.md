---
title: "Code Styles"
date: 2021-09-01T17:05:10+02:00
draft: false
description: "This is an ADR for our finding regarding Code Styles"
weight: 1
---

## Status

- proposed

## Context

- We need a structed set of rules to define how we go about code styling/formating

## Decision

- Using Sonar Cloud in our CI & Local Linting process to enforce code styles in the HandHeld Codebase
- Using ReSharper/Rider for local linting and formating

## Consequences

- Formatting and linting will be enforced in the CI process using Sonar linting for detecting coding issues in real-time and get clear guidance on how to fix them.
- Code will be more readable and structured.
- will require extra effort to ensure proper linting and code styling is enforced.
