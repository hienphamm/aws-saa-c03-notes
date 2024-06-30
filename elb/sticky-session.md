# Sticky Sessions

- Sticky sessions are a method to ensure that the same client is always redirected to the same instance behind a load balancer. This is useful for ensuring a user doesn't lose their session data.

- This feature is available for Classic Load Balancer, Application Load Balancer, and Network Load balancer.

- The cookie used for stickiness has an expiration date that you can control.

- However, enabling stickiness may lead to an imbalance in the load over the backend EC2 instances.

## Cookie Names

There are two types of cookies: Application-based and Duration-based.

### Application-based Cookies

- **Custom cookie**: Generated by the target and can include any custom attributes required by the application. The cookie name must be specified individually for each target group. Don't use AWSALB, AWSALBAPP or AWSALBTG as they are reserved for use by AWS.

- **Application cookie**: Generated by the load balancer. The cookie name is AWSALBAPP.

### Duration-based Cookies

- These cookies are generated by the load balancer. The cookie name is AWSALB for ALB, AWSELB for CLB.