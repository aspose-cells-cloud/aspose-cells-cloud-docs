---
title: "Konvertera kalkylblad till CSV – Aspose.Cells Cloud API-dokumentation"
second_title: "Dokument"
ArticleTitle: "Så här konverterar du ett kalkylarkskalkylblad till CSV med Aspose.Cells Cloud API"
linktitle: "Konvertera kalkylblad till CSV"
type: docs
url: /sv/convert-worksheet-to-csv/
keywords: "Aspose.Cells, CSV-konvertering, kalkylblad till CSV, REST API, molnkalkylark, Excel till CSV"
description: "Lär dig hur du konverterar ett specifikt kalkylblad från en Excel-fil till CSV med Aspose.Cells Cloud API (v4.0). Innehåller slutpunkt, parametrar, exempel på cURL, SDK-kod och felhantering."
weight: 100
---

**ConvertWorksheetToCsv**-slutpunkten omvandlar ett enskilt kalkylblad från en lokal kalkylarkfil till ett CSV-dokument helt på Aspose.Cells Cloud-servern. Genom att ladda upp källfilen och ange det önskade kalkylbladet får utvecklare en binär CSV-ström utan att behöva lagra filen i molnlagring. Denna API är idealisk för att automatisera datautvinning, integrera kalkylarksdata i efterföljande system och minska lagringsöverhead.

## Konvertera kalkylblad till CSV API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäranparametrar

| ParameterName | Typ    | Plats    | Krävs/Valfritt | Beskrivning                                                                                                                                 |
| :------------- | :----- | :------- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | Fil    | FormData | **Krävs**       | Binär fil för källkalkylarket (t.ex. `.xlsx`, `.xls`). Exempel: `myWorkbook.xlsx`.                                                         |
| worksheet      | Sträng | Query    | **Krävs**       | Namn på det kalkylblad som ska konverteras (skiftlägeskänsligt). Om utelämnas används det första kalkylbladet. Exempel: `Sheet1`.           |
| outPath        | Sträng | Query    | Valfritt         | Målmappens sökväg i molnlagring där den genererade CSV-filen ska sparas. Om utelämnas returneras CSV direkt i svarsströmmen.               |
| outStorageName | Sträng | Query    | Valfritt         | Namn på lagringstjänsten (t.ex. Azure, AWS S3) där utdatafilen ska placeras. Krävs endast när `outPath` används.                          |
| fontsLocation  | Sträng | Query    | Valfritt         | Sökväg till en anpassad teckensnittsmapp på servern, vilket gör att konverteringsmotorn kan använda icke-standardskriftsnitt.              |
| region         | Sträng | Query    | Valfritt         | Språk-ID som påverkar nummer-/datumformatering i CSV (t.ex. `sv-SE`, `en-US`, `fr-FR`).                                                     |
| password       | Sträng | Query    | Valfritt         | Lösenord för att öppna ett skyddat kalkylark. Måste matcha källfilens krypteringslösenord.                                                 |

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

| Kod | Betydelse              | Beskrivning                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärddetaljer. |
| 400  | Felaktig begäran       | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401  | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413  | Payload för stor      | Uppladdad fil överskrider storleksgränsen.                        |
| 500  | Internt serverfel      | Oväntat serverfel.                                                |

## När ska man använda API:et för att konvertera kalkylblad till CSV?

- **Datautvinning för BI-pipelines** – Extrahera ett specifikt kalkylblad från en Excel-rapport och mata direkt in den resulterande CSV-filen i Power BI eller Tableau utan mellanliggande filhantering.
- **Automatiserad fakturahantering** – Konvertera kalkylbladet som innehåller fakturarader till CSV för snabb import i bokföringssystem.
- **Integration med äldre system** – Exportera kalkylbladsdata till CSV för användning av äldre applikationer som endast accepterar avgränsade textfiler.
- **Direktgenerering av rapporter** – Generera CSV-ögonblicksbilder av live-kalkylarksdata i en webbtjänst och returnera filen omedelbart till klientens webbläsare.

## Varför använda API:et för att konvertera kalkylblad till CSV?

- **Ingen permanent molnlagring krävs** – Filen strömmas direkt till konverteringsmotorn och kasseras efter konvertering, vilket sparar bandbredd och lagringskostnader.
- **Hög prestanda i molnmiljö** – Konverteringen körs på Asposes optimerade servrar och tar vanligtvis högst 2 sekunder för filer upp till 100 MB.
- **Finjusterad kontroll** – Välj ett enskilt kalkylblad, tillämpa anpassade teckensnitt, regional formatering och lösenordsskydd i en enda begäran.
- **Konsekvent plattformsövergripande utdata** – Garanterar identisk CSV-utdata över .NET, Java, Python och andra SDK:er som använder samma REST-slutpunkt.

## Hur man använder API:et för att konvertera kalkylblad till CSV med SDK:er

### API-specifikation för att konvertera kalkylblad till CSV

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">API-specifikation för att konvertera kalkylblad till CSV</a> tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
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

Användning av SDK:n förenklar utvecklingen genom att abstrahera bort lågnivådetaljer, så att du kan sammanfoga kalkylark med varandra med koncist kod. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}