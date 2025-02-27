---
title: How to run a GitHub Actions Job in a Container from Artifactory
description: A GitHub Actions workflow that runs a job in a Docker container from Artifactory.
slug: actions-container-artifactory
date: 2025-02-26 00:00:00+0000
image: 
categories:
    - CI/CD
tags:
    - DevOps
    - Ci/CD
    - GitHub Actions
    - Docker
weight: 1 # You can add weight to some posts to override the default sorting (date descending)
---

## Intro

In a GitHub Actions workflow, you can define a Docker image to run a job on.
The GitHub documentation on this has an example for an image from the ghcr.io
registry, but this article provides an example of specifying an image from
Artifactory.
