> The cloud native landscape guide was initiated by the
> [CNCF Business Value Subcommittee](https://github.com/cncf/business-value)
> and [Cartografos group](https://github.com/cncf/cartografos). It was authored by
> [Jason Morgan](https://www.linkedin.com/in/jasonmorgan2/) and
> [Catherine Paganini](https://www.linkedin.com/in/catherinepaganini/),
> edited and reviewed by [Simon Forster](https://www.linkedin.com/in/forsters/) and
> [Ihor Dvoretskyi](https://www.linkedin.com/in/idvoretskyi/), built by
> [Jordi Noguera](https://www.linkedin.com/in/jordinoguera/) with UX consultation
> from [Andrea Velázquez](https://www.linkedin.com/in/andreavelazquez1/).

## Introduction

If you've researched cloud native applications and technologies, you've probably come
across the [CNCF cloud native landscape](https://landscape.cncf.io). Unsurprisingly,
the sheer scale of it can be overwhelming. So many categories and so many technologies.
How do you make sense of it?

As with anything else, if you break it down and analyze it one piece at a time, you'll
find it's not that complex and makes a lot of sense. In fact, the map is neatly organized
by functionality and, once you understand what each category represents, navigating it
becomes a lot easier.

In this guide, we’ll break this mammoth landscape down and provide a high-level overview
of its layers, columns, and categories.

### What is the cloud native landscape?

The goal of the cloud native landscape is to compile and organize all cloud native open
source projects and proprietary products into categories, providing an overview of the
current ecosystem. Organizations that have a cloud native project or product can
[submit a PR](https://github.com/cncf/landscape/) to request it to be added to the
landscape.

### How to use this guide

In this guide, you'll find one chapter per layer and column which discusses each category
within it. Categories are broken down into: what it is, the problem it addresses, how it
helps, and technical 101. While the first three sections assume no technical background,
the technical 101 is targeted to engineers just getting started with cloud native. We
also included a section for associated buzzwords and lists CNCF projects

![CNCF Landscape](https://landscape.cncf.io/images/landscape_preview.png "CNCF Landscape")

> ##### INFOBOX
>
> When looking at the landscape, you'll note a few distinctions:
>  * *Projects in large boxes* are CNCF-hosted open source projects. Some are still in
>    the incubation phase (light blue/purple frame), while others are graduated
>    projects (dark blue frame).
>  * *Projects in small white boxes* are open source projects.
>  * *Products in gray boxes* are proprietary products.
>
> Please note that new projects are continuously becoming part of the CNCF so
> always refer to the actual landscape – things are moving fast!

### Contribute to the CNCF Landscape

Are you searching for an exciting project to contribute to within the CNCF ecosystem? Look no further! The CNCF hosts a wide range of projects that span cloud-native computing. To find the perfect project for your skills and interests, check out our comprehensive contribution guide at [Getting Started](https://contribute.cncf.io/contributors/getting-started/). It provides you step-by-step instructions on getting started and offers valuable insights for both newcomers and experienced contributors. Join our vibrant community and make your mark on cloud-native innovation today!

### Summary: Platform

As we've seen there are multiple tools that help ease Kubernetes adoption. From Kubernetes
distributions and hosted Kubernetes to more barebones installers or PaaS, they all take various
installation and configuration burdens and pre-package them for you. Each solution comes with its
own "flavor." Vendor opinions about what's important and appropriate are built into the solution.

Before adopting any of these, you'll need to do some research to identify the best solution for
your particular use case. Will you likely encounter advanced Kubernetes scenarios where you'll need
control over the control plane? If so, hosted solutions may not be a good fit. Do you have a small
team that manages "standard" workloads and needs to offload as many operational tasks as possible?
There are multiple aspects to consider. While there is no single best tool for all use cases,
there certainly will be an optimal tool for your needs.

## Summary: Cloud Native Landscape

Now that we've broken the CNCF Cloud Native Landscape down and discussed it layer by layer,
category by category, it probably feels less overwhelming. There is a logical structure to it and,
once you understand it, navigating the landscape becomes a lot easier.

The layers of the CNCF Landscape build on each other. First, there is the **provisioning** layer
with the tools needed to lay the infrastructure foundation. Next is the **runtime** layer where
everything revolves around containers and what they need to run in a cloud native environment.
The **orchestration and management** layer contains the tools to orchestrate and manage your
containers and applications — in other words, the tools needed to create the platform on which
applications are built. The **application and definition and development** layer is concerned with the tooling
needed to enable applications to store and send data as well as with the ways we build and
deploy our applications.

Next to the layers, there are two columns. The **observability and analysis** column includes
tools that monitor applications and flag when something is wrong. Since all layers have to be
monitored, this category runs across all of them. And finally, there are **platforms**. Platforms
don't provide new functionality, instead, they bundle multiple tools across the different layers
together, configuring and fine-tuning them so they are ready to be used. This eases the adoption of
cloud native technologies and may even be the only way organizations are able to leverage them.

This concludes the CNCF Landscape guide. We hope you enjoyed the read and that we were able to
bring a little more clarity to the landscape.

> ##### NOTE
>
> The cloud native space evolves quickly. If you see anything that's outdated, please submit a PR
> so we can update it. We want this to be a living document and appreciate your contribution.
