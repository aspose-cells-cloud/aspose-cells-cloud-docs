---
title: "Aspose.Cells Cloud – Konvertera Excel-område till HTML"
description: "Konvertera ett specifikt område av en Excel-fil (t.ex. A1:C10) till en HTML-fil med Aspose.Cells Cloud REST API. Inkluderar autentisering, begärexempel, svarshantering, SDK-utdrag och felkoder."
keywords: "Aspose.Cells, Excel till HTML, områdeskonvertering, moln-API, kalkylark"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Konvertera ett valt område i en lokal Excel-arbetsbok till en HTML-fil direkt via Aspose.Cells Cloud. Konverteringen sker helt och hållet på molntjänstens servrar, så du behöver aldrig ladda upp hela arbetsboken eller ha Excel installerat lokalt.

## API för att konvertera område till HTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

Begärandetexten är `multipart/form-data` och innehåller kalkylarkfilen. Alla andra alternativ anges som frågeparametrar.

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:erna är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Namn               | Typ     | Plats      | Obligatorisk | Beskrivning                                                                  |
| ------------------ | ------- | ---------- | ------------ | ---------------------------------------------------------------------------- |
| **Spreadsheet**    | Fil     | FormData   | Ja           | Den Excel-arbetsbok som ska konverteras.                                     |
| **worksheet**      | Sträng  | Fråga      | Ja           | Namn på kalkylbladet som innehåller området.                                 |
| **range**          | Sträng  | Fråga      | Ja           | Cellområde som ska konverteras, t.ex. `A1:C10`.                              |
| **outPath**        | Sträng  | Fråga      | Nej          | Mappväg där den resulterande HTML-filen ska lagras (standard `null`).        |
| **outStorageName** | Sträng  | Fråga      | Nej          | Namn på lagringstjänsten för utdatafilen.                                    |
| **fontsLocation**  | Sträng  | Fråga      | Nej          | Sökväg till en anpassad typsnittsmapp.                                       |
| **AutoRowsFit**    | Boolean | Fråga      | Nej          | Justera automatiskt höjden på alla rader i kalkylbladet.                      |
| **AutoColumnsFit** | Boolean | Fråga      | Nej          | Justera automatiskt bredden på alla kolumner i kalkylbladet.                  |
| **region**         | Sträng  | Fråga      | Nej          | Språk- och regionsidentifierare (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummer- och datumformat. |
| **password**       | Sträng  | Fråga      | Nej          | Lösenord för att öppna ett skyddat kalkylark.                                |
| **fontsLocation**  | Sträng  | Fråga      | Nej          | Anpassad plats för typsnitt.                                                  |
| **region**         | Sträng  | Fråga      | Nej          | Inställning för kalkylarksregion/språk.                                      |
| **password**       | Sträng  | Fråga      | Nej          | Lösenord för att öppna kalkylarkfilen.                                       |

## Svar

API:et returnerar den konverterade HTML-filen som en **binär ström** (`application/octet-stream`).

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

### Exempel på lyckad respons (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Produkt</th><th>Pris</th></tr>
  <tr><td>Widget A</td><td>10 $</td></tr>
  <tr><td>Widget B</td><td>15 $</td></tr>
</table>
```

Spara responsens brödtext till en fil (t.ex. `report.html`) för att visa den renderade tabellen i en webbläsare.

---

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Hur använder man API:et för att konvertera område till HTML med SDK:er?

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) beskriver ett offentligt tillgängligt API, vilket möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Produkt</th><th>Pris</th></tr>
  <tr><td>Widget A</td><td>10 $</td></tr>
  <tr><td>Widget B</td><td>15 $</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljnivårelaterade aspekter och tillåter dig att konvertera ett datoområde till en HTML-fil med minimal kod.  
Utforska den fullständiga listan över Aspose.Cells Cloud SDK:er i vårt [GitHub-arkiv](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er. Om inläsning från Gist är blockerad kan du ladda ner exemplen direkt från arkivet.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}