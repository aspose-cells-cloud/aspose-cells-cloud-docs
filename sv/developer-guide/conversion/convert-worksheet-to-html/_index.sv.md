---
title: "Aspose.Cells Cloud Web API – Konvertera kalkylblad till HTML"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar ett kalkylblad till HTML med Aspose.Cells Cloud API"
linktitle: "Konvertera kalkylblad till HTML"
type: docs
url: /convert-worksheet-to-html/
description: "Lär dig hur du konverterar ett Excel-kalkylblad till HTML med Aspose.Cells Cloud API – utan uppladdning, anpassade teckensnitt, regionsinställningar och felhantering."
keywords: "Aspose.Cells, Excel till HTML, konvertering av kalkylblad, moln-API"
weight: 100
---

**ConvertWorksheetToHtml**-slutpunkten läser en Excel-arbetsbok från det lokala filsystemet, extraherar det angivna kalkylbladet och returnerar innehållet som en HTML-fil. Konverteringen sker helt på Asposes molntjänster, så ingen mellanliggande uppladdning eller lagring krävs. Idealisk för att skapa webbklara vyer av kalkylbladsdata, stöder API:t valfria utdatapathar, anpassade teckensnitt, regionsinställningar och lösenordsskyddade arbetsböcker.

## Konvertera kalkylblad till HTML API

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameternamn     | Typ    | Plats    | Krävs/Valfritt | Beskrivning                                                                                                                                                                                                 |
| :---------------- | :----- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Fil    | Krävs    | FormData       | Binär Excel-fil som ska bearbetas. Måste vara en giltig .xlsx-, .xls-, .xlsb-fil etc. Exempel: `myWorkbook.xlsx`. Excel-filen läses direkt från begäran; ingen tidigare uppladdning till molnlagring krävs. |
| worksheet         | Sträng | Krävs    | Frågeparameter | Namn på det kalkylblad som ska konverteras (skiftlägeskänsligt). Måste finnas i den angivna arbetsboken. Exempel: `Sheet1`.                                                                                 |
| outPath           | Sträng | Valfritt | Frågeparameter | Målmappens sökväg (i molnlagring) där den genererade HTML-filen ska sparas. Om utelämnad returneras filen direkt i svaret. Exempel: `/output/html/`.                                                     |
| outStorageName    | Sträng | Valfritt | Frågeparameter | Namn på den molnlagringstjänst som ska användas för `outPath`. Krävs endast om `outPath` pekar på en icke-standardlagring.                                                                                |
| fontsLocation     | Sträng | Valfritt | Frågeparameter | Absolut sökväg till en mapp som innehåller anpassade TrueType/OpenType-teckensnitt som ska användas vid konverteringen. Möjliggör korrekt visning av icke-standardtecken.                                   |
| region            | Sträng | Valfritt | Frågeparameter | Språkidentifikator som påverkar formatering av tal/datum (t.ex. `sv-SE`, `en-US`, `fr-FR`). Standardvärde är arbetsbokens interna regionsinställning.                                                      |
| password          | Sträng | Valfritt | Frågeparameter | Lösenord som krävs för att öppna en skyddad arbetsbok. Utelämna för oskyddade filer.                                                                                                                        |

### Svar

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

| Kod | Betydelse             | Beskrivning                                                              |
| --- | --------------------- | ------------------------------------------------------------------------ |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).         |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                          |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                        |
| 500 | Internt serverfel     | Oväntat serverfel.                                                       |

## Var ska vi använda API:et för att konvertera kalkylblad till HTML?

- **Inbädda live-kalkylbladsdata i en webbportalsida** – Konvertera ett finansrapportkalkylblad till HTML för direkt visning i webbläsare utan att kräva Excel-tillägg.
- **Generera utskriftsvänliga HTML-fakturor från Excel-mall** – Automatisera skapandet av webbklara fakturasidor från fördefinierade kalkylblad.
- **Skapa dokumentationsutdrag** – Konvertera designspecifikationsblad till HTML-fragment som kan infogas i tekniska manualer eller wikis.
- **Utveckla BI-dashboards med låg kodbeskrivning** – Hämta kalkylbladsdata, konvertera den till HTML och visa den i anpassade dashboard-widgetar.

## Varför bör du använda API:et för att konvertera kalkylblad till HTML?

- **Arbetsflöde utan uppladdning** – Konvertera lokala filer direkt i molnet, vilket eliminierar behovet av att överföra stora arbetsböcker till lagring först.
- **Högpresterande rendering** – Server-side-konvertering använder Asposes optimerade motor, vilket ger snabb och exakt HTML-utdata.
- **Full kontroll över utdata** – Valfria parametrar (anpassade teckensnitt, region, lösenord) låter dig anpassa HTML till lokala krav och varumärkesriktlinjer.
- **Sömlös integration** – Enkel PUT-begäran med multipart/form-data passar naturligt i CI/CD-pipelines, mikrotjänster eller serverlösa funktioner.

## Hur man använder API:et för att konvertera kalkylblad till HTML med SDK:er

### API-specifikation för att konvertera kalkylblad till HTML

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">API-specifikation för att konvertera kalkylblad till HTML</a> tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

Att använda SDK:et är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljerna på låg nivå och låter dig sammanfoga kalkylblad med kort och koncist kod.  
Kolla in <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud SDK GitHub-repositoriet</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.  
Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}
