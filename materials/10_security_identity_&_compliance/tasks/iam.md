# Task: Creating and using of IAM roles/policies.

## Problem to Be Solved
Study how to create IAM roles/policies and use them for different AWS services, e.g. assume role. 

## Implementation Details

### Pre-requisites:
- Already created S3 bucket
- Installed jq - https://stedolan.github.io/jq/download/ 
- Installed AWS cli v1 - https://docs.aws.amazon.com/cli/latest/userguide/install-cliv1.html
- https://awspolicygen.s3.amazonaws.com/policygen.html or https://aws.amazon.com/blogs/security/use-the-new-visual-editor-to-create-and-modify-your-aws-iam-policies/ 

### User and Role

 - Create a new user. 
 - Attach to the new user AWS managed policy: **S3 full access**. 
 - Attach to the new user an inline policy, that should contain the follow “Actions”:
    - **ssm:ReadOnly** 
    - **kms:Decrypt** 
    - **iam:ListRoles** 
    - **sts:AssumeRole** 

_It’s highly recommended to read about the last two “Actions” in the Tutorials and guides._ 
- Attach to the new user the Customer managed policy named “KmsDecryptPolicy”, that policy should contain “Action”: **kms:Decrypt**

_Hint: Use policy generator_

- After attaching all of that policies to the new user, add him permission for programmatic api access 
- Add Role named “S3ReadOnlyRole”, attach to the role AWS managed policy: **S3 read-only**

- Create a json and assume role policy that defines the trust relationship of the IAM role: 

```
{
    "Version": "2012-10-17",
    "Statement": {
        "Effect": "Allow",
        "Principal": { "AWS": "arn:aws:iam::123456789012:user/new_created_user" },
        "Action": "sts:AssumeRole"
    }
}
```


### Verification:

1. credentials retrieval from AWS CLI for the newly created user 
2. authorize in AWS CLI using credentials from the previous step 
3. write file to an existing s3 bucket to test full access using AWS CLI 
4. perform role assuming using command aws sts assume-role 
5. authorize in AWS CLI using credentials from the previous step 
6. make sure that you are authorized by using role 
7. make a try to write file from step 2 
8. copy file from s3, that was uploaded in step, using AWS CLI 

 


## Solution levels (could be done in a sequence):
- Basic - create IAM roles and user using AWS Console and policy generator, proceed with verification from cli
- Medium - create everything using AWS cli (hint: use policies in json forma from Basic level) and proceed with verification
- Pro - create everything using IaC approach with CloudFormation/Terraform, proceed with verification from cli


## Benefits / Outcomes / Pros and Cons / Summary
1.	Almost everything in AWS is tied with IAM.
2.	Usage of AWS managed and custom managed policies.
3.	Understanding of IAM roles precedence.
4.	Understanding of service-managed roles.
5.	Assuming roles practice and key points.
6.	Instance-profile
7.	Resource-based policies

## Tearing down
Delete all resources and delete IAM roles/policies, since you cannot delete policy or role that is in use.
