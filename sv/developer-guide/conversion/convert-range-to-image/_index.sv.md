---
title: "Konvertera Excel-område till bild – Aspose.Cells Cloud API"
description: "Konvertera ett specifikt område från en lokal Excel-fil till PNG, JPEG, SVG, TIFF eller BMP via Aspose.Cells Cloud REST API – inget uppladdning av hela arbetsboken krävs."
keywords: "Aspose.Cells Cloud, konvertera område till bild, Excel API, bildformat, PNG, JPEG, SVG, TIFF, BMP"
slug: konvertera-omrade-till-bild
api_version: "v4.0"
date: 2026-07-30
---

Anropet läser en lokal kalkylarksfil, konverterar det angivna området och returnerar bilden som en binär ström.

## Metod för att konvertera område till bild

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## Begärparametrar

| Namn               | Plats                             | Typ     | Krävs    | Beskrivning                                                                     |
| ------------------ | --------------------------------- | ------- | -------- | ------------------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data (`multipart/form-data`) | Fil     | **Ja**   | Den Excel-fil som ska bearbetas.                                                |
| **worksheet**      | Fråga                             | Sträng  | **Ja**   | Arbetsbladsnamn som innehåller området (t.ex. `Blad1`).                         |
| **range**          | Fråga                             | Sträng  | **Ja**   | Cellområde att konvertera, t.ex. `A1:C10`.                                      |
| **format**         | Fråga                             | Sträng  | **Ja**   | Utdataformat för bilden (`png`, `jpeg`, `svg`, `tiff`, `bmp`).                 |
| **printHeadings**  | Fråga                             | Boolean | Nej      | `true` för att inkludera rad-/kolumnrubriker i bilden.                         |
| **outPath**        | Fråga                             | Sträng  | Nej      | Mapp sökväg för den genererade filen om du vill lagra den i molnlagring.       |
| **outStorageName** | Fråga                             | Sträng  | Nej      | Namn på lagringstjänsten (t.ex. `MittLager`).                                  |
| **fontsLocation**  | Fråga                             | Sträng  | Nej      | URL eller sökväg till anpassade teckensnitt som används under konverteringen.  |
| **region**         | Fråga                             | Sträng  | Nej      | Språkidentifierare (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummer- och datumformat. |
| **password**       | Fråga                             | Sträng  | Nej      | Lösenord för krypterade arbetsböcker.                                           |
| **AutoRowsFit**    | Fråga                             | Boolean | Nej      | Justera radhöjd automatiskt innan rendering.                                   |
| **AutoColumnsFit** | Fråga                             | Boolean | Nej      | Justera kolumnbredd automatiskt innan rendering.                               |

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

### Exempel på lyckat svar (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="rapport.png"
Content-Length: 8423
```

Spara svarets brödtext till en fil (t.ex. `rapport.png`) för att visa den renderade bilden i en webbläsare.

---

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Hur använder man Convert Range to Image API med SDK:er?

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) beskriver ett offentligt tillgängligt API, vilket möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Blad1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Rapport.xlsx" \
     -F "outPath=output/rapport.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="rapport.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljnivådetaljerna och låter dig konvertera ett datoområde till en bildfil med minimal kod.  
Utforska den fullständiga listan över Aspose.Cells Cloud SDK:er i vårt [GitHub-arkiv](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er. Om inläsning från Gist är blockerad kan du ladda ner exemplen direkt från arkivet.