---
title: "Aspose.Cells Cloud Web API – Konvertera lokalt Excel-tabelldata till PDF-fil – Gratis onlineverktyg"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar lokalt kalkylarkstabelldata till PDF-fil: Steg-för-steg-guide"
linktitle: "Konvertera tabell till PDF"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells, Excel till PDF, Tabellkonvertering, moln-API"
description: "Konvertera en lokal Excel-tabell till en PDF-fil snabbt med Aspose.Cells Cloud REST API."
weight: 100
---

Exportera tabelldata från en lokal Excel-fil till en PDF-fil med moln-API:t.

## **Konvertera tabell till PDF-API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar:**

| Parameternamn     | Typ    | Path/Query String/HTTPBody | Beskrivning                                                                                     |
| :---------------- | :----- | :------------------------- | :---------------------------------------------------------------------------------------------- |
| Spreadsheet       | Fil    | FormData                   | Ladda upp kalkylarksfilen som ska konverteras.                                                  |
| worksheet         | Sträng | Query                      | Namnet på kalkylbladet i kalkylarket.                                                           |
| tableName         | Sträng | Query                      | Namnet på tabellen som ska konverteras.                                                         |
| outPath           | Sträng | Query                      | (Valfritt) Mappens sökväg där den konverterade PDF-filen kommer att lagras. Standard är null. |
| outStorageName    | Sträng | Query                      | Ange namnet på lagringsutmatningen.                                                             |
| fontsLocation     | Sträng | Query                      | Använd anpassade typsnitt för PDF-filen.                                                        |
| region            | Sträng | Query                      | Anger regioninställningen för kalkylarket.                                                      |
| password          | Sträng | Query                      | Lösenord för åtkomst till kalkylarksfilen.                                                      |

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

**Exempel på svarshuvuden**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## **Var bör du använda API:et för att konvertera tabell till PDF?**

- **Ekonomiska rapporter**: Konvertera balansrakningar, resultatredovisningar (specifika tabeller) till PDF för revisionsklar dokumentation.
- **Försäljningsrapporter**: Omvandla försäljningsdashboards eller provisionberäkningar till distribuerbara PDF-filer.
- **Operationella metriker**: Exportera KPI-tabeller och prestandametriker som formella PDF-rapporter.
- **Kontraktsdata**: Exportera prislistor och avtalsvillkor från kalkylark till PDF-bilagor.
- **Revisionsspår**: Bevara finansiella datatabeller som oföränderlig PDF-bevismaterial.
- **Portföljsammanfattningar**: Exportera investeringsprestandatabeller som kundklara PDF-rapporter.
- **Kvalitetskontrollrapporter**: Exportera inspektionsdatatabeller till PDF för efterlevnadsdokumentation.
- **Lageröversikter**: Omvandla lagerivåtabeller till PDF för ledningsgranskning.

## **Varför bör du använda API:et för att konvertera tabell till PDF?**

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskas utvecklingsarbetet avsevärt.
- **Kostnadseffektivt**: Du kan konvertera tabelldata utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.
- **Bevarar avancerad Excel-formatering** i ett universellt tillgängligt PDF-format.

## **Hur använder du API:et för att konvertera tabell till PDF med SDK:er?**

### Specifikation för API:et för att konvertera tabell till PDF

[Specifikationen för API:et för att konvertera tabell till PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.
Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och låter dig konvertera kalkylarkstabelldata till en PDF-fil med minimal kod. Besök [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}