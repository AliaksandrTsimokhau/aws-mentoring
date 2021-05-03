# Cloudformation


## Service Overview
AWS CloudFormation is a service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and CloudFormation takes care of provisioning and configuring those resources for you.
Generally speaking, it gives developers and systems administrators an easy way to create and manage a collection of related AWS resources.

### Official guide start page
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html


## Use cases and features
Builds the infrastructure using text templates or visually with Cloudformation Designer.
Infrastructure as Code implementation through version control.
Change Sets allow to preview proposed changes before applying.
Supports custom extensions creation using AWS Lambda.


## Pricing considerations
No additional charge for the service. You will be paid only for resources created using Cloudformation.


## More details
### Main concepts
Cloudformation operates with templates and stacks. Template contains all the resources you want to be created using JSON or YAML formatted text.
Stack is a logical unit of related resources. You create, update, and delete a collection of resources by creating, updating, and deleting stacks.
If you need to make changes to the running resources in a stack, you update the stack. Before making changes to your resources, you can generate a change set, which is a summary of your proposed changes. Change sets allow you to see how your changes might impact your running resources, especially for critical resources, before implementing them.

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-whatis-concepts.html

### How it works

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-whatis-howdoesitwork.html

### Template basics
A template is a declaration of the AWS resources that make up a stack. The template is stored as a text file whose format complies with the JSON or YAML standard. Because they are just text files, you can create and edit them in any text editor and manage them in your source control system with the rest of your source code. In the template, you declare the AWS resources you want to create and configure. You declare an object as a name-value pair or a pairing of a name with a set of child objects enclosed.
Templates include several major sections. The Resources section is the only required section. Some sections in a template can be in any order. However, as you build your template, it can be helpful to use the logical order shown in the following list because values in one section might refer to values from a previous section.

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/gettingstarted.templatebasics.html
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html

### Change sets
When you need to update a stack, understanding how your changes will affect running resources before you implement them can help you update stacks with confidence. Change sets allow you to preview how proposed changes to a stack might impact your running resources, for example, whether your changes will delete or replace any critical resources, AWS CloudFormation makes the changes to your stack only when you decide to execute the change set, allowing you to decide whether to proceed with your proposed changes or explore other changes by creating another change set. You can create and manage change sets using the CloudFormation console, AWS CLI, or CloudFormation API.

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html

### Deploying apps
You can use AWS CloudFormation to automatically install, configure, and start applications on Amazon EC2 instances. Doing so enables you to easily duplicate deployments and update existing installations without connecting directly to the instance, which can save you a lot of time and effort.
CloudFormation includes a set of helper scripts (cfn-init, cfn-signal, cfn-get-metadata, and cfn-hup) that are based on cloud-init. You call these helper scripts from your CloudFormation templates to install, configure, and update applications on Amazon EC2 instances that are in the same template.

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/deploying.applications.html


### Video
AWS Cloudformation Deep Dive and recent enhancements: https://www.youtube.com/watch?v=d6SJPMdBShI

