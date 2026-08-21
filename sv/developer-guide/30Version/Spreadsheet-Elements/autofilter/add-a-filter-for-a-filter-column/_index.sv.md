---
title: "Lägg till ett filter i ett Excel-ark"
second_title: "Dokument"
linktitle: "Lägg till filter"
type: docs
url: /sv/autofilter/add-filter/
aliases: [  /sv/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, moln, Excel, AutoFilter, lägg till filter, REST API, SDK"
description: "Lär dig hur du lägger till ett autofilter i en kolumn i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, SDK-exempel och parameterguide."
weight: 60
ArticleTitle: "Lägg till ett filter i ett Excel-ark med Aspose.Cells Cloud"
---

**Förutsättningar:** Innan du anropar detta API måste du hämta en giltig JWT-token, se till att målarboksen är uppladdad till det angivna lagringsutrymmet och ha de nödvändiga behörigheterna för att komma åt filen. En nyare version av cURL (7.68 eller senare) rekommenderas för kommandoradsexempel.

Detta REST API lägger till ett filter för en specifik kolumn i ett Excel-ark.

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranens parametrar

| Parameter_name | Typ     | Plats  | Beskrivning |
|----------------|---------|--------|-------------|
| name           | string  | Path   | Namnet på arbetsboken. |
| sheetName      | string  | Path   | Namnet på arket. |
| range          | string  | Query  | Cellområdet som innehåller filtret (t.ex. `A1:B1`). |
| fieldIndex     | integer | Query  | Nollbaserat index för kolumnen som filtret ska tillämpas på. |
| criteria       | string  | Query  | Filterkriterierna (t.ex. ett värde eller en uttryck). |
| matchBlanks    | boolean | Query  | Sätt till `true` för att inkludera tomma celler i filtret; annars `false`. |
| refresh        | boolean | Query  | Sätt till `true` för att uppdatera filtret efter tillämpning; annars `false`. |
| folder         | string  | Query  | Mappen där den ursprungliga arbetsboken lagras. |
| storageName    | string  | Query  | Namnet på lagringstjänsten. |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur du använder PutWorksheetFilter API med SDK:er

### PutWorksheetFilter API-specificering

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">OpenAPI-specificeringen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
-X PUT \
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

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}