---
title: "Ställ in intervallvärde i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Ställ in värden"
type: docs
url: /sv/ranges/update/values/
aliases: [  /sv/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel-API, ställ in intervallvärde, REST-API, moln-SDK, uppdatera arbetsblad"
description: "Lär dig hur du ställer in cell- eller intervallvärde i en Excel-arbetsbok med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, cURL-exempel, SDK-kodexempel och felhantering."
weight: 72
ArticleTitle: "Ställ in intervallvärde i ett Excel-arbetsblad – Aspose.Cells Cloud API"
---

Använd detta REST-API för att ställa in ett värde i det angivna intervallet. När lämpligt konverteras värdet till en annan datatyp och cellens nummerformåt återställs.

**Förutsättningar**  
- Ett giltigt Aspose Cloud-konto.  
- En JWT-token som inkluderar scope `Cells.ReadWrite`.  
- Arbetsboken måste redan vara uppladdad till målmapplagringen.

## PostWorksheetCellsRangeValue API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

Följande begäranparametrar används:

| Parametername  | Typ     | Plats  | Beskrivning                                                |
|----------------|---------|--------|------------------------------------------------------------|
| name           | string  | path   | Arbetsbokens namn                                          |
| sheetName      | string  | path   | Arbetsbladets namn                                         |
| value          | string  | query  | Inmatat värde                                              |
| range          | object  | body   | Intervallobjekt i arbetsbladet                             |
| isConverted    | boolean | query  | Anger om det inmatade värdet ska konverteras               |
| setStyle       | boolean | query  | Anger om stil ska tillämpas på målcellerna                 |
| folder         | string  | query  | Mapp för arbetsboken                                       |
| storageName    | string  | query  | Lagringsnamn                                               |

**Exempel på `range`-objekt** som kan skickas i begärandetexten:

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud-API:et med cURL. **Inkludera en giltig JWT-token i `Authorization`-headern.**

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
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

**Svarschema**

| Fält    | Typ     | Beskrivning                                              |
|---------|---------|----------------------------------------------------------|
| Code    | integer | HTTP-statuskod för åtgärden.                            |
| Status  | string  | Kort beskrivning av resultatet (t.ex. "OK").            |
| Message | string  | Detaljerad felmeddelande vid misslyckad begäran (valfritt). |
| Result  | object  | Ytterligare data returnerad vid lyckade anrop (valfritt).|

**Möjliga HTTP-statuskoder**

- **200 OK** – Intervallet värde har ställts in framgångsrikt.  
- **400 Bad Request** – Ogiltiga parametrar eller felaktigt formaterad begärandetext.  
- **401 Unauthorized** – Saknad eller ogiltig JWT-token.  
- **403 Forbidden** – Otillräckliga rättigheter för den begärda åtgärden.  
- **404 Not Found** – Den angivna arbetsboken, arbetsbladet eller intervallet finns inte.  
- **500 Internal Server Error** – Oväntat serverfel.

*Exempel på felaktigt svar vid 400 Bad Request:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Objektet 'range' saknar nödvändiga fält."
}
```

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}