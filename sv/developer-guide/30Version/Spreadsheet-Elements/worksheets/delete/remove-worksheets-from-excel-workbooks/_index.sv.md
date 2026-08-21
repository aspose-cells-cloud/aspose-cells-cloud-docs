---
title: "Ta bort kalkylblad"
second_title: "Dokument"
linktitle: "Ett kalkylblad"
type: docs
url: /sv/worksheets/delete-worksheet/
aliases: [  /sv/remove-worksheets-from-excel-workbooks/ ]
keywords: "Aspose.Cells Cloud, Ta bort kalkylblad, Excel, Kalkylark, REST API"
description: "Ta bort ett kalkylblad från en Excel-arbetsbok med Aspose.Cells Cloud REST API. Stöder SDK:er för C#, Java, PHP, Ruby, Node.js, Python, Perl, Go och cURL."
weight: 20
ArticleTitle: "Ta bort kalkylblad – Aspose.Cells Cloud API"
---

Denna REST API tar bort ett kalkylblad.  
Förutsättningar: För att anropa denna API måste du tillhandahålla en giltig JWT-autentiseringstoken i **Authorization**-headern och ha åtkomst till lagringsplatsen där arbetsboken finns.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*Obs: API:et använder version **v3.0**, vilket är den aktuella stabila versionen. Framtida versionsändringar kommer att meddelas i versionsanteckningarna.*

### **Förfrågningsparametrar**

| Parameter Name | Typ    | Plats  | Beskrivning             |
| -------------- | ------ | ------ | ----------------------- |
| name           | string | path   | Dokumentets namn.       |
| sheetName      | string | path   | Kalkylbladets namn.     |
| folder         | string | query  | Dokumentets mapp.       |
| storageName    | string | query  | Lagringsnamn.           |

Möjliga HTTP-svar:

| Statuskod | Beskrivning                          |
| --------- | ------------------------------------ |
| 200 OK    | Kalkylbladet har tagits bort.        |
| 400 Bad Request | Ogiltiga förfrågningsparametrar.  |
| 401 Unauthorized | Autentisering misslyckades eller token saknas. |
| 404 Not Found | Angiven arbetsbok eller kalkylblad finns inte. |
| 500 Internal Server Error | Oväntat serverfel. |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Alla förfrågningar måste göras över HTTPS; API:et stöder inte anslutningar utan TLS.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Molnsdk-familj

Att använda en sdk är det bästa sättet att påskynda utvecklingen. En sdk hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}