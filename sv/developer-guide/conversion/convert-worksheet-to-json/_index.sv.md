---
title: "Aspose.Cells Cloud Web API – Konvertera kalkylblad till JSON"
second_title: "Dokument"
ArticleTitle: "Så här konverterar du ett kalkylarksblad till JSON med Aspose.Cells Cloud API"
linktitle: "Konvertera kalkylblad till JSON"
type: docs
url: /sv/convert-worksheet-to-json/
keywords: "Aspose.Cells, kalkylblad till JSON, Excel-konvertering, moln-API, API v4, dataexport"
description: "Steg-för-steg-guide för att konvertera ett Excel-kalkylblad till JSON med Aspose.Cells Cloud API, inklusive begärparametrar, svarshantering, felkoder och SDK-exempel."
weight: 100
---

**ConvertWorksheetToJson**-ändpunkten läser en kalkylarksfil från det lokala filsystemet, extraherar det angivna kalkylbladet och returnerar dess innehåll som en JSON-fil. Konverteringen utförs helt på Aspose.Cells Cloud-servrar, så ingen mellanliggande uppladdning eller lagring krävs. Den stöder lösenordsskyddade arbetsböcker, anpassade teckensnittsplatser och regionala inställningar, och levererar en snabb, molnbaserad lösning för att exportera kalkylbladsdata till JSON för vidare bearbetning.

## **Konvertera kalkylblad till JSON API**

### Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

### **Begärparametrar:**

| Parameternamn     | Typ    | Plats       | Obligatoriskt/valfritt | Beskrivning                                                                                                                                                                     |
| :---------------- | :----- | :---------- | :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet       | fil    | FormData    | Obligatoriskt         | Den Excel-arbetsbok som ska bearbetas. Måste vara ett format som stöds (xls, xlsx, csv, etc.). Skickas som multipart/form-data. Exempel: `Spreadsheet=@C:\Docs\Sample.xlsx`.    |
| worksheet         | sträng | Frågesträng | Obligatoriskt         | Exakt namn på det kalkylblad som ska konverteras (skiftlägeskänsligt). Om utelämnas eller inte hittas returnerar API:et ett fel. Exempel: `worksheet=Sheet1`.                    |
| outPath           | sträng | Frågesträng | Valfritt              | Målmapp på den konfigurerade molnlagringen där den genererade JSON-filen sparas. Om inte angiven returneras JSON direkt i svarsströmmen. Exempel: `outPath=/converted/`.        |
| outStorageName    | sträng | Frågesträng | Valfritt              | Namn på mållagringen (t.ex. "MyStorage") som innehåller `outPath`. Använder standardlagring om utelämnas.                                                                        |
| fontsLocation     | sträng | Frågesträng | Valfritt              | Servermapp som innehåller anpassade teckensnitt som krävs för korrekt återgivning av text i kalkylbladet. Exempel: `fontsLocation=/fonts/custom/`.                             |
| region            | sträng | Frågesträng | Valfritt              | Kultur-/regionidentifierare som påverkar nummer-, datum- och valutainställningar i den genererade JSON-filen (t.ex. `sv-SE`, `en-US`, `fr-FR`).                                 |
| password          | sträng | Frågesträng | Valfritt              | Lösenord för att öppna en krypterad arbetsbok. Om arbetsboken inte är lösenordsskyddad kan denna parameter utelämnas.                                                           |

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

| Kod | Beteende              | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | Payload för stor      | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör vi använda API:et för att konvertera kalkylblad till JSON?

- **Webbdashboards** – Exportera kalkylbladsdata till JSON för klientsidans diagrambibliotek (t.ex. Chart.js, D3.js).
- **Datamigrering** – Flytta äldre Excel-data till NoSQL-databaser eller REST-tjänster som tar emot JSON.
- **Mobil- eller offlineappar** – Konvertera kalkylbladsinnehåll till JSON på servern, och synkronisera sedan den lätta payload till mobila enheter.
- **Rapporteringspipelines** – Mata in kalkylbladsdata direkt i analystjänster som accepterar JSON som indata utan mellansteg med CSV.

## Varför bör du använda API:et för att konvertera kalkylblad till JSON?

- **Arbetsflöde utan uppladdning** – Bearbeta lokala filer i molnet utan att först ladda upp dem till lagring, vilket sparar bandbredd och lagringskostnader.
- **Fullständig konvertering** – Stöder lösenordsskyddade arbetsböcker, anpassade teckensnitt och regional formatering för exakt datarepresentation.
- **Snabb och skalbar körning** – Utnyttjar Aspose.Cells högpresterande motor i molninfrastruktur och hanterar stora kalkylblad effektivt.
- **Enkel integration** – Ett enda PUT-anrop returnerar en redo-användbar JSON-fil eller lagrar den direkt, vilket minskar kodkomplexiteten i klientprogram.

## Hur man använder API:et för att konvertera kalkylblad till JSON med SDK:er

### API-specifikation för att konvertera kalkylblad till JSON

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">API-specifikationen för att konvertera kalkylblad till JSON</a> tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och låter dig arbeta med kalkylblad med kompakt kod. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.  
Följande kodexempel visar hur du interagerar med Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}