---
title: "Lägg till ett OLE-objekt i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Lägg till OLE-objekt"
type: docs
url: /sv/oleobjects/add/
aliases: [  /sv/add-oleobject-to-excel-worksheet/ ]
keywords: "Lägg till OLE-objekt, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Använd Aspose.Cells Cloud REST API för att lägga till OLE-objekt i Excel-arbetsblad. API:t kan anropas direkt eller via SDK:er för C#, Java, PHP, Ruby, Node.js, Python, Perl och Go."
ArticleTitle: "Lägg till OLE-objekt i Excel-arbetsblad med Aspose.Cells Cloud API"
weight: 20
---

Aspose.Cells Cloud API möjliggör programmatiserad manipulation av Excel-arbetsböcker, inklusive möjligheten att bädda in OLE-objekt (t.ex. Word-dokument, PDF-filer eller andra binärfiler) direkt i ett arbetsblad.

Detta REST API lägger till ett **OLE-objekt** i ett Excel-arbetsblad.

**Förutsättningar** – Du måste ha en giltig JWT-autentiseringstoken, och alla källfiler som refereras av `oleFile` eller `imageFile` bör vara uppladdade till den angivna lagringsplatsen innan slutpunkten anropas.

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| ParameterName   | Typ     | Plats  | Beskrivning                                        |
| --------------- | ------- | ------ | -------------------------------------------------- |
| name            | string  | path   | Namnet på arbetsboksfilen.                         |
| sheetName       | string  | path   | Namnet på arbetsbladet.                            |
| oleObject       | object  | body   | Definitionen av OLE-objektet.                      |
| upperLeftRow    | integer | query  | Radindex för övre vänstra hörnet (standard 0).     |
| upperLeftColumn | integer | query  | Kolumnindex för övre vänstra hörnet (standard 0).  |
| height          | integer | query  | Höjd på OLE-objektet (standard 0).                 |
| width           | integer | query  | Bredd på OLE-objektet (standard 0).                |
| oleFile         | string  | query  | Namn på OLE-källfilen.                             |
| imageFile       | string  | query  | Namn på förhandsgranskningsbildfilen.              |
| folder          | string  | query  | Mapp som innehåller arbetsboken.                   |
| storageName     | string  | query  | Namn på den lagringsplats som ska användas.        |

**Anteckningar** – `upperLeftRow` och `upperLeftColumn` använder nollbaserad indexering. `oleFile` (och valfritt `imageFile`) måste redan finnas i mållagringen; annars returneras ett fel i begäran.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) definierar ett offentligt tillgängligt programmeringsgränssnitt och tillåter dig att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells-webbtjänster. Exemplet nedan visar hur man lägger till ett OLE-objekt med cURL. **HTTPS krävs för alla produktionsanrop.**

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Skärmbild som visar ett OLE-objekt inkorporerat i ett Excel-arbetsblad](/cells/images/ole-object-example.png)

**Möjliga HTTP-statuskoder**

| Kod | Beskrivning                                  |
|-----|----------------------------------------------|
| 200 | OLE-objektet lades framgångsrikt till.       |
| 400 | Felaktig begäran – parametrar saknas eller är ogiltiga. |
| 401 | Inte auktoriserad – ogiltig eller saknad JWT-token. |
| 404 | Inte hittad – arbetsbok, arbetsblad eller källfil finns inte. |
| 500 | Internt serverfel – oväntat fel.              |

Ett typiskt framgångsrikt svar returnerar följande JSON-struktur:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Cloud SDK-familj

Användning av en SDK påskyndar utvecklingen. En SDK abstraher bort detaljer på lågnivå, så att du kan fokusera på din affärslogik. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur Aspose.Cells-webbtjänster anropas med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}