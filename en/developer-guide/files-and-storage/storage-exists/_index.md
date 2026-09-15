---
url: /storage-exists/
title: "Check if a Storage Exists – Aspose.Cells Cloud API (v4.0)"
date: 2024-05-10
lastmod: 2024-05-10
description: "Verify storage existence in Aspose.Cells Cloud via the GET /v4.0/cells/storage/{storageName}/exist endpoint. Includes REST, cURL, and SDK examples in C#, Java, Python, and Go."
keywords: ["storage exists API", "check storage exist", "Aspose.Cells Cloud storage", "REST API storage check", "cloud storage validation"]
type: docs
linktitle: "Storage Exists"
weight: 100
---

The `storageExists` API checks whether a specified storage container exists in the Aspose.Cells Cloud service. This health check is recommended before performing file-related operations to prevent runtime errors due to misconfigured or missing storage.

## Check Storage Existence (`storageExists` API)

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### Security and Authentication

Aspose.Cells Cloud APIs use [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Ensure a valid access token is included in the `Authorization` header.

### Request Parameters

| Parameter Name | Type   | Location | Description                                     |
| -------------- | ------ | -------- | ----------------------------------------------- |
| `storageName`  | String | Path     | The name of the storage to check for existence. |

### Response

The API returns a `StorageExist` object:

```json
{
  "Exists": true
}
```

**Field Description**

| Field   | Type    | Description                                      |
| ------- | ------- | ------------------------------------------------ |
| `Exists` | Boolean | `true` if the storage exists; otherwise, `false`. |

### HTTP Status Codes

| Code | Meaning               | Description                                       |
|------|-----------------------|---------------------------------------------------|
| 200  | OK                    | Request successful; storage status returned.     |
| 400  | Bad Request           | Missing or invalid `storageName` parameter.      |
| 401  | Unauthorized          | Invalid or missing JWT token.                    |
| 413  | Payload Too Large     | Request payload exceeds size limits.             |
| 500  | Internal Server Error | An unexpected error occurred on the server.      |

## Using the `storageExists` API

### cURL Example

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### SDK Examples

Using an SDK is the recommended approach for integrating with Aspose.Cells Cloud. SDKs handle authentication, request formatting, and response parsing automatically.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}

For full SDK documentation and source code, visit the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).

## OpenAPI Specification

The public REST interface for this operation is defined in the [Aspose.Cells Cloud OpenAPI Specification](https://reference.aspose.cloud/cells/#/StorageController/StorageExists). You can explore and test the endpoint directly in your browser.

## See Also

- [Managing Cloud Storage](/cells/cloud/storage-management/)
- [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)