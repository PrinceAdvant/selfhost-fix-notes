# Git sources for deploys: deploy keys, apps and tokens compared

A deploy server needs to read your repository. There are three common ways to grant that.

## Deploy keys

An SSH key added to a single repository, read-only by default. Simple and tightly scoped. The downside is one key per repository, which gets tedious across many services.

## Git provider apps

A GitHub or GitLab app installed on selected repositories issues short-lived tokens. Best for many repositories and for receiving push webhooks.

## Personal access tokens

Quick to set up, but tied to a person. When that person leaves, deploys break. Avoid for production.

## What I use

Apps for organizations, deploy keys for one-off repositories, never personal tokens on shared servers.

The Peon docs on [connecting Git sources](https://peon.sh/docs/git-sources) show how each option is configured. [Peon](https://peon.sh/) is an open-source self-hosted PaaS.
