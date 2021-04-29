---
title: Case study - MoJ form builder
last_modified_date: 2021-04-29
parent: form-terminology
---

The MOJ form builder is made using the following components.

**Components:**
- [Editor](#the-editor-component)
- [Runner](#the-runner-component)
- [Publisher](#the-publisher-component)
- [Metadata](#the-metadata-component)
- [Submitter](#the-submitter-component)


## The Editor Component

### Definition
The Editor component allows a user to create and edit a form, for example by adding or deleting pages or questions.  

### User need

As a form builder, I need to be able to create new forms / services.
As a form builder, I need to be able to make changes to my forms / services.

## Technical stack
- Ruby on Rails application with custom javascript frontend
- A gem is used that presents the metadata as the online form
- The same gem is used in both the Editor and Runner
- All form data is passed to the Metadata DB
- Makes sure the Metadata conforms to a published schema
- Access is authorised using Auth0 against MOJ AD (MS and Google)
- Hosted in MOJ’s Cloud Platform

## GitHub repo
https://github.com/ministryofjustice/fb-editor

## The Runner Component

### Definition

The Runner is the application that is running the ready form.

### User need
As a member of the public / MOJ employee, I want to be able to access the Justice services that I require.

### Technical components used:
- Ruby on Rails and uses a gem that presents the metadata as the online form
- The same gem is used in both the Editor and Runner
- Runner is published into a either test or production environment fully connected to the backend services with the configured URL (within the Justice domain)
- The Runner can be configured to meet the service requirements
- Hosted in MOJ’s Cloud Platform

### GitHub repo
https://github.com/ministryofjustice/fb-runner

## The Publisher Component

### Definition
The Publisher application allows teams to publish forms in test or production environments.

### User need
As a form builder / digital team, I want to publish and make the form available either in test or production environments

### Technical components
- Ruby on Rails and part of the Editor
- Creates a new Runner with configuration in either test or production environment
- Creates connection to the backend services with the configured URL (within the Justice domain)
- Hosted in MOJ’s Cloud Platform

### GitHub repo

https://github.com/ministryofjustice/fb-publisher

## The Metadata Component

### Definition
The Metadata component allows storage of the form metadata and using the Metadata API

### User need
As a form builder, I need to be able to create and edit forms, including accessing the right forms that I own  

### Technical components used:
- Rails application
- Postgres DB
- Checks the json file against the schema
- Manages versioning

### Github repo

- https://github.com/ministryofjustice/fb-metadata-api
- https://github.com/ministryofjustice/fb-metadata-presenter
- https://ministryofjustice.github.io/form-builder-metadata-api-docs/

## The Submitter Component

### Definition
The Submitter processes the data submitted when a form is completed so end users have their service request completed.

### User need / value
As a member of the public / MOJ employee, I need to be able to provide government with the information that they need to process my service request.


### Technical components used:
- Rails application
- Orgrestrates creating PDF, CSV and sending via email or API endpoint
- Built in queue

### Github repo
https://github.com/ministryofjustice/fb-submitter
