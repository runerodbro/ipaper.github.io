---
title: Custom Domain
permalink: /integration/custom-domain
redirect_from: "/display/DOC/Custom+Domain"
---

## Configuration

Before iPaper can setup the Custom Domain module, you need to setup the domain on your end first. The subdomain can be anything you want, but let's assume the following scenario:

```
Current catalog address: ipaper.ipapercms.dk
Main website: www.client.com
Subdomain: catalogs.client.com
```

In this case, catalogs.client.com needs to be setup as a CNAME record pointing to the partner address. That is, the following CNAME record should be made:

```
catalogs.client.com => ipaper.ipapercms.dk
```

If your catalogs are hosted through an iPaper partner, the CNAME alias should point to that specific partners address:

```
catalogs.client.com => ipaper.ipapercms.dk
```

{% include important.html content="The subdomain MUST be setup as a CNAME record. An A record will not work." %}

## Verification

To verify if the domain has been setup, you can use the following tool:
[http://network-tools.com/nslook/Default.asp?domain=publikationer.ipaper.dk&type=255&server=67.222.132.198&class=1&port=53&timeout=5000&go.x=-791&go.y=-257](http://network-tools.com/nslook/Default.asp?domain=publikationer.ipaper.dk&type=255&server=67.222.132.198&class=1&port=53&timeout=5000&go.x=-791&go.y=-257)

Replace "publikationer.ipaper.dk" with the desired subdomain. If the "Answer records" part looks like this, it indicates the CNAME record has been setup properly.

<img src="/images/nslookup.png" style="max-width: 100%; max-height: 100%" />