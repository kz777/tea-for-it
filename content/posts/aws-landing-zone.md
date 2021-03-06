---
author: "AsLan Ussayev"
date: 2020-04-14
linktitle: Creating a New Theme
title: Build an Automated Cloud Governance that Scales ♾️ Infinitely ♾️
categories: [ "AWS", "Governance" ]
tags: ["aws", "cloudLandingZone", "IaC", "CloudFormation"]
weight: 10
---
![This is an image of flying plane](https://media-exp1.licdn.com/dms/image/C5612AQHH8k0XwgcuxA/article-cover_image-shrink_600_2000/0?e=1592438400&v=beta&t=7CmJrJvVsa63UvKcCuh1PD5Ndi3j5EoHOQuV_RgwI7s)

##### *In a survey by Deloitte, 41% of respondents cited their cloud migration efforts as “mixed, problematic, or non-existent” - only 1 in 10 viewed their cloud migration journey as “successful”.*

## Cloud Journeys Have Far More Similarities Than Differences

"Cloud Journey is different for every company" is a saying we have all heard hundreds of times throughout the last decade. Different companies, different projects, and very unique infrastructures; no company is the same.

Despite everything listed above, all the companies lure themselves into the common pitfalls of "$0.0001 per hour" pricing model and provisioning all the "elastic" services without any strategy.

*“There is nothing wrong with making mistakes, but one should always make new ones. Repeating mistakes is a hallmark of dim consciousness.”
— Dave Sim*

![](https://media-exp1.licdn.com/dms/image/C5612AQEzgOGwIvFy0w/article-inline_image-shrink_1000_1488/0?e=1592438400&v=beta&t=BdpWL-Y1PHTN62CmxovnrKFSzl7KpYbNGgueq43PXUo)

## Importance of a Solid Governance Model

Establishing cloud presence of your company is much like constructing a house; you need a solid foundation that lets you scale and make improvements when needed. 

An inadequate attention to governance might cost your company an arm and a leg. 

## An environment that enables Governance at Scale - Landing Zone
To provide holistic and automated governance that scales infinitely you have to prepare the ground - **Cloud Landing Zone.** 

A ***'Landing Zone'*** in cloud terms is defined as, 'A configured environment with a standard set of secured cloud infrastructure, policies, best practices, guidelines, and centrally managed services'. 
  
Landing zones are delivered using **Infrastructure as Code (IaC)** which ensures consistently trusted, rapid and repeatable deployments.

You should strive for an environment where you can monitor near real time resource consumption, allocate funding, assign budgets, control costs, and compliance standards associated with operating your company on the cloud. 

Here’s a multi-account environment based on AWS best practices:
![](https://media-exp1.licdn.com/dms/image/C5612AQFab_e2J2lrtA/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=NGWO67-mXgQ4F_rvi5YwEFlhtIZ58wM7wt_L1h-P7Yc)


* **Organizations master account:** It provisions and manages member accounts under [AWS Organizations Service](https://aws.amazon.com/organizations/).
* **Business Unit accounts:** Sandbox/POC accounts for isolation testing, different security rules and policies.
* **Core accounts:** Provides essential functions that are common to all the accounts under the Organizations, such as Log Archive, Security management, and Shared Services like the directory service.
* **Developer accounts:** These are “sandboxes” for individual’s learning and experimentation.
And this is not the limit. You can expand and modify it as needed.

If you had this all in one AWS account, you'd have to create complex tagging rules and chargeback functions to understand the budget. Security🔐 & compliance🕵️ automation would become a burdensome task.

Benefits of using multi-account approach:

* **Autonomy and Authority:** You can centralize some of your governance but also can distribute authority across your business units. If you do it right you can allow your sub business units to do whatever they need to do as long it's conformant.
* **A Workload Boundary:** You can choose to peer (or not to peer) various workloads together within accounts, ensuring that my ‘blast radius’ for a poorly behaved application is minimized.
* **A Billing Entity:** Enforce and monitor budgets across many accounts, workloads, and users.

## Landing Zone Options in AWS
1. [AWS Control Tower](https://aws.amazon.com/controltower/), a managed service.
2. [Custom built Landing Zone](https://aws.amazon.com/solutions/aws-landing-zone/).

Here are the pros and cons for each approach provided by AWS Prescriptive Guidance (Landing Zone Guide):

![](https://media-exp1.licdn.com/dms/image/C5612AQFktMwXbNHp8g/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=fbXldXCVDErIBguJJVSC39ow0mERVmrMPXLobeFM2lg)

![](https://media-exp1.licdn.com/dms/image/C5612AQFktMwXbNHp8g/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=fbXldXCVDErIBguJJVSC39ow0mERVmrMPXLobeFM2lg)

# AWS Control Tower 
You can start your new landing zones with [AWS Control Tower](https://aws.amazon.com/controltower/) if none of the "Trade-offs" listed above are not conflicting with your companies requirements. Also, don't forget to check out the [pricing](https://aws.amazon.com/controltower/pricing/).

![](https://media-exp1.licdn.com/dms/image/C5612AQGFjdLQ0gzIPw/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=n_mLlCNr8FjgKUirCfcEBwYMDbG--eQolViK_E2k_FI)

# AWS Account Vending Machine
However, if you want to build all of your environment components from scratch, or if you have requirements that only a custom solution can support, built your own custom Landing Zone. 

Make a sure to have enough expertise in AWS to manage, upgrade, maintain, and operate the solution once it’s deployed.

You can find an example solution for your custom Landing Zone in this [GitHub Repo](https://github.com/aws-samples/aws-account-vending-machine). It deploys AWS Account Vending Machine (AVM) for automated deployment of additional accounts using [AWS Service Catalog](https://aws.amazon.com/servicecatalog/?aws-service-catalog.sort-by=item.additionalFields.createdDate&aws-service-catalog.sort-order=desc). 

Simply download the example solution from the github repo and modify it to meet the needs of your organization.

Here's the high level overview of the process flow involved with account building using [AWS Service Catalog](https://aws.amazon.com/servicecatalog/?aws-service-catalog.sort-by=item.additionalFields.createdDate&aws-service-catalog.sort-order=desc):

![](https://media-exp1.licdn.com/dms/image/C5612AQHP572_S7lmTw/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=GvjkPZWpKbB7X0dg1h--dMRfyRwb-o6NwQ0TA8ayf7Q)


## Conclusion
### Don't Loose Sight of The Big Picture from the Beginning
"We all want to scale quickly with confidence in the cloud, and stay secure & compliant at the same time" is just a dream without strategic clarity.

The promise of cloud is to make provisioning simple, fast and cheap. Nevertheless, don't be fooled by those promises and make time to build a **holistic governance** from the beginning.

At the end of the day, who wants to go back to the drawing board❓