---
title: "Technical Incidents"
date: 2022-09-29T12:30:51+02:00
draft: false
description: "Technical Incident reporting"
weight: 10
---

# Technical Incidents

## Priority Codes

These are largely defined from [this resource](https://piousbox.com/2019/06/definition-of-priority-codes-p0-p1-p2-p3-p4-in-technical-development/),
but adapted for our use-case:

- P0: The product is unavailable or there is a breach of confidential information; the task has the highest priority
- P1: A task blocking other stakeholders or customers
- P2: A task affects customers, but there is a non-technical workaround
- P3: A task that does not affect customers

Note: incidents can be upgraded or downgraded as more information becomes available. When downgrading an incident,
re-confirm priority of the task with your product owner.

## Guidelines

Generally, the tech team and product owners raise incidents upon discovery. For P1 and lower priority, the Product Owner
still sets priority for the team. Incident priority can be raised or lowered as more information is gathered.

In the case of P0 incidents, a Technical Incident Report needs to be written to document what happened. Use the
[template](./technical-incident-report-template.md) to document P0 incidents. This is used to increase transparency
with the client, for analysis later with the rest of the tech team. It also serves to document system and data changes
later on when debugging problems which may stem from the incident, or the changes implemented to resolve it.

**N.B.** Incidents are _not_ to be used to circumvent priority rules for the team.
