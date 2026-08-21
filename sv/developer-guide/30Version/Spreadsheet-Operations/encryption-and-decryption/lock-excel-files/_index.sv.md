---
title: "Lås Excel-filer"
second_title: "Dokument"
linktitle: "Lås Excel-filer"
type: docs
url: /lock-excel-files/
aliases: [/lock/without-storage/, /lock/, /lock/without-using-storage/]
keywords: "Lås, Excel, API, Aspose.Cells, Moln, REST, Arbetsbok, Kalkylark, SDK"
description: "Lär dig hur du låser Excel-arbetsböcker med Aspose.Cells Cloud REST API (v3.0). Inkluderar HTTPS-slutpunkt, autentisering, cURL-förfrågan, svarschema och SDK-kodexempel för C#, Java, Python och mer."
ArticleTitle: "Lås Excel-filer – Aspose.Cells Cloud API-dokumentation"
weight: 70
---

**API-version:** v3.0 (nuvarande)

Detta REST API **låser** Excel-arbetsböcker.

## PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Förutsättningar** – Förfrågan måste skickas via **HTTPS** och inkludera ett giltigt OAuth 2.0 Bearer-token i `Authorization`-headern.

### Följande parametrar används i förfrågan

| Parametername | Typ   | Plats                   | Beskrivning                                  |
| ------------- | ----- | ----------------------- | -------------------------------------------- |
| file          | fil   | form-data (multipart body) | Den Excel-arbetsbok som ska laddas upp och låsas. |
| password      | sträng | frågesträng             | Lösenord för arbetsboken (valfritt).         |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du **anropar** moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*Du kan ladda ner en exempelarbetsbok — [Sample.xlsx](https://example.com/Sample.xlsx) — för att testa förfrågan.*

**Obs:** API:et stöder filer upp till 100 MB; större förfrågningar kan resultera i ett svar med statuskod 413 (Förfrågan för stor).

### **Svarsdetaljer**

| Fält        | Typ             | Beskrivning                                      |
| ----------- | --------------- | ------------------------------------------------ |
| Filename    | sträng          | Namn på den låsta arbetsboken som returneras av tjänsten. |
| FileSize    | heltal          | Storlek på den låsta filen i byte.               |
| FileContent | sträng (Base64) | Den låsta arbetsboken kodad som en Base64-sträng. |

För att hämta den låsta arbetsboken, avkoda `FileContent`-värdet från Base64 och spara den med det `Filename` som anges i svaret.

### **Felhantering**

– API:et returnerar standard-HTTP-statuskoder (t.ex. `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) tillsammans med ett JSON-felobjekt som innehåller fälten `Code` och `Message`.

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}