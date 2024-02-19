# Hosting a Static Portfolio Website on S3

**Objective**: Learn to host a static website (such as a personal portfolio) on Amazon S3.

**Approach**:

1. **Create an S3 Bucket**: Start by creating a new S3 bucket. Configure the bucket for website hosting, which includes setting permissions to make the content publicly accessible.
2. **Upload Website Files**: Upload the static files of your portfolio website (HTML, CSS, JavaScript, images) to the S3 bucket.
3. **Configure DNS**: Use Amazon Route 53 or another DNS service to point a domain name to the S3 bucket. This makes the website accessible via a user-friendly URL.
4. **Enable Additional Features** (Optional): Implement features like HTTPS for secure access and CloudFront for content delivery optimization.

**Goal**: Students will understand how to use S3 for hosting static websites, manage bucket permissions, and integrate with other AWS services for a complete web hosting solution.


- **Let's Start**

- First , Create a bucket

#img1


- now, add bucket policies

#img2


- go to `properties` table and enable static hosting

#img3


- now let's upload our static file into s3 bucket

#img4

- now , if we one this url , we can see our hosted website

#img5

- **Our static Website**

#img6


- **Route 53 domain not accessiable in this account**

#img7