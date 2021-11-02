# Access Tiers

There are four types of access tiers available:

Premium Storage (preview): It provides high-performance hardware for data that is accessed frequently.

Hot storage: It is optimized for storing data that is accessed frequently.

Cool Storage: It is optimized for storing data that is infrequently accessed and stored for at least 30 days.

Archive Storage: It is optimized for storing files that are rarely accessed and stored for a minimum of 180 days with flexible latency needs (on the order of hours).
While a blob is in the Archive tier, it can't be read or modified. To read or download a blob in the Archive tier, you must first rehydrate it to an online tier, either Hot or Cool.

To move an existing blob to the Archive tier in the Azure portal, follow these steps:

Navigate to the blob's container.

Select the blob to archive.

Select the Change tier button.

Select Archive from the Access tier dropdown.

Select Save.

Archieve Storage is applied at the object level.

# Rehydrte a blob after archival
To read a blob that is in the Archive tier, you must first rehydrate the blob to an online tier (Hot or Cool) tier. You can rehydrate a blob in one of two ways:

By copying it to a new blob in the Hot or Cool tier with the Copy Blob operation. Microsoft recommends this option for most scenarios.
By changing its tier from Archive to Hot or Cool with the Set Blob Tier operation

