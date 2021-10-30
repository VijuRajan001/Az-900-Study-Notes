# Azure Regions and Region Pairs

## Azure Regions
An Azure region is a set of datacentres, deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network.
A Region could be made up of just 1 dataceneter or multiple datacenters. 
Azure has 60+ regions and is available in 140+ countries

## Azure Region Pairs
An Azure Region Pair is a relationship between 2 Azure Regions within the same geographic region for disaster recovery purposes. If one of the regions were to experience a disaster or failure, then the services in that region will automatically failover to that regions secondary region in the pair. For example, North Central US region’s pair is South Central US.

Each Azure Region in a pair are always located greater than 300 miles apart when possible.

West India is paired to South India in one direction only. South India’s region pair is Central India.
Brazil South is paired (in one direction) with the South Central US region outside its geographic region. This is a unique region, as it’s the only one without a pair in the same geographic region.

When setting up services like SQL Database Geo-Replication and other services, the Azure Portal will guide you by telling you the “recommended” Azure Region to use as a secondary. 

Note that not all Azure services automatically replicate data, nor do all Azure services automatically fallback from a failed region to its pair. In such cases, recovery and replication must be configured by the customer.


## Benefits of Azure Region Pair

- Regional isolation
- Data Residency
- Microsoft will update a single region in the pair first. Then they will validate the update before moving on to the next region in the pair. By using Azure Region Pairs for replication and redundancy will ensure your applications and services are not adversely affected by a rare bad update event.
- In the event of a massive Azure outage, each Azure Region Pair has a single region that is prioritized over the other for recovery. Systems deployed across multiple Azure Regions within a pair are guaranteed to have an Azure Region that will be recovered with high priority.
- There are some services within Microsoft Azure that provide automatic geo-redundant storage. These services will do this by utilizing the paired region automatically.For example, when you provision an Azure Storage account and configure it for geo-replication then it will automatically use the region the Storage Account is provisioned in as the primary with replication to that regions secondary paired region without any additional configuration.


# Can I select my regional pairs?
No. Some Azure services rely upon regional pairs, such as Azure's redundant storage. These services don't allow you to create new regional pairings. Similarly, because Azure controls planned maintenance and recovery prioritization for regional pairs, you can't define your own regional pairs to take advantage of these services.

# Am I limited to using services within my regional pairs?
No. While a given Azure service may rely upon a regional pair, you can host your other services in any region that satisfies your business needs.

# Must I use Azure regional pairs?
No. Customers can leverage Azure services to architect a resilient service without relying on Azure's regional pairs. 

