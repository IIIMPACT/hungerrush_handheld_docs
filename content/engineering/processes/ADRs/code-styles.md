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

- Using Sonar Cube in our CI process to enforce code styles in the HandHeld Codebase
- Using ReSharper/Rider for local linting and fomating

## Consequences

- Formatting and linting will be enforced in the CI process
- Code will be more readable and structured.
- will require extra effort to ensure proper linting and code styling is enforced.
