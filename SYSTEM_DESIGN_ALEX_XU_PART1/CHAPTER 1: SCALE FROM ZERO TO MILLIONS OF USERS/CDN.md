#### Content Delivery Network (CDN):

**CDN:**  Network of geographically dispersed servers used to deilver static content like images,videos, CSS, Javascript files etc.,

**How CDN works at a high level?** 
when users visit a website, a CDN server closest to the user will deliver static content.
For eg: If CDN servers are in San Francisco, the users in Los Angeles will get content faster when compared to the users in Europe.

![alt text](CDNworflow.png)


![alt text](CDNworkflow2.png)

**CDN Workflow:**
1. User A tries to get image.png using image URL.
URL's domain is provided by CDN provider, Below are the two sample image URLs look like on Amazon and Akamai CDNs:
• https://mysite.cloudfront.net/logo.jpg
• https://mysite.akamai.com/image-manager/img/logo.jpg

2. CDN server does not have image.png in cache, it requests the file from the origin, (web server or online storage like Amazon S3).
3. The origin returns the image.png to CDN server, which included optional HTTP header Time-to-Live (TTL) which describes how long the image is cached.
4. The CDN caches the images and return it to the user A. The image remains cached in the CDN until the TTL expires.
5. User B sends a request to get the same image.
6. The image is returned by CDN as long as the TTL is not expired. 


**Considerations of using a CDN:**
* Cost: CDNs are run by third party providers, and you are charged for data transfers in and out of the CDN. Caching infrequently used assest provides no longer benefits, consider moving them out of CDN network.
  
* Appropriate Cache Expiry: For time-sensitive content, setting time expiry is important.
                            The cache expiry time should neither be long nor too short. 
* CDN fallback: 
* Invalid
