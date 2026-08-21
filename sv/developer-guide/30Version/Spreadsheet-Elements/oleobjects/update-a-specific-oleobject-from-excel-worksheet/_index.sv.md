---
title: "Uppdatera ett OLE-objekt i ett Excel-ark"
second_title: "Dokument"
linktitle: "Uppdatera"
type: docs
url: /oleobjects/update/
aliases: [/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "uppdatera OLE-objekt, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Lär dig hur du uppdaterar ett OLE-objekt (bild, diagram etc.) i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller cURL- och SDK-exempel, autentiseringssteg och felhantering."
weight: 30
author: "Aspose Cloud-dokumentationsteam"
lastmod: "2024-03-01"
ArticleTitle: "Uppdatera ett OLE-objekt i ett Excel-ark – Aspose.Cells Cloud API-guide"
---

Denna REST API uppdaterar ett **OLE-objekt** i ett Excel-ark.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## PostUpdateWorksheetOleObject API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

Följande parametrar används i begäran:

| Parameternamn    | Typ     | Parametrplats | Beskrivning                                           |
| ---------------- | ------- | ------------- | ----------------------------------------------------- |
| name             | string  | path          | Arbetsbokens namn.                                    |
| sheetName        | string  | path          | Arkets namn.                                          |
| oleObjectIndex   | integer | path          | Index för OLE-objektet inom arket.                   |
| ole              | object  | body          | JSON-representation av det OLE-objekt som ska uppdateras. |
| folder           | string  | query         | Mappen som innehåller arbetsboken.                   |
| storageName      | string  | query         | Namnet på lagringstjänsten.                          |

### Fält i begärandetexten

| Fält                | Typ      | Obligatoriskt | Beskrivning                                              |
| ------------------- | -------- | ------------- | -------------------------------------------------------- |
| ImageSourceFullName | string   | valfritt      | Sökvägen till den bildfil som används för OLE-objektet. |
| IsAutoSize          | boolean  | valfritt      | Om OLE-objektet ska automatiskt anpassas i storlek.     |
| SourceFullName      | string   | obligatoriskt | Källfilen (t.ex. en bild eller ett diagram) för OLE-objektet. |
| UpperLeftRow        | integer  | obligatoriskt | Radindex (nollbaserat) för övre vänstra hörnet.          |
| UpperLeftColumn     | integer  | obligatoriskt | Kolumnindex (nollbaserat) för övre vänstra hörnet.       |
| Left                | integer  | valfritt      | Horisontell offset, i punkter, från övre vänstra hörnet. |
| Top                 | integer  | valfritt      | Vertikal offset, i punkter, från övre vänstra hörnet.    |
| Width               | integer  | obligatoriskt | Bredden på OLE-objektet, i punkter.                      |
| Height              | integer  | obligatoriskt | Höjden på OLE-objektet, i punkter.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Felaktiga svar

| HTTP-status | Kod  | Meddelande                                                    |
| ----------- | ---- | ------------------------------------------------------------ |
| 400         | 4000 | Felaktig begäran – saknade eller ogiltiga parametrar.         |
| 401         | 4010 | Inte auktoriserad – ogiltig eller saknad JWT-token.           |
| 404         | 4040 | Ej funnen – arbetsboken, arket eller OLE-objektet finns inte. |
| 500         | 5000 | Internt serverfel – oväntat fel på serversidan.                |

API:et returnerar även ett anpassat **Code**-fält i svarstexten som motsvarar HTTP-statuskoden (t.ex. 200 → 2000, 400 → 4000 etc.).

## När ska du använda detta API?

Använd detta slutsteg när du behöver ändra ett befintligt OLE-objekt – såsom en inbäddad bild, ett diagram eller ett dokument – utan att ladda upp hela arket på nytt. Vanliga användningsfall inkluderar att uppdatera källfilen för en bild, ändra objektets storlek eller ändra dess position efter att arbetsboken har genererats. Se även [Lägg till ett OLE-objekt](/oleobjects/add/) och [Ta bort ett OLE-objekt](/oleobjects/delete/) för relaterade åtgärder.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraherar bort detaljer på lågnivå så att du kan fokusera på ditt projekt. Besök [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Nedan följer ett kort C#-exempel som uppdaterar ett OLE-objekt med Aspose.Cells Cloud SDK:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}