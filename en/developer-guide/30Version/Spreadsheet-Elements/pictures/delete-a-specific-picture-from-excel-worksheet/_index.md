---
title: "Delete a Picture from an Excel Worksheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud API, delete picture, Excel worksheet, REST"
description: "Delete a picture from an Excel worksheet using Aspose.Cells Cloud REST API. Learn the DELETE endpoint, required parameters, authentication, error codes, and example code."
weight: 50
---

This REST API deletes a picture from an Excel worksheet.

## Prerequisites

* Aspose.Cells Cloud API version **v3.0** (or later).  
* A workbook must already be uploaded to your Aspose Cloud storage.  
* The picture you want to delete can be identified with the **Get all pictures** operation to obtain its zero‑based `pictureIndex`.  

## Authentication

To call any Aspose.Cells Cloud endpoint you need a valid **JWT access token**.  
Obtain the token by sending an OAuth 2.0 request with your client‑id and client‑secret:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

The response contains an `access_token` field. Use this token in the `Authorization` header of subsequent API calls:

```
Authorization: Bearer <access_token>
```

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Request Parameters

| Parameter Name | Type    | Location | Required | Description                                            |
|----------------|---------|----------|----------|--------------------------------------------------------|
| name           | string  | path     | Yes      | The name of the workbook file.                         |
| sheetName      | string  | path     | Yes      | The name of the worksheet that contains the picture.  |
| pictureIndex   | integer | path     | Yes      | The zero‑based index of the picture to be deleted.    |
| folder         | string  | query    | No       | The folder where the workbook is stored.               |
| storageName    | string  | query    | No       | The name of the storage service (optional).           |

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make the call with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Error Handling

| HTTP Code | Meaning                              | Sample Error Payload |
|-----------|--------------------------------------|----------------------|
| 200       | Picture deleted successfully.        | `{ "Code": 200, "Status": "OK" }` |
| 400       | Bad request – invalid parameters.   | `{ "Code": 400, "Message": "Invalid pictureIndex." }` |
| 401       | Unauthorized – missing/invalid token.| `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| 404       | Not found – workbook, worksheet, or picture does not exist. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500       | Internal server error.               | `{ "Code": 500, "Message": "Unexpected server error." }` |

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Conclusion & See Also

You have learned how to delete a specific picture from an Excel worksheet using the Aspose.Cells Cloud REST API, including authentication, required parameters, possible error responses, and sample code.  

**Next steps**

* **Add a picture** – see the *Add a picture* documentation.  
* **Update a picture** – see the *Update a picture* documentation.  
* **Clear all pictures** – see the *Clear all pictures* documentation.  

---  

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How do I delete a specific picture from an Excel worksheet using Aspose.Cells Cloud?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Send a DELETE request to `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}` with a valid JWT token. Replace `{name}`, `{sheetName}` and the zero‑based `{pictureIndex}` with your workbook name, worksheet name, and picture index respectively."
      }
    },
    {
      "@type": "Question",
      "name": "What HTTP status codes can I expect when deleting a picture, and what do they mean?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "200 OK – picture deleted successfully.<br>400 Bad Request – invalid parameters.<br>401 Unauthorized – missing or invalid JWT token.<br>404 Not Found – workbook, worksheet, or picture does not exist.<br>500 Internal Server Error – server‑side problem."
      }
    },
    {
      "@type": "Question",
      "name": "Do I need to specify the storage name when deleting a picture?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`storageName` is optional; if omitted, the default storage configured for your Aspose Cloud account is used."
      }
    }
  ]
}
</script>