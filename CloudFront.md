#### CloudFrount

It is a content delivery network (CDN).

Parts:
- Origin. This is the origin of all files that the CDN will distribute. It can be S3, EC2 instance, ELB or Route53.
- Distribution is the name of the CDN, two types:
    - Web distribution
    - RTMP Used for media streaming

**Edge location**

An Edge Location is a location where the content is cached. Not the same as an AZ.
Objects are cached for the life of the TTL
It is not just READ only, you can write to them too.
It is possible to clear cached objects by invalidating with an associated cost.

If you want to update your files frequently, AWS recommends that you primarily use file versioning because it enables you to control which file a request returns even when the user has a version cached either locally or behind a corporate caching proxy. If you invalidate the file, the user might continue to see the old version until it expires from those caches.