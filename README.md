# Launch Your First Website using AWS S3

This is a continuation on the [previous S3 project](https://github.com/hann-cyber/AWS-S3-Bucket), where I illustrate how I deployed a static webpage on AWS S3, with versioning.

1. First, I'm going to upload an index page. It's just crude html, for a basic example, and calls one of the images to the landing page.

<p align="center">
 <img src="https://i.imgur.com/7oyXGNk.png">
</p>

S3 automatically detects index pages and provides a publicly accessible link.

<p align="center">
 <img src="https://i.imgur.com/ZlkBXHa.png">
</p>

2. Navigate to the webpage:

When navigating to the provided link, you'll notice my landing page with an image of my summer hobby.

<p align="center">
 <img src="https://i.imgur.com/LSVXPP6.png">
</p>

When inspecting the image location you'll notice the myBBQ.png from earlier.

<p align="center">
 <img src="https://i.imgur.com/VHX54ff.png">
</p>

Even though its not displayed on the webpage, if someone knows other common file names they could potentially navigate to them.

<p align="center">
 <img src="https://i.imgur.com/cOR8huj.png">
</p>

3. Versioning

Another optional key feature of S3 is versioning. Since I'll be using it in the next writeup I'll go over it here, briefly.

Navigating to the properties tab versioning is disabled by default, which can be enabled by hitting the edit button.

<p align="center">
 <img src="https://i.imgur.com/3h2f3PO.png">
</p>

Once versioning is enabled, it can be verified by seeing the "Show Versions" button within the S3 Bucket. In the following example I reuploaded a modified index.html page with new content. Note: there's now a version ID however, all version IDs will be listed as "Null" if versioning was not enabled prior to uploading files.

<p align="center">
 <img src="https://i.imgur.com/thqUGWO.png">
</p>

When navigating to the same link, or refreshing the page, the landing page is instantly adjusted to show the updated content.

<p align="center">
 <img src="https://i.imgur.com/asRdgeb.png">
</p>

A good reason for versioning is that you can rollback to previous versions of content you had recently updated within a bucket. But, versioning is also required for other features, which you can read about in my [next project](http://github.com/hann-cyber/AWS-S3-Replication) on replication!
