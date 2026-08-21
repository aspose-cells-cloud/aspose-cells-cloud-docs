---
title: "Aspose.Cells Cloud Web API – Konvertera lokalt Excel-tabelldata till en bildfil – Gratis onlineverktyg"
second_title: "Dokument"
ArticleTitle: "Så här konverterar du lokalt kalkylbladstabelldata till en bildfil: Steg-för-steg-guide"
linktitle: "Konvertera tabell till bild"
type: docs
url: /convert-table-to-image/
keywords: "Aspose.Cells, molntjänst-API, konvertera tabell till bild, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Konvertera lokalt Excel-kalkylbladstabell till en bildfil snabbt med Aspose.Cells Cloud API. Stöder PNG, JPEG, TIFF, BMP, SVG och andra format."
weight: 100
---

Exportera tabelldata från en lokal Excel-fil till en [bildfil](https://docs.fileformat.com/image/) med Moln-API:t.

**STÖDDA BILDFORMAT:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Konvertera tabell till bild – API**

Innan du använder denna slutpunkt, se till att du har följande förutsättningar:

- En giltig JWT-åtkomsttoken som du får genom Aspose.Cells Cloud-autentisering.
- Ett åtkomligt lagringskonto om du vill använda parametrarna `outPath` eller `outStorageName`.
- Källarbetsboken (lokal Excel-fil) måste vara läsbar och, om den är lösenordsskyddad, måste rätt lösenord anges.

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäransparametrar:**

| Parameternamn  | Typ    | Sökväg/frågesträng/HTTP-nyttolast | Beskrivning                                                                                                                           |
| :------------- | :----- | :------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | Fil    | FormData                        | Ladda upp kalkylbladsfilen.                                                                                                          |
| worksheet      | Sträng | Fråga                           | Namnet på kalkylbladet i kalkylblads-/Excel-filen.                                                                                  |
| tableName      | Sträng | Fråga                           | Namnet på den tabell som ska konverteras.                                                                                            |
| format         | Sträng | Fråga                           | Önskat bildfilformat (t.ex. png, svg).                                                                                               |
| outPath        | Sträng | Fråga                           | (Valfritt) Sökvägen till mappen där den konverterade bilden ska sparas. Standard är null.                                          |
| outStorageName | Sträng | Fråga                           | Anger lagringsnamnet för utdatafilen.                                                                                                |
| fontsLocation  | Sträng | Fråga                           | Använd anpassade teckensnitt om nödvändigt.                                                                                          |
| region         | Sträng | Fråga                           | Kalkylbladets region/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, datumtolkning och regionala beteenden. |
| password       | Sträng | Fråga                           | Lösenord som krävs för att komma åt kalkylbladsfilen.                                                                                |

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

| Kod | Betydelse               | Beskrivning                                                      |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Oauktoriserad         | Ogiltig eller saknad JWT-token.                                  |
| 413  | Nyttolast för stor    | Den uppladdade filen överskrider storleksgränsen.                |
| 500  | Internt serverfel     | Oväntat serverfel.                                               |

## **Var bör du använda API:t för att konvertera tabell till bild?**

- **Statiska rapportögonblicksbilder**: Konvertera finansiella tabeller, beräkningsresultat eller andra formaterade data till bilder för inkludering i PDF-rapporter, PowerPoint-bildspel eller utskriftsdokument där redigering inte krävs.
- **Datavisualisering i presentationer**: Gör komplexa kalkylbladstabeller – inklusive villkorsformatering eller enkel visualisering – om till bilder som kan bäddas in i presentationer (PPTX, Google Slides).
- **Dokumentation och utbildningsmaterial**: Fånga upp kalkylbladsexempel, mallar eller inmatningsformulär som bilder för användarhandböcker, handledningar eller kunskapsbasartiklar.
- **Miniatyrbildsförhandsvisningar**: Skapa små förhandsvisningsbilder av viktiga kalkylbladsavsnitt för filbläddrare, dokumentbibliotek eller sökresultat.

## **Varför bör du använda API:t för att konvertera tabell till bild?**

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga egna renderingslösningar minskar detta betydligt utvecklingsarbete.
- **Kostnadseffektivt**: Du kan konvertera tabelldata utan att först ladda upp hela arbetsboken, vilket sparar lagringsutrymme och minskar kostnader.
- **Pixel-perfekt bevarande**: Återskapar Excel:s utseende troget – inklusive cellformatering, formler (visade värden), ramar, färger och villkorsformatering – i utdatafilen.
- **Universell kompatibilitet**: Bildformat (PNG, JPEG, TIFF, BMP, SVG, etc.) kan visas på alla enheter eller plattformar utan specialprogramvara, vilket säkerställer maximal tillgänglighet.

## **Hur använder du API:t för att konvertera tabell till bild med SDK:er?**

### API-specifikation för konvertering av tabell till bild

[API-specifikationen för konvertering av tabell till bild](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Moln-API:t med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Blad1&tableName=Tabell1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@minArbetsbok.xlsx" \
  -o konverterad.png
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och gör det möjligt att konvertera kalkylbladstabelldata till en bild med minimal kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}