<!-- TITLE: Andy's S3 Notes -->
<!-- SUBTITLE: These are notes from  a udemy course Andy is taking -->

# S3 101

**S3** - Simple Storage Service

S3 is a safe place to store files. It is Object-based storage. You can store pdf's, images, text files, etc

## S3 Basics
* S3 is Object based - (in other words, it allows you to upload files)
* Files can be from 0 Bytes to 5TB
* There is unlimited storage
* Files are stored in Buckets 
* Bucket is a folder inside the cloud that has a universal namespace (it will have a DNS address)
* Bucket name -> https://s3-eu-west-1.amazonaws.com/bucketname
* You receive a HTTP 200 code when an upload is successful

### Data Consistancy model For S3
* Read after Write consistancy for PUTS of new Objects
    * Wehn you upload a new file you are able to read that file immidiately
* Eventual Conisstancy for overwrite PUTS and DELETES (can take some time to propagate)
    * If you update or delete a file you may get the new version or the old version, but eventually the file will be consistant

### S3 is a simple key-value store

* In S3, Objects consist of
    * Key - The name of the object
    * Value - the data and is made up of a sequence of bytes
    * Version ID
    * Metadata
    * Subresources:
        * Access control lists
        * Torrent - If you want to torrent the file
### More about S3
* Built for 99.99% availablity for the S3 platform
* Amazon guarentee of 99.9% availability - service level agreement
* Amazon guarentees 99.999999999% durability for S3 information
* Tiered Storage Available
* Lifecycle Management - Rotate to archive
* Versioning
* Encryption
* Secure your data using Access control lists and bucket policies

### S3 Storage Tiers/Classes
* S3 Standard: 
    * 99.99% availabilty 
    * 99.999999999% durability
    * stored redundantly across multiple devices in multiple facilities
    * Designed to sustain the loss of 2 facilities concurrently
    * No retrieval fee
* S3 - IA (Infrequently Accessed):
    *  For data accessed infrequently but  requires rapid access when needed. 
    *  Lower fee
    *  Charged for retrieval
*  S3 One Zone - IA
    *  Lower-cost than  IA
    *  Similar to regular IA but only stored in one Availablity Zone
*  Glacier - Reduced Redundancy 
    * Very cheap and meant for archival storage.
    *  Three models
        *  Expedidited - restored within in a few minutes
        *  Standard - restored in 3 - 5 hours
        *  Bulk - restored in 5 -12 hours

### S3 Charges
* Charged for 
    * Storage
    * Requests
    * Storage management pricing - Being charged for metadata tags
    * Data transfer pricing
    * Transfer Acceleration
        * Enables fast, easy, and secure transfers of files over long distances between your end users and an S3 bucket
        * Transfer Acceleration takes advantage of CloudFront's (Amazon CDM netword) globally distributed edge locations. 

Checkout the S3 FAQ before exam [here](https://aws.amazon.com/s3/faqs/)

# Create and S3 Bucket - Lab Notes
* S3 Buckets are managed at a Global level
* Objects in buckets don't inherite tags of the bucket itself
* Encrption
    * Client side Encryption
    * Server side Encryption
        * Server side encrpytion with Amazon S3 Managed Keys (SSE-S3)
        * Server side encryption with KMS (SSE-KMS)
        * Server side encryption with Customer Provided Keys (SSE-C)
        * Control access to buckets using either a bucket ACL or using Bucket policies
* **By default buckets are private and all objects stored inside them are private**
 
# Version Control - Lab Notes
* You cannot disable versioning once you enable it, you can only suspend it
* You should take time to consider whether you want to enable  versioning because each version will be kept as it's own individual object, which can become pricey
* Great backup tool
* Integrates with Lifecycle rules
* Versioning's MFA Delete capability, which uses multi-factor authentication, can be used to provide extra security