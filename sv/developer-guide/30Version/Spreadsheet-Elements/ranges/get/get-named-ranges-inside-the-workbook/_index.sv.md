---
title: "Hämta namngivna intervall i en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Namn"
type: docs
url: /sv/ranges/get/name/
aliases: [  /sv/get-named-ranges-inside-the-workbook/ ]
keywords: "namngivna intervall, Excel, Aspose.Cells, moln-API, kalkylblad"
description: "Hämta namngivna intervall från en Excel-arbetsbok med Aspose.Cells Cloud REST API. Innehåller begärandedetaljer, exempel på cURL-kommandon och SDK-exempel för flera programmeringsspråk."
ArticleTitle: "Hämta namngivna intervall i en Excel-arbetsbok – Aspose.Cells Cloud API"
weight: 10
---

Denna REST API returnerar information om namngivna intervall som definierats i kalkylblad.

**Bakgrund** – Ett *namngivet intervall* är en användardefinierad identifierare som pekar på en specifik cell eller cellgrupp i ett kalkylblad. Namngivna intervall förenklar formelskapande, förbättrar läsbarheten och möjliggör programmässig åtkomst till ofta använda områden i en arbetsbok.

**Förutsättningar** – Åtkomst till Aspose.Cells Cloud API kräver en giltig JWT-åtkomsttoken. Skaffa token genom att autentisera med ditt Aspose Cloud-klient-ID och klienthemlighet via OAuth 2.0-tokenändpunkten. Inkludera token i `Authorization: Bearer <jwt token>`-huvudet i varje begäran.

## GetNamedRanges API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn   | Typ    | Plats        | Beskrivning                                   |
| --------------- | ------ | ------------ | --------------------------------------------- |
| name            | string | Sökväg       | Namnet på Excel-dokumentet.                   |
| folder          | string | Frågesträng  | Mappen som innehåller dokumentet.             |
| storageName     | string | Frågesträng  | Lagringsnamnet där dokumentet är lagrat.      |

**HTTP-statuskoder**

| Kod  | Betydelse                   | Beskrivning                                             |
|------|-----------------------------|---------------------------------------------------------|
| 200  | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Otillåten                   | Ogiltig eller saknad JWT-token.                          |
| 413  | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.        |
| 500  | Internt serverfel           | Oväntat serverfel.                                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att anropa Aspose.Cells-webbtjänster. Exemplet nedan visar hur du hämtar namngivna intervall med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Svarsmodell**

| Fält           | Typ     | Beskrivning                                              |
|----------------|---------|----------------------------------------------------------|
| `ColumnCount`  | heltal  | Antal kolumner i intervallet.                            |
| `ColumnWidth`  | nummer  | Bredd på varje kolumn (i punkter).                       |
| `FirstColumn`  | heltal  | Nollbaserat index för den första kolumnen i intervallet. |
| `FirstRow`     | heltal  | Nollbaserat index för den första raden i intervallet.    |
| `Name`         | sträng  | Den användardefinierade namn på intervallet.             |
| `RefersTo`     | sträng  | En formel som definierar cellreferensen (t.ex. `=Sheet1!$B$10:$H$10`). |
| `RowCount`     | heltal  | Antal rader i intervallet.                               |
| `RowHeight`    | nummer  | Höjd på varje rad (i punkter).                           |
| `Worksheet`    | sträng  | Namnet på kalkylbladet som innehåller intervallet.       |

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att integrera denna funktionalitet. SDK:er hanterar detaljer på lågnivå så att du kan fokusera på din affärslogik. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}