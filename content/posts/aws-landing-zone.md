---
author: "AsLan Ussayev"
date: 2020-04-12
linktitle: Creating a New Theme
title: Build an Automated Governance that Scales ♾️ Infinitely ♾️
categories: [ "AWS", "Governance" ]
tags: ["aws", "cloudLandingZone", "IaC", "CloudFormation"]
weight: 10
---
![This is an image](https://media-exp1.licdn.com/dms/image/C5612AQHH8k0XwgcuxA/article-cover_image-shrink_600_2000/0?e=1592438400&v=beta&t=7CmJrJvVsa63UvKcCuh1PD5Ndi3j5EoHOQuV_RgwI7s)

## Cloud Journeys Have Far More Similarities Than Differences.

"Cloud Journey is different for every company" is a saying we have all heard hundreds of times throughout the last decade. Different companies, different projects, and very unique infrastructures; no company is the same.

Despite everything listed above, we all want to scale very quickly with confidence in the cloud, and stay secure & compliant at the same time.

![](https://media-exp1.licdn.com/dms/image/C5612AQEzgOGwIvFy0w/article-inline_image-shrink_1000_1488/0?e=1592438400&v=beta&t=BdpWL-Y1PHTN62CmxovnrKFSzl7KpYbNGgueq43PXUo)

## Importance of a Solid Governance Model

In a survey by Deloitte, 41% of respondents cited their cloud migration efforts as “mixed, problematic, or non-existent” - only 1 in 10 viewed their cloud migration journey as “successful”.

Establishing a cloud presence of your company is much like constructing a house; you need a solid foundation that lets you scale and make improvements when needed. 

Inadequate attention to governance might cost your company an arm and a leg. 

## An environment that enables Governance at Scale - Landing Zone.
To provide holistic and automated governance that scales infinitely you have to prepare the ground - Cloud Landing Zone. 

A 'Landing Zone' in cloud terms is defined as, 'A configured environment with a standard set of secured cloud infrastructure, policies, best practices, guidelines, and centrally managed services'. Landing zones are delivered using Infrastructure as Code (IaC) which ensures consistently trusted, rapid and repeatable deployments.

You have to prepare an environment where you can monitor near real time resource consumption, allocate funding, assign budgets, control costs, and compliance standards associated with operating your company on the cloud. 

Here’s a multi-account environment based on AWS best practices:
![](https://media-exp1.licdn.com/dms/image/C5612AQFab_e2J2lrtA/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=NGWO67-mXgQ4F_rvi5YwEFlhtIZ58wM7wt_L1h-P7Yc)


* **Organizations master account:** It provisions and manages member accounts under AWS Organizations Service.
* **Business Unit accounts:** Sandbox/POC accounts for isolation testing, different security rules and policies.
* **Core accounts:** Provides essential functions that are common to all the accounts under the Organizations, such as Log Archive, Security management, and Shared Services like the directory service.
* **Developer accounts:** These are “sandboxes” for individual’s learning and experimentation.
And this is not the limit. You can expand and modify it as needed.

If you had this all in one AWS account, it would seem like boiling the ocean🌊 to create complex tagging rules and chargeback functions to understand the budget. It would be difficult to implement the security🔐 & compliance🕵️ automation.

Benefits of using multi-account approach:

* **Autonomy and Authority:** You can centralize some of your governance but also can distribute authority across your business units. If you do it right you can allow your sub business units to do whatever they need to do as long it's conformant.
* **A Workload Boundary:** You can choose to peer (or not to peer) various workloads together within accounts, ensuring that my ‘blast radius’ for a poorly behaved application is minimized.
* **A Billing Entity:** Enforce and monitor budgets across many accounts, workloads, and users.

## Landing Zone Options in AWS.
1. [AWS Control Tower](https://aws.amazon.com/controltower/), a managed service.
2. Custom build Landing Zone.
Here are the pros and cons for each approach provided by AWS Prescriptive Guidance (Landing Zone Guide):

![](https://media-exp1.licdn.com/dms/image/C5612AQFktMwXbNHp8g/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=fbXldXCVDErIBguJJVSC39ow0mERVmrMPXLobeFM2lg)

![](https://media-exp1.licdn.com/dms/image/C5612AQFktMwXbNHp8g/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=fbXldXCVDErIBguJJVSC39ow0mERVmrMPXLobeFM2lg)

You can start your new landing zones with [AWS Control Tower](https://aws.amazon.com/controltower/) if none of the "Trade-offs" listed above not conflicting with your companies requirements. Also, don't forget to check out the [pricing](https://aws.amazon.com/controltower/pricing/).

![](https://media-exp1.licdn.com/dms/image/C5612AQGFjdLQ0gzIPw/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=n_mLlCNr8FjgKUirCfcEBwYMDbG--eQolViK_E2k_FI)

However, if you want to build all of your environment components from scratch, or if you have requirements that only a custom solution can support, built your own custom Landing Zone. Make a sure to have enough expertise in AWS to manage, upgrade, maintain, and operate the solution once it’s deployed.

You can find an example solution for your Custom Landing zone in this [GitHub Repo](https://github.com/aws-samples/aws-account-vending-machine). It deploys AWS Account Vending Machine (AVM) using [AWS Service Catalog](https://aws.amazon.com/servicecatalog/?aws-service-catalog.sort-by=item.additionalFields.createdDate&aws-service-catalog.sort-order=desc). Simply download the example solution from the github repo and modify it to meet the needs of your organization.

Here's the high level overview of the process flow involved with account building using [AWS Service Catalog](https://aws.amazon.com/servicecatalog/?aws-service-catalog.sort-by=item.additionalFields.createdDate&aws-service-catalog.sort-order=desc):

![](https://media-exp1.licdn.com/dms/image/C5612AQHP572_S7lmTw/article-inline_image-shrink_1500_2232/0?e=1592438400&v=beta&t=GvjkPZWpKbB7X0dg1h--dMRfyRwb-o6NwQ0TA8ayf7Q)


## Conclusion
### Don't Loose Sight of The Big Picture from the Beginning.
The promise of cloud is to make provisioning simple, fast and cheap. However, don't be fooled by those promises and stop provisioning the "elastic" services right and left right away. Make time to build a holistic governance from the beginning.

At the end of the day, who wants to go back to the drawing board?