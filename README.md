# HW.js

> A free and open source library for homework (HW).

This README is for developers who want to contribute to HW.js.
Additional documentation can be found at [the HW homepage](https://www.youtube.com/watch?v=o-YBDTqX_ZU).
Working examples can be found in [the developer docs](https://www.youtube.com/watch?v=o-YBDTqX_ZU).

**Table of Contents**

- [Codebase](#Codebase)
- [Install](#Install)
  - [Development env](#Development env)
  - [Project](#Project)
- [Run](#Run)
- [The development process](#The development process)
  - [Naming rules](#Naming rules)
  - [PR review](#PR review)
- [Deployment](#Deployment)

<a name="Usage"></a>

## Codebase

A Node.js project with Jest integration consists of a well-structured codebase organized according to Node.js development principles. It includes essential components, modules, and tests to ensure the functionality of the application. Jest tests verify the correctness of the code, while Jest configuration and npm scripts streamline testing and build processes.

## Install

### Development env (Optional)

The basis of this project is [Node js](https://nodejs.org/en), to install it, we recommend using the [Node Version Manager](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating)

To work more effectively with the team and git, you can use aliases accepted in the team. To do this, copy them from the `config/config.example` to your local config

```
list of accepted aliases
    co = checkout
    ci = commit
    st = status
    br = branch
    history = log --graph
```

### Project

The project uses npm for package management. To install the modules, use the command

```
npm install
```

## Run

To start the project, use the following command

```
 npm run start
```

## The development process

The team has strict naming and review rules. Make sure that you follow all the points set out below before creating a PR

### Naming rules

The current branches for features, improvements and bugs are named according to the following pattern

```
brunch_type/ticket_code-ticket_name
```

Couple of examples

```
feat/HW-1238-Emails_templates_for_subdomains
fix/HW-1334-500_error_after_login_with_user_who_has_Partner_role
chore/HW-1121-nuxt-upgrade
```

For release, we use 

```
release/33.3
```

Your pr title/commit must follow the https://www.conventionalcommits.org/en/v1.0.0/

### PR review
> Please read https://medium.com/@mrjoelkemp/giving-better-code-reviews-16109e0fdd36#.xa8lc4i23 to understand how a PR review should be conducted. 

We take PR review seriously. Be rational and strict in your review, make sure you understand exactly what the submitter's intent is.


To submit a ticket for review, you must complete a few simple steps

- Create a PR in accordance with all the rules
- Delete all WIP labels, if any have been set
- Get a green check from [Mr.Jenkins](https://www.youtube.com/watch?v=o-YBDTqX_ZU)

To merge your pr you must get **at least 2** approvals from the core development team
All branches are merged to the main only via GitHub UI with using squash (except for release branches)

## Deployment

> Instructions for the deployment:

1. Create release branch 
2. Set the tag
3. Collect the release notes
4. Open PR in the main, add release notes to the description
5. Get **at least 2** approvals from the core development team
6. Run [PROD-deploy job](https://www.youtube.com/watch?v=o-YBDTqX_ZU) for release brunch without additional parameters
7. Wait for the job to finish and check that everything is ok
8. Publish release notes
9. Merge release brunch to main **(do not use squash for it!!!)**