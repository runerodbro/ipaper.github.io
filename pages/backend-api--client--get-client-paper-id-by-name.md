---
title: Client.GetClientPaperIDByName
permalink: /backend-api/client/get-client-paper-id-by-name
redirect_from: "/display/DOC/GetClientPaperIDByName"
---

## Description
Creates a new premium client in the partner solution.

## Parameters

| Name       | Values
|------------|---------------------------------------------------------------------------
| clientName | The name of the client whose PaperID to retrieve


## Sample Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<result>
  <code><![CDATA[SUCCESS]]></code>
  <message><![CDATA[Client found.]]></message>
  <data>
    <paperID id="4899" />
  </data>
</result>
```

## Return Codes

* SUCCESS
* ERROR
* CLIENT_UNKNOWN
* LOGIN_SECURITY_VIOLATION