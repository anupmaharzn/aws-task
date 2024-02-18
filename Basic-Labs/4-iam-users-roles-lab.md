# IAM Users and Roles

- **Objective**: To understand `AWS Identity and Access Management` (IAM) by creating and managing users, groups, and roles.
- **Approach**: Students will create new IAM users, assign them to groups, and apply policies to manage permissions. The lab will also involve creating roles for AWS services and understanding the use of IAM roles for cross-service access.
- **Goal**: Students will learn about user and permission management in AWS, the importance of roles for security and best practices for IAM.



## AWS Identity and Access Management (IAM)

- Use IAM to manage access to AWS resources:
    - A resource is an entity in an AWS account that you can work with.Example resources,An amazon EC2 instance or an amazon s3 bucket.
- Example - Control who can terminate Amazon EC2 instances

- Define fine-grained access rights
    - who can access the resource
    - which resource can be accessed and what can the user do to the resource.
    - How resource can be accessed
- IAM is a no-cost AWS account feature.

### IAM:Essential components
- IAM user : A person or application that can authenticate with an AWS account
- IAM group : A collection of IAM users that are granted identical authorization (Example: admins,developer,tester)
- IAM role : Useful mechanism to grant a set of permissions for making aws service requests(role provides 
      temporary security credentials)
- IAM policy : The document that defines which resources can be accessed and the level of access to each
    
![IAM essential components](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/45c94dba-b78d-484d-af7d-619c1db5917b)


### Authenticate as an IAM user to gain access

- type of access the user is permitted to use
    - programmatic access
        - authenticate using
            - access key ID
            - secret access key
            (key pair)
        - provide aws cli and aws sdk access
    - aws management console access
        - authenticate using
            - 12-digit account id or alias
            - IAM user name
            - IAM password
        - if enabled multi-factor authentication (MFA) prompts for an authentication code.
          
### IAM:Authorization
- Assign permissions by creating an IAM policy.
- Permission determine which resources and operations are allowed:
    - all permissions are implicitly denied by default
    - if something is explicitly deined, it is never allowed
- NOTE: The scope of IAM service configurations is global.Setting apply across all AWS Regions.
  
![authorization what actions are permitted](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/233bf922-12cb-4d89-969b-ef572b7baecc)

![IAM permission flow](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/980747f2-f491-4cc9-81f4-bb5495cd8d13)

### IAM policies
- An IAM policy is a document written in javascript object notation (or visual way to do so) that defines permissions
    - enables fine-grained access control

- Two types of policies - identity-based and resource-based
    - Identity-based policies
        - Attach a policy to any IAM entity
            - An IAM user, An IAM group or An IAM role
        - Policies specify:
            - actions that may be performed by the entity
            - actions that may not be performed by the entity
        - A single policy can be attached to mutiple entites
        - A single entity can have multiple policies attached to it
    - Resource-based policies
        - attached to a resource (such as an ec2, s3 bucket) 

![example of iam role](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/5a072705-b2e8-4892-9ca8-50ff936f16c4)


## Lab Task

### Lab overview

#img2

- Create IAM User

#img3

#img4

#img5

- IAM User cannot be created

#img6

- Create User group

#img7

**user group cannot be created**
