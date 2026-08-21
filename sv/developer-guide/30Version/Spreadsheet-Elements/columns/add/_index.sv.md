---
title: "Lägg till en tom kolumn i ett Excel-arbetsblad - Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /sv/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "lägg till, kolumn, Excel, API, Aspose.Cells, moln, REST, infoga"
description: "Lär dig hur du infogar en ny kolumn i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller begäransyntax, cURL-exempel och SDK-kodexempel."
weight: 20
ArticleTitle: "Lägg till en tom kolumn i ett Excel-arbetsblad med Aspose.Cells Cloud API"
---

Denna REST API infogar en eller flera kolumner i ett arbetsblad.

**Förutsättningar**  
Innan du anropar detta slutpunkt, se till att du har slutfört följande steg:

- Skaffa ett giltigt OAuth 2.0-åtkomsttoken och inkludera det i `Authorization`-headern.  
- Spara målarbokshandboken i vald lagring (standard = “Default”) eller ange lämpliga parametrar för `folder` och `storageName`.  
- Verifiera att arbetsbladsnamnet som anges i `sheetName` finns i arbokshandboken.

## PutInsertWorksheetColumns API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parametername       | Typ     | Plats  | Beskrivning                                                         |
| ------------------- | ------- | ------ | ------------------------------------------------------------------- |
| **name**            | sträng  | path   | Namnet på arbokshandbokens fil.                                     |
| **sheetName**       | sträng  | path   | Namnet på arbetsbladet.                                             |
| **columnIndex**     | heltal  | path   | Nollbaserat index för kolumnen dit infogningen börjar.             |
| **totalColumns**    | heltal  | query  | Antal kolumner som ska infogas.                                     |
| **updateReference** | boolean | query  | När **true** uppdateras cellreferenser för att återspegla infogningen. |
| **folder**          | sträng  | query  | Sökvägen till mappen som innehåller arbokshandboken.               |
| **storageName**     | sträng  | query  | Namnet på lagringstjänsten.                                        |

**Anteckningar**

- `columnIndex` måste vara mellan 0 och det aktuella antalet kolumner i arbetsbladet. Infoga utanför det befintliga intervallet expanderar arket automatiskt.  
- Infoga flera kolumner (`totalColumns` > 1) skjuter befintliga kolumner åt höger.  
- `updateReference`-flaggan är som standard `false`; ställ in på `true` för att uppdatera formler och namngivna intervall.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för att anropa Aspose.Cells webbtjänster. Följande exempel visar en komplett begäran inklusive autentisering och korrekt sökvägsparameter.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**Svars-koder**

| Kod | Beskrivning                                  |
|-----|----------------------------------------------|
| 200 | Kolumn(er) infogades framgångsrikt.          |
| 400 | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401 | Ej auktoriserad – ogiltig eller saknad token. |
| 404 | Arbokshandbok eller arbetsblad hittades inte. |
| 500 | Internt serverfel.                           |

**Exempel på felaktiga svar**

```json
// 400 Bad Request – saknade eller ogiltiga parametrar
{
  "Code": 400,
  "Message": "Ogiltig parameter: totalColumns måste vara ett positivt heltal."
}

// 401 Unauthorized – ogiltig eller saknad token
{
  "Code": 401,
  "Message": "Autentisering misslyckades. Åtkomsttoken saknas eller är ogiltig."
}

// 404 Not Found – arbokshandbok eller arbetsblad finns inte
{
  "Code": 404,
  "Message": "Arbokshandboken 'test.xlsx' hittades inte."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "Ett oväntat fel uppstod på servern."
}
```

## Moln SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på din projekts logik. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}