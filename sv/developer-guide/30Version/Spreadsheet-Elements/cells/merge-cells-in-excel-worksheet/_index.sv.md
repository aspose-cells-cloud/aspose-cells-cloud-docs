---
title: "Så här sammanfogar du celler i ett Excel-arbetsblad – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /sv/merge-cells-in-excel-worksheet/
weight: 110
keywords: "sammanfoga celler, Aspose.Cells, molntjänst-API, Excel"
description: "Instruktion för hur du sammanfogar celler i ett Excel-arbetsblad med Aspose.Cells Cloud REST API, inklusive exempel med cURL och SDK:er."
ArticleTitle: "Så här sammanfogar du celler i ett Excel-arbetsblad – Aspose.Cells Cloud API (v3.0)"
---

Aspose.Cells Cloud REST API sammanfogar ett rektangulärt område av celler till en enda cell som sträcker sig över de angivna raderna och kolumnerna.

**Förutsättningar**  
- Ett giltigt JWT-token för autentisering.  
- Arbetsboken måste redan finnas i den angivna lagringsmappen.  
- Lagringskonfiguration (mapp och lagringsnamn) måste vara inställd i ditt Aspose.Cloud-konto.

## PostWorksheetMerge API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Namn            | Typ     | Plats  | Beskrivning                                           |
|-----------------|---------|--------|-------------------------------------------------------|
| name            | string  | path   | Arbetsbokens namn.                                    |
| sheetName       | string  | path   | Arbetsbladets namn.                                   |
| startRow        | integer | query  | Nollbaserat index för första raden (0 = första raden). |
| startColumn     | integer | query  | Nollbaserat index för första kolumnen (0 = första kolumnen). |
| totalRows       | integer | query  | Antal rader som ska sammanfogas.                      |
| totalColumns    | integer | query  | Antal kolumner som ska sammanfogas.                   |
| folder          | string  | query  | Mappen som innehåller arbetsboken.                    |
| storageName     | string  | query  | Lagringsnamnet.                                       |

*Ingen begärandetext krävs för denna åtgärd.*

## **Svar**

Returnerar CellsCloudResponse.

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                    | Beskrivning                                           |
|-----|------------------------------|-------------------------------------------------------|
| 200 | OK                           | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran             | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                     | Ogiltigt eller saknat JWT-token. |
| 413 | För stor nyttolast           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel            | Oväntat serverfel. |

## Hur du använder PostWorksheetMerge API med SDK:er

### PostWorksheetMerge API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}