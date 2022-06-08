+++
title = "Language Reference"
date = 2022-06-08T15:52:11+01:00
weight = 2
chapter = true
pre = "<b>2. </b>"
+++

### Language Reference

# Industry

This document describes language used in industry which is not currently modelled in our systems, but is useful to 
understand for communicating with stakeholders in a precise language.

## Ticket

A ticket is derived from a [docket]({{< ref "domain/payments#docket" >}}) and includes instructions for the kitchen to 
fulfill the order. These typically include the time the order was placed, what has been ordered, which waiter is serving
the table, and which table the ticket is for.

## Prep Instruction

The term "Prep Instruction" refers to modifications or personal preferences relating to meals on a
[ticket]({{< ref "#ticket" >}}). This is related to a [Docket]({{< ref "domain/payments#docket" >}}).

Examples:
1. Meat temperature
2. Timing for starters vs mains
3. Removal or addition of ingredients
4. Packaging instructions
5. etc

## Floor Space

The term "Floor Space" refers to the division of seating areas within a restaurant. Floor spaces contain tables with
individual table-numbers. These typically represent [Revenue Centres]({{< ref "domain/payments#revenue-centre" >}}).

## Kitchen Display Systems (KDS)

The term "Kitchen Display System" (KDS) refers to a display within the kitchen of restaurants which displays
[ticket]({{< ref "#ticket" >}}) information, 
[prep instructions]({{< ref "#prep-instruction" >}}), priority and age.

## Food Menu

The term "Food Menu" refers to the listing of food available at a restaurant.

A food menu is an aggregation of categories (E.g. Starters, Deserts), which are themselves an aggregation of food items.
Each food item will have an associated price, availability and may include possible modifiers.

{{< mermaid >}}
classDiagram
class FoodMenu
class FoodCategory
class FoodItem
class FoodItemModification

FoodMenu "1" o-- "*" FoodCategory
FoodCategory "1" o-- "*" FoodItem
FoodItem "1" o-- "*" FoodItemModification
{{< /mermaid >}}

## Digital Food Menu

The term "Digital Food Menu" refers to a digital version of the traditional printed
[food menu]({{< ref "#food-menu" >}}) available at restaurants with the ability to customise their meals and place
orders for in-store payment.

## Digital Menu Boards

The term "Digital Menu Boards" refers to physical displays used to show [food menus]({{< ref "#food-menu" >}})
and promotions within restaurants.

 ## Kiosk

The term "Kiosk" refers to a device (typically touch-screen) with which 
[consumers]({{< ref "domain/identity#consumer" >}}) can physically interact, and place meal orders.