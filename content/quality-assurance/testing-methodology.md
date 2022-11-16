+++
date = 2022-10-11T23:00:00Z
description = "A mixture of automation and manual testing will be conducted ensuring products conform to design requirements and behave as expected."
title = "Testing Methodology"
weight = 2

+++

### **TESTING METHODOLOGY**

---

A mixture of automation and manual testing will be conducted ensuring products conform to business requirements, designs and behave as expected.

**Unit Testing**

> We are using NUnit for Unit Testing.

- First level of testing to be scripted and conducted by developers
- Ensure individual units of code work as intended / designed at code level

**Integration Testing**

- Ensure individual components work as intended
- Framed by user scenario stories
- Automated tests by developers / manually tested by QA

**End-to-End Testing**

> We are using NJUnit for Unit Testing.

- Ensure whole segments of an application behave as expected together
- Framed by user scenario stories
- Last phase of [functional testing](https://www.guru99.com/functional-testing.html "functional testing") including [exploratory testing](https://www.guru99.com/exploratory-testing.html "exploratory testing")
- Ensure the product adheres to original business criteria and end user’s needs
- Automated tests by developers / manually tested by QA

**Regression Testing**

- Run at timed intervals with varying combinations of P0, P1, P2 and P3 test cases
- Ensure no defects are added back into the development cycle
- Manually tested by QA
