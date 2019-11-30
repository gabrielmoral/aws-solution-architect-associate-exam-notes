#### IAM (Identity Access Management)

IAM allows you to manage users and their level of access to the AWS Console.

Features:
-   Centralised control of your AWS account.
-   Shared access to your AWS account.
-   Granular permissions.
-   Identity Federation (including active directopry, Facebook, etc)
-   2FA
-   Temporary access for users/ devices where necessary.
-   Password rotation policy.
-   Integrates with many AWS services.
-   Support PC DSS Compliance


**Users**, end users such as people.
**Groups**, collection of users.
**Policies**, documents in JSON format. They give permissions as to what a user.group/role is able to do.
**Roles**, is a way to give permissions to an AWS resource to do something with another AWS resource.

IAM is universal, there is no region.
Root account is the account created when tou create the AWS account. It has admin access.
New users have no permissions when created.
New users are assigned Access Key Id & Secret Access Key when first created if selected.
You will only see passwords and access users once.
