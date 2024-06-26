# Elastic Network Interface (ENI)

An ENI is a logical component within a VPC that represents a virtual network card. It can have the following attributes:

- Primary private IPv4, one or more secondary IPv4
- One Elastic IP (IPv4) per private IPv4
- One public IPv4 Elastic IP
- One or more security groups
- A MAC address

ENIs can be created independently and attached on the fly (or moved) to EC2 instances for failover. They are bound to a specific Availability Zone (AZ).

## Hibernate

Hibernate allows the in-memory (RAM) state of an instance to be preserved. This results in a much faster boot time as the OS is not stopped or restarted. Under the hood, the RAM state is written to a file in the root EBS volume.

Use cases for hibernation include long-running processes, saving the RAM state, and services that take time to initialize.

### Important Notes

- The instance's RAM size must be less than 150GB.
- Hibernation is not supported for bare metal instances.
- The root volume must be an EBS volume, encrypted, not an instance store, and large enough to store the RAM state.
- Hibernation is available for On-Demand, Reserved, and Spot instances.
- An instance cannot be hibernated for more than 60 days.

## EBS Snapshots

EBS Snapshots allow you to make a backup (snapshot) of your EBS volume at a specific point in time.