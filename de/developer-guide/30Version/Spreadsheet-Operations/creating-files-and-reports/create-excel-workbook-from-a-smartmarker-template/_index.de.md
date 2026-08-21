---
title: "Excel-Berichte mit Smart-Marker-Vorlagen erstellen"
second_title: "Dokument"
linktype: "SmartMarker"
type: docs
url: /de/build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Arbeitsmappe, SDK, API, Berichtserstellung"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mithilfe von Smart-Marker-Vorlagen mit der Aspose.Cells Cloud REST API generieren. Enthält Details zu Anforderung und Antwort, ein cURL-Beispiel, Voraussetzungen, Hinweise und SDK-Codebeispiele."
weight: 40
ArticleTitle: "Excel-Berichte mit Smart-Marker-Vorlagen erstellen – Aspose.Cells Cloud API-Anleitung"
---

Diese REST API erstellt eine Arbeitsmappe mithilfe einer Smart-Marker-Vorlage.

## Workbook SmartMarker API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Was ist ein Smart Marker?**

Ein Smart Marker ist eine Platzhaltersyntax, die Datenfelder in einer XML- (oder JSON-) Datei mit Zellen einer Excel-Vorlage verknüpft. Zur Laufzeit ersetzt Aspose.Cells die Marker durch die entsprechenden Daten, sodass Sie vollständig ausgefüllte Berichte programmgesteuert generieren können.

### **Abfrageparameter**

| Parametername   | Typ    | Beschreibung                                                       |
| --------------- | ------ | ------------------------------------------------------------------ |
| outPath         | string | Zielpfad, in dem die generierte Arbeitsmappe gespeichert wird.    |
| folder          | string | Ordner, der die ursprüngliche Arbeitsmappe enthält.                |
| storageName     | string | Name des zu verwendenden Speicherdienstes.                        |

### **Parameter im Anforderungstext**

| Parametername | Typ  | Beschreibung                                             |
| ------------- | ---- | -------------------------------------------------------- |
| xmlFile       | file | XML-Datendatei für Smart Marker, die mit der Anforderung hochgeladen wird. |

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

**Hinweise / Einschränkungen:**  
- Die API unterstützt Excel-Dateien mit einer Größe von bis zu **50 MB**.  
- Akzeptierte Formate sind ausschließlich **.xlsx**, **.xlsm** und **.xlsb**.  
- Es gilt ein Limit von **20 Anforderungen pro Sekunde** pro Konto.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                         |
|------|-----------------------------|----------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.               |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                           |

## Verwendung der Workbook SmartMarker API

### Spezifikation der Workbook SmartMarker API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

**Kurzes Einzeiler-Beispiel**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Fehlerbehandlung**

| HTTP-Status | Beschreibung           | Typische Ursache                                               |
| ----------- | ---------------------- | -------------------------------------------------------------- |
| 400         | Bad Request            | Fehlende Vorlage, fehlerhafte XML oder ungültige Parameter.   |
| 401         | Unauthorized           | Ungültiges oder fehlendes Authentifizierungstoken.            |
| 404         | Not Found              | Die angegebene Arbeitsmappe oder Speicherposition existiert nicht. |
| 500         | Internal Server Error  | Unerwarteter Serverfehler.                                     |

**Beispiel für eine Fehlerantwort (400)**

```json
{
  "Code": 400,
  "Message": "Die XML-Datendatei fehlt oder ist fehlerhaft."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}