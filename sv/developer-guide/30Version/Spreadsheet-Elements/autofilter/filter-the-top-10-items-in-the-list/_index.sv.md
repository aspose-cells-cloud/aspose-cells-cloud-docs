---
title: "Lägg till Top 10-filter i ett Excel-arbetsblad (Aspose.Cells Cloud)"
ArticleTitle: "Lägg till Top 10-filter i ett Excel-arbetsblad – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Lägg till top 10-filter"
type: docs
url: /sv/autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, Top 10-filter, Excel API"
description: "Lär dig hur du tillämpar ett Top 10 AutoFilter på ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Inkluderar slutpunkt, parametrar, HTTPS cURL-exempel, autentiseringsuppgifter, felhantering och SDK-utdrag för C#, Java, Python med mera."
weight: 65
---

Denna REST API filtrerar **Top 10**-objekten i en lista.

> **Förutsättningar**  
> • Skaffa ett giltigt JWT-token med Aspose.Cells Cloud-autentisering.  
> • Ladda upp Excel-arbetsboken till din Aspose Cloud-lagring (eller ange lagring/mapp där den finns).  
> • Känn till namnet på arbetsbladet och cellintervallet som du vill filtrera.

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn   | Typ     | Plats   | Obligatoriskt | Standard | Beskrivning                                                                 |
| --------------- | ------- | ------- | ------------- | -------- | --------------------------------------------------------------------------- |
| **name**        | sträng  | sökväg  | Ja            | —        | Namnet på Excel-filen.                                                      |
| **sheetName**   | sträng  | sökväg  | Ja            | —        | Namnet på arbetsbladet som innehåller data.                                 |
| **range**       | sträng  | fråga   | Ja            | —        | Cellintervallet som filter tillämpas på (t.ex. `A1:B10`).                   |
| **fieldIndex**  | heltal  | fråga   | Ja            | —        | Nollbaserat index för kolumnen som filter tillämpas på.                      |
| **isTop**       | boolean | fråga   | Ja            | `true`   | `true` för att filtrera de högsta objekten; `false` för de lägsta objekten.   |
| **isPercent**   | boolean | fråga   | Nej           | `false`  | `true` för att tolka `itemCount` som en procentandel; `false` för ett absolut antal. |
| **itemCount**   | heltal  | fråga   | Nej           | `10`     | Antal objekt som ska inkluderas i filtert.                                   |
| **matchBlanks** | boolean | fråga   | Nej           | `false`  | `true` för att inkludera tomma celler i filterresultatet.                    |
| **refresh**     | boolean | fråga   | Nej           | `false`  | `true` för att uppdatera filtret efter att det tillämpats.                   |
| **folder**      | sträng  | fråga   | Nej           | —        | Mappen i lagringen där Excel-filen finns.                                    |
| **storageName** | sträng  | fråga   | Nej           | —        | Namnet på Aspose Cloud-lagringen.                                            |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Typiska felresponser**

```json
{
    "Code":400,
    "Message":"Bad Request – saknade eller ogiltiga parametrar."
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – ogiltigt eller saknat JWT-token."
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – den uppladdade filen överskrider tillåten storlek."
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – oväntat serverfel."
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller operationsdetaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltigt eller saknat JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel. |

## Hur du använder PutWorksheetFilterTop10 API med SDK:er

### PutWorksheetFilterTop10 API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}