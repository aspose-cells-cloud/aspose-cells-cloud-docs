---
title: "Aspose.Cells Cloud Excel-komprimering – Webb-API för att minska styrarkfilens storlek programmeringsmässigt"
second_title: "Dokument"
ArticleTitle: "Så här komprimerar du Excel-filer – minska styrarksfilens storlek och optimerar prestanda"
linktitle: "Komprimera styrark"
type: docs
url: /sv/compress-spreadsheet/
keywords: "Excel-komprimering, Aspose.Cells Cloud, minskning av styrarksfilens storlek, API, optimering av arbetsbok"
description: "Lär dig hur du komprimerar Excel-arbetsböcker med Aspose.Cells Cloud API. Få steg-för-steg-exempel, parametrar, autentisering och bästa praxis."
weight: 100
---

Komprimera Excel-styrark programmeringsmässigt och minska filstorleken med Aspose.Cells Cloud API. Optimera arbetsbokens prestanda genom att ta bort oanvänt data, komprimera inbäddade objekt och rensa formatering. Detta REST-baserade API möjliggör automatiserade Excel-filkomprimerings- och optimeringsarbetsflöden.

## **API för komprimering av styrark**

### Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäransparametrar

| Parametername | Typ    | Path/Query/String/HTTP Body | Beskrivning                                                                                                                           |
| -------------- | ------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Fil    | FormData                    | **Obligatoriskt.** Källfilen för Excel-arbetsboken (`.xlsx`, `.xls`, etc.) som ska komprimeras.                                      |
| level          | Heltal | Query                       | **Valfritt.** Komprimeringsintensitet (0 = snabbast/lägst, 9 = långsammast/högst). Om utelämnas tillämpas en balanserad standardvärde (5). |
| outPath        | Sträng | Query                       | **Valfritt.** Målmappens sökväg i din molnlagring. Om utelämnas sparas filen i samma mapp som källarbetsboken.                        |
| outStorageName | Sträng | Query                       | **Obligatoriskt.** Identifierare för den konfigurerade molnlagringstjänsten (t.ex. `CorporateDrive`).                                |
| region         | Sträng | Query                       | **Valfritt.** Språkinställning (t.ex. `sv-SE`) som kan påverka region-specifik datahantering.                                        |
| password       | Sträng | Query                       | **Valfritt.** Lösenord för att dekryptera en skyddad styrark. Lämna tomt om filen inte är krypterad.                                  |

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

| Kod | Betydelse             | Beskrivning                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Komprimering lyckades; svaret innehåller åtgärdens detaljer.     |
| 400  | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401  | Auktorisering nekad   | Ogiltig eller saknad JWT-token.                                   |
| 413  | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500  | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör vi använda API:et för komprimering av styrark?

- **Automatiserad rapportdistribution** – Komprimera månadsvisa finansrapporter innan de skickas per e-post för att säkerställa framgångsrik leverans och förbättra mottagarnas upplevelse.
- **Optimering av användarfiluppladdning** – Komprimera uppladdade Excel-filer i bakgrunden för att spara plats i molnlagringen och minska lagringskostnaderna.
- **Dataflödesbearbetning och migration** – Komprimera mellanliggande Excel-filer som genereras under ETL-processer för att snabba upp nätverksöverföringar och minska belastningen på temporär lagring.

## Varför bör du använda API:et för komprimering av styrark?

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling med omfattande dokumentation.
- **Lägre arbetskostnad** – Upphäver behovet av personer som manuellt sammanfogar dokument.
- **Betala per användning** – Inga förhandsutgifter; du betalar endast för de API-anrop du faktiskt gör.
- **Ingen serverunderhållning krävs** – Inga servrar att underhålla, inga programuppdateringar och inga kompatibilitetsproblem.

## Hur man använder API:et för komprimering av styrark med SDK:er

### API-specifikation för komprimering av styrark

[API-specifikationen för komprimering av styrark](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) tillhandahåller ett offentligt tillgängligt gränssnitt för REST-interaktioner, vilket möjliggör direkta API-anrop från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
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

Att använda ett SDK är det snabbaste sättet att utveckla, eftersom det abstraherar lågnivådetaljer och låter dig komprimera en styrark med bara några få kodrader. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du interagerar med Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}