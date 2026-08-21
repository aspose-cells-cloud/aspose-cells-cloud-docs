---
title: "Stapelverarbeitungsdaten in Excel-Arbeitsblatt importieren"
second_title: "Dokument"
linktitle: "Stapelverarbeitungsdaten importieren"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, Cloud API, Stapelverarbeitungsdaten importieren, Excel, CSV, JSON, XML, Arrays"
description: "Erfahren Sie, wie Stapelverarbeitungsdaten (CSV, JSON, XML, Arrays) mit der Aspose.Cells Cloud REST API in ein Excel-Arbeitsblatt importiert werden. Enthält Authentifizierung, Beispiele für Anforderungen/Antworten, SDK-Snippets und Fehlerbehandlung."
weight: 19
ArticleTitle: "Stapelverarbeitungsdaten in Excel-Arbeitsblatt importieren – Aspose.Cells Cloud-Dokumentation"
---

Diese REST-API **importiert Stapelverarbeitungsdaten** in ein Excel-Arbeitsblatt. Sie akzeptiert eine Multipart-Anfrage, wobei der erste Teil das Objekt **ImportBatchDataOption** und der zweite Teil die eigentliche Datendatei (CSV, JSON, XML usw.) enthält.

Der Vorgang nutzt eine HTTP-Anfrage mit Multipart-Inhalt (siehe [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### ImportBatchDataOption

| Parametername          | Typ               | Beschreibung                                                                                                                                                                                  |
| ---------------------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**          | `List<CellValue>` | Sammlung von Zellwerten, die direkt geschrieben werden sollen.                                                                                                                                |
| **DestinationWorksheet** | `string`          | Name des Arbeitsblatts, in das die Daten importiert werden.                                                                                                                                  |
| **IsInsert**           | `bool`            | Wenn `true`, werden die Daten eingefügt und vorhandene Zellen verschoben; bei `false` überschreiben die Daten vorhandene Zellen.                                                              |
| **ImportDataType**     | `string`          | Format der zu importierenden Daten. Zulässige Werte: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**             | `FileSource`      | Gibt den Speicherort der Datendatei an, wenn **BatchData** `null` ist.                                                                                                                        |

### CellValue

| Parametername   | Typ      | Beschreibung                                               |
| --------------- | -------- | --------------------------------------------------------- |
| **rowIndex**    | `int`    | Nullbasiert Zeilenindex der Zielzelle.                    |
| **columnIndex** | `int`    | Nullbasiert Spaltenindex der Zielzelle.                   |
| **type**        | `string` | Datentyp des Werts (z. B. `int`, `double`, `string`).     |
| **value**       | `string` | Der tatsächlich in die Zelle zu schreibende Wert.         |
| **style**       | `Style`  | Optionale Formatierungsinformationen für die Zelle.       |

### FileSource

| Parametername      | Typ      | Beschreibung                                                               |
| ------------------ | -------- | -------------------------------------------------------------------------- |
| **FileSourceType** | `string` | Quelle der Datei: `InMemoryFiles`, `CloudFileSystem` oder `RequestFiles`. |
| **FilePath**       | `string` | Pfad oder Bezeichner der Datei innerhalb der gewählten Quelle.            |

### Beispiel (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
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
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.             |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.               |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Verwendung der PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Methode zur Integration dieser Funktionalität. SDKs übernehmen die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}