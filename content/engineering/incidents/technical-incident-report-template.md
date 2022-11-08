---
title: "Technical Incident Report Template"
date: 2022-09-29T12:31:51+02:00
draft: false
description: "Incident report template"
weight: 20
---

# IIIMPACT Technical Incident Report

**Account**: The name of the client account affected  
**Severity**: A value of p0,p1,p2,p3 depending on the severity of the incident  
**Reported At**: An ISO 8601 sortable format, eg: 2021-07-12T10:00:32 SAST  
**Resolved At**: An ISO 8601 sortable format, eg: 2021-07-12T10:00:32 SAST  
**Reported By**: The name of the individual who reported the incident  
**Triaging Engineers**: The name of the engineers who handled the incident

## Summary

A high level summary of the incident. This should include brief information describing when it happened, a high level overview of the impact such as the number of requests or users affected. It may also briefly describe the root cause.

## Timeline

A precise timeline of events starting with the conditions which led to the incident occurring and the relevant steps taken during the incident up to resolution.

## Impact

The impact of the incident. This may be the number of users affected, the cost of an outage, or a timeline, the number of requests, etc. This may include log correlation information.

## Root Cause

The initial condition or error which resulted in the incident, described in as much detail as possible.

## Resolution and Recovery

The time of and steps taken to resolve the incident, or recover from the outage. This should also include actions taken which did not resolve the incident successfully.

## Corrective and Preventative Measures

This section describes what measures should be taken to avoid the recurrence of a similar incident. These take the form of recommendations and may be considered follow-up work.
