---
title: Client.CreateBasicClient
permalink: /backend-api/client/create-basic-client
redirect_from: "/display/DOC/CreateBasicClient"
---

## Description
Creates a new basic client in the partner solution.

## Parameters

| Name       | Values
|------------|--------------------------------------------------------------------------------
| clientName | The name of the client to update. Must be unique across all license types
| units      | The amount of processings to include in the license. Must be a positive number

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
* CLIENT_INVALID_UNIT_COUNT
* LOGIN_SECURITY_VIOLATION