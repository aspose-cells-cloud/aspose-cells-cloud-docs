---
title: "Object Exists API – Check File/Folder Presence in Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Object Exists API – Verify File or Folder Presence in Aspose.Cells Cloud"
linktitle: "Object Exists"
type: docs
url: /object-exists/
keywords: "object exists, Aspose.Cells Cloud, storage API, file existence, Excel API"
description: "Use the Object Exists API to quickly verify whether a file or folder exists in Aspose.Cells Cloud storage. Supports optional storage name and version ID."
weight: 100
---

## **Excel API: Object Exists**

The **Object Exists API** lets developers determine whether a specific file or folder is present in Aspose.Cells Cloud storage. It returns a simple Boolean indicating existence and whether the path points to a folder.

### Web API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ is the full path to the file or folder in storage.

### Request Parameters

| Parameter Name | Type   | Location | Required | Description                                                         |
| -------------- | ------ | -------- | -------- | ------------------------------------------------------------------- |
| `path`         | string | Path     | Yes      | Full path to the file or folder.                                    |
| `storageName`  | string | Query    | No       | Name of the storage; defaults to the primary storage if omitted.    |
| `versionId`    | string | Query    | No       | Specific version identifier of the file (if versioning is enabled). |

### Response Codes

| Code | Meaning               | Description                                           |
| ---- | --------------------- | ----------------------------------------------------- |
| 200  | OK                    | The request succeeded; response body contains result. |
| 401  | Unauthorized          | Missing or invalid authentication token.              |
| 404  | Not Found             | The specified path does not exist.                    |
| 500  | Internal Server Error | An unexpected error occurred on the server.           |

### Response Description

A successful call returns a JSON payload with two properties:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true` if the file or folder exists; otherwise `false`.
- **IsFolder** – `true` when the path points to a folder; `false` for a file.

### Notes / Limitations

- Rate limits are applied per account; consult the **Rate Limits** page for exact values.
- If `storageName` is omitted, the default storage configured for the account is used.
- The API currently supports version 5.0; older version paths (`/v4.0/`) are deprecated.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ObjectExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ObjectExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ObjectExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ObjectExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ObjectExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ObjectExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ObjectExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ObjectExists.go" >}}
{{</tab>}}
{{< /tabs >}}
