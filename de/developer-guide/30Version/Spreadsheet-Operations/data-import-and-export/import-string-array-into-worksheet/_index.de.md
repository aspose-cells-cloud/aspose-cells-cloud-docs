---
title: "Zeichenfolgenarray in Excel-Arbeitsblatt importieren – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Zeichenfolgenarray importieren"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, Zeichenfolgenarray importieren, Excel REST API, Multipart-Upload, Arbeitsblattdatenimport, Cloud SDK"
description: "Erfahren Sie, wie Sie ein Zeichenfolgenarray mit der Aspose.Cells Cloud REST API (v3.0) in ein Excel-Arbeitsblatt importieren. Enthält Anforderungsformat, Parameter und SDK-Beispiele."
weight: 40
ArticleTitle: "Zeichenfolgenarray in Excel-Arbeitsblatt importieren – Aspose.Cells Cloud"
---

Das Importieren eines Zeichenfolgenarrays in ein Excel-Arbeitsblatt ist eine gängige Aufgabe beim Befüllen von Tabellen mit listengestützten Daten. Dieser Vorgang ist nützlich für Szenarien wie das Laden von Konfigurationswerten, die Übertragung von Daten aus externen Quellen oder die Initialisierung von Arbeitsblättern mit vordefinierten Zeichenfolgencollections.

**Voraussetzungen:**  
- Ein gültiges JWT-Token, das über den Aspose.Cells Cloud-Authentifizierungsfluss erhalten wurde.  
- Eine vorhandene Arbeitsmappe (oder die Möglichkeit, eine zu erstellen) in Ihrem Aspose-Cloud-Speicher.  
- Die entsprechende SDK-Version, die das Modell `ImportStringArrayOption` unterstützt.

Diese REST-API importiert Zeichenfolgenarray-Daten in ein Excel-Arbeitsblatt.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

Die Anforderung nutzt multipart-HTTP-Inhalte (siehe [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Der erste Teil des multipart-Body enthält ein **ImportStringArrayOption**-Payload; der zweite Teil enthält die Quelldatendatei.

Die wichtigsten Parameter sind in der folgenden Tabelle beschrieben:

<caption>ImportStringArrayOption-Parameter</caption>
### **ImportStringArrayOption**

| Parametername        | Typ        | Beschreibung                                                                                                                                                                         |
| -------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Der Startzeilenindex (1-basiert), an dem die Daten platziert werden.                                                                                                               |
| FirstColumn          | int        | Der Startspaltenindex (1-basiert), an dem die Daten platziert werden.                                                                                                              |
| IsVertical           | boolean    | `true`, um Daten vertikal einzufügen; `false`, um horizontal einzufügen.                                                                                                           |
| Data                 | String[]   | Das zu importierende Zeichenfolgenarray.                                                                                                                                            |
| DestinationWorksheet | string     | Der Name des Arbeitsblatts, das die Daten empfangen soll.                                                                                                                          |
| IsInsert             | boolean    | `true`, um Zeilen/Spalten einzufügen (vorhandene Zellen verschieben); `false`, um vorhandene Zellen zu überschreiben.                                                             |
| ImportDataType       | string     | Art der zu importierenden Daten (z. B. `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Gibt an, wo sich die Datendatei befindet, wenn **BatchData** null ist (z. B. `CloudFileSystem`, `LocalFile`). Erforderlich, wenn `BatchData` nicht bereitgestellt wird.            |

### Beispiel

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### Antwort

Eine erfolgreiche Anforderung gibt **HTTP 200** mit einer JSON-Payload zurück, die folgendermaßen aussieht:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Mögliche Statuscodes:

| Code | Bedeutung                               |
| ---- | --------------------------------------- |
| 200  | Import erfolgreich                      |
| 400  | Ungültige Anforderung – fehlende oder ungültige Daten |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token |
| 500  | Interner Serverfehler                   |


## Verwenden der PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---