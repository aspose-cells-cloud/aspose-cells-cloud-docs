---
title: "Matcha alla tomma celler i ett Excel-arbetsblad"
ArticleTitle: "Matcha alla tomma celler i ett Excel-arbetsblad – Aspose.Cells Cloud API-guide"
second_title: "Dokument"
linktitle: "Matcha alla tomma celler"
type: docs
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, tomma celler, AutoFilter, REST API, Excel"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att filtrera och matcha alla tomma celler i ett Excel-arbetsblad. Innehåller slutpunkt, parametrar, autentiseringssteg, cURL-exempel och SDK-utdrag för C#, Java, Python och mer."
weight: 100
---

Denna REST API matchar alla **tomma celler** i filterlistan på ett Excel-arbetsblad.

**Förutsättningar:** Innan du anropar denna slutpunkt, se till att du har en giltig JWT-åtkomsttoken, att arbetsboken är uppladdad till Aspose Cloud-lagring och att du känner till lagringsmappen (om tillämpligt). Ange parametrarna `folder` och `storageName` om filen inte finns i standardrotmappen.

## PostWorksheetMatchBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begäran parametrar

| Parameter Name   | Typ     | Plats  | Beskrivning                                                      |
|------------------|---------|--------|------------------------------------------------------------------|
| name             | string  | path   | Namnet på arbetsbokfilen.                                        |
| sheetName        | string  | path   | Namnet på arbetsbladet som innehåller filtret.                   |
| fieldIndex       | integer | query  | Nollbaserat index för kolumnen som filtret tillämpas på.         |
| folder           | string  | query  | Mappens sökväg i lagringen där arbetsboken finns.                |
| storageName      | string  | query  | Namnet på Aspose Cloud-lagringen.                                 |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                       |
|-----|-----------------------------|-------------------------------------------------------------------|
| 200 | OK                          | Filtret tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token.                                   |
| 413 | Begärandetext för stor      | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel           | Oväntat serverfel.                                                |

## Hur du använder PostWorksheetMatchBlanks API med SDK:er

### PostWorksheetMatchBlanks API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
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

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}