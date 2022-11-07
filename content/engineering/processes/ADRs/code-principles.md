---
title: "Code Patterns"
date: 2021-09-01T17:05:10+02:00
draft: false
description: "This is an ADR for our finding regarding Code Patterns"
weight: 2
---

## Status

- (proposed)

## Context

- We need a structured set of rules to define how we go about code patterns, such as how we handle exceptions, logging, etc.
- We need to define a set of patterns that we can use to ensure consistency across the codebase

## Decision

- Using MVVM as our base pattern for all UI code
- Using SOLID/DRY/KISS/YAGANI Design Principles as our base patterns

## Consequences

- Code will be more readable and structured.
- Code will take longer to write as a result.
