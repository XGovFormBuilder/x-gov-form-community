---
title: Case study - Cross government form builder
last_modified_date: 2021-04-29
nav_exclude: true
---
The cross government form builder uses the following components:-

**Components:**

- [Designer](#the-designer-component)
- [Runner](#the-runner-component)

## The Designer Component

### Definition

The application that allows users to edit/create forms.
Forms are downloaded as a single JSON payload (or optionally persisted in S3)

### User need / value

- As a form designer, I want to be able to edit/create forms/services without the help of a developer so that I can rapidly create prototypes for user research
- As a form designer, I want to be able to edit/create forms/services so that I can provide a service for citizens or civil servants (internal)

### Technical components

- React
- Node.js (proxies requests to preview instance)
- Deploy agnostic. FCDO are deploying with AWS + Kubernetes, HO are deploying in HO ACP (Application Container Platform). The open source team is deploying in Heroku.
- Docker image (for deploys or extensions - ie if a department wanted to make further changes) https://github.com/orgs/XGovFormBuilder/packages/container/package/digital-form-builder-designer
- Optional AWS S3 integration (stores forms in a bucket when saved)


## The Runner Component
*(/preview)*

### Definition
This application is able to render applicant-facing pages. CRUD Endpoints are open when in preview mode, to allow the designer to “publish” forms for previewing.

Complete forms are deployed as part of the docker image.

This application will also integrate with external services, including
- GOV.UK Pay
- GOV.UK Notify
- Webhooks (integrate with any external service. The only requirement is that it returns a 2xx when successful, and optionally a reference number)
These should be used when submitting to a CMS or if there are dead letter queue requirements

### User need / value

As a form designer, I want to preview the pages I have created/edited so that I can ensure it is as the applicant would see it.  
As an applicant, I want to be able to complete a form, so that the department or team can fulfill my request

### Technical stack

- Node.js
- Nunjucks (govuk components)
- Deploy agnostic. FCDO are deploying with AWS + Kubernetes, HO are deploying in HO ACP (Application Container Platform)
- Docker images (for deploys/extensions) https://github.com/orgs/XGovFormBuilder/packages/container/package/digital-form-builder-runner
- Redis for user session management
In memory is used for preview or local development, however redis can be used when in these environments also

## Roadmap
- Planned components:
- Persistence microservice so form design can be stored in a DB rather than .json in filesystem
- SSO
- RBAC (Roles Based Access Control)

## Other information
Monorepo: https://github.com/XGovFormBuilder/digital-form-builder

Entity relationship diagram (data model): https://github.com/XGovFormBuilder/digital-form-builder/blob/master/docs/adr/0000-ERD.svg

**Note: None of the components are centrally managed - it is not yet a “service” / centrally managed system. As of now, these are Bring Your Own Cloud**
