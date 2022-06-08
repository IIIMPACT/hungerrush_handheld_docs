---
title: "Payments"
date: 2022-06-08T14:34:06+01:00
draft: false
weight: 1
---
Payments refers to a secondary bounded context involving payment mechanisms. Currently, these are common to both
[customers]({{< ref "domain/identity#customer" >}}) and [consumers]({{< ref "domain/identity#consumer" >}}). This will
likely be refined when this work is planned out further.

## Docket

The term "Docket" refers to all information relating to an [open table]({{< ref "#open-table" >}}) or a
[consumer]({{< ref "domain/identity#consumer" >}}) order, that is relevant to the consumer themselves. A docket does not
include information that is only relevant to the kitchen,


A docket typically includes information such as:

1. Date and Time
2. Waiter
3. Meals ordered
4. Total value
5. Gratuity
6. etc

## Check

The term "Check" is an informal reference to the [docket]({{< ref "#docket" >}}). This is typically used by
[consumers]({{< ref "domain/identity#consumer" >}}) when asking for the bill.

E.g. "Check, please"

## Coupon

The term "Coupon" refers to a meal item that can be credited against a meal order.

## Voucher

The term "Voucher" refers to a dollar amount that can be credited against a meal order.

## Revenue Centre

The term "Revenue Centre" refers to an arbitrary section of the restaurant which is able to generate revenue. These are
typically comprised of 

A revenue centre is often described as a restaurant within a restaurant, generating its own revenue.

An example of a restaurant with multiple revenue centres would be a hotel restaurant where the seated floor space is
considered one revenue centre, and the room service is considered a separate revenue centre.

## Order

The term "Order" refers to an order for food, by a consumer.

## Point of Sale

The term "Point of Sale" refers to the system which is responsible for [Docket]({{< ref "#docket" >}}) lifecycle
events, payments, reports and auditing functionality.

## Open Table

The term "Open Table" can have different meanings depending on the context:

In terms of 
, "Open Table" refers to a table that is cleared and
available for new [consumers]({{< ref "domain/identity#consumer" >}}).

When referring to an "Open Table" within the context of a [POS]({{< ref "domain/payments#point-of-sale" >}}), the term
refers to the sit-down restaurant model in which the [docket]({{< ref "domain/payments#docket" >}}) is opened and
remains in flight until payment is received. In this case, the docket is closed when the consumers have paid, typically
after finishing their meal.

## Payment Instrument

The term "Payment Instrument" refers to a consumer owned device which can be used to make payments, for example; a
credit card, an Apple Pay account, etc.