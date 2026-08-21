---
title: "Aspose.Cells Cloud Web API – Konvertera kalkylark till PDF"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar ett lokalt kalkylark till PDF med Aspose.Cells Cloud API"
linktype: "Konvertera kalkylark till PDF"
type: docs
url: /convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, kalkylark till PDF, Excel-konvertering, moln-API, PDF-generering, REST API, v4.0"
description: "Steg-för-steg-guide för att konvertera ett lokalt kalkylark till PDF med Aspose.Cells Cloud API. Innehåller begärsyntax, parametrar, svarsdetaljer, felhantering och praktiska användningsfall."
weight: 100
---

Slutpunkten **ConvertSpreadsheetToPdf** läser in ett kalkylark från en lokal enhet, bearbetar det på Aspose.Cells Cloud-servern och returnerar den resulterande PDF-filen som en binär ström. Denna molnbaserade konvertering eliminera behovet av att ladda upp källfilen till lagring, minskar resursförbrukningen och förenklar arbetsflöden genom att leverera PDF:en direkt till klienten. De format som stöds beror på underliggande bibliotek; API:et validerar filens existens, behörigheter och konverteringsintegritet, och kastar lämpliga HTTP-fel för ogiltiga indata eller bearbetningsfel.

## **Konvertera kalkylark till PDF API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

### **Begärparametrar:**

| Parameternamn   | Typ    | Plats    | Krävs/Valfri | Beskrivning                                                                                                                                                                                    |
| :-------------- | :----- | :------- | :----------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Fil    | FormData | Krävs        | Källkalkylarkfilen (XLS, XLSX, CSV osv.) som ska konverteras. Måste vara en giltig, läsbar fil; maximal storlek är 100 MB. Exempel: `mittArbetsbok.xlsx`.                                        |
| outPath         | Sträng | Fråga    | Valfri       | Målmappens sökväg där den konverterade PDF:en ska lagras på servern (om du vill spara den). Om utelämnas returneras filen direkt i svaret. Exempel: `/output/rapporter/`.                         |
| outStorageName  | Sträng | Fråga    | Valfri       | Namn på mållagrings tjänsten (t.ex. `MittMolnlager`). Krävs endast när `outPath` används och lagringen inte är standard.                                                                      |
| fontsLocation   | Sträng | Fråga    | Valfri       | Sökväg till en anpassad teckensnittsmapp på servern för att säkerställa korrekt textrendering i PDF:en. Exempel: `/fonts/anpassat/`.                                                             |
| region          | Sträng | Fråga    | Valfri       | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och språkspecifikt beteende.                                                     |
| password        | Sträng | Fråga    | Valfri       | Lösenord som krävs för att öppna ett skyddat kalkylark. Utelämna om filen inte är krypterad.                                                                                                   |

### **Svar**

Lyckat svar (200 OK)  
Content-Type: application/pdf  
Content‑Disposition: attachment; filename="konverterad.pdf"  
Content‑Length: `<storlek i byte>`

Kropp: binär ström av den genererade PDF-filen

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filtrering lyckades; svaret innehåller åtgärdsdetaljer.          |
| 400 | Ogiltig begäran       | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad     | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var ska vi använda API:et för att konvertera kalkylark till PDF?

- **Automatiserade rapporteringspipeline** – Konvertera dagligen genererade Excel-rapporter till PDF för arkivering eller e-postdistribution utan manuella steg.
- **Dokumenthanteringssystem** – Spara PDF:er direkt i ett DMS efter konvertering, och behåll källkalkylarket endast på klientsidan.
- **Webbapplikationer med export på begäran** – Låt slutanvändare ladda ner en PDF-version av ett kalkylark de redigerar i webbläsaren, med molnbaserad konvertering för att bevara layout.
- **Regelverksöverensstämmelse** – Skapa oföränderliga PDF-ögonblicksbilder av finanskalkylark för revisionsdokumentation, vilket säkerställer att källfilen aldrig lämnar klientmiljön.
- **Konverteringsarbetsflöden mellan format** – Kombinera med andra konverteringsändpunkter, t.ex. [Konvertera kalkylark till CSV](/convert-spreadsheet-to-csv/) API för att skapa arkiv i flera format.

## Varför bör du använda API:et för att konvertera kalkylark till PDF?

- **Uppgiftsflöde utan uppladdning** – Inget behov av att ladda upp källfilen till molnlagring; konverteringen sker direkt från den uppladdade strömmen, vilket sparar bandbredd och lagringskostnader.
- **Hög fidelity-rendering** – Aspose.Cells bevarar komplexa formler, diagram och formatering vid konvertering till PDF och matchar utdata från Excel på skrivbordet.
- **Skalbar molnbaserad körning** – Utnyttjar Asposes molninfrastruktur för snabb, tillförlitlig konvertering oavsett klientens hårdvara.
- **Enkelt REST-gränssnitt** – En enda `PUT`-begäran med valfria frågeparametrar; returnerar en PDF-ström redo att ladda ner, vilket gör integrationen enkel i valfritt programmeringsspråk.

## Hur man använder API:et för att konvertera kalkylark till PDF med SDK:er

### API-specifikation för Konvertera kalkylark till PDF

[API-specifikation för Konvertera kalkylark till PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@mittArbetsbok.xlsx" \
  -o konverterad.pdf
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

Att använda SDK:et är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljnivådetaljerna och tillåter dig att slå samman kalkylark med kort kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er. Följande kodexempel visar hur man interagerar med Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}