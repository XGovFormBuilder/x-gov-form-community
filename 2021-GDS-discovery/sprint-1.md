---
title: Sprint 1: problems faced by local government and limitations of teams using form builders
last_modified_date: 2021-01-29
parent: 2021 GDS Discovery
---

# Sprint 1: problems faced by local government and limitations of teams using form builders

Written by [Harry Vos](https://twitter.com/vosageroll)

## Problems local government faces when collecting information from users

The original GOV.UK Submit team was focused on supporting central government. Most members of the cross-government forms community are from central government. At the start of this discovery, we knew comparatively little about the problems local government faces when collecting information from users. Roughly half of public services are run locally. To try to fix this gap, we started interviewing people working in local government.

We're running some analysis next week, but here are a few of our initial observations, focusing on some of the differences between central and local government:

- some local authorities have less freedom to change the ways they collect information from users. To make a small change to an online form, they may have to scope a change request with their large outsourced service provider, and wait around six months for the change
- some teams in local authorities or their outsourced service providers are using form builders for higher volume services around waste, recycling, and council tax, but rely on in-house web or digital teams to lobby service providers to get their form builders to produce accessible forms
- where they are using online forms, some teams in local authorities struggle to integrate the data they collect with their case management systems, citing a lack of APIs. This sometimes results in receiving the form data over email, and manually pasting the data into their case management systems

What central and local government has in common is that most forms used to collect information from members of the public or businesses are still PDFs, which tend to be hard to make accessible.

Until we've interviewed more people and analysed our notes, I'm going to hold off jumping to conclusions about what this means for GDS.

## Limitations of multi-disciplinary teams using form builders

The good news is that in some cases, a multi-disciplinary team using a form builder can half the cost of transforming a PDF form into an online service. This comes from speeding up the development time, and reducing the number of technical specialists needed. However, even at half the original costs, there are still forms that aren't used enough to justify the investment.

We wanted to understand these limitations and which services they don't work so well for. We did some 'back of an envelope' calculations using some [2017 data about form downloads on GOV.UK](https://github.com/alphagov/government-form-data/blob/master/data/download.tsv), and the costs the Ministry of Justice Forms team shared with us.

We learnt the majority of the forms on GOV.UK:

- are PDFs, which tend to be hard to make accessible
- aren't downloaded enough to justify multi-disciplinary teams using form builders to transform them
- could be replaced by an OpenDocument file to make them more accessible, but in many cases this would make them harder to use

These forms account for around 22% of total form downloads, not including digital services.

We currently estimate that it isn't cost effective to have a multi-disciplinary team use a form builder for services with fewer than around 3,750 to 1,750 transactions per year, depending on their complexity. Yet these smaller services account for the majority of forms on GOV.UK.

While faster than those not using form builders, current teams using form builders are still quite slow. At the current rate, it would take government around 70 years to digitally transform 5000 forms on GOV.UK. This would just address the backlog. This doesn't even factor in the capacity needed to produce forms for new or changing services.

These limitations leave us with some big questions:

- to justify transforming forms with 1000 or 100 transactions per year, is it possible to reduce the time and cost of producing an accessible HTML form by around 38% or even 94%?
- how likely is it that these problems will be solved by existing public or private sector teams using form builders?

We know [where government stands on the accessibility of forms](https://www.gov.uk/guidance/make-your-website-or-app-accessible-and-publish-an-accessibility-statement). We know [where government stands on the quality of services with over 100,000 transactions per year](https://www.gov.uk/service-manual/service-standard). But how usable does government believe lesser-used forms need to be?

"You can have it good, fast, or cheap. Pick two."

## Questions we most need to answer in this discovery

We want to share our research questions because we're hoping that people reading this update will have some research that would help us to answer these questions. Please [get in touch](https://twitter.com/vosageroll).

This isn't a complete list of questions, but our team prioritised these. We gave high priority to questions that:

- would have a big impact if we didn't have a confident answer by the end of this quarter
- we cannot confidently answer now

Going from high to low priority:

1. How much does it cost government departments to build and support form builders?
2. How accessible and usable are forms currently produced by form builders in use in the public sector?
3. What are the market conditions for GDS to enable the public sector to more easily collect information from their users?
4. If GDS were to invest in solving these problems, what might a roadmap look like for the first year?
5. How do larger and smaller public sector organisations currently collect data from users?
6. Is there a case for investing in a form builder that can be used without access to professional designers, but isn’t GOV.UK branded?
7. What’s the tipping point for organisations to migrate from current form builders to a common platform for the public sector?
8. What are the potential benefits of GDS facilitating the standardisation of data structures that describe forms?
9. How much of the work to produce a usable form builder for the public sector has already been done by departments, and how does this affect the potential investment costs for GDS?
10. What are the unmet user needs considering current commercial and open-source products?
11. What are the trade-offs when looking at building versus buying component parts of the solution? How does this impact the cost-benefit ratio?
12. What are the costs of ongoing support that GDS would need to provide to teams?
13. How much design capacity does the public sector need to replace 200 paper forms with a digital solution over the next five years?
14. Who owns and maintains forms once created by a form builder?

## What we did in the past two weeks

- interviewed people working in local government
- learnt about the Ministry of Justice's costs to run their forms service
- learnt about the problems with inaccessible forms on GOV.UK
- modelled the break-even points for investing in services of various transaction volumes
- spoke to the GOV.UK Design System team about the roadmap for the [GOV.UK Design System](https://design-system.service.gov.uk/), [GOV.UK Frontend](https://frontend.design-system.service.gov.uk/#gov-uk-frontend) and the [GOV.UK Prototype Kit](https://govuk-prototype-kit.herokuapp.com/)

[<- Previous update](/x-gov-form-community/2021-discovery/sprint-0)

[Next update ->](/x-gov-form-community/2021-discovery/sprint-2)
