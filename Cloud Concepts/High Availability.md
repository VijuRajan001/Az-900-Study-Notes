# High Availability

High availability is a characteristic of your application which specifies certain level of operational performance and uptime for your application for a certain period.

- Usually defined in terms of percentage (99% availability | 99.9% availability) etc

## Events which can cause unavailability
1. Planned Maintenance
2. Unplanned Maintenance
3. Unexpected downtimes

## How does azure help you make systems highly available ?

- Many azure services come with published SLA's. Such as azure functions, app service, azure ad refer [Azure SLA summary](https://azure.microsoft.com/en-in/support/legal/sla/summary/) 

- You can use azure to replicate your services across availability zones or region pairs

## How to calculate availability of your system ?

- To calculate availability of your solution in azure you need to know which components are in a critical path of your system. 

- For Example: 
  Single Instance of Solution: 
  You solution uses App Service (99.95% availability) and Sql Database ( 99.99% availability)
  Total Availability  = 99.95 * 99.99 
                      = 99.94 %

  Parallel Instances of Solution :
  Suppose you have two instances of your solution in primary and secondary region   

  Total Availability = 1 - (Probability of Service not available in primary) * (Probabily of service not availble in secondary)

  Probability of Service not available = 1 - (probability of service being available)

  Total Availability = 1 - (1- 99.94%)*(1-99.94%)
                     = 1 - (0.06)(0.06)
                     = 1 - 0.0036
                     = 99.9964%

## Azure Core Services their Availability

| Service                               |  Availability         |
|:--------                              |:---------:            |
|  VM + Premium SSD                     |          99.9%        | 
|  VM + Standard SSD                    |          99.9%        |
|  VMs + avilability set                |          99.95%       |
|  VMs + avilability Zone               |          99.99%       |    
|  App Services                         |          99.95%       |
|  App Services  Free Tier              |          No SLA       |
|  App Services shared Tier             |          No SLA       |
|  Container Instances                  |          99.9%        |
|  Kubernetes Services                  |          99.9%        |
|  Kubernetes Services + Az             |          99.95%       |
|  Functions                            |          99.95%       |
|  Virtual Desktops                     |          99.9%        |
|  Virtual Network                      |          No SLA       |
|  Load Balancer                        |          99.99%       |
|  VPN Gateway                          |          99.9%        |
|  Express Route                        |          99.9%        |
|  Application Gateway                  |          99.95%       |
|  CDN                                  |          99.9%        |
|  Managed Disk                         |          No SLA       |
|  Blob, File, Storage Account          | Hot-99.99%,Cool-99.9% |
|  Cosmos,sql,mysql,sql managed         |         99.99%        |

## Availability Metrics
 - Percentage of uptime
 - Mean time to recover
 - Mean time between failures
 - Recovery Time objective
 - Recovery Point objective



 ## How to make VM's Highly Available
 1. Deploy VM's To an availability set
 2. Group Simailar VM's to scale sets
 3. Deploy azure vm's to region pairs 

 ## What is Availability Set? 
 When we put VM's in an availability set. They are distributed across hardware which is n/w isolated, power isolated from each other.

 This is done by using fault domains and update domains






