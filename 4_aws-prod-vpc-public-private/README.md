# AWS PROJECT

### Overview
VPC with private and public subnets with two availability zones in production
Each public subnet contains a NAT gateway and laod balancer node.
The servers run in private subnets, are launched and terminated by using an AutoScaling group(making replicas to handle burden etc.),
and recieve traffic from load balancer(sending requests to mange traffic).
Servers connect to internet using NAT gateway.

### Let's Start the Project
