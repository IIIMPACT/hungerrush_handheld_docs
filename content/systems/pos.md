---
title: "POS Setup"
date: 2022-06-08T16:05:49+01:00
draft: false
weight: 1
description: Setup guides for the POS device
---

## HARDWARE

### Prerequisites

- Make sure you have the right `POS` device.
  - [Hera51](https://www.mplustech.com/en/product-634853/Hera51.html)
- If POS device isn't available, an Android phone is fine for testing.


#### Operating System

Ensure the device runs Android Nougat (version 7.1.0 or higher)


---

# Platform Repositories

## Hungerrush-handheld-order-and-pay

This represents the POS app. We’ve followed a an MMVM approach in the implementation of this app.

#### Setup

```shell
git clone git@github.com:IIIMPACT/hungerrush-handheld-order-and-pay.git
```



---

## Documentation

#### Setup

- The documentation is built using `GitHub pages`, `Hugo` and the `Hugo-Learn template`.
  - [GitHub pages](https://www.youtube.com/watch?v=QyFcl_Fba-k)
  - [Hugo](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
  - [Learn theme](https://learn.netlify.app/en/basics/installation/)

```shell
git clone git@github.com:IIIMPACT/hungerrush-docs.git
```

#### Running

```shell
# run hugo locally
hugo server
```

```shell
# url, port
http://localhost:1313/
```