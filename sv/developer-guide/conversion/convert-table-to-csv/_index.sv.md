---
title: "Aspose.Cells Cloud Web-API – Konvertera en tabell i ett kalkylblad till en CSV-fil – Gratis onlineverktyg"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar tabelldata i kalkylblad till CSV-fil: Steg-för-steg-guide"
linktitle: "Konvertera tabell till CSV"
type: docs
url: /sv/convert-table-to-csv/
keywords: "Aspose.Cells Cloud, tabell till CSV, konvertering av kalkylblad, Excel till CSV, API, REST, export av data"
description: "Konvertera en tabell i ett Excel-kalkylblad till en CSV-fil snabbt med Aspose.Cells Cloud API."
weight: 100
---

Exportera tabelldata från en lokal Excel-fil till en CSV-fil med Cloud-API:et.

## **Konvertera tabell till CSV-API**

### Web-API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Begärparametrar:**

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning                                                                                                                             |
| ------------- | ----- | -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | Fil   | FormData                         | Ladda upp kalkylbladsfilen.                                                                                                            |
| worksheet     | Sträng | Frågesträng                       | Namn på kalkylbladet i kalkylbladsfilen.                                                                                               |
| tableName     | Sträng | Frågesträng                       | Namn på tabellen som ska konverteras.                                                                                                      |
| outPath       | Sträng | Frågesträng                       | (Valfritt) Mapp-sökväg där arbetsboken lagras; standardvärde är null.                                                                  |
| outStorageName| Sträng | Frågesträng                       | Namn på lagringsplatsen för utdatafilen.                                                                                                |
| fontsLocation | Sträng | Frågesträng                       | Sökväg för anpassade typsnitt.                                                                                                            |
| region        | Sträng | Frågesträng                       | Kalkylbladsregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och regionberoende beteende. |
| password      | Sträng | Frågesträng                       | Lösenord för att öppna kalkylbladsfilen.                                                                                              |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-statuskoder**

| Kod | Betydelse              | Beskrivning                                                       |
| --- | ---------------------- | ----------------------------------------------------------------- |
| 200 | OK                     | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan     | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering saknas   | Ogiltig eller saknad JWT-token.                                     |
| 413 | För stor nyttolast     | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel      | Oväntat serverfel.                                                |

## **Var bör du använda API:et för att konvertera tabell till CSV?**

- **Databasmigrering**: Konvertera Excel-tabeller till CSV för massimport till SQL-databaser (MySQL, PostgreSQL, SQL Server).
- **Data warehouse-laddning**: Omvandla Excel-baserade rapporttabeller till CSV för inläsning i Snowflake, Redshift eller BigQuery.
- **Bulk-API-begärningar**: Konvertera Excel-tabelldata till CSV för massuppladdning till REST-tjänster.
- **Tjänst-till-tjänst-kommunikation**: Använd CSV som ett lättviktigt datautbytesformat mellan mikrotjänster.
- **Förberedelse av maskininlärningsdata**: Konvertera funktionstabeller från Excel till CSV för användning med Python/R-baserade maskininlärningsbibliotek.
- **Statistisk analys**: Omvandla forskningsdata-tabeller till CSV för import till SPSS, SAS eller Stata.
- **Innehållsmigrering**: Flytta strukturerat innehåll från Excel till CMS-system via CSV.

## Varför bör du använda API:et för att konvertera tabell till CSV?

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling, samt har omfattande dokumentation. Jämfört med att bygga egna lösningar minskas utvecklingsarbetet betydligt.
- **Kostnadseffektivt**: Du kan konvertera tabelldata utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.
- **Rent datautdrag utan formatering**.
- **CSV stöds av nästan alla system**:
  - Databaser (alla större relationella DBMS)
  - programmeringsspråk (inbyggda tolkare i alla)
  - verksamhetsanalysverktyg (Tableau, Power BI, Looker)
  - kalkylbladsprogram (Excel, Google Sheets, LibreOffice)
  - kommandoradsverktyg (awk, sed, grep)

## Hur använder man API:et för att konvertera tabell till CSV med SDK:er?

### API-specifikation för konvertering av tabell till CSV

[API-specifikation för konvertering av tabell till CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att REST-interaktioner kan ske direkt från en webbläsare.
Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Blad1&tableName=Tabell1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@minArbetsbok.xlsx" \
  -o konverterad.csv
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodad)",
  "contentType": "MIME-typ",
  "fileDownloadName": "valfritt filnamn"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den döljer detaljer på lågnivå och låter dig konvertera tabelldata i kalkylblad till en CSV-fil med minimal kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}