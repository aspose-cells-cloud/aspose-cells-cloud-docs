---
title: "Visa en dold Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Visa"
type: docs
url: /sv/worksheets/unhide/
aliases: [  /sv/unhide-excel-worksheets/ ]
keywords: "Aspose.Cells, visa arbetsblad, Excel API, moln spreadsheet, REST, synlighet för arbetsblad, Excel-arbetsbok"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att visa ett dolt arbetsblad i en Excel-arbetsbok. Innehåller begärandedetaljer, cURL-exempel och SDK-kodavsnitt för flera programmeringsspråk."
weight: 60
---

Denna REST API tillhandahåller en slutpunkt för att **visa ett dolt arbetsblad** i en Excel-arbetsbok.

**Förutsättningar**  
Innan du anropar denna åtgärd måste du ha:

* Ett giltigt Aspose Cloud-åtkomsttoken (JWT) inkluderat i `Authorization`-huvudet.  
* Arbetsboken lagrad på en lagringsplats som stöds, som du anger med frågeparametrarna `folder` och `storageName`.  
* Arbetsboken måste vara i ett format som stöds av Aspose.Cells (t.ex. `.xls`, `.xlsx`, `.xlsm`).  

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **Begärparametrar**

| Parameternamn | Typ    | Plats  | Beskrivning                                   |
| ------------- | ------ | ------ | --------------------------------------------- |
| name          | string | path   | Dokumentets namn.                             |
| sheetName     | string | path   | Arbetsbladets namn.                           |
| isVisible     | boolean | query | Nytt synlighetsvärde för arbetsbladet (`true`). |
| folder        | string | query | Dokumentets mapp.                             |
| storageName   | string | query | Lagringsnamn.                                 |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt som låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att enkelt anropa Aspose.Cells-webbtjänster. Exemplet nedan visar hur man gör en begäran med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # ersätt <jwt token> med din åtkomsttoken
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Möjliga svarskoder**

| HTTP-kod | Betydelse                                             | Exempel på svar (vid behov)                                 |
| -------- | ----------------------------------------------------- | ----------------------------------------------------------- |
| 200      | Synlighet för arbetsblad uppdaterades korrekt         | `{ "Code": 200, "Status": "OK" }`                           |
| 400      | Felaktig begäran – saknade eller ogiltiga parametrar | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401      | Auktorisering misslyckades – saknad eller ogiltig JWT-token | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404      | Hittades inte – arbetsboken eller arbetsbladet finns inte | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500      | Internt serverfel                                      | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}