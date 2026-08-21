---
title: "CSV-Daten in Excel-Arbeitsblatt importieren"
second_title: "Dokument"
linktitle: "CSV-Daten importieren"
type: docs
url: /de/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "CSV-Daten importieren, Excel, Aspose.Cells Cloud, REST API, Tabellendokument, CSV-Import"
description: "Die Aspose.Cells Cloud REST API ermöglicht das Importieren von CSV-Daten in Excel-Arbeitsblätter. Unterstützte SDKs umfassen Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift."
weight: 19
---

Diese REST API **importiert CSV-Daten** in ein Excel-Arbeitsblatt.

Die Anfrage ist eine HTTP-Anfrage mit multipart-Inhalt (siehe [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des multipart-Inhalts enthält die `ImportCSVDataOption`-Daten, der zweite Teil enthält die CSV-Datei.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

Die wichtigsten Parameter sind in den folgenden Tabellen beschrieben.

### ImportCSVDataOption

| Parametername      | Typ                        | Beschreibung                                                              |
| ------------------ | -------------------------- | ------------------------------------------------------------------------ |
| SeparatorString    | string                     | Zeichen zur Trennung von Feldern in der CSV-Datei (z. B. `,` oder `;`).  |
| ConvertNumericData | string (`true`/`false`)    | Gibt an, ob numerische Zeichenfolgen in numerische Werte konvertiert werden sollen. |
| FirstRow           | int                        | 1-basierter Index der ersten Zeile, in der die Daten eingefügt werden.  |
| FirstColumn        | int                        | 1-basierter Index der ersten Spalte, in der die Daten eingefügt werden. |
| SourceFile         | string                     | Name der zu importierenden Quell-CSV-Datei.                              |
| CustomParsers      | List\<CustomParserConfig\> | Sammlung benutzerdefinierter Parserkonfigurationen für spezifische Spalten. |

### CustomParserConfig

| Parametername | Typ    | Beschreibung                                                           |
| ------------- | ------ | ---------------------------------------------------------------------- |
| ColumnIndex   | int    | Nullbasierter Index der Spalte, für die der benutzerdefinierte Parser gilt. |
| ParseMethod   | string | Parse-Methode für die Spalte (z. B. `ToString`, `ToDate`, `ToNumber`). |
| CustomStyle   | string | Benutzerdefinierter Stil (z. B. Zahlenformat), der auf die geparsten Zellen angewendet wird. |

**Beispiel**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                       |
|------|-----------------------------|--------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                               |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größeinschränkung.       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                         |

## So verwenden Sie die PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Geschäftslogik zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Das folgende Codebeispiel zeigt, wie der Aspose.Cells-Webdienst mithilfe des PHP-SDKs aufgerufen wird:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}