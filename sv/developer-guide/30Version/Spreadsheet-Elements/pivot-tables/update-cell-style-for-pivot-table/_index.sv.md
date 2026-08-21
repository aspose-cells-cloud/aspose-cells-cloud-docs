---
title: "Uppdatera cellstil för pivottabell"
second_title: "Dokument"
linktitle: Formatera
type: docs
url: /sv/pivot-tables/format/
aliases: [/sv/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, pivottabellstil, API för att uppdatera cellstil, REST API, Excel API, kalkylbladsformatering, moln-SDK, cellstil, pivottabell"
description: "Lär dig hur du uppdaterar stilen för en specifik cell i en pivottabell i Aspose.Cells Cloud via REST API. Inkluderar endpoint, parametrar, autentisering, cURL-exempel, Go SDK-kodavsnitt och SEO-optimerad vägledning."
weight: 90
ArticleTitle: "Uppdatera cellstil för pivottabell – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API uppdaterar **stilen** på en cell i en pivottabell.

**Förutsättningar / Autentisering**  
För att anropa denna endpoint måste du ha en giltig Aspose Cloud JWT-åtkomsttoken. Skaffa token via OAuth 2.0-flödet som beskrivs i [Autentiseringshandboken](/sv/authentication/). Inkludera token i begärandehuvudet:

```http
Authorization: Bearer <jwt token>
```

JWT-token krävs för alla Aspose.Cells Cloud API-anrop.

## PostPivotTableCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärandeparametrar**

| Parametername   | Typ     | Plats  | Beskrivning                                                                                             |
| --------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------- |
| name            | string  | path   | Dokumentets namn (obligatoriskt).                                                                       |
| sheetName       | string  | path   | Kalkylbladets namn (obligatoriskt).                                                                     |
| pivotTableIndex | integer | path   | Index för pivottabellen (obligatoriskt).                                                                |
| column          | integer | query  | Nollbaserat kolumnindex för den cell som ska formateras (obligatoriskt).                                |
| row             | integer | query  | Nollbaserat radindex för den cell som ska formateras (obligatoriskt).                                   |
| style           | object  | body   | Style DTO (data transfer object) som definierar den nya cellstilen.                                    |
| needReCalculate | boolean | query  | Anger om pivottabellen ska omberäknas efter formatering. Standardvärdet är **false**.                   |
| folder          | string  | query  | Mapp där dokumentet lagras (valfritt).                                                                  |
| storageName     | string  | query  | Namn på lagringen (valfritt).                                                                           |
| Method          | string  | N/A    | HTTP-metod som används för begäran (**POST**).                                                          |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

**Svar**  
Vid lyckad åtgärd returnerar tjänsten HTTP 200 med en tom kropp, vilket indikerar att stilen har tillämpats. Vid fel returneras en JSON-payload med felkod och meddelande.

| HTTP-status | Beskrivning                                           |
|------------|-------------------------------------------------------|
| 200        | Stilen har tillämpats korrekt.                        |
| 400        | Felaktig begäran – t.ex. ogiltigt kolumn-/radindex.   |
| 401        | Auktorisering misslyckades – JWT-token saknas eller är ogiltig. |
| 404        | Hittades inte – det angivna dokumentet, kalkylbladet eller pivottabellen finns inte. |
| 500        | Internt serverfel – oväntat tillstånd.                |

Svarsbodyn är tom vid lyckad åtgärd.

Mer information finns i dokumentationen för **Get Pivot Table** API.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på lägre nivå och låter dig fokusera på din affärslogik. Ta en titt på <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med **Go**-SDK:en:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Uppdatera cellstil för pivottabell",
  "description": "Guide för att uppdatera stilen för en specifik cell i en pivottabell i Aspose.Cells Cloud med REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, pivottabell, cellstil, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>