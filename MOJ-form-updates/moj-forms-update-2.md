---
title: MOJ Forms cross-government update 2 - April 2021
last_modified_date: 2021-04-19
parent: MOJ form updates
---

# MOJ Forms cross-government update 1 - April 2021

With the longer, warmer days and our (re)new(ed) freedoms to socialise with friends and family there are lots of reasons to be cheerful about. At MOJ Forms we have even more reasons to be optimistic. 

In this update our technical architect Matt Tei and I will write about the launch of our new MVP form building tool and the private beta, our future roadmap and the technology that underpins our product.  

## Releasing our MVP
As you might recall from my [previous post](https://xgovformbuilder.github.io/x-gov-form-community/MOJ%20Forms%20Updates/moj-forms-update-1.html), over the last 6 months we’ve been busy redesigning and rebuilding the MOJ Forms product to make it self-service for digital teams. 
Through the new MOJ Forms web application users will be able to log in using an MOJ account to create, edit, preview and publish their forms all in one place without the need to code. To allow this, we’ve built a new Editor application for creating and editing a form, a metadata API to hold the form data structures, a Runner that renders the forms, and we’ve also updated our Publisher so forms get published directly to the form.service.justice.gov.uk domain using the MOJ CloudPlatform.
As it’s an MVP that we wanted to get out to real users as early as possible, we’ve had to be quite ruthless in terms of features we prioritise and release now. We focused on allowing the user to complete an end-to-end journey that provides the most common / useful functionality of a form. Throughout the next few months we will keep adding new features such as branching and complex validations, and expand our private beta to more participants so we can test further. We’ve published our [high-level roadmap](https://trello.com/b/bkbyX3fp/moj-forms-public-roadmap) where you can find out more about what we’ve done and what we're considering for the future. 
Now that we’ve released the first iteration of the new tool, we're starting to work with services as our private beta partners. Our first partner is from the Office of the Public Guardian (OPG) who have been using our legacy product and can’t wait to get the benefit of the new self-service tool. We are also exploring collaborations with service teams from HM Courts and Tribunals Service (HMCTS) and HM Prison and Probation Service (HMPPS). 
In private beta, we’ll do a longitudinal study to assess our hypothesis that form editors (the primary user we’re focusing on) will be able to use our tool in a self-service way and will find the product valuable. We’ll also do more accessibility and usability testing to ensure that our evolving designs and increasingly more complex features meet the needs of all of our potential users. 

## What about non-digital teams?
We’re also excited because we’ve had the ‘green light’ to explore how best to support MOJ teams and services without any digital capabilities who own the majority of existing paper forms or services. We will do this through a structured 10-12 weeks exploration with a new dedicated sub-team, including a new service designer and user researcher, who will work alongside our main product team. 

Our hypothesis is that if we want to transform the majority of paper forms in MOJ in a cost-efficient way that meets the standards, then we will need to provide non-digital teams with more than just a self-service tool. 

The outcomes we want to achieve through this discovery work include:
- Identify citizen-facing paper forms that need transformation, their current use & submission rate, who owns them
- Identify needs and problems of our users when it comes to transforming paper services/ forms using MOJ Forms
- Identify a viable model(s) to support teams that have no digital capabilities to transform paper forms and services
- Quantify and better understand the benefits and business case for transforming the long-tail of paper services in MOJ   
We will provide an update on our progress and findings in our next post.

## Theme of the Month - The tech that underpins our product 
Moving from a desktop to online application isn’t as easy as “just run it in a container” (although this could have been an option that wouldn’t really meet our needs). There were lots of user stories and choices we had to make in a short period. 

To enable the best use of time and ensure we’re aligned, the “tech team” hold a specific kick off session at the start of the more complicated tickets (often including the wider team as well) - this gives the developers the context and explanation to quickly start coding. As a team, we like to pair or mob on tickets, and we also have a weekly deep-dive meeting where we can explore concepts, discuss newer tech or get to the bottom of technical issues we are facing. 

Our legacy desktop Editor application used Github to store the form metadata in it’s own repository. This gave us some good features out of the box - collaboration, versioning and transparency. However, our users found Github a complex technology to deal with and we decided to remove it from the new self service product. By moving to store the metadata in the platform took away the burden of the user having to manage the metadata themselves. This also allowed us to flatten and document the form metadata schema to optimise our technical architecture.

The Runner architecture hasn’t changed; each form is self contained, running independently within our platform. The codebase however has been rewritten in Ruby on Rails as we knew we would be rewriting our Editor in Ruby on Rails too. We created a Metadata-Presenter as a Ruby Gem, taking valid form metadata (in a JSON format from the storage) and converting it to valid HTML, using the GOV.UK design system components. This gem is consumed by both the Runner and the preview feature in the Editor.

The Publisher - originally the legacy service was going to remain as is but early on we decided to recode it into the Editor, giving us the opportunity to structure the code in a manner that makes it usable elsewhere without much rework. 

As ever, we’d like to hear from you with feedback, questions or suggestions, including what you think about our roadmap. Please write to me on the cross-government Slack space or on Twitter (@euro_tweety) 
