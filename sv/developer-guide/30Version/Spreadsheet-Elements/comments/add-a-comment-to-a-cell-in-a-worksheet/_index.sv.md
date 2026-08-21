---
---
title: "Lägg till kalkylbladskommentar"
description: "Lägg till en kommentar till en specifik cell i ett Excel-kalkylblad med Aspose.Cells Cloud REST API (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, molntjänst-API, lägg till kalkylbladskommentar, Excel, kalkylark, cellkommentar"
weight: 20
api_version: "v3.0"
---

# Lägg till kalkylbladskommentar

Lägg till en kommentar till en specifik cell i ett kalkylblad i en Excel-arbetsbok med Aspose.Cells Cloud REST API.

---

## Förutsättningar / Autentisering

* Ett **Bearer JWT-token** krävs för varje begäran.  
  *Hämta ett token* via **/connect/token**-slutpunkten (se [autentiseringsguide](/cells/authentication/)).  
* Inkludera token i `Authorization`-hoften:

```http
Authorization: Bearer <jwt token>
```

* Alla anrop måste göras över **HTTPS** för att skydda token och data.

---

## HTTP-begäran

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Parametrar för sökväg

| Namn        | Typ    | Krävs    | Beskrivning |
|-------------|--------|----------|-------------|
| `name`      | string | ✔️ | Arbetsbokens filnamn (t.ex. `test.xlsx`). |
| `sheetName` | string | ✔️ | Kalkylbladets namn (t.ex. `Sheet1`). |
| `cellName`  | string | ✔️ | Adressen till målcellen (t.ex. `A1`). |

### Frågeparametrar

| Namn           | Typ    | Krävs    | Beskrivning |
|----------------|--------|----------|-------------|
| `folder`       | string | valfritt | Mappen som innehåller arbetsboken. |
| `storageName`  | string | valfritt | Namnet på lagringstjänsten där filen finns. |

### Begärandetext

Texten måste innehålla ett **Comment**-objekt i JSON-format.

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

**Fält i Comment-objektet**

| Fält                      | Typ     | Krävs    | Beskrivning |
|---------------------------|---------|----------|-------------|
| `CellName`                | string  | ✔️ | Celladress (måste matcha värdet för `{cellName}` i sökvägen). |
| `Author`                  | string  | valfritt | Namn på kommentarens författare. |
| `HtmlNote`                | string  | valfritt | HTML-formaterad kommentartext. |
| `Note`                    | string  | valfritt | Komplett textkommentar (ren text). |
| `AutoSize`                | boolean | valfritt | Autoanpassning av kommentarsboxens storlek. |
| `IsVisible`               | boolean | valfritt | Visa kommentaren som standard. |
| `Width` / `Height`        | number  | valfritt | Storlek på kommentarsboxen (i points). |
| `TextHorizontalAlignment`| string  | valfritt | Horisontell justering (`Left`, `Center`, `Right`). |
| `TextOrientationType`     | string  | valfritt | Textrotation (`NoRotation`, `Rotate90`, …). |
| `TextVerticalAlignment`  | string  | valfritt | Vertikal justering (`Top`, `Center`, `Bottom`). |

---

## cURL-exempel

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
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

## Svarschema

| Fält      | Typ    | Beskrivning |
|-----------|--------|-------------|
| `Comment` | object | Det skapade kommentarobjektet (se **fält i Comment-objektet** ovan, plus länkmetadata). |
| `Code`    | integer | HTTP-statuskoden som returneras av API:t (t.ex. `200`). |
| `Status`  | string  | Textuell statusmeddelande (t.ex. `"OK"`). |

`Comment`-objektet innehåller också ett **link**-underobjekt:

| Underfält | Typ    | Beskrivning |
|-----------|--------|-------------|
| `Href`    | string | URL för självreferens till kommentarsresursen. |
| `Rel`     | string | Typ av relation (`self`). |
| `Title`   | string | Valfri titel (kan vara `null`). |
| `Type`    | string | Valfri MIME-typ (kan vara `null`). |

---

## Exempel på lyckat svar

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

## Felaktiga svar

| HTTP-kod | Beskrivning | Exempel |
|----------|-------------|---------|
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**  | Autentisering krävs – token saknas eller är ogiltig. | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**  | Hittades inte – arbetsbok, kalkylblad eller cell finns inte. | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500**  | Internt serverfel – oväntat tillstånd på servern. | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## SDK-exempel

Följande SDK:n tillhandahåller klara wrapper för denna operation. Ersätt platshållarvärden (`<YOUR_TOKEN>`, `<FILE_NAME>` etc.) med faktisk data.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Konfigurera API-klient
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Förbered kommentarobjekt
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
        .cellName("A1")
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
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
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
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
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
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Se även

* **Hämta kalkylbladskommentar** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Uppdatera kalkylbladskommentar** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Ta bort kalkylbladskommentar** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Rensa alla kommentarer** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## Ytterligare anteckningar

* Sökvägsparametern för slutpunkten innehåller **v3.0**. En nyare version (**v3.1**) finns tillgänglig; uppdatera bas-URL:n därefter om du behöver de senaste funktionerna.  
* För fullständig OpenAPI-definiton, besök [Aspose.Cells Cloud API-referens](/cells/#/Worksheets/PutWorksheetComment).  
* Kom ihåg att hantera rate-limiting (HTTP 429) och återförsök enligt API-riktlinjerna.  

---
---