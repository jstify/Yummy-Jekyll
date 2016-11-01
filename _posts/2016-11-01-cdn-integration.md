---
layout: post
title: CDN Integration for Web Applications
category: Web Apps
tags: [CDN, CDN Integration, Web Application, Javascript]
---

To integrate CDN in web apps:
- We Need to prepend CDN url to all links in index.hmtl file, But **HTML and Images will be load from Main server not from CDN**
- We need to prepend CDN url to image url also if you want to load it CDN, **still images which are used in css will load from main server only**

https://www.maxcdn.com/one/tutorial/custom-cdn-integration/
http://hippocurious.com/setup-a-cdn-to-speed-up-your-website/

We need to make a lot of changes to load every thing from CDN if we going to prepend CDN to every url. 

If you are planning to load all files from CDN expect the service/ajax calls, we can implement in simple steps:
 
 **Step 1**
 Add CDN url to base tag in index.html. `ex: <base  href="cdn.url.com">`
 
**Step2**
Maintain Server URL in one variable and prepend to api when you are making ajax calls.
> ex:
> 
> var sererUrl = "www.mainurl.com";
> var apiName = "getData";
> $.get( sererUrl +apiName , function( data ) {
		> //success response
>});

**Note**: If you are using Angular and facing block listing issue, Please refer to [Secure Url](https://docs.angularjs.org/api/ng/provider/$sceDelegateProvider)
