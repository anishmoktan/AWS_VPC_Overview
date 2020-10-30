# AWS_VPC_Overview

Amazon Virtual Private Cloud (VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles traditional network that you'd operate in your own data center but with the benefits of using scalable infrastructure of AWS. 

There are three types of IP address in AWS. A private IP address that's not reachable over the Internet and is used for communication between instances in the same network. A public IP address that is reachable from the internet, which you can use for communication between your instances and the internet. And finally, an elastic IP address this is a static public persistent IP address that persists after an instance restarts whereas a public IP address is risked associated after each restart. 

Amazon defines a subnet as a range of IP addresses in your VPC. You can launch AWS resources into a subnet, which is always mapped to a single availability zone. We use a public subnet resources that must be connected to the internet and a private subnet for resources that won't be connected to the Internet. To allow your VPC the ability to connect to the internet you need to attach an Internet gateway, which only one Internet gateway can exist per VPC. 

A route table determines where network traffic is directed. It defines a set of rules every subnet has to be associated with a root table and a subnet can only have an association with one root table, however, multiple subnets can be associated to the same root table. 

You can use a NAT device to enable instances in a private subnet to connect to the internet or other AWS services, but that device will prevent the internet from initiating connections with instances inside your private subnet. 

Security group acts as a virtual firewall that controls the traffic for one or more instances. You add rules to each security group that allow traffic to or from its associated instances.  

A network access control list (network ACL) is an optional layer of security for a VPC that acts as a firewall for controlling traffic in and out of one or more of your subnets.

