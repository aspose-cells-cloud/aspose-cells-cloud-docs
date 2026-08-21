---
title: "Ta bort flera rader från ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Rader"
type: docs
url: /sv/rows/delete/rows/
keywords: "Aspose.Cells Cloud, ta bort rader, ta bort flera rader, Excel-arbetsblad, REST API, SDK"
description: "Lär dig hur du tar bort en eller flera rader från ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Innehåller detaljerad endpoint-info, parametrar, ett cURL-exempel och SDK-kodexempel för olika språk."
weight: 80
ArticleTitle: "Ta bort flera rader från ett Excel-arbetsblad med Aspose.Cells Cloud API"
---

Denna REST API tar bort flera rader **från** ett Excel-arbetsblad.

**Förutsättningar:** För att kunna anropa denna endpoint måste du ha ett giltigt JWT-åtkomsttoken som du får genom Aspose Cloud-autentisering, samt lämpliga lagringsbehörigheter för arbetsboken.

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parameter Name  | Typ     | Sökväg / Frågesträng / HTTP-brödtext | Beskrivning                                                       |
| --------------- | ------- | ------------------------------------ | ----------------------------------------------------------------- |
| name            | sträng  | sökväg                               | Arbetsbokens namn.                                                |
| sheetName       | sträng  | sökväg                               | Arbetsbladets namn.                                               |
| startrow        | heltal  | fråga                                | Nollbaserat index för den första raden som ska tas bort (t.ex. `0` = första raden). |
| totalRows       | heltal  | fråga                                | Antalet rader som ska tas bort.                                   |
| updateReference | boolesk | fråga                                | Om referenser ska uppdateras efter borttagning (`true`/`false`). |
| folder          | sträng  | fråga                                | Dokumentmappen.                                                   |
| storageName     | sträng  | fråga                                | Lagringsnamnet.                                                   |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL. **Alla endpoints kräver HTTPS; HTTP är föråldrat.**

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

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

**Möjliga svarsstatuskoder**

| HTTP-status | Beskrivning |
|-------------|-------------|
| 200 | Rader har tagits bort utan problem. |
| 400 | Felaktig begäran – ogiltiga parametrar. |
| 401 | Otillåten – saknat eller ogiltigt JWT-token. |
| 404 | Inte hittad – arbetsbok eller arbetsblad finns inte. |
| 500 | Internt serverfel – oväntat tillstånd. |

## Cloud SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}