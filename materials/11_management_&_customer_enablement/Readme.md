# Management & Customer Enablement

## [AWS Support](docs/Support_center.md)

### General description:

AWS Support offers a range of plans that provide access to tools and expertise that support your AWS solutions&#39; success and operational health. All support plans provide 24/7 access to customer service, AWS documentation, technical papers, and support forums. For technical support and more resources to plan, deploy, and improve your AWS environment, you can choose a support plan that best aligns with your AWS use case.

AWS for each account provides a basic plan. The basic plan is free for each AWS customer. You are able to change the basic plan to three different paid plans:

- Developer
- Business
- Enterprise

### Detailed overview

A detailed overview and compare existing plans are available here:

[https://aws.amazon.com/premiumsupport/plans/](https://aws.amazon.com/premiumsupport/plans/)

Keep in mind most major features available across all plans.

All AWS customers automatically have 24/7 access to these features of Basic Support:

- One-on-one responses to account and billing questions;
- Support forums;
- Service health checks;
- Documentation, technical papers, and best practice guides.


Customers with a Developer Support plan have access to these additional features:

- Everything covered from the basic plan;
- Best practice guidance;
- Building-block architecture support: guidance on how to use AWS products, features, and services together;
- Supports an unlimited number of support cases that can be opened by one primary contact, which is the AWS account root user.

Business Support or Enterprise Support plan have access to the next features:

- Use-case guidance – What AWS products, features, and services to use to best support your specific needs;
- AWS Trusted Advisor – A feature of AWS Support, which inspects customer environments and identifies opportunities to save money, close security gaps, and improve system reliability and performance. You can access all Trusted Advisor checks;
- The AWS Support API to interact with Support Center and Trusted Advisor. You can use the AWS Support API to automate support case management and Trusted Advisor operations;
- Third-party software support – Help with Amazon Elastic Compute Cloud (Amazon EC2) instance operating systems and configuration. Also, help with the performance of the most popular third-party software components on AWS. Third-party software support isn&#39;t available for customers on Basic or Developer Support plans;
- Supports an unlimited number of AWS Identity and Access Management (IAM) users who can open technical support cases.


Enterprise Support plan have access to next features:

- Application architecture guidance – Contextual guidance on how services fit together to meet your specific use case, workload, or application;
- Infrastructure event management – Short-term engagement with AWS Support to get a deep understanding of your use case. After analysis, provide architectural and scaling guidance for an event;
- Technical account manager – Work with a technical account manager (TAM) for your specific use cases and applications;
- White-glove case routing;
- Management business reviews.


##### _Note_:

_Good idea moving from basic to more high plan just when it needs only. For instance, if you need additional support from AWS or_ _temporarily_ _need to have some features which available only in more high plans, you can get it in the next 30 days. And after, to move back to the basic (develop) plan._

##### _Keep in mind_:

_For urgently contact with AWS support, use a chat or phone call as an answer method._

### Monitoring status

You can easy to monitor all statuses of your case in the Support Center. A flow looks like this:

1. Unassigned
2. Work in Progress (WIP)
3. Pending Customer Action (ask for more information) or Pending Amazon Action (let you know that the case is being investigated)
4. The last status is close Case. It means your problem is solved.  If you don&#39;t respond within ten days, the case is closed automatically. Nevertheless, you can always reopen a resolved or closed case.

For each update, you receive email with the correspondence and a link to the case in Support Center.

##### _Important note_:

- _You can&#39;t respond to case correspondence by email. Use the link in the email to navigate to the support case._
- _You must sign in to the AWS account that submitted the support case. If you sign in as an IAM user, you must have the required permissions to view support cases._

### Useful links:

- AWS Knowledge Center Videos: How do I change my AWS Support plan?

[https://www.youtube.com/watch?v=TM98uI7TYPs&amp;ab\_channel=AmazonWebServices](https://www.youtube.com/watch?v=TM98uI7TYPs&amp;ab_channel=AmazonWebServices)

- AWS Knowledge Center Videos: How do I sign up for an AWS Support plan?

[https://www.youtube.com/watch?v=E6fMAMCE\_dc&amp;ab\_channel=AmazonWebServices](https://www.youtube.com/watch?v=E6fMAMCE_dc&amp;ab_channel=AmazonWebServices)

- Getting started with AWS Support:

[https://docs.aws.amazon.com/awssupport/latest/user/getting-started.html](https://docs.aws.amazon.com/awssupport/latest/user/getting-started.html)

- Access AWS Support

[https://docs.aws.amazon.com/awssupport/latest/user/accessing-support.html](https://docs.aws.amazon.com/awssupport/latest/user/accessing-support.html)

- Changing your AWS Support plan

[https://docs.aws.amazon.com/awssupport/latest/user/changing-support-plans.html](https://docs.aws.amazon.com/awssupport/latest/user/changing-support-plans.html)

---
## [AWS service quotas](docs/Service_quotas.md)

### Service Overview

Each AWS account has default quotas. Default quotas calls like limits, and that limits linked with each AWS services. Unless otherwise noted, each quota is Region-specific. Along with looking up the quota values, you can also request a quota increase from the Service Quotas console.

### Use cases / Considerations

When your infrastructure grows you can meet with default AWS limits for your Account. For instance, Amazon EC2 Auto Scaling has a limit of 200 groups per region. If you should have more resources than is defined in the limits, you have few options to achieve it::

- Open the Service Quotas console _(__reference link: D__)._ In the navigation pane, choose AWS services. Select a service, select a quota, and follow the directions to request a quota increase. For more information, see Requesting a Quota Increase in the Service Quotas User Guide _(__reference link: E__)._ (This way is recommended);
- Use the request-service-quota-increase AWS CLI command _(__reference link: F__)_;
- Open the AWS Support Center page _(__reference link: G__),_ sign in if necessary, and choose to Create case. Choose Service limit increase. Complete and submit the form.


##### _Keep in mind_:

If a service is not yet available in Service Quotas, use AWS Support Center instead. Increases are not granted immediately. It might take a couple of days for your increase to become effective.

Also, an important note, all services are separated into two different groups, where the first is adjustable, and the second one is not adjustable. If a service is adjustable then you can make a request for increasing a quota for service. And if a service is not adjustable you can not be increasing a quota for it. For instance, you are able to make a request for Auto Scaling groups per region service, but you can not do anything with SNS topics per Auto Scaling group.

Also, you can easily view current service quotas applied to your AWS account. There are few options which you can follow:

- Open the Service endpoints _(__reference link: A__)_ and quotas page in the documentation, search for the service name, and click the link to go to the page for that service. To view the service quotas for all AWS services in the documentation without switching pages, view the information in the Service Endpoints and Quotas page _(__reference link: A__)_ in the PDF instead.
- Open the Service Quotas console _(__reference link: B__)._ In the navigation pane, choose AWS services and select a service.
- Use the list-service-quotas _(__reference link: C__)_ and list-aws-default-service-quotas AWS CLI commands _(__reference link: С__)._


### Reference links:

1. Service endpoints and quotas page:

    - [https://docs.aws.amazon.com/general/latest/gr/aws-service-information.html](https://docs.aws.amazon.com/general/latest/gr/aws-service-information.html)
    - Link for PDF file: [https://docs.aws.amazon.com/general/latest/gr/aws-general.pdf#aws-service-information](https://docs.aws.amazon.com/general/latest/gr/aws-general.pdf#aws-service-information)
    <br />

1. Link for a dashboard with service quotas in the current region:

    - [https://console.aws.amazon.com/servicequotas/home](https://console.aws.amazon.com/servicequotas/home)
    <br />

1. Link for AWS CLI command for a request service quotas for current aws account:

    - [https://docs.aws.amazon.com/cli/latest/reference/service-quotas/list-service-quotas.html](https://docs.aws.amazon.com/cli/latest/reference/service-quotas/list-service-quotas.html) (get current quotas)
    - [https://docs.aws.amazon.com/cli/latest/reference/service-quotas/list-aws-default-service-quotas.html](https://docs.aws.amazon.com/cli/latest/reference/service-quotas/list-aws-default-service-quotas.html) (get default qoutas)
    <br />

1. Link to service quotas console:

    - [https://console.aws.amazon.com/servicequotas/home](https://console.aws.amazon.com/servicequotas/home)
    <br />

1. Requesting a quota increase:

    - [https://docs.aws.amazon.com/servicequotas/latest/userguide/request-quota-increase.html](https://docs.aws.amazon.com/servicequotas/latest/userguide/request-quota-increase.html)
    <br />

1. Link for AWS CLI command for a quota increase

    - [https://docs.aws.amazon.com/cli/latest/reference/service-quotas/request-service-quota-increase.html](https://docs.aws.amazon.com/cli/latest/reference/service-quotas/request-service-quota-increase.html)
    <br />

1. Link for AWS Support Center page:

    - [https://console.aws.amazon.com/support/home#/](https://console.aws.amazon.com/support/home#/)

### General useful links:

- View and Manage Quotas for AWS Services Using Service Quotas:

[https://www.youtube.com/watch?v=ZTwfIIf35Wc&amp;ab\_channel=AmazonWebServices](https://www.youtube.com/watch?v=ZTwfIIf35Wc&amp;ab_channel=AmazonWebServices)

---
## [Trusted advisor](docs/trusted_advisor.md)

### Service Overview

AWS Trusted Advisor is an online tool that provides a real time guidance to help provision resources following AWS best practices. Trusted Advisor inspects resources across all AWS Regions and presents a summary of check results. Trusted Advisor checks help optimize AWS infrastructure, improve security and performance, reduce overall costs, and monitor service limits.

### Use cases / Considerations

Trusted Advisor includes an ever-expanding list of checks in the following five categories:

- Cost optimization – recommendations that can potentially save money by highlighting unused resources and opportunities to reduce the bill.
- Security - Trusted Advisor can improve the security of application by closing gaps, enabling various AWS security features, and examining permissions.
- Fault Tolerance - recommendations that help increase the resiliency of Amazon Web Services solution by highlighting redundancy shortfalls, current service limits, and overutilized resources.
- Performance - recommendations that can help to improve the speed and responsiveness of applications.
- Service Limits – Trusted Advisor checks for service usage that is more than 80% of the service limit.

The status of checks are:

- Red: action recommended
- Yellow: investigation recommended
- Green: no problem detected

### Cautions

Trusted Advisor Service Limits values are based on a snapshot, so current usage might differ. Limit and usage data can take up to 24 hours to reflect any changes.

### Pricing considerations

Available categories and number of checks depends on AWS support plan (Basic, Developer, Business, Enterprise).

### More details

[AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

[AWS Trusted Advisor best practice checklist](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/best-practice-checklist/)

[AWS support plans](https://aws.amazon.com/premiumsupport/plans/)

---
## [CloudTrail](docs/CloudTrail.md)

### Service Overview

AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting. In addition, you can use CloudTrail to detect unusual activity in your AWS accounts. These capabilities help simplify operational analysis and troubleshooting.

### Use cases / Considerations

AWS CloudTrail allows AWS customers to record API calls, sending log files to Amazon S3 buckets for storage. The service provides API activity data including the identity of an API caller, the time of an API call, the source of the IP address of an API caller, the request parameters and the response elements returned by the AWS service.

You can get more detailed information from this links:

• General overview of CloudTrail [https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)

• Actions covered by CloudTrail [https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-concepts.html#cloudtrail-concepts-events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-concepts.html#cloudtrail-concepts-events)

• CloudTrail supported services [https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-aws-service-specific-topics.html](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-aws-service-specific-topics.html)

### Cautions

There are number of limitations in CloudTrail service, that you should know:

- You can have only **5** trails per region
- You have only **10** transactions per second (TPS) for Get, describe, and list APIs
- You have only **2** TPS for LookupEvents API
- You have **1** TPS for all other APIs
- Limits of Events Selectors are **5** per trail
- For all Advanced Event Selectors you have **500** conditions
- You can use **250** Data resources in event selectors across all Event Selectors in a trail
- Events over **256 KB** size can&#39;t be sent to CloudWatch Logs
- Event version **1.05** and newer has total event size limit of **256 KB**
- CloudTrail file size sent to Amazon S3 limited by **50 MB** ZIP file, after compression
- To view events for Route 53 API requests, you must choose US East (N. Virginia) in the region selector at the top of the console

You can get detailed information by this link:
[https://docs.aws.amazon.com/awscloudtrail/latest/userguide/WhatIsCloudTrail-Limits.html](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/WhatIsCloudTrail-Limits.html)

### Pricing considerations

You can get started with AWS CloudTrail for free ( see [https://aws.amazon.com/free/](https://aws.amazon.com/free/) for more details about Free Tier ):

- Log and search events with Event History AWS CloudTrail logs management events across AWS services by default. You can view, search, and download the most recent 90-day history of your account&#39;s management events for free using CloudTrail in the AWS console or the AWS CLI Lookup API.
- Deliver events by creating trails You can deliver one copy of your ongoing management events to Amazon S3 for free by creating trails. This lets you store events in S3 past 90 days.

You will pay for:

- Deliver additional copies of events and data events by using trails You can deliver additional copies of events, including data events, using trails. Trails can be created for a single AWS account, or for multiple AWS accounts using AWS Organizations. See pricing in the table below.
- Identify unusual activity in your account AWS CloudTrail Insights analyzes write management event API calls in your AWS account and detects unusual activity. See pricing in the table below.

| **Feature** | **Pricing** |
| --- | --- |
| Management events delivered to S3 | First copy of management events is delivered free; additional copies: $2.00 per 100,000 management events delivered |
| Data events delivered to S3 | $0.10 per 100,000 data events delivered |
| CloudTrail Insights | $0.35 per 100,000 events analyzed |

[https://aws.amazon.com/cloudtrail/pricing/](https://aws.amazon.com/cloudtrail/pricing/)

### More details

- CloudTrail using sample

[https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-tutorial.html](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-tutorial.html)

- Creating IAM user and grant him right permissions for using CloudTrail:

[https://docs.aws.amazon.com/awscloudtrail/latest/userguide/security\_iam\_id-based-policy-examples.html#grant-permissions-for-cloudtrail-administration](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/security_iam_id-based-policy-examples.html#grant-permissions-for-cloudtrail-administration)
