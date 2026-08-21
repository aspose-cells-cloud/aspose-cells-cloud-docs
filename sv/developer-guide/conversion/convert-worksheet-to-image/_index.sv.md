---
title: "Arbetsbladskonvertering – Aspose.Cells Cloud API-dokumentation"
second_title: "Dokument"
ArticleTitle: "Så här konverterar du lokalt arbetsbladsspreadsheetdata till en bildfil: Steg-för-steg-guide"
linktype: "Konvertera arbetsblad till bild"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, arbetsblad till bild, konvertera arbetsblad till bild, Excel till PNG, Excel till SVG, Excel till TIFF, Excel till JPEG, Excel till BMP, API för bildkonvertering, REST API, export av spreadsheetbilder, SDK-exempel"
description: "Steg-för-steg-guide för att konvertera ett Excel-arbetsblad till bildformat (PNG, SVG, TIFF, JPEG, BMP, etc.) med Aspose.Cells Cloud API, inklusive begärparametrar, svarsinformation, felkoder, användningsscenarier och SDK-kodexempel."
weight: 100
---

Exportera data från ett arbetsblad i en lokal Excel-fil till en [Image](https://docs.fileformat.com/image/)-fil med Aspose.Cells Cloud API. Denna åtgärd stöder flera bildformat och är idealisk för att skapa visuella ögonblicksbilder av spreadsheetdata.

**STÖDT BILDFORMAT**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Konvertera arbetsblad till bild-API**

### Web-API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parameternamn  | Typ    | Path/Query String/HTTPBody | Beskrivning                                                                                      |
| :------------- | :----- | :------------------------- | :----------------------------------------------------------------------------------------------- |
| Spreadsheet    | Fil    | FormData                   | Ladda upp spreadsheetfilen.                                                                      |
| worksheet      | Sträng | Query                      | Namn på det arbetsblad som ska konverteras.                                                      |
| format         | Sträng | Query                      | Önskat bildformat (`svg`, `png`, `tiff`, `jpeg`, `bmp`, etc.).                                  |
| outPath        | Sträng | Query                      | _(Valfritt)_ Mappväg där utdatabilden ska lagras; standardvärdet är `null`.                      |
| outStorageName | Sträng | Query                      | Namn på lagringsplatsen för utdatafilen.                                                         |
| fontsLocation  | Sträng | Query                      | Sökväg till en anpassad teckensnittsmapp om du behöver använda teckensnitt som inte finns på servern. |
| region         | Sträng | Query                      | Inställning för spreadsheetregion (t.ex. `sv-SE`, `en-US`).                                      |
| password       | Sträng | Query                      | Lösenord som krävs för att öppna en skyddad spreadsheetfil.                                      |

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

| Kod | Betydelse             | Beskrivning                                                     |
| --- | --------------------- | --------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten             | Ogiltig eller saknad JWT-token.                                 |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.               |
| 500 | Internt serverfel     | Oväntat serverfel.                                              |

## **Var bör du använda API:et för att konvertera arbetsblad till bild?**

- **Statiska rapportögonblicksbilder** – Konvertera finansiella tabeller, beräkningar eller annan data till bilder för inkludering i PDF-rapporter, PowerPoint-bilder eller utskriftsdokument där redigering inte krävs.
- **Datavisualisering i presentationer** – Omvandla komplexa spreadsheettabeller (inklusive villkorsformatering eller enkla diagram) till bilder som kan bäddas in i presentationer (PPTX, Google Slides).
- **Dokumentation och utbildningsmaterial** – Fånga exempel, mallar eller inmatningsformulär i spreadsheets som bilder för användarhandböcker, handledningar eller kunskapsdatabasartiklar.
- **Miniatyrbildsförhandsvisningar** – Skapa små förhandsvisningsbilder av viktiga spreadsheetavsnitt för filbläddrare, dokumentbibliotek eller sökresultat.

## **Varför bör du använda API:et för att konvertera arbetsblad till bild?**

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga en egen lösning för diagramrendering minskar detta markant utvecklingsarbetet.
- **Kostnadseffektivt** – Du kan konvertera tabelldata utan att först lagra arbetsboken permanent, vilket sparar lagringsutrymme och minskar kostnaderna.
- **Pixel-perfekt bevarande** – Troget återskapar Excel-utseendet – inklusive cellformatering, formler (som visade värden), kanter, färger och villkorsformatering – i utdatabilden.
- **Allmän kompatibilitet** – Bildformat (PNG, JPEG, TIFF, BMP, SVG, etc.) kan visas på alla enheter eller plattformar utan specialiserad programvara, vilket säkerställer maximal tillgänglighet.

## **Hur använder du API:et för att konvertera arbetsblad till bild med SDK:er?**

### Konvertera arbetsblad till bild-API-specificering

[Konvertera arbetsblad till bild-API-specificeringen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

Att använda ett SDK är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljer på låg nivå och låter dig konvertera arbetsbladdata till en bild med minimal kod. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}