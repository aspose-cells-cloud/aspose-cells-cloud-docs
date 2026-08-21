---
title: "Aspose.Cells Cloud Web API – Konvertera kalkylark till CSV"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar ett kalkylark till CSV med Aspose.Cells Cloud API"
linktitle: "Konvertera kalkylark till CSV"
type: docs
url: /sv/convert-spreadsheet-to-csv/
keywords: "Aspose Cells, CSV-konvertering, Excel API, molnkonvertering"
description: "Lär dig hur du konverterar Excel-filer (XLS, XLSX, XLSM osv.) till CSV med Aspose.Cells Cloud API. Innehåller autentiseringssteg, cURL-exempel, SDK-kodavsnitt och felhantering."
weight: 100
---

**ConvertSpreadsheetToCsv**-ändpunkten läser in ett kalkylark som laddats upp från en lokal enhet, utför konverteringen helt på Aspose.Cells Cloud-servrar och returnerar den resulterande CSV-filen som en binär ström. Denna molnbasera operation eliminerar behovet av att ladda upp källfilen till molnlagring, minskar lagringskostnader och förenklar arbetsflödet för utvecklare som behöver snabb konvertering från kalkylark till CSV. Stödda format beror på de underliggande biblioteken, och korrekt behörighet krävs för att läsa källfilen. Fel som saknade filer, ogiltiga förfrågningar eller konverteringsfel returneras med standard HTTP-statuskoder.

## **Konvertera kalkylark till CSV API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar:**

| Parameter Name   | Typ    | Plats     | Krävs     | Beskrivning                                                                                                                                                                |
| :--------------- | :----- | :-------- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fil    | FormData  | Krävs     | Kalkylarksfilen som ska konverteras. Godkänner vanliga format som .xls, .xlsx, .xlsm. Måste anges som multipart/form‑data. Exempel: `myWorkbook.xlsx`.                      |
| outPath          | Sträng | Fråga     | Valfritt  | Målmappens sökväg där den konverterade CSV-filen ska sparas. Om utelämnas returneras CSV direkt i svarskroppen. Exempel: `/output/reports/`.                                |
| outStorageName   | Sträng | Fråga     | Valfritt  | Namn på molnlagringstjänsten där utdatafilen ska sparas. Om inte angiven används standardlagringen som konfigurerats för Aspose.Cells-kontot.                              |
| fontsLocation    | Sträng | Fråga     | Valfritt  | Sökväg till en mapp med anpassade typsnitt som krävs av kalkylarket. möjliggör korrekt visning av celler som använder icke-standardtypsnitt.                                 |
| region           | Sträng | Fråga     | Valfritt  | Kalkylarkets regionspråkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och språkspecifika beteenden.                               |
| password         | Sträng | Fråga     | Valfritt  | Lösenord för att öppna lösenordsskyddade kalkylark. Om filen är krypterad och lösenordet saknas eller är felaktigt returneras ett 400/401-fel.                               |

### **Svar**

Vid lyckad förfrågan returnerar API:et **HTTP 200** (eller **202** för asynkron bearbetning) med headern `Content-Type: application/octet-stream`. Svarskroppen innehåller den genererade CSV-filen som en binär ström.

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

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filtrering lyckades; svaret innehåller åtgärdens detaljer.       |
| 400 | Ogiltig förfrågan     | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Oauktoriserad         | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör du använda API:et för att konvertera kalkylark till CSV?

- **Dataexport för rapporteringssystem** – Generera CSV-extrakt från Excel-baserade rapporter för att mata in data i BI-verktyg eller datalagrum utan manuell filhantering.
- **Automatiserad batchbearbetning** – Konvertera stora mängder lokalt lagrade kalkylark till CSV i ett serverseit jobb, och strömma sedan resultaten direkt till efterföljande tjänster.
- **Webbapplikationer med filuppladdning** – Låt slutanvändare ladda upp en Excel-fil och omedelbart få en CSV-version för vidare analys eller import till andra plattformar.
- **Integration med äldre system** – Översätt äldre kalkylarkformat till CSV för system som endast accepterar textbaserade filer med avgränsare.

## Varför använda API:et för att konvertera kalkylark till CSV?

- **Arkitektur utan uppladdning till molnlagring** – Behöver inte lagra källfilen i molnlagring; konverteringen sker direkt från den uppladdade strömmen, vilket sparar tid och lagringskostnader.
- **Högpresterande molnbearbetning** – Använder Aspose.Cells optimerade konverteringsmotor på skalbara moln servrar och levererar snabb CSV-utdata även för stora arbetsböcker.
- **Enkel integration** – Enkel PUT-förfrågan med valfria frågeparametrar; returnerar CSV som en färdig nedladdningsbar binär ström, vilket eliminerar efterbehandlingsskeden.
- **Full funktionsunderstöd** – Hanterar lösenordsskyddade filer, anpassade typsnitt och språkspecifika inställningar för att säkerställa korrekt konvertering av komplexa kalkylark.

## Hur man använder API:et för att konvertera kalkylark till CSV med SDK:er

### **API-specifikation för att konvertera kalkylark till CSV**

[API-specifikation för att konvertera kalkylark till CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Använd Aspose.Cells Cloud SDK:er**

Att använda SDK är det snabbaste sättet att utveckla, eftersom den döljer de detaljerade tekniska detaljerna och låter dig arbeta med kalkylark med koncist kod. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er. Följande kodexempel visar hur man interagerar med Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}