# Purpose

If you have to create a jira tickets for your commits, you can use this tool
to automate the process

Just replace `git commit` with `git jira`

# Installation

Copy git-jira into your `$PATH`.

Install `jq` (`apt-get install jq`)

# How it works

It will take the brief description of your git commit message as ticket
title and will put the body of the git commit message into the description.

The commit message you specify will get put in front of your git commit message.

For example: `git jira -m "Bar"` will create a ticket in the project `FOO` (see
configuration) and will put the newly created ticket key (e.g. `FOO-123`) in front
of the commit message: `FOO-123: Bar` - without specifying the body the
description in the newly created ticket will stay empty.

# Setup

Make sure to configure your jira related data before.

## set the jira project name

```sh
git config jira.project <project>
```

## set the jira base url

```sh
git config jira.url https://jira
```

## set the jira login data

```sh
git config jira.password <pwd>
git config jira.username <user>
```
