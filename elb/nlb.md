# Network load balancer (v2)

- Network load balancers (Layer 4) allow to
Forward TCP & UDP traffic to your instances.
Handle millions of request per seconds
Less latency ~100 ms(vs 400 ms for ALB)

- NLB has one static IP per AZ, and supports assigning Elastic IP (helpful for whitelisting specific IP).
NLB are used for extreme performance, TCP or UDP traffic.
Not included in AWS free tier

![img.png](../z_resources/images/elb/nlb.png)