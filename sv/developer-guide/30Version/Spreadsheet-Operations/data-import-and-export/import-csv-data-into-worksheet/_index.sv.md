---
title: "Importera CSV-data till Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Importera CSV-data"
type: docs
url: /sv/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "Importera CSV-data, Excel, Aspose.Cells Cloud, REST API, Kalkylark, CSV-import"
description: "Aspose.Cells Cloud REST API gör det möjligt att importera CSV-data till Excel-arbetsblad. Stödda SDK:er inkluderar Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift."
weight: 19
---

Denna REST API **importerar CSV-data** till ett Excel-arbetsblad.

Förfrågan är en HTTP-förfrågan med multipart-innehåll (se [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av multipart-innehållet innehåller `ImportCSVDataOption`-data och den andra delen innehåller CSV-filen.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

De viktiga parametrarna beskrivs i tabellerna nedan.

### ImportCSVDataOption

| Parameternamn      | Typ                        | Beskrivning                                                             |
| ------------------ | -------------------------- | ----------------------------------------------------------------------- |
| SeparatorString    | sträng                     | Tecken som används för att separera fält i CSV-filen (t.ex. `,` eller `;`). |
| ConvertNumericData | sträng (`true`/`false`)    | Anger om numeriska strängar ska konverteras till numeriska värden.      |
| FirstRow           | int                        | 1-baserat index för den första raden dit data ska placeras.            |
| FirstColumn        | int                        | 1-baserat index för den första kolumnen dit data ska placeras.         |
| SourceFile         | sträng                     | Namn på käll-CSV-filen som ska importeras.                              |
| CustomParsers      | List\<CustomParserConfig\> | Samling av anpassade parserkonfigurationer för specifika kolumner.      |

### CustomParserConfig

| Parameternamn | Typ    | Beskrivning                                                              |
| ------------- | ------ | ------------------------------------------------------------------------ |
| ColumnIndex   | int    | 0-baserat index för kolumnen till vilken den anpassade parsern tillämpas. |
| ParseMethod   | sträng | Parsermetod för kolumnen (t.ex. `ToString`, `ToDate`, `ToNumber`).      |
| CustomStyle   | sträng | Anpassad stil (t.ex. nummerformat) som tillämpas på de parslade cellerna. |

**Exempel**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Blad1</DestinationWorksheet>
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
### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Beteende                    | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksbegränsningen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur du använder PostImportData-API:t med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på din affärslogik. Besök [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänsten med PHP SDK:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}