# Azure Load Balancer

Load balancing is when you evenly distribute load across a group of backend resources. 

Azure load balancer operates at layer 4 of the OSI model. As the point of contact for clients,
traffic arrives at the front end of the load balancer and is distributed to the backend based
on rules and metrics.

## Public load balancers
Public load balancers balance traffic from the internet to your VMs or other resources.
This is done by translating private IP addresses to public IPs. The IP address of
your load balancer determines if it's public or private.

## Private/Internal load balancers
Internal load balancers are used when private IP addresses are going to be hitting
the front end of the load balancer. This is so that traffic on your internal network can be evenly
distributed across the backend.

## Backend pool
The backend pool is the group of VMs or instances in VM scale sets that are receiving traffic
from the load balancer. Scaling instances up or down causes the load balancer to automatically
adjust itself without any additional input from you.

Sources:
- https://learn.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
- https://learn.microsoft.com/en-us/azure/load-balancer/components