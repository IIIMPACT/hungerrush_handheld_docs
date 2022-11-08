---
title: "Naming Convention Guidelines"
date: 2021-08-31T18:11:15+02:00
draft: false
description: "A guideline to naming conventions, including file names, variables, functions, classes, and more"
weight: 1
---

# Naming Guidelines

### Avoid Noise Words

Noise words are the words that do not offer any additional information about the variable. They are redundant and should be removed.

Some popular noise words are:

- The (prefix)
- Info
- Data
- Variable
- Object
- Manager

  If your class is named UserInfo, you can just remove the Info and make it User. Using BookData instead of Book as class name is just a no-brainer, as a class stores Data anyways.

---

### Use Pronounceable Names

If you can't pronounce a name, you can't discuss it without sounding silly.

#### Bad:

const yyyymmdstr = moment().format("YYYY/MM/DD");

#### Good:

const currentDate = moment().format("YYYY/MM/DD");

---

### Use Searchable Names

Avoid using magic numbers in your code. Opt for searchable, named constants. Do not use single-letter names for constants since they can appear in many places and therefore are not easily searchable.

#### Bad:

if (student.classes.length < 7) {
// Do something
}

#### Good:

if (student.classes.length < MAX_CLASSES_PER_STUDENT) {
// Do something
}

---

## File Names

File names should be named in PascalCase and should be named after the class they contain. If a file contains multiple classes, the file name should be named after the main class in the file.

## Class Names

Class names should be named in PascalCase.

## Method Names

Method names should be named in PascalCase.

## Variable Names

Variable names should be named in camelCase.

## Constants

Constants should be named in UPPER_SNAKE_CASE.

## Enumerations

Enumerations should be named in PascalCase.

## Enumerations Members

Enumeration members should be named in PascalCase.

## Interface Names

Interface names should be named in PascalCase.
and be Prefixed with the letter I.

## Property Names

Property names should be named in PascalCase.

## Event Names

Event names should be named in PascalCase.

## Namespace Names

Namespace names should be named in PascalCase.

## Struct Names

Struct names should be named in PascalCase.

## Delegate Names

Delegate names should be named in PascalCase.

## Type Parameter Names

Type parameter names should be named in PascalCase.
