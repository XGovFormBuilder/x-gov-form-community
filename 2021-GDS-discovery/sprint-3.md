---
title: Sprint 3 which problems should we solve?
last_modified_date: 2021-02-26
parent: 2021 GDS Discovery
---

# Sprint 3: which problems should we solve?

Written by [Harry Vos](https://twitter.com/vosageroll)

## Is anyone close to solving problems with low volume forms?

When we started this, we said we would only go beyond discovery if nobody else was close to solving problems with low volume forms. So far, we have found lots of good teams in the public sector solving problems with their organisations' medium volume forms, but nothing aimed at low volume forms. We're yet to do a proper analysis of off-the-shelf form builders, but an initial scan looks like they aren't good value for low volume forms, and few are accessible. I hope we are proved wrong.

If we find that existing products and services are accessible, good value for low volume forms, usable, and interchangeable, GDS might not need to invest in solving these problems. Instead, we would need to understand why the public sector isn't commonly buying and using these products and services.

If our initial scan was right, I think we can be quite confident that GDS would need to invest in solving problems with low volume forms.

## Which problems should we solve first?

If we do need to make an investment, we need to focus on solving a specific problem first. I think we can rule out solving problems with high or medium volume forms. Other people are close to solving those problems. That leaves two different groups of low volume forms to focus on: central and local government.

### Low volume forms in local government

Under around 5,000 transactions per year, we know these tend to be PDFs which are often inaccessible, inefficient and hard to use.

In contrast to central government, local public services are also very similar. For example, most local authorities have a ‘Book a bulky waste collection’ service.

As a result of these problems, they would massively benefit from a Government as a Platform approach. There is a big opportunity to make these forms more accessible, and easier to use.

However, we would need to consider the following:

1. Medium volume services already use some sort of form builder, either standalone, built into their content or customer relationship management systems, or whole services like parking are completely outsourced to a systems integrator like Serco, Capita, Civica or Northgate. While these aren’t currently economically viable for low volume services, as they become used more often on medium volume services, volume discounts may allow them to be used for lower volume services
2. Their supplier contracts are between 2 to 5 years, sometimes longer if whole services are outsourced
3. The buyers in IT tend to be different from the users. Users don’t seem to have much influence over spending
4. GDS has fewer relationships with them
5. We’d need to make forms somewhat consistent with their websites

### Low volume forms in central government

Under around 1,750 transactions per year, we know these tend to be PDFs which are often inaccessible, inefficient and hard to use. These make up the majority of forms on GOV.UK.

While these forms aren’t as similar as in local government, there is still a massive opportunity here for GDS to solve these problems.

At the moment, these inaccessible PDFs are published using GOV.UK Whitehall publisher. It's a problem we should be able to influence. For this reason, along with some of the challenges with solving these problems for local government, my hunch is that we should start with central government.

Experimenting with interventions on GOV.UK Whitehall publisher should make changing behaviour easier because:

1. The users are already there. Unlike with local government, we don’t need to onboard new organisations or teams
2. That is where publishers are uploading inaccessible PDF or other forms without accessible alternatives

If we succeeded in changing publisher behaviour, and problems in local government remained unsolved, we could potentially expand outwards to meet their needs.

## What our first experiment might look like

![Now: 1. Legislation changes 2. Policy tell web team to publish new PDF form 3. Web team prioritise high volume forms, making accessibility an issue for low volume forms 4. Inaccessible PDF gets published. Next: 1. Web team warned before publishing a PDF. Prompt to build a form. 2. Web team build an HTML form, directing responses to email. 3. New form is live on GOV.UK. (Possible 4.) Email to web team if form is projected to have more than 1,750 transactions per year.](https://raw.githubusercontent.com/XGovFormBuilder/x-gov-form-community/main/img/forms-sketch-optimised.jpg "forms-sketch-optimised")

## Finding more public sector form building teams

We found two more public sector teams working on forms. [HM Land Registry have a form builder](https://govuk-frontend-wtf.herokuapp.com/) for GOV.UK services. HM Revenue & Customs has a dedicated delivery team working on accessible forms, and are evaluating to what extent existing products meet user needs. One of the cross-government form building community's goals is to encourage and enable reuse of products across different public sector organisations. With these teams seemingly unaware of the community until now, I think we need to reach out and engage more people.

Finding more of these teams might also suggest that there are problems that haven't yet been solved. I'm looking forward to learning more about their work.

## Clarifying what GDS believe to be a good low volume service

In our user research, we observed some more digitally-capable teams in local authorities going above and beyond what the 2018 public sector accessibility regulations require. They were not only trying to convert PDF forms into HTML forms that meet the web content accessibility guidelines (WCAG), they were also redesigning them to make them easier to use. Their intentions are good, though the overall process of making their forms accessible was taking much longer.

If this behaviour is common, lots of well-intending digital public servants are making a trade-off — by making sure everybody can easily use a service, they make people with access needs wait longer for accessible forms.

I'm in the process of trying to clarify how desirable the GDS accessibility and Service Standard teams believe this behaviour to be.

## What we did in the past two weeks

- wrapped up our interviews with users in local government
- drafted recommendations to clarify our stance on what good low volume services look like
- started making a list of existing products and services we want to learn more about
- looked for a frontend developer to help us evaluate the accessibility of existing products
- sketched what our first experiment might be

[<- Previous update](/x-gov-form-community/2021-GDS-discovery/sprint-2)

[Next update ->](/x-gov-form-community/2021-GDS-discovery/sprint-4)
