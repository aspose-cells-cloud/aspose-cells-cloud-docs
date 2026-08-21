---
title: "Erstellen einer leeren Excel-Arbeitsmappe"
second_title: "Dokument"
linktitle: "Leere Arbeitsmappe"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, leere Arbeitsmappe, REST-API, SDK"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST-API eine leere Excel-Arbeitsmappe erstellen. Enthält cURL- und SDK-Beispiele."
weight: 20
ArticleTitle: "Erstellen einer leeren Excel-Arbeitsmappe mit der Aspose.Cells Cloud API"
---

Diese REST-API erstellt eine **leere Arbeitsmappe**.

## PutWorkbookCreate API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Abfrageparameter

| Parametername     | Typ    | Beschreibung                                                    |
| ----------------- | ------ | --------------------------------------------------------------- |
| templateFile      | string | Pfad zu einer Vorlagenarbeitsmappe, die als Basis verwendet werden soll (optional). |
| dataFile          | string | Pfad zu einer Datendatei zum Füllen der Arbeitsmappe (optional). |
| isWriteOver       | boolean | `true`, um eine vorhandene Datei zu überschreiben; `false` andernfalls. |
| folder            | string | Zielordner für die erstellte Arbeitsmappe (optional).           |
| storageName       | string | Name des zu verwendenden Speicherdienstes.                      |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung                                |
| ------------- | --- | ------------------------------------------- |
| data          | file | Binärinhalt der zu erstellenden Arbeitsmappe. |

### **Antwort**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                           | Wann zurückgegeben                                      |
|------|-------------------------------------|---------------------------------------------------------|
| 200 OK | Arbeitsmappe erfolgreich erstellt   | Normaler Ablauf                                         |
| 201 Created | Arbeitsmappe erstellt (alternativer Antwortstatus) | Wenn die API einen „Created“-Status zurückgibt |
| 400 Bad Request | Ungültige Parameter             | Client-seitiger Fehler                                  |
| 401 Unauthorized | Fehlendes oder ungültiges Token | Authentifizierungsfehler                              |
| 409 Conflict | Datei existiert und `isWriteOver=false` | Konflikt mit vorhandener Datei                      |

## Verwendung der PutWorkbookCreate API mit SDKs

### PutWorkbookCreate API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** zur Nutzung der Aspose.Cells-Webservices verwenden. Fügen Sie den Header `Authorization` mit einem gültigen OAuth2-/JWT-Zugriffstoken hinzu. Für eine leere Arbeitsmappe ist der Anforderungstext optional; falls Sie eine Datei hochladen müssen, fügen Sie `--data-binary @empty.xlsx` wie unten gezeigt hinzu.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Erstellen einer leeren Arbeitsmappe mit dem Namen newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Diese Zeile für eine wirklich leere Arbeitsmappe weglassen
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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK abstractisiert Low-Level-Details, sodass Sie sich auf Ihre Projektinhalte konzentrieren können. Prüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---