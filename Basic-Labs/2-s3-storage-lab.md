# S3 Storage

- **Objective**: To gain hands-on experience with Amazon S3 by performing basic storage operations.
- **Approach**: This lab involves creating an S3 bucket, uploading files to it, and setting up bucket policies for access control. Students will explore the S3 management console, learn about object storage, and understand the concepts of buckets and objects.
- **Goal**: Students will understand how to use S3 for storing and managing data, learn about S3 security and permissions, and become familiar with S3's user interface.



## Amazon S3 (Simple Storage Service)

- Amazon S3 is `highly scalable` and widely used `object storeage service.`

- What objects in S3 can be:
    - `Files`
        - text,images,videos,audio files,PDFs,Words,SpreadSheets etc
    - `Databases`
        - Backups or snapshots of databases can be stored as objects in S3
    - `Logs`
    - `Static Website Content`
        - S3 is commonly used to host static website content.
    - `Containers and Images`
        - Container images for services like Docker can be stored in S3.

- S3 is designed to store and retrieve any amount of data from anywhere on the web.

- S3 is an object storage service,meaning it stores data as objects.
    - Each object consists of data, a unique key and metadata.

- S3 stores data as objects in resources that are called `Bucket`.
    - `Bucket` is a fundamental container for storing and organizing objects.
    - It is a top-level container with a `globally unique name ` within the S3 service.

![storage4](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/3ac70579-6a7b-4b94-a718-ad7153604adf)


- `path-style` url endpoint is normally used when you need to access objects
- `virtual-hosted-style` url endpoint is used when you are using `bucket as a website` for static data.


- Access the data anywhere thru
    - `aws management console`
    - `aws command line interface`
    - `sdk`



## Lab Task

- Create a s3 bucket
#img1

- Bucket created
#img2

- upload a file

#img3


- **changing permission for public access of bucket objects**

- first change the **`block all public access`** `off`
#img4

- then add `bucket policy` so that we can `read` the bucket object `publically`
#img5

- now we can see that object is accessiable thru `object URL`
#img 6


