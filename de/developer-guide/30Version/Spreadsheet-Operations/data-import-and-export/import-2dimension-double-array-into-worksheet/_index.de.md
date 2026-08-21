---
title: "2‑dimensionales Double‑Array in Excel‑Arbeitsblatt importieren"
second_title: "Dokument"
linktitle: "2‑dimensionales Double‑Array importieren"
type: docs
url: /de/import-a-2d-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "2‑dimensionales Double‑Array importieren, Excel, Aspose Cells Cloud, REST‑API, Tabellenkalkulation, Datenimport"
description: "Erfahren Sie, wie Sie ein zweidimensionales Double‑Array mit der Aspose.Cells Cloud REST‑API in ein Excel‑Arbeitsblatt importieren. Enthält Anforderungsformat, Parameter und SDK‑Codebeispiele."
weight: 20
---

Diese REST‑API **importiert ein zweidimensionales Double‑Array** in ein Excel‑Arbeitsblatt.

Die Anforderung ist ein HTTP `POST` mit multipart‑inhalt (siehe [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des multipart‑Körpers enthält die **Import2DimensionDoubleArrayOption**‑Daten, der zweite Teil die Quelldatendatei.

## REST‑API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

Die wichtigsten Parameter sind in der folgenden Tabelle beschrieben:

### Import2DimensionDoubleArrayOption

| Parametername            | Typ          | Beschreibung                                                                                                            |
| ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | `int`        | Zeilenindex (1‑basiert), ab dem der Import beginnt.                                                                    |
| **FirstColumn**          | `int`        | Spaltenindex (1‑basiert), ab dem der Import beginnt.                                                                   |
| **Data**                 | `Double[,]`  | Zweidimensionales Array mit Double‑Werten, das importiert werden soll.                                                 |
| **DestinationWorksheet** | `string`     | Name des Arbeitsblatts, das die Daten empfangen soll.                                                                  |
| **IsInsert**             | `string`     | `"true"`, um Zeilen einzufügen; `"false"`, um vorhandene Zellen zu überschreiben.                                      |
| **ImportDataType**       | `string`     | Art der importierten Daten (z. B. `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData`, etc.). |
| **Source**               | `FileSource` | Gibt den Speicherort der Datendatei an, wenn der Parameter `BatchData` null ist.                                       |

**Beispiel**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP‑Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                           |
|------|-----------------------------|------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.        |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).|
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT‑Token.                                   |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größenbeschränkung.              |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                             |

## Verwendung der PostImportData‑API mit SDKs

### PostImportData‑API‑Spezifikation

Die [OpenAPI‑Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST‑Interaktionen direkt aus einem Webbrowser durchgeführt werden können.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, diese Funktionalität zu integrieren. SDKs übernehmen die Low‑Level‑Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub‑Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells‑Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}