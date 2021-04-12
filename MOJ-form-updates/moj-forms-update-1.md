---
title: MOJ Forms cross-government update 1 - February 2021
last_modified_date: 2021-03-01
---

# MOJ Forms cross-government update 1 - February 2021

Hi all! For those of you who don’t know me, I’m Irina and I’m the Senior Product Manager on [MOJ Forms](https://moj-forms.service.justice.gov.uk/) - the form builder product developed by the Ministry of Justice and currently used by 16 of our services to build and publish online forms.

I was inspired to start these updates by [Harry Vos’s sprint notes on the GDS ‘re-Discovery’ on Submit](https://xgovformbuilder.github.io/x-gov-form-community/2021-GDS-discovery.html). We are very keen to work in the open and get feedback and input into our work from the community, so I thought it might be useful to also share our product updates on a regular basis.
In each of these updates we plan to share what we’ve been up to in the last month or so, and talk honestly from our experience and work about a theme that we think will be of interest and benefit to the whole community.  

## About MOJ Forms
For anyone who’s not familiar with our product, MOJ Forms allows teams to easily prototype, build and publish online forms and services as part of one product and without needing to know how to code. With MOJ Forms, everything:

- meets government design patterns and security standards
- is fully accessible
- is free to build, publish and host on the MOJ Cloud Platform (ran as Kubernetes cluster on AWS)

Our product (formerly known as MOJ Form Builder) passed it’s Alpha assessment in 2018 and since then we’ve been developing and implementing our tool to transform existing paper forms, as well as prototype and build new services.   
We want to establish it as a common, reusable product which will become the component of choice for most forms and simpler services within MOJ. We believe MOJ Forms will help to increase the pace of digital transformation within MOJ.

## Updates from the last few months

To this end, over the last 6 months we’ve focused our work on making the product fully self-service for digital teams, in particular user-centred design professionals who we think are most likely to use the tool (more on that choice in the next section).

This has meant redesigning the product so it’s all in a single online application with intuitive UI that allows for direct interaction and manipulation. We’ve focused on allowing users to:
- make use of pre-populated page templates based on the GOV.UK Design Patterns (e.g. Start page, Check Your Answers, Single/ Multiple questions)
- edit directly on the page, whilst also viewing it as an end-user would see it
- view their end-to-end form and logic in a clear flow, and make changes to the logic and branching through that flow
- quickly manage the settings of their forms and publish in the same application

There’s a whole load more to it, so please shout if you want to find out more.

We’ve done 4 rounds of user research on the new product and are excited that our designs are testing really well. Users are largely successful in completing an end-to-end journey from the first time!

In terms of technology, we’ve chosen to rewrite our Editor, Runner and Publisher to enable the new designs and also address our technical debt. We’re writing everything in Ruby on Rails and you can view our high-level technical architecture [here](https://docs.google.com/document/d/1yebtw2R_tmJ_jhA_KOp167cbpfNMAznyZ783ShA9ceE/edit?usp=sharing).
We are planning to release our MVP and start working with private beta participants in MOJ from late March, and then iterate the tool to deliver more features throughout the spring. We also hope to go for a Beta service assessment in late spring / early summer (subject to our Private Beta going well).

## Theme of the Month - Who uses a form builder tool? Who benefits from it?

When I started on the team in September 2020, one of the first questions I had was ‘who are our users?’. Who should we be building and designing for? What value are we trying to deliver? (and from engagement with others across the community, it seems that these are common questions for many developing a form builder tool.)

At that time in MOJ, we had a product that albeit not fabulous to use, ultimately worked to build online forms. We had more than 10 forms online, most of which we had developed, published and supported ourselves. We recognised that this model just won’t scale. We also agreed that until we have a clear view of who we’re designing for, we will always miss the mark with the quality of our product.

From analysis of our user research and work to date, we agreed that at least in MOJ there are two very distinct user groups, which correspond to distinct business goals:

1. people in digital teams or with digital capabilities (i.e. in particular, our UCD professionals). For them, a good tool with a robust support mechanism is sufficient and they could use it in a self-service way to prototype, develop and publish online forms or services largely independently - this is so far supported by our user research. The business value from this use case is saving money from using reusable components, so teams are freed up to spend their design and development time on more value-adding work.
2. operational teams with very limited resources and no digital capabilities (such as UCD skills and complex back-end systems). Often these are the owners of the ‘long-tail’ of paper forms that need transformation but are too small to get a dedicated digital team. For them, just offering a simple tool is probably not enough and they need additional support in terms of form design and other products like case management systems. The business value from this use case is eliminating citizen-facing paper services and forms and inefficient, error-prone processes - the original goal that the MOJ Forms Discovery cited.

Having made this clear distinction, we have decided to prioritise the first user group, and once we’ve cracked that, start exploring how best to support and tackle the second use case. We feel that until we have a good product that can be used independently as a platform component, we are unlikely to make a significant dent in the second use case either.

But more on how we’re delivering against this first use case and what we plan to do as part of our longer term roadmap, next time!

## Your views
Do you agree with our views? Do you like what we’re doing so far or are there things that we’re missing? Do you have any suggestions or ideas about the frequency, topics that you’re interested in or any other feedback about these updates?

I’d love to hear from you. Please ping me on the cross-government Slack space or get in touch with me on Twitter (@euro_tweety)
