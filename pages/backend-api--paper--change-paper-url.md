---
title: Paper.ChangePaperUrl
permalink: /backend-api/paper/change-paper-url
redirect_from: "/display/DOC/ChangePaperUrl"
---

## Description

Changes a papers URL.

## Parameters

| Name    | Value
|---------|---------------------------------------------------
| paperID | The ID of the iPaper whose URL should be changed
| newUrl  | The new relative URL of the iPaper. Must be unique

## Sample Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<result>
  <code><![CDATA[SUCCESS]]></code>
  <message><![CDATA[Url changed.]]></message>
</result>
```

## Return Codes

* SUCCESS
* ERROR
* READONLY