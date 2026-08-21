---
---
title: "Ordner löschen – Aspose.Cells Cloud API | Ordner über REST entfernen"
description: "Erfahren Sie, wie Sie einen Ordner (optional rekursiv) aus dem Aspose.Cells Cloud-Speicher mithilfe des DELETE /v4.0/cells/storage/folder/{path}-Endpunkts entfernen. Enthält Anforderungssyntax, Parameter, Authentifizierung, Beispielcode und Fehlerbehandlung."
keywords: "Aspose.Cells, Ordner löschen, Cloud-Speicher, API, REST, Excel, Dateiverwaltung"
slug: delete-folder
date: 2026-07-30
---

# Ordner löschen – Aspose.Cells Cloud API

Entfernen Sie einen Ordner (optional inklusive aller Inhalte) aus dem Aspose.Cells Cloud-Speicher.

---

## Übersicht

Mit der **Delete Folder**-Operation wird ein Ordner dauerhaft aus einem Speicherkonto entfernt, das von Aspose.Cells Cloud verwendet wird.  
Sie können einen leeren Ordner löschen oder, indem Sie das Flag `recursive` auf `true` setzen, den Ordner zusammen mit allen enthaltenen Dateien und Unterverzeichnissen löschen. Dieser Endpunkt wird häufig in Aufräumskripten, automatisierten Workflows oder dann verwendet, wenn temporäre Verzeichnisse nicht mehr benötigt werden.

---

## HTTP-Anforderung

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – der vollständige Pfad des zu löschenden Ordners (URL-kodiert).

### Erforderliche HTTP-Header

| Header            | Wert                               | Beschreibung                               |
|-------------------|------------------------------------|--------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | JWT-Token, das vom Authentifizierungsservice erhalten wurde. |
| `Accept`          | `application/json`                | Erwartetes Antwortformat.                  |
| `Content-Type`    | `application/json` *(optional)*   | Für DELETE nicht erforderlich, kann jedoch gesendet werden. |

---

## Authentifizierung

Aspose.Cells Cloud verwendet eine **JWT-Token-basierte Authentifizierung**.  
Ein Zugriffstoken erhalten Sie über den [Authentifizierungs-Endpunkt](/authentication/) und geben es wie oben gezeigt im `Authorization`-Header an.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Parameter

| Name          | Typ     | Ort     | Erforderlich | Beschreibung                                                                 |
|---------------|---------|---------|--------------|------------------------------------------------------------------------------|
| `path`        | Zeichenkette | Pfad    | Ja           | Pfad des zu löschenden Ordners (URL-kodiert).                               |
| `storageName` | Zeichenkette | Abfrage | Nein         | Name des Speichers, der den Ordner enthält. Falls weggelassen, wird der Standard-Speicher verwendet. |
| `recursive`   | Boolean | Abfrage | Nein         | `true` → löscht den Ordner **sowie alle enthaltenen Inhalte**. Standardwert ist `false`. |

**Beispiel-Abfragezeichenfolge**

```
?storageName=MyStorage&recursive=true
```

---

## Beispielanforderung (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Antwort

Bei einer erfolgreichen Anforderung wird **HTTP 200 OK** zurückgegeben, gefolgt von einem leeren JSON-Objekt:

```json
{}
```

Es wird kein weiterer Inhalt übermittelt, da das Ergebnis der Operation binär ist – der Ordner wird entweder entfernt oder es wird eine Fehlermeldung zurückgegeben.

---

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                          |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK                          | Vorgang erfolgreich; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                  |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                            |

Bei einem Fehler enthält der Antworttext ein JSON-Objekt mit den Feldern `code` und `message`, die das Problem beschreiben.

---

## SDK-Beispiele

Die folgenden Beispiele zeigen, wie Sie **Delete Folder** mit den offiziell unterstützten SDKs aufrufen. Ersetzen Sie `{access_token}` und Parameterwerte durch Ihre eigenen Werte.

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API-Client konfigurieren
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Ordner löschen (rekursiv)
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

// API-Client initialisieren
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

// Konfigurieren
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Ordner rekursiv löschen
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

## Siehe auch

- **[Create Folder](/create-folder/)** – Erstellen Sie einen neuen Ordner im Cloud-Speicher.  
- **[Copy Folder](/copy-folder/)** – Kopieren Sie einen Ordner und seine Inhalte.  
- **[Move Folder](/move-folder/)** – Verschieben Sie einen Ordner an einen anderen Pfad.  
- **[OpenAPI-Spezifikation]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder-Vorgang</a> (interaktiver API-Explorer).

---

## SEO & Barrierefreiheits-Checkliste (intern)

- Titel und H1 enthalten den korrekten en‑dash (`–`) sowie das Haupt-Stichwort *Delete Folder*.  
- Alle Überschriften folgen einer logischen Hierarchie (`H1 → H2 → H3`).  
- Es sind keine UTF‑8-Kodierungsfehler vorhanden.  
- Meta-Keywords sind in einer einzigen, sauberen Liste zusammengefasst (oder bei Vorliebe weggelassen).  
- Externe Links enthalten `rel="noopener noreferrer"` zur Sicherheit.  
- UI-Symbole und Sprachflaggen (sofern auf der Seite gerendert) sollten `aria-label`-/`alt`-Attribute besitzen (z. B. `aria-label="English (US)"`).  
- `<link rel="alternate" hreflang="xx" href="…">`-Tags werden im `<head>`-Bereich der Seite für jede Sprachversion empfohlen.

---
---