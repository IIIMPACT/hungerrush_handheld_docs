---
title: "Hungerrush"
date: 2022-06-08T15:56:18+01:00
draft: false
---

This document describes terms used internally at HungerRush which do not necessarily match terminology that we use. This
is because we have tried to use language which makes sense in the context of each domain, or matches industry standard
language.

## Site

The term "Site" refers to a single restaurant chain managed by a [Customer]({{< ref "domain/identity#customer" >}}). As
a [Customer]({{< ref "domain/identity#customer" >}}), I can manage multiple restaurant chains under a single account.

A site is analogous to a merchant.

## Rooftop

A rooftop is a single restaurant location, and is a unit of billing within the HungerRush systems.

A rooftop is analogous to a store.

## Order

The term "Order" refers to a customer's order for hardware, such as a kiosk or point-of-sale device.
