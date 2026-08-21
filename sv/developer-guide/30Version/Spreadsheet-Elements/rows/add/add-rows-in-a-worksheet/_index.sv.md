---
title: "Lägg till flera rader i ett Excel-ark"
ArticleTitle: "Lägg till flera rader i ett Excel-ark med Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Rader"
type: docs
url: /sv/rows/add/rows/
keywords: "Aspose.Cells Cloud, infoga rader, Excel-ark, REST API, SDK, lägg till flera rader"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att infoga flera rader i ett Excel-ark. Den här guiden täcker slutpunkten, begärparametrar, exempel på cURL-kommandon och SDK-användningsexempel."
weight: 20
---

Denna REST API lägger till flera nya rader i ett Excel-ark.

## PutInsertWorksheetRows API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| ParameterNamn   | Typ     | Plats  | Beskrivning                                                          |
| --------------- | ------- | ------ | -------------------------------------------------------------------- |
| name            | string  | path   | Arbetsbokens namn.                                                   |
| sheetName       | string  | path   | Arkets namn.                                                         |
| startrow        | integer | query  | Indexet för den första rad som ska infogas (**0-baserat**).          |
| totalRows       | integer | query  | Antalet rader som ska infogas.                                       |
| updateReference | boolean | query  | Om cellreferenser ska uppdateras efter infogning (`true` eller `false`). |
| folder          | string  | query  | Mappen som innehåller dokumentet.                                   |
| storageName     | string  | query  | Lagringsnamnet.                                                      |

**Förutsättningar**  
Arbetsboken måste redan finnas i den angivna lagringen (eller mapp) innan du anropar den här åtgärden.

**Autentisering**  
API:et kräver en giltig JWT-token. Inkludera den i `Authorization`-headern enligt exemplet med cURL nedan.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Obs:** Denna `PUT`-åtgärd kräver inte en begäran med brödtext; ett tomt JSON-objekt (`{}`) kan skickas om klientbiblioteket tvingar fram en payload.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Möjliga svarskoder*  

- **200 OK** – Rader infogades framgångsrikt.  
- **400 Bad Request** – Ogiltiga parametrar (t.ex. negativ radindexering).  
- **401 Unauthorized** – Saknad eller ogiltig JWT-token.  
- **404 Not Found** – Angiven arbetsbok eller ark finns inte.  
- **500 Internal Server Error** – Oväntat serverfel.

{{< /tab >}}

{{< /tabs >}}

För ytterligare åtgärder på rader, se relaterade sidor: **Ta bort rader**, **Hämta rader** och **Kopiera rader**.

## Cloud SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå så att du kan fokusera på ditt projekt. Kontrollera [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}