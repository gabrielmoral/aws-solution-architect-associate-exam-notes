#### Amazon Cognito

Amazon Cognito provider Web Identity Federation

-   Sign-up and sign-in to your apps.
-   Access for guest users.
-   Acts as an Identity Broker between you application and Web ID providers, you don't need to write any additional code.
-   Synchronises user data for multiple users.
-   It is recommended for all mobile applications AWS services.

**User pools** are user directories used to manage sign-up and sign-in for mobile and web applications.
Users can sign-in directly to the User Pool, or using Facebok, Amazon, or Google. Cognito. Successful authentication generates a JWT.
Multi factor authentication can be activated to a user pool to protect the identity of your users. 

**Identity pools** are able to provide temporary AWS credentials to access AWS services like S3 or DynamoDB.