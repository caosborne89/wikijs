<!-- TITLE: Raquels Test Page -->
<!-- SUBTITLE: A quick summary of Raquels Test Page -->

# Project Document/Readme Template:
Let's standardize the type of information we provide in our project documentation. This is a suggested template for a readme based upon our best practice suggestions and this example: https://github.com/jehna/readme-best-practices combined with real examples sourced from our Redmine Wiki's and readme files.

## Project Summary

Describe why the project was started, what it does, what tools/languages are used to build it, generally who is the owner/interested party or department.

>Example:
>
>The Library Tools Tab (LTT) is a web application that integrates with D2L to
make it easier for instructors and librarians to share library resources with
students.  It consists of two main parts: a front-end application written in
Backbone and a back-end application written in Symfony using the Doctrine ORM.
{.is-info}

## Enviroments

> Note: This information probably shouldn't be in any public facing readme's.
{.is-warning}

List the enviroments with URLS, describe their intended use.

>Example:
>
{.is-info}

## Requirements
Describe relevant requirements for OS, PHP, if we use composer, node, etc.

>Example:
>
{.is-info}

## Repository
Maybe not list the specific location since this will be linked to the remine project, but we can put the repo names and descriptions if there are multiple repos needed for a project, or if we are holding onto something old for some reason. For example UA Press we can specify that `uapress-3` is the production repo, for LTT we can describe that LTT2 is using `ltt_git`, and LTT1 is still using the `subversion` repo despite them being tangled together in both repos.


## Getting started / how to develop locally
How to build locally if there are any specifics to the project (such as using env or needing to dump the database off the server).

>Example:
>
{.is-info}

## Deployment Workflow
Describe how to work on and deploy. Git flow? Intentional non-git flow? Deployment scripts? Additional quirks? How to verify deployment was successful? Who to notify before deploying? Which enviroments we should deploy to?

>Example:
>
{.is-info}

## Documentation
If this is in the readme, describe where to find the rest of the documentation if there is any.

## License
Standard readme license info.