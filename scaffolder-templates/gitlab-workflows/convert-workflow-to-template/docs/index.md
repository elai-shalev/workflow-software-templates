---
id: convert-workflow-to-template-gitlab
title: Convert serverless workflow to a template
description: Create a software template out of an existing serverless workflow.
---

# Creating a Software Template for Running a Serverless Workflow

## Overview

This template allows the user to generate a software template from a serverless workflow deployed for the Orchestrator.
The artifacts will be pushed to GitLab.

## Prerequisites

- An OCP/k8s cluster and an RHDH instance. 
- A GitLab account
- An account on Quay.io 

## Steps

To run the template, the user will need to provide the ID of a serverless workflow and GitLab repository for storing the generated output (the software template).

### Page 1: Workflow Identifier To Generate The Template For


On this page the user will provide input for the following parameters:

- Workflow ID: A unique ID for the serverless workflow in SonataFlow. The allowed pattern for the string will be enforced. 

### Page 2: Repository Location
On this page the user will provide input for the following parameters:

- Host: gitlab.com
- Owner: the organization on GitLab owning the project
- Project: the project name
  
Choose one from
- Submit a merge request to the same project
  - create a branch in the existing project and file a new merge request out of it
  - Additional input needs to be provided:
    - Branch Name: branch to be created
    - Target Branch Name: to merge the new changes into (i.e. the `main`)
- Create a new project within the specified organization
  - to create a brand new project under the `owner` organization

### Page 4: Review

The user can review their input parameters and click "Create" to run the template. After completed, a link to the created source code repository will be provided.
