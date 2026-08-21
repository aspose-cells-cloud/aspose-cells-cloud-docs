---
title: "Text in Excel-Dateien suchen – Aspose.Cells Cloud API"
description: "Suchen Sie nach spezifischem Text in Excel-Dateien (XLS, XLSX, XLSM, XLSB) und ODS-Dateien mit der Aspose.Cells Cloud API. Enthält Anforderungsdetails, cURL- und SDK-Beispiele sowie Fehlerbehandlung."
keywords: "Aspose.Cells, Excel, Suche, API, REST"
type: docs
url: /de/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Text in Excel-Dateien suchen – Aspose.Cells Cloud API

## Übersicht
Aspose.Cells Cloud bietet einen **POST**-Endpunkt, der einen angegebenen Textstring in Excel-Arbeitsmappen (XLS, XLSX, XLSM, XLSB) und OpenDocument-Tabellendokumenten (ODS) durchsucht. Die API gibt jede Zelle zurück, die den gesuchten Text enthält, zusammen mit einem Link zur Arbeitsmappe, in der der Treffer gefunden wurde.

> **Anwendungsfälle**  
> - Überprüfen Sie, ob ein bestimmter Wert in einem Bericht vorhanden ist, bevor mit der weiteren Verarbeitung fortgefahren wird.  
> - Erstellen Sie ein schnelles „Suchen und Ersetzen“-Tool, das zunächst alle Vorkommen auflistet.  
> - Generieren Sie einen Index von Schlüsselbegriffen über mehrere Tabellenkalkulationen hinweg.

---

## Voraussetzungen
| Anforderung | Details |
|-------------|---------|
| **Authentifizierung** | JWT-Token, das über den Aspose Cloud OAuth-Flow erhalten wurde. Das Token muss den Bereich **Cells** enthalten. |
| **Unterstützte Formate** | XLS, XLSX, XLSM, XLSB, ODS |
| **Maximale Dateigröße** | 150 MB (komprimiert). Größere Dateien führen zu **413 Payload Too Large**. |
| **Erforderliche Header** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **Berechtigungen** | Das Token muss *Lese*-Berechtigung für den Ziel-Speicher besitzen (sofern ein Remote-Speicher verwendet wird) – nicht erforderlich, wenn die Datei als `multipart/form-data` hochgeladen wird. |

