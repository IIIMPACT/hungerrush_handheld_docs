+++
date = 2022-10-11T23:00:00Z
description = "Defect handling process"
title = "Defect handling"
weight = 5

+++
### DEFECT HANDLING

***

When an issue is observed the QA team should:

* Make sure the issue is reproducible
* Get another team member to verify
* Raise necessary bug ticket and share with the team

**Bug prioritisation** should follow the below rating system, which takes into account how severely the bug impacts the system and how urgently it should be fixed / eradicated from the site. If necessary QA should consult a developer or PO to make sure the correct priority is given.

**Blocker** _(P0)_ / Highest

* Release can’t go out
* Affects business revenue
* Users or testers cannot proceed
* Same day fix or within 24HRS

**Critical** _(P1)_ / High

* Release can go out
* Affects major functionality / data
* Users or testers have a workaround
* Resolved as soon as possible

**Minor** _(P2)_ / Medium

* Release can go out
* Does not affect major functionality / data
* System still useable
* Resolved during usual course of activities (even next sprint)

**Improvement** _(P3)_ / Low

* Does not affect functionality / data
* More cosmetic or UI driven
* Resolved after critical defects or not at all