---
title: "ListObject-Daten in einem Excel-Arbeitsblatt sortieren"
second_title: "Dokument"
linktitle: "Sortieren"
type: docs
url: /de/list-objects/sort-data/
aliases: [  /de/get-a-list-object-or-table-inside-the-worksheet/ , /de/tables/sort-data/ ]
keywords: "Aspose.Cells Cloud, Excel, ListObject, Daten sortieren, REST API, Arbeitsblatt"
description: "Erfahren Sie, wie Sie ListObject-Daten (Tabelle) in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) sortieren. Enthält Endpunkt, Parameter, Beispiel-cURL-Anfrage und SDK-Beispiele."
weight: 40
ArticleTitle: "ListObject-Daten in einem Excel-Arbeitsblatt sortieren – Aspose.Cells Cloud API"
---

**Voraussetzungen**  
Um diese API aufzurufen, benötigen Sie ein gültiges Aspose Cloud JWT-Access-Token, und die Arbeitsmappe muss in den Aspose Cloud-Speicher hochgeladen sein. Fügen Sie den Header `Authorization: Bearer <jwt token>` in jede Anfrage ein.

Diese REST API sortiert die Daten einer Tabelle in einem Excel-Arbeitsblatt.  
Um diesen Vorgang auszuführen, geben Sie den Arbeitsmappen-Namen, den Arbeitsblattnamen und den Index des Ziel-ListObjects zusammen mit einem JSON-Body `dataSorter` an, der die Sortierkriterien definiert.

## PostWorksheetListObjectSortTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anfrageparameter**

| Parametername      | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                      |
| ------------------ | ------ | ---------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| name               | string | path                               | Der Name der Excel-Datei im Aspose Cloud-Speicher.                                                               |
| sheetName          | string | path                               | Der Name des Arbeitsblatts, das das ListObject enthält.                                                          |
| listObjectIndex    | integer| path                               | Nullbasierter Index des ListObjects (Tabelle) innerhalb des Arbeitsblatts.                                       |
| dataSorter         | object | body                               | JSON-Objekt, das Sortieroptionen definiert (z. B. `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder             | string | query                              | Ordnerpfad im Speicher, in dem sich die Excel-Datei befindet.                                                    |
| storageName        | string | query                              | Name des Aspose Cloud-Speichers.                                                                                  |

**Hinweise**  
Der Anforderungstext muss ein gültiges JSON-Objekt sein, das dem `dataSorter`-Schema entspricht. Stellen Sie sicher, dass die Arbeitsmappe, das Arbeitsblatt und das ListObject vor dem Aufruf des Sortiervorgangs vorhanden sind.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**HTTP-Statuscodes**

| Statuscode | Beschreibung                                      |
|------------|---------------------------------------------------|
| 200        | OK – Sortierung erfolgreich abgeschlossen.       |
| 400        | Bad Request – ungültige Parameter.               |
| 401        | Unauthorized – Authentifizierung fehlgeschlagen. |
| 404        | Not Found – Arbeitsmappe, Arbeitsblatt oder ListObject nicht gefunden. |
| 500        | Internal Server Error – serverseitiges Problem.  |

**Antwortparameter**

| Parameter | Typ    | Beschreibung                                 |
|-----------|--------|----------------------------------------------|
| Code      | integer| Vom API zurückgegebener HTTP-Statuscode.     |
| Status    | string | Textuelle Beschreibung des Ergebnisses (z. B. "OK"). |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[Zurück zur ListObjects-Übersicht](/list-objects/)
---