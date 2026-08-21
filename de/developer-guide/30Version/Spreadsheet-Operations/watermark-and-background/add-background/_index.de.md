---
title: "Hintergrundbild in Arbeitsmappe hinzufügen"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, Hintergrundbild hinzufügen, Excel-API, REST, Cloud-SDK, cURL, Arbeitsmappenhintergrund"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST-API ein Hintergrundbild zu einer Excel-Arbeitsmappe hinzufügen. Enthält erforderliche Parameter, Authentifizierungsdetails, ein vollständiges cURL-Beispiel sowie Informationen zur Fehlerbehandlung."
weight: 160
---

## REST-API

Diese REST-API fügt ein **Hintergrundbild** zu einer Excel-Arbeitsmappe hinzu.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Abfrageparameter

| Parametername   | Typ    | Beschreibung                                                   |
| --------------- | ------ | -------------------------------------------------------------- |
| `picPath`       | string | Pfad zur Bilddatei, die als Hintergrund verwendet werden soll. |
| `folder`        | string | Ordner, der die ursprüngliche Arbeitsmappe enthält.            |
| `storageName`   | string | Name des Speichers, in dem sich die Datei befindet.            |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung                                                     |
| ------------- | --- | ---------------------------------------------------------------- |
| `datafile`    | file | Die Arbeitsmappe, der der Hintergrund hinzugefügt werden soll. |

**Pfadparameter** – `{name}` in der URL stellt den **Namen der Arbeitsmappendatei** dar (z. B. `Book1.xlsx`).


### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.        |
| 400  | Ungültige Anforderung       | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Nicht autorisiert           | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Anforderungstext zu groß    | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Interner Serverfehler       | Unerwarteter Serverfehler.                                                   |

## Verwendung der PutWorkbookBackground-API mit SDKs

### PutWorkbookBackground-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

Sie können das **cURL**-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt eine vollständige Anforderung, einschließlich des Flags für den multipart-Dateiupload und des erforderlichen Authentifizierungsheaders.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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


### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstractisiert Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}