# Availability zones
Azure availability zones are physically separate locations within each Azure region that are tolerant to local failures. Failures can range from software and hardware failures to events such as earthquakes, floods, and fires. Tolerance to failures is achieved because of redundancy and logical isolation of Azure services. To ensure resiliency, a minimum of three separate availability zones are present in all availability zone-enabled regions.

- Azure availability zones are connected by a high-performance network with a round-trip latency of less than 2 ms. They help your data stay synchronized and accessible when things go wrong.
- Each zone is composed of one or more datacenters equipped with independent power, cooling, and networking infrastructure. 
-Azure availability zones-enabled services are designed to provide the right level of resiliency and flexibility. They can be configured in two ways. They can be either zone redundant, with automatic replication across zones, or zonal, with instances pinned to a specific zone. You can also combine these approaches.

Azure services supporting Availability Zones fall into two categories: zonal and zone redundant. 

# Zonal architecture

With zonal architecture, a resource can be deployed to a specific, self-selected Availability Zone to achieve more stringent latency or performance requirements. Resiliency is self-architected by replicating applications and data to one or more zones within the region. You can choose specific Availability Zones for synchronous replication, providing high availability, or asynchronous replication, providing backup or cost advantage. You can pin resources-for example, virtual machines, managed disks, or standard IP addresses-to a specific zone, allowing for increased resilience by having one or more instances of resources spread across zones.

# Zone Redundant Arachitecture
With zone-redundant architecture, the Azure platform automatically replicates the resource and data across zones. Microsoft manages the delivery of high availability, since Azure automatically replicates and distributes instances within the region.