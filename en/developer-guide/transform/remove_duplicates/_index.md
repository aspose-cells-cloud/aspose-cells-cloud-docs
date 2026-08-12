---
title: "Remove Duplicates"
ArticleTitle: "Remove Duplicates – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Remove Duplicates"
type: docs
url: /cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Remove Duplicates, API"
description: "Removes duplicate values in a worksheet, range, or table."
weight: 1000
---

## The Remove Duplicates of Aspose.Cells Cloud Web Services

Removes duplicate values in the worksheet, range, or table. This method scans the target scope for rows with identical values in the specified columns to check. For each set of duplicates, all but the first occurrence are removed. The comparison is typically case‑sensitive and matches the exact cell value.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | File   | FormData                    | Upload spreadsheet file. |
| worksheet      | String | Query                       | The worksheet name. (optional) |
| range          | String | Query                       | Range name that need deduplication. (optional) |
| table          | String | Query                       | Table name that need deduplication. (optional) |
| outPath        | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query                       | Output file Storage Name. |
| region         | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Response**

```json
{
  "File": "binary stream of the resulting spreadsheet (e.g., .xlsx)"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The resulting spreadsheet with duplicates removed is returned as a file stream. |
| 400 | Bad Request | Invalid request parameters or malformed URL. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data or other server‑side error. |

## How to Use the Remove Duplicates with SDKs

### Remove Duplicates Specification

The [Remove Duplicates API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "binary stream of the resulting spreadsheet (e.g., .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low‑level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
```csharp
// SDK example code for C#
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// SDK example code for Java
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# SDK example code for Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception when calling TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`