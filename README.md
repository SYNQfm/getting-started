Welcome to Vardoge's R&D team's getting started guide. This document describes our development philosophy and outlines things we care about as a team.

## Our Mission

`To deliver business value quickly and iteratively`

## Doing it right with Core Behaviors

If you are on the Vardoge Engineering team you already exhibit some (or all) of these behaviors, but if you don't exhibit all, don't worry. We understand some of these behaviors rely on a bridge of trust, and we're happy to build that with you.

- **Psychological Safety** - It starts here; without Psychological Safety we cannot Communicate and we cannot Care. These are some examples of creating a psychologically safe team, everyone must be responsible and exhibit these behaviors at Vardoge. Some examples:
  - Encourage team mate participation.
  - Engage and investigate all ideas equally.
  - Define problems collectively as a group.
  - Make sure everyone has a chance to participate.
  - No blame, succeed or fail together mentality.
  - Willingness to try without fear.
  - For more details and examples read [here](https://en.wikipedia.org/wiki/Psychological_safety)

* **Communication** - Communication can take many forms, but it is important that we are always communicating at Vardoge. Without communication, none of this is possible. The only clause here is that we don't want to be jerks; if you are feeling upset please take time to construct your narrative before sharing it (see psychological safety). Some examples:

  - Creating PRs.
  - Writing documentation.
  - Communicating in person or online.
  - Giving and receiving feedback constructively and in real time

* **Care about...** - If you don't care about Vardoge, about your craft, about engineering, or about your coworkers, working here will be tough. You don't have to care about everything, but caring about something is important. Without caring you wouldn't be motivated to do the work that's required of you here. Some examples:
  - Care about Vardoge.
  - Care about your coworkers and their success.
  - Care about standards or quality.
  - Care about the craftsmanship of your work.
  - Care about learning and growing your skills.

If you retain anything from this article, it is the 3 core behaviors from above. We live by this, we hire by this, we fire by this.

## How and why we do it

Here are things we specifically do to help achieve our mission

[**Code**](code.md)

| What                  | Reasoning                                                                                           | Tooling             |
| :-------------------- | --------------------------------------------------------------------------------------------------- | ------------------- |
| (Near) Atomic Changes | Pushing smaller changes allows us to deliver incremental value; also reduces chance of breakage     | GitHub              |
| High code coverage    | CI is useless without good quality coverage, and we can't ship to production confidently without it | CircleCI, Coveralls |
| Refactor constantly   | Code debt slows us down and counters our fast PR turnaround                                         | GitHub              |

[**Docs**](docs.md)

| What                    | Reasoning                                                                                                                                   | Tooling         |
| :---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------- |
| Branches and PRs        | introduce small changes safely, ensure the code fits our philosophy, knowledge sharing                                                      | GitHub, Slack   |
| Effective documentation | moving quickly means we work on a lot of different things, coming back to it later or having another teammate look at it, they need to know | GitHub Markdown |
| Aligned Development     | Make sure what we're working on brings business value                                                                                       | Trello, GitHub  |

[**DevOps**](devops.md)

| What                        | Reasoning                                                                                 | Tooling                              |
| :-------------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------ |
| Tight CI/CD                 | The way we can ship the code quickly and confidently                                      | GitHub, CircleCI, Heroku, AWS Lambda |
| Automated System/UI Testing | Once code is in production, is it really working?                                         | CircleCI                             |
| DevOps Culture              | Everyone should know how stuff runs and keep an eye that services are working as expected | Slack                                |

## Technology Overview

[System Diagram](https://trello.com/c/oUDoJ2HJ/824-system-diagram)

**Core Services**

| Name                                         | Build | Code Coverage | Description             | Maintainer(s) |
| :------------------------------------------- | ----- | ------------- | ----------------------- | ------------- |
| [Dorado](https://github.com/SYNQfm/dorado)   |       |               | ReactJS based Dashboard | Fiona         |
| [Polaris](https://github.com/SYNQfm/polaris) |       |               | API Core                | Chris         |

**Processing Services**

| Name                                           | Build                                                                                                                                                               | Code Coverage                                                                                                                           | Description                | Maintainer(s) |
| :--------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | -------------------------- | ------------- |
| [Eros](https://github.com/SYNQfm/eros)         | [![CircleCI](https://circleci.com/gh/SYNQfm/eros.svg?style=svg&circle-token=002438cd9550fee6c741a4f53f1280200d1ed94a)](https://circleci.com/gh/SYNQfm/eros)         | [![Coverage Status](https://coveralls.io/repos/github/SYNQfm/eros/badge.svg?t=K1g7tv)](https://coveralls.io/github/SYNQfm/eros)         | Email Service              | Jessica       |
| [Pegasus](https://github.com/SYNQfm/pegasus)   |                                                                                                                                                                     |                                                                                                                                         | PDF Generator              | Fiona         |
| [Scorpius](https://github.com/SYNQfm/scorpius) |                                                                                                                                                                     |                                                                                                                                         | Indexed Search             | Michael       |
| [Ursa](https://github.com/SYNQfm/ursa)         | [![CircleCI](https://circleci.com/gh/SYNQfm/ursa.svg?style=svg&circle-token=c672476c3bea9cedfaeb8044370a266945e919c1)](https://circleci.com/gh/SYNQfm/ursa)         | [![Coverage Status](https://coveralls.io/repos/github/SYNQfm/ursa/badge.svg?t=OFF6wU)](https://coveralls.io/github/SYNQfm/ursa)         | S3 Upload Signer           | Jessica       |
| [Virgo](https://github.com/SYNQfm/virgo)       |                                                                                                                                                                     |                                                                                                                                         | Autodesk forge Integration | Fiona         |
| [Wormhole](https://github.com/SYNQfm/wormhole) | [![CircleCI](https://circleci.com/gh/SYNQfm/wormhole.svg?style=svg&circle-token=124f1778702b1e7559513e1bd9773134a749fb32)](https://circleci.com/gh/SYNQfm/wormhole) | [![Coverage Status](https://coveralls.io/repos/github/SYNQfm/wormhole/badge.svg?t=QdyNIi)](https://coveralls.io/github/SYNQfm/wormhole) | Programmable webhooks      | Jessica       |

**Other Services**

| Name                                     | Build | Code Coverage | Description    | Maintainer(s) |
| :--------------------------------------- | ----- | ------------- | -------------- | ------------- |
| [Indus](https://github.com/SYNQfm/indus) | N/A   | N/A           | Infrastructure | Jahm          |
