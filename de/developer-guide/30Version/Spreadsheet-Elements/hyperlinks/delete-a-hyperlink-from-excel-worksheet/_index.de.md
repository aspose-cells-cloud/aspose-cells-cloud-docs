---
title: "Hyperlink in Arbeitsblatt löschen"
type: docs
url: /de/hyperlinks/delete/
description: "Löschen Sie ein Hyperlink in einem Arbeitsblatt anhand seines Index über die Aspose.Cells Cloud API. Erfahren Sie, welche Parameter erforderlich sind, wie die Authentifizierung funktioniert und sehen Sie Codebeispiele für C#, Java, Python und weitere Sprachen."
keywords: "Aspose.Cells, Cloud, Hyperlink löschen, Excel API, REST, Hyperlink im Arbeitsblatt"
ArticleTitle: "Hyperlink in Arbeitsblatt löschen – Aspose.Cells Cloud API-Dokumentation"
weight: 40
---

Diese REST-API löscht einen Hyperlink in einem Excel-Arbeitsblatt anhand seines Index.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### REST-API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Anforderungsparameter

| Parametername      | Typ     | Position | Erforderlich | Beschreibung                                                   |
| ------------------ | ------- | -------- | ------------ | -------------------------------------------------------------- |
| **name**           | string  | path     | ✅           | Name der Excel-Datei.                                          |
| **sheetName**      | string  | path     | ✅           | Name des Arbeitsblatts.                                        |
| **hyperlinkIndex** | integer | path     | ✅           | Nullbasierter Index des zu löschenden Hyperlinks.             |
| **folder**         | string  | query    | ❌           | Ordner, der das Dokument enthält (Standard: root).            |
| **storageName**    | string  | query    | ❌           | Name des Speicherdienstes (Standard-Speicher wird verwendet, falls weggelassen). |

#### Antworten

| Statuscode                    | Beschreibung                                              | Beispiel-Response-Body                             |
| ----------------------------- | --------------------------------------------------------- | -------------------------------------------------- |
| **200 OK**                    | Hyperlink erfolgreich gelöscht.                           | `{"Code":200,"Status":"OK"}`                       |
| **400 Bad Request**           | Fehlende oder ungültige Parameter.                       | `{"Code":400,"Message":"Ungültiger hyperlinkIndex."}` |
| **401 Unauthorized**          | Authentifizierungstoken fehlt oder ist ungültig.         | `{"Code":401,"Message":"Ungültiges Access-Token."}`   |
| **404 Not Found**             | Die Datei, das Arbeitsblatt oder der Hyperlinkindex existiert nicht. | `{"Code":404,"Message":"Ressource nicht gefunden."}`     |
| **500 Internal Server Error** | Unerwarteter Serverfehler.                               | `{"Code":500,"Message":"Interner Serverfehler."}`  |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden. Für Zuverlässigkeit sind Inline-Snippets enthalten; ein Link zum ursprünglichen Gist dient zur Referenz.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Hyperlink deleted"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlink deleted')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Quelle: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hyperlink deleted")
    }
}
```

{{< /tab >}}

{{< /tabs >}}