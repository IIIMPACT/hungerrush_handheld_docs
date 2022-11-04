---
title: "Recommendations"
date: 2022-09-29T12:22:51+02:00
draft: false
description: "Coding practices and recommendations"
weight: 8
---

## Working with Time

- Always use and store date-time as **UTC time**
- **Use unix timestamps** as they are the lowest common denominator, easy to generate, easy to validate, are UTC by default, the smallest data over the wire and in storage
- **Store or retrieve user timezone/locale date independently**, when required for user locale based operations on the server (ie: timed notifications)
- Always store as **locale rather than offset**, as offsets can be inconsistent due to day light saving etc.
- [unixtimestamp.com](https://www.unixtimestamp.com/)

## Use BEM

We try to use BEM (Block Element Modifier) for everything we can, not just class names, but test IDs as well. Here is a good introduction: [BEM 101](https://css-tricks.com/bem-101/).

## DRY (Don't Repeat Yourself)

As far as possible and within reason we strive to fulfil the [DRY principle](https://www.plutora.com/blog/understanding-the-dry-dont-repeat-yourself-principle). This means that we try to avoid repeating code, and instead try to reuse code as much as possible. This is not only good for the codebase, but also for the developers, as it reduces the amount of code that needs to be maintained and understood. It also reduces the amount of code that needs to be tested.
