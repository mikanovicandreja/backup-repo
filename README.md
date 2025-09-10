This Pulumi Python program provisions an Amazon S3 bucket configured for static website hosting and automatically uploads all files from a specified local directory.

How it works:

Reads the siteDir configuration value, which points to your local static website files (HTML, CSS, JS, images, etc.).

Creates an S3 bucket with website hosting enabled, using index.html as the default entry point.

Iterates through every file in siteDir and uploads it to the S3 bucket with the correct MIME type (e.g., text/html, image/png).

Sets all uploaded objects to be publicly readable.

Exports:

Bucket name (bucket_name)

Website endpoint (bucket_endpoint), which is the public URL to access your site.

Use case:
This is a minimal example of deploying a static website to AWS S3 with Pulumi. It can serve as a foundation for more complex infrastructure setups (CDN integration, HTTPS via CloudFront, CI/CD automation, etc.).
