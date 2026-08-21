---
title: "Ändra kolumnbredder inom ett intervall"
ArticleTitle: "Ändra kolumnbredder inom ett intervall – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Kolumnbredd"
type: docs
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells, kolumnbredd, REST API, Excel, SDK, intervall, moln"
description: "Lär dig hur du ändrar kolumnbredder inom ett intervall med Aspose.Cells Cloud REST API eller SDK:er (C#, Java, Python etc.). Innehåller cURL, begäran/svarsdetaljer och autentiseringssteg."
weight: 74
---

Denna REST API ställer in kolumnbredden för ett intervall.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Förutsättningar** – Innan du anropar endpointet måste du:

1. Skapa ett Aspose Cloud-konto och erhålla ett *client ID* och *client secret*.  
2. Begära en JWT-token genom att anropa OAuth-endpointen (`/connect/token`). Token returneras i fältet `access_token`.  
3. Ladda upp den målverksfilen till din Aspose Cloud-lagring (eller säkerställa att den redan finns i den angivna mappen).  

Begäransparametrarna är:

| Parameter Name | Typ    | Plats  | Beskrivning |
|----------------|--------|--------|-------------|
| name           | string | path   | Namn på arbetsbokensfil |
| sheetName      | string | path   | Namn på kalkylbladet |
| value          | number | query  | Önskt kolumnbreddvärde |
| range          | object | body   | Intervallobjekt som definierar målcellerna |
| folder         | string | query  | Mappsökväg där arbetsboken lagras |
| storageName    | string | query  | Namn på lagringstjänsten |

Den [OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

<h3 id="request">Begäran</h3>

```bash
# Anropa endpointet för kolumnbredd för arbetsboken *test.xlsx*,
# kalkylbladet *Sheet1*, genom att ställa in bredden på de markerade kolumnerna till 20 punkter.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">Svar</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

* Möjliga fel-svar  

| HTTP-kod | Beskrivning                               |
|----------|-------------------------------------------|
| 400      | Felaktig begäran – ogiltig JSON eller parametrar |
| 401      | Otillåten – saknad eller ogiltig token   |
| 404      | Hittades inte – arbetsbok eller kalkylblad saknas   |

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Vanliga frågor (FAQ)

**Fråga:** *Vilken endpoint ska jag anropa för att ställa in kolumnbredden för ett intervall i en Excel-arbetsbok?*  
**Svar:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth`, där `{name}` är arbetsbokens filnamn och `{sheetName}` är målkalkylbladet.

**Fråga:** *Hur autentiserar jag begäran när jag använder API:et för kolumnbredd?*  
**Svar:** Inkludera ett `Authorization: Bearer <jwt token>`-header. Skaffa JWT-token via Aspose Cloud OAuth-flödet (`/connect/token`) med ditt client ID och client secret.

**Fråga:** *Vilken JSON-kropp ska jag skicka för att ändra bredden på kolumnerna A–C till 25 punkter?*  
**Svar:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

Lägg till frågeparametern `value=25` i begärans URL.