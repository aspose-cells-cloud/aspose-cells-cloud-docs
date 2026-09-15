---
title: "Add Worksheet Comment (v3.1)"
url: /comments/add/
aliases: [/add-a-comment-to-a-cell-in-a-worksheet/]
description: "Add a comment to a specific cell in an Excel worksheet using Aspose.Cells Cloud REST API v3.1 (PUT /v3.1/cells/{name}/worksheets/{sheetName}/comments/{cellName}). Includes cURL, SDK examples, request/response schemas, and error handling."
keywords: "Aspose.Cells, Cloud API, Add Worksheet Comment, Excel, Spreadsheet, Cell Comment"
weight: 20
api_version: "v3.1"
date: 2024-05-15
---

# Add Worksheet Comment

Add a comment to a specific cell in a worksheet of an Excel workbook using the Aspose.Cells Cloud REST API.

> ⚠️ **Deprecated**: This page documents the v3.0 API. For the latest features, see [v3.1 documentation](https://docs.aspose.cloud/cells/#/Worksheets/PutWorksheetComment). As of 2024-05, v3.1 is the current stable version. While v3.0 remains functional, new features and improvements are only available in v3.1. We recommend upgrading.

---

## Prerequisites / Authentication

- A **Bearer JWT token** is required for every request.  
  _Obtain a token_ via the **/connect/token** endpoint (see the [Authentication guide]({{< relref "/cells/authentication/" >}})).
- Include the token in the `Authorization` header:

```http
Authorization: Bearer <jwt_token>
```

- All calls must be made over **HTTPS** to protect the token and data.

> 💡 **Tip**: Replace `<jwt_token>` with your actual JWT token. To generate one programmatically:
> ```bash
> TOKEN=$(curl -s -X POST "https://api.aspose.cloud/connect/token" \
>   -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>" \
>   | jq -r '.access_token')
> ```

---

## HTTP Request

```http
PUT https://api.aspose.cloud/v3.1/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Path Parameters

| Name        | Type   | Required | Description                                  |
| ----------- | ------ | -------- | -------------------------------------------- |
| `name`      | string | ✔️       | The workbook file name (e.g., `test.xlsx`).  |
| `sheetName` | string | ✔️       | The worksheet name (e.g., `Sheet1`).         |
| `cellName`  | string | ✔️       | The address of the target cell (e.g., `A1`). |

### Query Parameters

| Name          | Type   | Required | Description                                         |
| ------------- | ------ | -------- | --------------------------------------------------- |
| `folder`      | string | optional | The folder that contains the workbook.              |
| `storageName` | string | optional | The storage service name where the file is located. |

### Request Body

The body must contain a **Comment** object in JSON format.

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Comment Object Fields**

| Field                     | Type    | Required | Description                                            |
| ------------------------- | ------- | -------- | ------------------------------------------------------ |
| `CellName`                | string  | ✔️       | Cell address (must match the `{cellName}` path value). |
| `Author`                  | string  | optional | Name of the comment author.                            |
| `HtmlNote`                | string  | optional | HTML‑formatted comment text.                           |
| `Note`                    | string  | optional | Plain‑text comment.                                    |
| `AutoSize`                | boolean | optional | Auto‑size the comment box.                             |
| `IsVisible`               | boolean | optional | Show the comment by default.                           |
| `Width` / `Height`        | number  | optional | Size of the comment box (points).                      |
| `TextHorizontalAlignment` | string  | optional | Horizontal alignment (`Left`, `Center`, `Right`).      |
| `TextOrientationType`     | string  | optional | Text rotation (`NoRotation`, `Rotate90`, …).           |
| `TextVerticalAlignment`   | string  | optional | Vertical alignment (`Top`, `Center`, `Bottom`).        |

---

## cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.1/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## Response Schema

| Field     | Type    | Description                                                                           |
| --------- | ------- | ------------------------------------------------------------------------------------- |
| `Comment` | object  | The created comment object (see **Comment Object Fields** above, plus link metadata). |
| `Code`    | integer | HTTP status code returned by the API (e.g., `200`).                                   |
| `Status`  | string  | Textual status message (e.g., `"OK"`).                                                |

The `Comment` object also contains a **link** sub‑object:

| Sub‑field | Type   | Description                                  |
| --------- | ------ | -------------------------------------------- |
| `Href`    | string | Self‑reference URL for the comment resource. |
| `Rel`     | string | Relationship type (`self`).                  |
| `Title`   | string | Optional title (may be `null`).              |
| `Type`    | string | Optional MIME type (may be `null`).          |

---

## Successful Response Example

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Error Responses

| HTTP Code | Description                                                 | Example                                                                                                                                             |
| --------- | ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **400**   | Bad request – missing or invalid parameters.                | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | Unauthorized – token missing or invalid.                    | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }`                               |
| **404**   | Not found – workbook, worksheet, or cell does not exist.    | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }`                         |
| **500**   | Internal server error – unexpected condition on the server. | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }`                |

---

## SDK Examples

The following SDKs provide ready‑made wrappers for this operation. Replace placeholder values (`<YOUR_CLIENT_ID>`, `<YOUR_CLIENT_SECRET>`, etc.) with real data.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Configure API client
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Prepare comment object (PascalCase for C#)
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")  // Note: SDK uses camelCase internally despite class name PascalCase
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require("asposecellscloud");

let config = new Configuration();
config.clientId = "<your_client_id>";
config.clientSecret = "<your_client_secret>";

let api = new WorksheetsApi(config);

let comment = new Comment({
  cellName: "A1",  // camelCase for JS/Node.js
  author: "test",
  note: "this is a comment",
  htmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  autoSize: true,
  isVisible: true,
  width: 10,
  height: 10,
});

api
  .putWorksheetComment("test.xlsx", "Sheet1", "A1", comment)
  .then((response) => console.log(response))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    cell_name='A1',  # snake_case for Python
    author='test',
    note='this is a comment',
    html_note='<font style="font-weight:bold;">this is a comment</font>',
    auto_size=True,
    is_visible=True,
    width=10,
    height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
    } else {
        fmt.Printf("Response: %+v\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

> ⚠️ **Note**: Field names follow the SDK’s language-specific naming conventions:
> - C#/Java/Go: `CellName` (PascalCase)
> - JS/Python/Ruby/PHP/Perl: `cellName` / `cell_name` (camelCase/snake_case)
> Ensure your SDK version matches the casing in this example.

---

## See Also

- **Get Worksheet Comment** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`
- **Update Worksheet Comment** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`
- **Delete Worksheet Comment** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`
- **Clear All Comments** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`

---

## Additional Notes

- The endpoint path includes **v3.1** — the current stable version. While `v3.0` remains functional, new features and improvements are only available in v3.1.
- For the full OpenAPI definition, visit the [Aspose.Cells Cloud API reference](https://docs.aspose.cloud/cells/#/Worksheets/PutWorksheetComment).
- Remember to handle rate‑limiting (HTTP 429) and retry according to the API guidelines.
- To migrate from v3.0 to v3.1, update your base URL from `https://api.aspose.cloud/v3.0` to `https://api.aspose.cloud/v3.1` and verify field casing consistency in your SDK implementations.