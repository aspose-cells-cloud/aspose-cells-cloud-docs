---
title: "Ta bort mapp – Aspose.Cells Cloud API | Ta bort mappar via REST"
description: "Lär dig hur du tar bort en mapp (valfritt rekursivt) från Aspose.Cells Cloud-lagring med DELETE /v4.0/cells/storage/folder/{path}-ändpunkten. Inkluderar begärandesyntax, parametrar, autentisering, exempelkod och felhantering."
keywords: "Aspose.Cells, ta bort mapp, molnlagring, API, REST, Excel, filhantering"
slug: ta-bort-mapp
date: 2026-07-30
---

# Ta bort mapp – Aspose.Cells Cloud API

Ta bort en mapp (valfritt hela dess innehåll) från Aspose.Cells Cloud-lagring.

---

## Översikt

**Ta bort mapp**-åtgärden tar bort en mapp permanent från ett lagringskonto som används av Aspose.Cells Cloud.  
Du kan ta bort en tom mapp eller, genom att sätta flaggan `recursive` till `true`, ta bort mappen tillsammans med alla filer och undermappar den innehåller. Denna slutpunkt används vanligtvis i rensningsskript, automatiserade arbetsflöden eller när temporära kataloger inte längre behövs.

---

## HTTP-begäran

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – den fullständiga sökvägen till mappen som ska tas bort (URL-kodad).

### Nödvändiga HTTP-rubriker

| Rubrik            | Värde                              | Beskrivning                              |
|-------------------|------------------------------------|------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | JWT-token som erhållits från autentiseringstjänsten. |
| `Accept`          | `application/json`                | Förväntat svarsformat.                |
| `Content-Type`    | `application/json` *(valfritt)*   | Krävs inte för DELETE, men kan skickas. |

---

## Autentisering

Aspose.Cells Cloud använder **JWT-tokenbaserad autentisering**.  
Skaffa en åtkomsttoken via [autentiseringsändpunkten](/authentication/) och inkludera den i `Authorization`-rubriken enligt ovan.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Parametrar

| Namn          | Typ     | Plats   | Obligatorisk | Beskrivning                                                               |
|---------------|---------|---------|--------------|---------------------------------------------------------------------------|
| `path`        | sträng  | Sökväg  | Ja           | Sökvägen till mappen som ska tas bort (URL-kodad).                               |
| `storageName` | sträng  | Fråga   | Nej          | Namnet på lagringen som innehåller mappen. Om utelämnas används standardlagring. |
| `recursive`   | boolesk | Fråga   | Nej          | `true` → ta bort mappen **och allt dess innehåll**. Standard är `false`. |

**Exempel på frågesträng**

```
?storageName=MyStorage&recursive=true
```

---

## Exempel på begäran (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Svar

En lyckad begäran returnerar **HTTP 200 OK** med ett tomt JSON-objekt:

```json
{}
```

Ingen ytterligare nyttolast tillhandahålls eftersom åtgärdens resultat är binärt – mappen är antingen borttagen eller så returneras ett fel.

---

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad               | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

När ett fel inträffar innehåller kroppen ett JSON-objekt med fälten `code` och `message` som beskriver problemet.

---

## SDK-exempel

Följande exempel visar hur du anropar **Ta bort mapp** med de officiellt stödda SDK:erna. Ersätt `{access_token}` och parametervärden med dina egna.

<details><summary>🟦 C# (.NET)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Konfigurera API-klient
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Ta bort mapp (rekursivt)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// Initiera API-klient
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// Konfigurera
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Ta bort mapp rekursivt
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Folder deleted.";
} catch (Exception $e) {
    echo 'Exception when calling FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Folder deleted.'
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Folder deleted'))
    .catch(err => console.error('Error:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Folder deleted")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Folder deleted.\n";
};
if ($@) {
    warn "Error deleting folder: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println("Folder deleted")
}
```
</details>

---

## Se även

- **[Skapa mapp](/create-folder/)** – Skapa en ny mapp i molnlagring.  
- **[Kopiera mapp](/copy-folder/)** – duplicera en mapp och dess innehåll.  
- **[Flytta mapp](/move-folder/)** – flytta en mapp till en annan sökväg.  
- **[OpenAPI-specifikation]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder-åtgärd</a> (interaktiv API-utforskare).

---

## SEO- och tillgänglighetschecklista (internt)

- **Titel och H1** använder rätt bindestreck (`–`) och innehåller nyckelordet *Ta bort mapp*.  
- Alla rubriker följer en logisk hierarki (`H1 → H2 → H3`).  
- Inga UTF-8-kodningsartifactefter finns kvar.  
- Meta-nyckelord sammanfogade till en enda, ren lista (eller utelämnade om önskvärt).  
- Externa länkar inkluderar `rel="noopener noreferrer"` för säkerhet.  
- UI-ikoner och språkflaggor (om visade på sidan) bör ha `aria-label`/`alt`-attribut (t.ex. `aria-label="Svenska (Sverige)"`).  
- `<link rel="alternate" hreflang="xx" href="…">`-taggar rekommenderas i sidhuvudet för varje språkversion.