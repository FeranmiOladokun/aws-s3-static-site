http://feranmis3website001.s3-website.eu-north-1.amazonaws.com

# AWS S3 Static Website

My first static website hosted on AWS S3, as part of my hands-on AWS learning journey 
(just passed AWS Certified Cloud Practitioner, now working toward Solutions Architect Associate).

## What I built
A simple static website hosted on Amazon S3 using its static website hosting feature.

## What tripped me up
After uploading my files and turning on static website hosting, the site still wouldn't load — even after unchecking "Block all public access" on the bucket.

Turns out unchecking that setting isn't enough on its own — it just *allows* the bucket to be made public, it doesn't actually make it public.
 I had to also add a bucket policy to actually grant public read access before the site worked. Once I did that, the site finally loaded.

Still learning exactly how S3 permissions work under the hood, but this was a good first lesson in the difference between "allowing" public access vs actually "granting" it.

## Next steps
- Connect this to GitHub Actions so updates deploy automatically.
