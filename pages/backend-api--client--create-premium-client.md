---
title: Client.CreatePremiumClient
permalink: /backend-api/client/create-premium-client
redirect_from: "/display/DOC/CreatePremiumClient"
---

## Description
Creates a new premium client in the partner solution.

## Parameters

| Name       | Values
|------------|---------------------------------------------------------------------------
| clientName | The name of the client to update. Must be unique across all license types


## Sample Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<result>
  <code><![CDATA[SUCCESS]]></code>
  <message><![CDATA[Client created.]]></message>
  <data>
    <paperID id="4905" />
  </data>
</result>
```

## Return Codes

* SUCCESS
* ERROR
* READONLY
* LOGIN_SECURITY_VIOLATION