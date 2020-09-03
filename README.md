[stack.yaml](stack.yaml) is the AWS CloudFormation stack template to deploy a high-availability static website whose files are stored at an S3 bucket. The VPC is established to have a pair of public subnets and a pair of private subnets. Each subnet in the pair resides on a separate Availability Zone for better availability. The stack deploys an Internet Gateway and two NAT Gateways. The Internet Gateway enables two-way communications between the VPC and the Internet. Each NAT Gateway resides in a public subnet and enables instances in a private subnet to connect to the Internet or other AWS services, but prevent the Internet from initiating a connection with those instances. Network communications between public subnets and the Internet, and between private subnets and public subnets, are regulated by route tables. Also, Security Group, Load Balancing, web server EC2 instances, Auto Scaling, IAM Roles and IAM Policies are all established in the stack template.

---

Final Output of LoadBalancerDNS: 

http://udaci-webap-s7j3hosxhxf9-545676656.us-east-2.elb.amazonaws.com/