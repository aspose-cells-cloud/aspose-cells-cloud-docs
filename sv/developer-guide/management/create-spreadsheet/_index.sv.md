---
title: "Skapa Spreadsheet API – Aspose.Cells Cloud (v5.0) | Generera Excel-filer"
second_title: "Dokument"
ArticleTitle: "Hur man skapar nya Excel-kalkylark – Generera tomma eller mallbaserade filer"
linktitle: "Skapa kalkylark"
type: docs
url: /sv/create-spreadsheet/
keywords: "Aspose.Cells, spreadsheet API, skapa Excel, moln, XLSX, ODS, CSV, mall, SDK, automatisering"
description: "Lär dig hur du skapar tomma eller mallbaserade Excel-arbetsböcker med Aspose.Cells Cloud API (v5.0). Inkluderar slutpunkt, parametrar, felkoder, autentiseringssteg och SDK-exempel."
weight: 100
---

Skapa nya Excel-kalkylark programmvis med Aspose.Cells Cloud API. Generera tomma arbetsböcker eller instansiera filer från anpassade mallar. Den REST-baserade API:en möjliggör automatiserad skapande av Excel-filer, vilket är perfekt för rapportgenerering, dokumentautomatisering och datahanteringsarbetsflöden.

## **Skapa Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameter Name     | Typ    | Plats  | Beskrivning                                                                                                                                         |
| ------------------ | ------ | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | Sträng | Fråga  | **Obligatoriskt**. Filformat för det nya kalkylarket (t.ex. `XLSX`, `XLS`, `ODS`, `CSV`).                                                          |
| **template**       | Sträng | Fråga  | **Valfritt**. Namn på en mallfil som är lagrad i ditt molnlagring (t.ex. `invoice_template.xlsx`). Om utelämnas skapas en tom arbetsbok.             |
| **outPath**        | Sträng | Fråga  | **Valfritt**. Målmappens sökväg i molnlagring för den genererade filen. Om `null` eller utelämnas sparas kalkylarket till standardplatsen.          |
| **outStorageName** | Sträng | Fråga  | **Obligatoriskt**. Identifierare för den konfigurerade molnlagringen (t.ex. `MyDrive`).                                                            |
| **region**         | Sträng | Fråga  | **Valfritt**. Språkinställning (t.ex. `sv-SE`) som bestämmer standardformat för datum, tal och valuta.                                             |
| **password**       | Sträng | Fråga  | **Valfritt**. Lösenord för en krypterad mallfil. Lämna tomt om mallen inte är skyddad.                                                               |

### Svar

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filtrering lyckades; svaret innehåller åtgärdens detaljer.       |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör vi använda Skapa Spreadsheet API?

- **Initialisering av automatiskt rapporteringssystem** – Skapa en ny tom arbetsbok eller generera en rapportfil från en standardmall i början av varje daglig/veckovis automatiseringscykel.
- **Kundens egen serviceportal** – Låt kunder välja en mall (offert, projektplan, etc.) och omedelbart ladda ner en anpassad Excel-fil.
- **Batch-dataexport och distribution** – Skapa separata arbetsböcker med ett enhetligt format för varje exporterat dataset, vilket förenklar vidare distribution och bearbetning.

För efterföljande åtgärder såsom lägg till kalkylblad eller fyll i celler, se **Lägg till kalkylblad API**, **Uppdatera cell API** och **Exportera arbetsbok API**.

## Varför bör du använda Skapa Spreadsheet API?

- **Utvecklarvänligt** – Erbjuder SDK-bibliotek för flera språk och omfattande dokumentation, vilket förenklar integration jämfört med att bygga egna lösningar.
- **Arbetseffektivitet** – Möjliggör automatisering av dokumentkonsolidering, vilket minskar manuellt arbete.
- **Betala per användning** – Avgifterna baseras på API-användning utan förvalda licensavgifter.
- **Hanterad tjänst** – API:et är helt värdt, vilket innebär att du slipper underhåll av lokala servrar eller programuppdateringar.

## Hur man använder Skapa Spreadsheet API med SDK:er

### Skapa Spreadsheet API-specifikation

[Skapa Spreadsheet API-specifikationen](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodad)",
  "contentType": "MIME-typ",
  "fileDownloadName": "valfritt filnamn"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Användning av ett SDK är det snabbaste sättet att utveckla, eftersom det abstraherar lågnivådetaljer och låter dig bygga kalkylarket med koncist kod. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}