---
title: "2D-Ganzzahl-Array in Excel-Arbeitsblatt importieren"
second_title: "Dokument"
linktitle: "2D-Ganzzahl-Array importieren"
type: docs
url: /import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, 2D-Ganzzahl-Array importieren, Excel-Arbeitsblatt, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API ermöglicht das Importieren zweidimensionaler Ganzzahl-Arrays in Excel-Arbeitsblätter. SDKs sind für Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift verfügbar."
weight: 20
---

Diese REST API **importiert ein zweidimensionales Ganzzahl-Array** in ein Excel-Arbeitsblatt.

Die Anforderung ist eine HTTP-Anforderung mit multipart-Inhalt (siehe [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des multipart-Inhalts enthält die `Import2DimensionIntegerArrayOption`-Daten, der zweite Teil enthält die Datendatei.

Die wichtigsten Parameter sind in der folgenden Tabelle beschrieben:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Import2DimensionIntegerArrayOption**

| Parametername        | Typ        | Beschreibung                                                                                                                                                                                  |
| --------------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Der 1-basierte Index der ersten Zeile, in die die Daten eingefügt werden.                                                                                                                     |
| FirstColumn          | int        | Der 1-basierte Index der ersten Spalte, in die die Daten eingefügt werden.                                                                                                                    |
| Data                 | Integer[,] | Zweidimensionales Ganzzahl-Array, das die zu importierenden Werte enthält.                                                                                                                    |
| DestinationWorksheet | string     | Name des Zielarbeitsblatts.                                                                                                                                                                   |
| IsInsert             | string     | `"true"`, um die Daten einzufügen (bestehende Zellen werden verschoben), `"false"`, um bestehende Zellen zu überschreiben.                                                                   |
| ImportDataType       | string     | Gibt das Datenformat an. Unterstützte Werte: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source               | FileSource | Gibt den Speicherort der Datendatei an, wenn `BatchData` `null` ist.                                                                                                                          |

### **Beispiel**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
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

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Verwendung der PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}