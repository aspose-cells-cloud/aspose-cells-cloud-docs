---
title: "OLE-Objekt aus Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Abrufen"
type: docs
url: /de/oleobjects/get/
aliases: [  /de/get-oleobject-from-a-worksheet/ ]
keywords: "aspose, cells, ole-objekt, excel, arbeitsblatt, ole-objekt abrufen, rest-api"
description: "Rufen Sie ein OLE-Objekt (Bild, Diagramm oder eingebettete Datei) aus einem Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API ab. Enthält HTTPS-Endpunkt, erforderliche Parameter, Beispiel-cURL und SDK-Code in mehreren Sprachen."
ArticleTitle: "OLE-Objekt aus Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
weight: 10
---

Diese REST API ruft ein **OLE-Objekt** aus einem Excel-Arbeitsblatt ab.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST-API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Anforderungsparameter

| Parametername   | Typ    | Ort   | Beschreibung                                                |
| --------------- | ------ | ----- | ----------------------------------------------------------- |
| name            | string | path  | Name des Dokuments.                                         |
| sheetName       | string | path  | Name des Arbeitsblatts.                                     |
| objectNumber    | integer| path  | Die Objektnummer innerhalb des Arbeitsblatts.              |
| format          | string | query | Gewünschtes Exportformat für das Objekt (z. B. `png`, `jpeg`). |
| folder          | string | query | Ordner, der das Dokument enthält.                           |
| storageName     | string | query | Name des zu verwendenden Speichers.                         |

### Speicheroptionen

- **folder** – gibt den Unterordner im Standardspeicher an, in dem sich die Arbeitsmappe befindet.
- **storageName** – überschreibt den Standard-Speichernamen, falls sich die Arbeitsmappe an einem anderen Speicherort befindet.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um den Aspose.Cells-Webservice aufzurufen. Das folgende Beispiel zeigt, wie ein OLE-Objekt als PNG-Bild angefordert wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### Binäre Bildantwort

Wenn `format` auf einen Bilddatentyp (z. B. `png`) gesetzt ist, gibt die API die binären Bilddaten mit dem Header zurück:

```
Content-Type: image/png
```

_(Die Bilddatei wird direkt an den Client gestreamt.)_

### JSON-Metadaten-Antwort

Wenn `format` weggelassen oder auf `json` gesetzt wird, gibt die API eine JSON-Payload zurück, die das OLE-Objekt beschreibt:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Fehlerantworten

| HTTP-Status | Fehlercode   | Beschreibung                                   |
| ----------- | ------------ | --------------------------------------------- |
| 400         | BadRequest   | Fehlende oder ungültige Parameter.            |
| 401         | Unauthorized | Ungültiger oder fehlender JWT-Token.          |
| 404         | NotFound     | Arbeitsmappe, Arbeitsblatt oder OLE-Objekt nicht gefunden. |
| 500         | ServerError  | Unerwarteter Serverfehler.                    |

**Beispiel für eine 404-Antwort**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "Das angeforderte OLE-Objekt mit der Nummer 0 wurde im Arbeitsblatt 'Sheet1' nicht gefunden."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die API zu integrieren. SDKs übernehmen die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}