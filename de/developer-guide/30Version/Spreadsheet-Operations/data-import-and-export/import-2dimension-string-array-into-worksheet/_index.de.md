---
title: "2D-Zeichenfolgenarray in Excel-Arbeitsblatt importieren"
second_title: "Dokument"
linktitle: "2D-Zeichenfolgenarray importieren"
type: docs
url: /de/import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-string-array-into-excel-worksheet/",
    "/import-2dimension-string-array-into-worksheet/",
    "/import-data/-2dimension-string-array/",
    "/import-data/2dimension-string-array/",
    "/import/2dimension-string-array/",
  ]
keywords: "Aspose.Cells Cloud, 2D-Zeichenfolgenarray importieren, Excel, REST-API, SDK"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST-API ein zweidimensionales Zeichenfolgenarray in ein Excel-Arbeitsblatt importieren. Enthält Anforderungsformat, Parameterdetails und SDK-Codebeispiele für C#, PHP und Ruby."
weight: 20
---

Diese REST-API **importiert ein zweidimensionales Zeichenfolgenarray** in ein Excel-Arbeitsblatt.

Die Anforderung ist eine HTTP-Anforderung mit multipart-Inhalt (siehe [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des multipart-Inhalts enthält die `Import2DimensionStringArrayOption`-Daten, der zweite Teil die Datendatei.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

Die wichtigsten Parameter sind in der folgenden Tabelle beschrieben:

### **Import2DimensionStringArrayOption**

| Parametername         | Typ                 | Beschreibung                                                                 |
| --------------------- | ------------------- | -----------------------------------------------------------------------------|
| FirstRow             | int                 | Nullbasierter Index der Zeile, ab der der Import beginnt.                   |
| FirstColumn          | int                 | Nullbasierter Index der Spalte, ab der der Import beginnt.                  |
| Data                 | String[,]           | Zweidimensionales Array mit den zu importierenden Zeichenfolgenwerten.      |
| DestinationWorksheet | string              | Name des Arbeitsblatts, in das die importierten Daten eingefügt werden.     |
| IsInsert             | string (true/false) | Falls **true**, werden die Daten eingefügt und vorhandene Zellen entsprechend verschoben. |
| ImportDataType       | string              | Gibt den Datentyp an; verwenden Sie für diesen Vorgang `TwoDimensionStringArray`. |
| Source               | FileSource          | Gibt den Speicherort der Datendatei an, wenn der Parameter `BatchData` null ist. |

### Beispiel für Anforderungstext

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
}
```

### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                 | Beschreibung                                                                 |
|------|---------------------------|------------------------------------------------------------------------------|
| 200  | OK                        | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request               | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized              | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large         | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error     | Unerwarteter Serverfehler.                                                  |

## Verwendung der PostImportData-API mit SDKs

### PostImportData-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, diese Funktion zu integrieren. Ein SDK abstractisiert die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}