*Tipp:* Verwenden Sie den **/connect/token**-Endpunkt, um ein JWT-Token zu generieren. Details finden Sie im [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Endpunkt

| Element | Wert |
|---------|------|
| **HTTP-Methode** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **Zweck** | Suchen Sie nach einem angegebenen Text in einer hochgeladenen Excel-Arbeitsmappe. |
| **Sicherheit** | JWT-Token (Bearer) – siehe *Voraussetzungen* oben. |

---

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## Anforderungsparameter

| Name | Typ | Ort | Erforderlich | Beschreibung |
|------|-----|-----|--------------|-------------|
| `file` | **Datei** | `formData` (multipart) | **Ja** | Die hochzuladende Tabellendatei. |
| `text` | **Zeichenkette** | Abfragezeichenfolge | **Ja** | Der zu suchende Textstring. |
| `password` | **Zeichenkette** | Abfragezeichenfolge | Nein | Passwort zum Öffnen einer passwortgeschützten Arbeitsmappe, falls erforderlich. |
| `sheetname` | **Zeichenkette** | Abfragezeichenfolge | Nein | Name des Arbeitsblatts, auf das die Suche beschränkt werden soll. Falls weggelassen, werden alle Arbeitsblätter durchsucht. |
| `checkExcelRestriction` | **boolean** | Abfragezeichenfolge | Nein (Standard: `true`) | Wenn `true`, validiert die API Excel-spezifische Einschränkungen (z. B. schreibgeschützte Zellen) vor der Suche. |

---

## Anforderungsbeispiel (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Rechnung&sheetname=Blatt1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@Rechnungsbericht.xlsx"
```

*Ersetzen Sie `<jwt-token>` durch ein gültiges Token und passen Sie die Abfrageparameter nach Bedarf an.*

---

## Erfolgreiche Antwort

**HTTP 200 – Suche erfolgreich; Antwort enthält gefundene Textelemente.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Rechnung #12345",
        "link": {
          "Href": "Rechnungsbericht.xlsx/worksheets/Blatt1",
          "Rel": "parent",
          "Title": "Blatt1",
          "Type": "string"
        }
      },
      {
        "Text": "Rechnung #12346",
        "link": {
          "Href": "Rechnungsbericht.xlsx/worksheets/Blatt1",
          "Rel": "parent",
          "Title": "Blatt1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Antwortfelder

| Feld | Typ | Beschreibung |
|------|-----|-------------|
| `Status` | Zeichenkette | Gesamtstatus der Anforderung (`OK` bei Erfolg). |
| `Code` | Ganzzahl | HTTP-Statuscode (200). |
| `TextItems.link` | Objekt | Hypermedia-Link zur Sammlungsressource. |
| `TextItems.TextItemList` | Array | Liste der Treffer. Jedes Element enthält: |
| `Text` | Zeichenkette | Der Zellwert, der mit dem Suchtext übereinstimmt. |
| `link` | Objekt | Hyperlink zum Arbeitsblatt, in dem der Treffer gefunden wurde (`Href` verweist auf `Workbook/worksheets/SheetName`). |

---

## Fehlerantworten

| HTTP-Code | Bedeutung | Typische Ursache | Beispiel-Body |
|-----------|-----------|------------------|---------------|
| **400** | Bad Request | Fehlende erforderliche Parameter, nicht unterstützter Dateityp oder ungültige Abfragewerte. | `{ "Status":"Error","Code":400,"Message":"Der Abfrageparameter 'text' ist erforderlich." }` |
| **401** | Unauthorized | Fehlendes oder ungültiges JWT-Token. | `{ "Status":"Error","Code":401,"Message":"Ungültiges oder abgelaufenes Zugriffstoken." }` |
| **413** | Payload Too Large | Die hochgeladene Datei überschreitet das 150 MB-Limit. | `{ "Status":"Error","Code":413,"Message":"Die Dateigröße überschreitet das zulässige Limit." }` |
| **500** | Internal Server Error | Unerwartetes serverseitiges Problem. | `{ "Status":"Error","Code":500,"Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

---

## SDK-Beispiele

Im Folgenden finden Sie minimale Code-Snippets für den **PostSearch**-Vorgang mit den offiziellen Aspose.Cells Cloud SDKs. Ersetzen Sie `YOUR_JWT_TOKEN` und den Dateipfad durch Ihre eigenen Werte.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("Rechnungsbericht.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Rechnung",
            sheetname: "Blatt1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("Rechnungsbericht.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Rechnung",
                null,          // password
                "Blatt1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("Rechnungsbericht.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Rechnung",
        password=None,
        sheetname="Blatt1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("Rechnungsbericht.xlsx"),
    text: "Rechnung",
    sheetname: "Blatt1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(SDKs für PHP, Ruby, Go und Perl sind im [Aspose.Cells Cloud GitHub-Repository](https://github.com/aspose-cells-cloud) verfügbar.)*

---

## Zusätzliche Hinweise

- **`checkExcelRestriction`** ist standardmäßig auf `true` gesetzt. Setzen Sie diesen Wert nur dann auf `false`, wenn Sie sicher sind, dass die Arbeitsmappe keine schützten Zellen enthält, die die Suche beeinträchtigen könnten.
- Die API gibt **Hypermedia-Links** (`Href`) zurück, die mit anderen Aspose.Cells Cloud-Endpunkten verwendet werden können (z. B. zum Herunterladen des Arbeitsblatts oder zum Abrufen der Zellformatierung).
- Bei der Suche in großen Arbeitsmappen sollten Sie den Suchbereich mit dem `sheetname`-Parameter einschränken, um die Antwortzeit zu verbessern.

---

## Verwandte Links

- **Authentifizierungsleitfaden** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **OpenAPI-Spezifikation für PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDKs** – <https://github.com/aspose-cells-cloud>
- **Ratenlimits und Quoten** – <https://docs.aspose.cloud/total/getting-started/limits/>

---