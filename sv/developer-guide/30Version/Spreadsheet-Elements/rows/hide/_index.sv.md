---
title: "Dölj rader i ett Excel-ark"
second_title: "Dokument"
linktitle: "Dölj"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "dölj rader, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "Lär dig hur du döljer en eller flera rader i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, SDK-utdrag, parametrar, autentisering, svarsdetaljer och felhantering."
weight: 40
ArticleTitle: "Dölj rader i Excel-ark med Aspose.Cells Cloud API"
---

Denna REST API döljer rader i ett Excel-ark.

**Förutsättningar:** En giltig JWT Bearer-token från Aspose Cloud OAuth-slutpunkten, arbetsboken lagrad i Aspose Cloud-lagring och namnet på arket som innehåller de rader som ska döljas. API:et fungerar med Excel-filer i XLS, XLSX och andra format som stöds.

## PostHideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameter       | Typ     | Plats   | Beskrivning                                                         |
| --------------- | ------- | ------- | ------------------------------------------------------------------- |
| **name**        | string  | path    | Namnet på arbetsboksfilen.                                          |
| **sheetName**   | string  | path    | Namnet på arket som innehåller de rader som ska döljas.            |
| **startrow**    | integer | query   | Nollbaserat index för den första raden som ska döljas.             |
| **totalRows**   | integer | query   | Antalet på varandra följande rader som ska döljas, börjande från **startrow**. |
| **folder**      | string  | query   | Mappen i lagringen där arbetsboken finns.                          |
| **storageName** | string  | query   | Namnet på lagringstjänsten.                                         |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells webbtjänster. API:et kräver en JWT Bearer-token från Aspose Cloud OAuth-slutpunkten; inkludera den i `Authorization`-headern. Exemplet nedan visar hur du döljer en rad med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
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

**HTTP-statuskoder för svar**

| Kod | Beskrivning |
|-----|-------------|
| 200 | Lyckades – rader dolda |
| 400 | Felaktig begäran – ogiltiga parametrar |
| 401 | Otillåten – saknad eller ogiltig JWT |
| 404 | Inte hittad – arbetsbok eller ark finns inte |
| 500 | Serverfel – internt bearbetningsfel |

Ett lyckat anrop returnerar ett JSON-objekt med fälten `Code` och `Status`. Vid fel inkluderar svaret ytterligare fält såsom `Message` och lämpliga HTTP-statuskoder (t.ex. 400, 401, 404, 500).

**Notera:** Se till att `startrow`-värdet ligger inom arkets radintervall; annars returnerar API:et ett 400-fel. Radindex är nollbaserade, så `startrow=0` hänvisar till den första raden.

## Molnsdks-familj

Att använda ett SDK är det snabbaste sättet att integrera den här funktionaliteten i din applikation. SDK:er hanterar detaljer på lågnivå så att du kan fokusera på affärslogik. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man döljer rader med olika SDK:er. (Exempelfilnamnen hänvisar till "Unhide" på grund av äldre namngivning; koden i varje gist utför åtgärden **Dölj**.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}