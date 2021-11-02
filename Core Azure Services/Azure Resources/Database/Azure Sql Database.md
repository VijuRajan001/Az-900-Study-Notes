# Azure Sql Database

Azure SQL is a family of managed, secure, and intelligent products that use the SQL Server database engine in the Azure cloud.

Azure SQL Database: Support modern cloud applications on an intelligent, managed database service, that includes serverless compute.
Azure SQL Managed Instance: Modernize your existing SQL Server applications at scale with an intelligent fully managed instance as a service, with almost 100% feature parity with the SQL Server database engine. Best for most migrations to the cloud.
SQL Server on Azure VMs: Lift-and-shift your SQL Server workloads with ease and maintain 100% SQL Server compatibility and operating system-level access.

In Azure, you can have your SQL Server workloads running as a hosted service (PaaS), or a hosted infrastructure (IaaS). Within PaaS, you have multiple product options, and service tiers within each option. The key question that you need to ask when deciding between PaaS or IaaS is do you want to manage your database, apply patches, and take backups, or do you want to delegate these operations to Azure?

For both Azure SQL Database and Azure SQL Managed Instance, Microsoft provides an availability SLA of 99.99%. For the latest information, see Service-level agreement.

For SQL on Azure VM, Microsoft provides an availability SLA of 99.95%

# Azure SQL Database
Azure SQL Database is a relational database-as-a-service (DBaaS) hosted in Azure that falls into the industry category of Platform-as-a-Service (PaaS).

Best for modern cloud applications that want to use the latest stable SQL Server features and have time constraints in development and marketing.
A fully managed SQL Server database engine, based on the latest stable Enterprise Edition of SQL Server. SQL Database has two deployment options built on standardized hardware and software that is owned, hosted, and maintained by Microsoft.

You can use advanced query processing features, such as high-performance, in-memory technologies and intelligent query processing. In fact, the newest capabilities of SQL Server are released first to SQL Database, and then to SQL Server itself. You get the newest SQL Server capabilities, with no overhead for updates or upgrades, tested across millions of databases.

# Azure SQL Managed Instance
Azure SQL Managed Instance falls into the industry category of Platform-as-a-Service (PaaS), and is best for most migrations to the cloud. SQL Managed Instance is a collection of system and user databases with a shared set of resources that is lift-and-shift ready.

Best for new applications or existing on-premises applications that want to use the latest stable SQL Server features and that are migrated to the cloud with minimal changes. An instance of SQL Managed Instance is similar to an instance of the Microsoft SQL Server database engine offering shared resources for databases and additional instance-scoped features.
SQL Managed Instance supports database migration from on-premises with minimal to no database change. This option provides all of the PaaS benefits of Azure SQL Database but adds capabilities that were previously only available in SQL Server VMs. This includes a native virtual network and near 100% compatibility with on-premises SQL Server. Instances of SQL Managed Instance provide full SQL Server access and feature compatibility for migrating SQL Servers to Azure.

Azure SQL Database and Azure SQL Managed Instance offer many of the same features; however, Azure SQL Managed Instance provides several options that might not be available to Azure SQL Database. For example, Tailwind Traders currently uses several on-premises servers running SQL Server, and they would like to migrate their existing databases to a SQL database running in the cloud. However, several of their databases use Cyrillic characters for collation. In this scenario, Tailwind Traders should migrate their databases to an Azure SQL Managed Instance, since Azure SQL Database only uses the default SQL_Latin1_General_CP1_CI_AS server collation.

# SQL Server on Azure VM
SQL Server on Azure VM falls into the industry category Infrastructure-as-a-Service (IaaS) and allows you to run SQL Server inside a fully managed virtual machine (VM) in Azure.

SQL Server installed and hosted in the cloud runs on Windows Server or Linux virtual machines running on Azure, also known as an infrastructure as a service (IaaS). SQL virtual machines are a good option for migrating on-premises SQL Server databases and applications without any database change.
Best for migrations and applications requiring OS-level access. SQL virtual machines in Azure are lift-and-shift ready for existing applications that require fast migration to the cloud with minimal changes or no changes. SQL virtual machines offer full administrative control over the SQL Server instance and underlying OS for migration to Azure.

Optimized for migrating existing applications to Azure or extending existing on-premises applications to the cloud in hybrid deployments. In addition, you can use SQL Server in a virtual machine to develop and test traditional SQL Server applications. With SQL virtual machines
