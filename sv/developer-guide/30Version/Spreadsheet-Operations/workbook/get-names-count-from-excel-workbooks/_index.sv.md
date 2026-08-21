---
title: "Hämta namn från en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Namn"
type: docs
url: /sv/get-names-from-an-excel-file/
aliases:
  [
    /get-names-count-from-excel-workbooks/,
    /workbook/names/,
    /workbook/get/names/,
  ]
keywords: "Aspose.Cells, moln, Excel, Arbetsbok, Namn, REST API, SDK"
description: "Hämta alla definierade namn från en Excel-arbetsbok med Aspose.Cells Cloud REST API. Inkluderar vägledning om autentisering, cURL-exempel, svarsschema, felhantering och SDK-exempel."
weight: 120
ArticleTitle: "Hämta namn från en Excel-arbetsbok – Aspose.Cells Cloud API"
---

Denna REST API hämtar de definierade namnen från en Excel-arbetsbok.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## GetWorkbookNames API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

Begärans parametrar är:

| Parameternamn | Typ    | Plats  | Beskrivning                            |
| ------------- | ------ | ------ | -------------------------------------- |
| name          | string | path   | Arbetsbokens filnamn.                  |
| folder        | string | query  | Mappen som innehåller arbetsboken.     |
| storageName   | string | query  | Namnet på den lagring som ska användas. |

Begäran måste innehålla följande HTTP-huvuden:

| Huvud        | Typ    | Beskrivning                              |
|--------------|--------|------------------------------------------|
| Authorization | string | Bearer JWT-token (obligatoriskt)         |
| Accept        | string | `application/json`                       |
| Content-Type  | string | `application/json` (för begäranden med en kropp) |

**Autentisering** – API:et kräver en OAuth2/JWT-bearer-token. Skaffa en token från `https://api.aspose.cloud/connect/token` med ditt client-id och client-secret, och inkludera sedan huvudet `Authorization: Bearer <jwt token>` i varje begäran.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att komma åt Aspose.Cells-webbtjänster. Exemplet nedan visar hur du anropar Aspose.Cells Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_Svarsfält_

- **Status** _(string)_ – Meddelande om åtgärdens status.
- **Names.link** _(object)_ – Hyperlänksinformation för samlingen.
- **Names.Count** _(integer)_ – Totalt antal returnerade definierade namn.
- **Names.NameList** _(array)_ – Lista med namnobjekt; varje objekt innehåller ett **link**-objekt med navigeringsinformation.

**Felhantering** – Tjänsten kan returnera följande HTTP-statuskoder:

| Kod | Betydelse             | Rekommenderad åtgärd                                          |
|-----|-----------------------|---------------------------------------------------------------|
| 401 | Obehörig              | Kontrollera att en giltig JWT-token tillhandahålls.            |
| 404 | Hittades inte         | Kontrollera att arbetsbokens namn, mapp och lagring är korrekta. |
| 500 | Internt serverfel     | Försök igen senare eller kontakta Aspose-supporten om problemet kvarstår. |

{{< /tab >}}

{{< /tabs >}}

## Moln SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå och låter dig fokusera på ditt projekt. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}