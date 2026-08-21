---
title: "Aspose.Cells Cloud Web API – Konvertera kalkylark till JSON"
second_title: "Dokument"
ArticleTitle: "Så här konverterar du ett lokalt kalkylark till JSON med Aspose.Cells Cloud API"
linktitle: "Konvertera kalkylark till JSON"
type: docs
url: /convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, konvertera kalkylark till JSON, Excel till JSON API, Aspose.Cells Cloud API, REST API, konvertering av kalkylark"
description: "Lär dig hur du konverterar lokala Excel-filer till JSON med Aspose.Cells Cloud API. Inkluderar endpoint, parametrar, exempelkod och felhantering för sömlös integration."
weight: 100
---

**ConvertSpreadsheetToJson**-endpoint konverterar ett kalkylark lagrat på en lokal enhet till en JSON-fil helt och hållet på Aspose.Cells Cloud-servern. Genom att skicka kalkylarket som `multipart/form-data` returnerar tjänsten en JSON-ström redo för nedladdning eller vidare bearbetning. Denna molnbaserade konvertering eliminerar behovet av först att ladda upp filen till lagring, minskar lagringskostnaderna och förenklar arbetsflödet för applikationer som kräver kalkylarksdata i JSON-format för analys, rapportering eller datautbyte.

**Förutsättningar**: Du måste ha ett Aspose Cloud-konto, en giltig JWT-åtkomsttoken och Aspose.Cells Cloud SDK eller API-nyckel konfigurerad.

**Bakgrund**: Att konvertera kalkylark till JSON är ett vanligt steg vid integration av Excel-data med webbtjänster, NoSQL-databaser eller klientsidiga JavaScript-applikationer. API:t för att konvertera kalkylark till JSON erbjuder snabb server-side-konvertering utan att behöva lagra originalfilen.

## API för att konvertera kalkylark till JSON

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameternamn   | Typ                        | Plats     | Krävs/valfri | Beskrivning                                                                                                                                                                    |
| :-------------- | :------------------------- | :-------- | :----------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Fil (multipart/form-data)  | FormData  | Krävs        | Källfilen för kalkylarket (t.ex. .xls, .xlsx, .xlsm). Exempel: `curl -F "Spreadsheet=@myfile.xlsx"`                                                                            |
| outPath         | Sträng                     | Query     | Valfri       | Målmappens sökväg i molnlagring där den konverterade JSON-filen ska sparas. Om utelämnas returneras JSON direkt i svarsströmmen. Exempel: `outPath=/output/`.                |
| outStorageName  | Sträng                     | Query     | Valfri       | Namn på molnlagringen (t.ex. Amazon S3, Azure Blob) där utdatafilen ska skrivas. Krävs endast när `outPath` används med en icke-standardlagring.                               |
| fontsLocation   | Sträng                     | Query     | Valfri       | Sökväg till en anpassad typsnittsmapp på servern. Använd detta när kalkylarket refererar till typsnitt som inte finns i standardbiblioteket.                                   |
| region          | Sträng                     | Query     | Valfri       | Inställning för kalkylarkets region/språk (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, datum och valuta vid konvertering.                                     |
| password        | Sträng                     | Query     | Valfri       | Lösenord för att öppna ett lösenordsskyddat kalkylark. Utelämna för oskyddade filer.                                                                                           |

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
| --- | ---------------------- | ----------------------------------------------------------------- |
| 200 | OK                     | Filtrering lyckades; svaret innehåller åtgärdsdetaljer.           |
| 400 | Felaktig begäran       | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig               | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast     | Uppladdad fil överskrider storleksgränsen.                        |
| 500 | Internt serverfel      | Oväntat serverfel.                                                |

## Var bör vi använda API:t för att konvertera kalkylark till JSON?

- **Dataöverföringspipeliner** – Konvertera äldre Excel-rapporter till JSON för inläsning i moderna NoSQL-databaser eller datadal.
- **Mobil- eller webbapplikationer** – Snabbt omvandla användaruppladdade kalkylark till JSON för klient-side-rendering utan att lagra originalfilen i molnet.
- **Automatiserad rapportering** – Generera JSON-förfrågningar till efterföljande analys tjänster (t.ex. Power BI, Tableau) direkt från kalkylarksinmatningar.
- **Serverless-funktioner** – Använd API:t i AWS Lambda eller Azure Functions för att utföra konverteringar i realtid utan att hantera temporär lagring.

## Varför bör du använda API:t för att konvertera kalkylark till JSON?

- Molnbaserad konvertering eliminerar behovet av att ladda upp stora filer till lagring innan bearbetning, vilket minskar latens och lagringskostnader.
- Enkelt begäranarbetsflöde: ladda upp kalkylarket och motta JSON i samma HTTP-anrop, vilket förenklar integrationslogiken.
- Stöder lösenordsskyddade och regionspecifika kalkylark, vilket säkerställer korrekt datarepresentation över olika regioner.
- Skalbar på Asposes infrastruktur – hanterar stora arbetsböcker och komplexa formler utan att påverka egna serverresurser.

## Hur använder man API:t för att konvertera kalkylark till JSON med SDK:er

### API-specifikation för att konvertera kalkylark till JSON

[API-specifikation för att konvertera kalkylark till JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

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

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljer på låg nivå och låter dig konvertera ett kalkylark till JSON med bara några rader kod.  
Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.  
Följande kodexempel visar hur du interagerar med Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}