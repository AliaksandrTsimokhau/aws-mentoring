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
