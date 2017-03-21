---
title: Client.AddModule
permalink: /backend-api/client/add-module
redirect_from: "/display/DOC/AddModule"
---

## Description
Adds a module to an existing client.

## Parameters
<table>
	<thead>
		<td><strong>Name</strong></td>
		<td><strong>Value</strong></td>
	</thead>
	<tbody>
		<tr>
			<td>clientName</td>
			<td>The name of the client to update.</td>
		</tr>
		<tr>
			<td>moduleName</td>
			<td>
				The modules to add. Valid modules are:
				<ul>
					<li>API</li>
					<li>CollabNotes</li>
					<li>CustomDomain</li>
					<li>CustomLanguage</li>
					<li>CustomLinkImport</li>
					<li>ExtendedSearch</li>
					<li>FilePublisher</li>
					<li>Forms</li>
					<li>FrontendBuilder</li>
					<li>Globase</li>
					<li>IPFilter</li>
					<li>LinkImport</li>
					<li>Links</li>
					<li>LocationMonitor</li>
					<li>OfflinePaper</li>
					<li>Password</li>
					<li>RemoteAuthentication</li>
					<li>Shop</li>
					<li>SimpleUpload</li>
					<li>Templates</li>
					<li>UserEventTracking</li>
					<li>UsersAndGroups</li>
				</ul>
			</td>
		</tr>
	</tbody>
</table>

## Sample Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<result>
  <code><![CDATA[SUCCESS]]></code>
  <message><![CDATA[Module added.]]></message>
</result>
```


## Return Codes

* SUCCESS
* ERROR
* READONLY
* CLIENT_ALREADY_HAS_MODULE
* CLIENT_UNKNOWN 