---
title: "Aspose.Cells Cloud Web API – Konvertera Excel-diagram till bild – Gratis onlineverktyg"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar diagram i kalkylark till bild: Steg-för-steg-guide"
linktitle: "Konvertera diagram till bild"
type: docs
url: /sv/convert-chart-to-image/
keywords: "konvertera diagram till bild, Aspose.Cells, exportera Excel-diagram, PNG, SVG, JPEG, BMP, TIFF"
description: "Använd Aspose.Cells Cloud Web API för att konvertera ett Excel-diagram direkt till PNG-, SVG-, TIFF-, JPEG- eller BMP-bilder från en kalkylarksfil."
weight: 100
---

Excel-diagram är visuella representationer av data som kan infogas i kalkylblad. Att konvertera dessa diagram till bildformat gör det enkelt att återanvända dem i dokument, webbsidor och rapporter utan att behöva ha Excel installerat.

Konvertera ett diagram från ett lokalt kalkylark eller en Excel-fil till en bildfil. **STÖDDA BILDFORMAT:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **Konvertera diagram till bild – API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Parametrar för begäran:**

| ParameterName    | Typ     | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                          | Obligatoriskt |
| :--------------- | :------ | :-------------------------- | :----------------------------------------------------------------------------------- | :------------ |
| Spreadsheet      | Fil     | FormData                    | Ladda upp kalkylarksfilen som innehåller diagrammet.                                | Ja            |
| worksheet        | Sträng  | Frågesträng                 | Ange kalkylbladsnamnet om relevant.                                                  | Nej           |
| chartIndex       | Heltal  | Frågesträng                 | Index för det diagram som ska konverteras.                                           | Ja            |
| format           | Sträng  | Frågesträng                 | (Obligatoriskt) Önskad bildtyp (t.ex. svg, png, jpg).                               | Ja            |
| outPath          | Sträng  | Frågesträng                 | (Valfritt) Sökvägen till mappen där utdatafilen ska lagras; standardvärde är null.  | Nej           |
| outStorageName   | Sträng  | Frågesträng                 | Namn på lagringsutrymmet för utdatafilen.                                            | Nej           |
| fontsLocation    | Sträng  | Frågesträng                 | Ange anpassade teckensnitt om nödvändigt.                                            | Nej           |
| region           | Sträng  | Frågesträng                 | Ställ in kalkylarksregionen.                                                         | Nej           |
| password         | Sträng  | Frågesträng                 | Lösenord för att öppna kalkylarksfilen.                                              | Nej           |

## **Svar**

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

| Kod | Betydelse             | Beskrivning                                                         |
| --- | --------------------- | ------------------------------------------------------------------- |
| 200 | OK                    | Filter har tillämpats korrekt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).    |
| 401 | Otillåten (Unauthorized) | Ogiltig eller saknad JWT-token.                                    |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                   |
| 500 | Internt serverfel     | Oväntat serverfel.                                                  |

## Var bör du använda API:et för att konvertera diagram till bild?

- **Rapportgenerering och instrumentpaneler**: Konvertera automatiskt diagram från Excel-data till bilder (PNG, JPEG osv.) för infogning i PDF-rapporter, webbaserade instrumentpaneler eller PowerPoint-presentationer.
- **Webb-/e-postapplikationer**: Leverera diagrambilder direkt i webbsidor eller e-postmeddelanden utan att kräva att användare laddar ner eller öppnar Excel-filer. Användbar för dynamiska rapportverktyg, nyhetsbrev eller automatiska meddelanden.
- **Dokumentbearbetningsarbetsflöden**: Integrera i automatiserade pipeline (t.ex. fakturering, analys) där diagram från Excel behöver infogas i andra format (Word, PDF, HTML).
- **Mobil-/skrivbordsapplikationer**: Visa Excel-diagram i appar där fullständig kalkylarksuppladdning är onödig eller opraktisk.
- **Arkivering och visualisering**: Spara diagram som fristående bilder för långsiktig lagring, miniatyrer eller snabba förhandsvisningar utan beroende av Excel.

## Varför bör du använda API:et för att konvertera diagram till bild?

- **Bevara visuell trogenhet**: Bevarar exakt diagramformat (färger, etiketter, skalning) som visas i Excel, vilket garanterar professionell kvalitet i utdata.
- **Plattformsoberoende**: Ingen Excel-installation krävs. Fungerar plattformsoberoende (Windows, Linux, macOS) via REST API och är lämpligt för molnbaserade eller server-side-applikationer.
- **Automatisering och skalbarhet**: Konvertera flera diagram eller filer i batch via programmering, vilket sparar tid jämfört med manuell export. Hanterar stora volymer effektivt i molnet.
- **Flexibla utdataformat**: Stöder populära bildformat (PNG, JPG, BMP, SVG osv.), vilket möjliggör integration med olika system och medier.
- **Säkert och pålitligt**: Bearbeta filer i Asposes molnmiljö utan att utsätta känslig data för klientverktyg. Hög tillgänglighet och konsekvent prestanda.
- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga egna diagramrenderingslösningar minskar detta betydligt utvecklingsarbete.
- **Kostnadseffektivt**: Du kan konvertera diagram utan att först ladda upp hela arbetsboken, vilket sparar lagringsutrymme och minskar kostnader.

## Hur använder man API:et för att konvertera diagram till bild med SDK:er?

### API-specifikation för att konvertera diagram till bild

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">API-specifikationen för att konvertera diagram till bild</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljnivådetaljerna och gör det möjligt att konvertera ett diagram till en bild med kort kod.  
Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}

---