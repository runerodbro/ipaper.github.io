---
permalink: /technical-information/upload-troubleshooting
title: Upload Troubleshooting
redirect_from: "/display/DOC/Upload+Troubleshooting"
summary: This section contains techincal information about troubleshooting upload issues from iPaper
---

## Problem

When uploading files to the media library, the files are uploaded directly from the client to Amazon Web Services. However, under some circumstances it may not possible to upload directly from client to Amazon, due to some restrictions on CORS requests. In these cases, we fallback to an upload method where our server acts as a streaming proxy.

If your oganizations users have experiences that the uploads are slow, or that the uploads hangs at 99%, it could be a symptom that our fallback upload method is being used.

## CORS OPTIONS Request

Whenever the browser has to perform a multipart upload, it initially makes a pre-flight OPTIONS request to Amazon. Some VPNs, Firewalls or Proxy servers may have security settings enabled, that block theese requests - This results in our fallback proxy being used. In order to experience faster uploads, OPTIONS requests may not be blocked.

### Known software to cause issues
* Cisco AnyConnect VPN, with WebSecurity Module installed.

### OPTION Request
The options request sent by the browser before initiating upload, may look something like this:

```
OPTIONS http://s3-eu-west-1.amazonaws.com/ipaper.partnerdata/ HTTP/1.1
Host: s3-eu-west-1.amazonaws.com
Connection: keep-alive
Access-Control-Request-Method: POST
Origin: http://ipaper.admin.ipapercms.dk
User-Agent: Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.71 Safari/537.36
Access-Control-Request-Headers: content-type
Accept: */*
Referer: http://ipaper.admin.ipapercms.dk/Sys/Modules/Media/
Accept-Encoding: gzip, deflate, sdch
Accept-Language: da-DK,da;q=0.8,en-US;q=0.6,en;q=0.4

HTTP/1.1 200 OK
x-amz-id-2: o8iLf+kwn8J8sQOMBk+EA6drRY4Zf7CcFzw2V3lDmgiXqwyUJjgOGizoZPzLEVQ8dnrg+2MhOjs=
x-amz-request-id: 640A3666D29EB454
Date: Thu, 04 Dec 2014 12:31:42 GMT
Access-Control-Allow-Origin: *
Access-Control-Allow-Methods: GET, POST, PUT
Access-Control-Allow-Headers: content-type
Access-Control-Max-Age: 3000
Vary: Origin, Access-Control-Request-Headers, Access-Control-Request-Method
Content-Length: 0
Server: AmazonS3
```