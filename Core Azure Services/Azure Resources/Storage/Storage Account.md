# Azure Storage Account
An Azure Storage Account is a secure account, which provides you access to services in Azure Storage. The storage account is like an administrative container, and within that, we can have several services like blobs, files, queues, tables, disks, etc. And when we create a storage account in Azure, we will get the unique namespace for our storage resources. That unique namespace forms the part of the URL. The storage account name should be unique across all existing storage account name in Azure.

## Types of Storage Accounts
- General-purpose V2
Supported services : Blob, File, Queue, Table, and Disk
Supported performance tiers : Standard, Premium
Supported access tiers : Hot, Cool, Archive
Replication options : LRS, ZRS, GRS, RA-GRS
Encryption : True

- General-purpose V1
Supported services : Blob, File, Queue, Table, and Disk
Supported performance tiers : Standard, Premium
Supported access tiers : N/A
Replication options : LRS, GRS, RA-GRS
Encryption : True

- Blob Storage
Supported services : Blob (block blobs and append blobs only)
Supported performance tiers : Standard
Supported access tiers : N/A
Replication options : LRS, GRS, RA-GRS
Encryption : True



## Replication Options
### Locally redundant storage (LRS)
It helps to replicate our data in the same data center, and it is a low-cost data redundancy technique. LRS is the lowest-cost replication option and offers the least durability compared to other options. It provides at least 99.999999999% (11 nines) durability of objects over a given year.

This is helpful when we can easily reconstruct the data in case of data loss, or we have restricted data to replicate only within the country/region.

### Zone-redundant storage (ZRS)
It helps us for excellent performance, low latency and replicate our data synchronously across three storage clusters in a single region. Each storage cluster is physically separated but within the same region. ZRS offers durability for storage objects of at least 99.9999999999% (12 9's) over a given year.

### Geo-redundant storage (GRS)
As I explained above it helps us in replicating our data to another region which is far away hundreds of miles away from the primary region. It provides at least 99.99999999999999% (16 9's) durability of objects over a given year. GRS replicates our data to another region, but data will be available to be read-only if Microsoft initiates a failure from primary to the secondary region.

### Read-access geo-redundant storage (RA-GRS)
It is based on the GRS, but it also provides an option to read from the secondary region, regardless of whether Microsoft initiates a failover from the primary to the secondary region.

Migrating to or from LRS, GRS, and RA-GRS is straightforward – we can use the Azure portal or the Storage Resource Provider API to change your account's redundancy type.


## Types of performance tiers

Standard performance: This tier is backed by magnetic drives and provides low cost/GB. They are best for applications that are best for bulk storage or infrequently accessed data.

Premium storage performance: This tier is backed by solid-state drives and offers consistency and low latency performance. They can only be used with Azure virtual machine disks, and are best for I/O intensive workload such as the database.

(So every virtual machine disk will be stored on a storage account. So, if we are associating a disk, then we will go for the premium storage. But if we are using storage account specifically to store blobs, then we will go for standard performance.)

## Storage account endpoints

Whenever we create a storage account, we will get an endpoint to access the data within the storage account. So each object that we stored in Azurestorage has an address, which includes your unique account name and the combination of an account name, and service endpoint, which forms the endpoint for your storage account.

For example, if your general-purpose account name is mystorageaccount then generally the default endpoints for different services looks like:

Azure Blob storage: http://mystorageaccount.blob.core.windows.net.

Azure Table storage: http://mystorageaccount.table.core.windows.net

Azure Queues storage: http://mystorageaccount.queue.core.windows.net


Azure files: http://mystorageaccount.file.core.windows.net

