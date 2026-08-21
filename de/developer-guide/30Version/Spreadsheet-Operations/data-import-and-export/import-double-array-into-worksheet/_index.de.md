---
title: "Doppelte Array in Excel-Arbeitsblatt importieren"
second_title: "Dokument"
linktitle: "Doppeltes Array importieren"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, doppeltes Array importieren, Excel-API, Cloud-SDK"
description: "Erfahren Sie, wie Sie ein doppeltes Array (double array) mit der Aspose.Cells Cloud REST API in ein Excel-Arbeitsblatt importieren. Enthält Authentifizierung, Anforderungsformat, Parameter, Beispiel-XML/JSON und Antwortdetails."
weight: 20
ArticleTitle: "Doppeltes Array in Excel-Arbeitsblatt importieren – Aspose.Cells Cloud-Anleitung"
---

Diese REST API **importiert Daten aus einem doppelten Array (double array)** in ein Excel-Arbeitsblatt.

> **Voraussetzungen:** Sie müssen über ein gültiges JWT-Token verfügen, bevor Sie diese API aufrufen können. Weitere Details finden Sie in der Authentifizierungsanleitung.

Sie senden eine HTTP-Anfrage mit <strong>Multipart</strong>-Inhalt (siehe [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Der erste Teil des Multipart-Textkörpers enthält die **ImportDoubleArrayOption**-Daten, der zweite Teil enthält die Datendatei.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

#### **ImportDoubleArrayOption**

| Parametername        | Typ        | Beschreibung                                                                                              |
| -------------------- | ---------- | --------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Nullbasierter Index der ersten Zeile, in der die Daten eingefügt werden.                                 |
| FirstColumn          | int        | Nullbasierter Index der ersten Spalte, in der die Daten eingefügt werden.                                |
| IsVertical           | boolean    | `true` / `false` – legt fest, ob das Array vertikal (`true`) oder horizontal (`false`) eingefügt wird.   |
| Data                 | Double[]   | Array mit Double-Werten, die importiert werden sollen.                                                   |
| DestinationWorksheet | string     | Name des Zielarbeitsblatts.                                                                               |
| IsInsert             | boolean    | `true` / `false` – bei `true` werden die Daten eingefügt, bei `false` werden vorhandene Zellen überschrieben. |
| ImportDataType       | string     | Art der zu importierenden Daten (z. B. `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`). |
| Source               | FileSource | Gibt den Speicherort der Datendatei an, wenn der Parameter `BatchData` null ist.                         |

#### Beispiel (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Beispiel (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### Antwort

Bei erfolgreicher Anfrage wird **HTTP 200** mit einer JSON-Antwort im folgenden Format zurückgegeben:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Mögliche Statuscodes:

| Code | Bedeutung                                     |
| ---- | --------------------------------------------- |
| 200  | Import erfolgreich                            |
| 400  | Ungültige Anforderung – fehlende oder ungültige Daten |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token |
| 500  | Interner Serverfehler                         |

### Fehlerbehandlung

Im Fehlerfall gibt die API ein JSON-Objekt mit Fehlercode und einer beschreibenden Nachricht zurück. Beispiel für eine nicht autorisierte Anforderung:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

Weitere Informationen zu verwandten Importvorgängen finden Sie auf den Dokumentationsseiten „2‑Dimensionales Double‑Array importieren“ und „Integer‑Array importieren“.

## Verwendung der PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}