---
title: "Konvertera listobjekt till intervall – Aspose.Cells Cloud API"
ArticleTitle: "Konvertera listobjekt till intervall med Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Konvertering"
type: docs
url: /list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, konvertera listobjekt till intervall, Excel REST API"
description: "Lär dig hur du konverterar ett Excel-listobjekt (tabell) till ett intervall med Aspose.Cells Cloud REST API. Innehåller begäransyntax, parametrar, exempel på cURL, svarschema, autentiseringsinformation, felkoder och SDK-exempel."
weight: 30
---

Denna REST API konverterar ett **listobjekt (tabell)** till ett **intervall** i ett Excel-ark.

**Förutsättningar:**  
Innan du anropar endpointet, se till att arbetsboken är uppladdad till din Aspose Cloud-lagring, att arket innehåller det mål-listobjektet och att du använder ett format som stöds (t.ex. .xlsx, .xlsm).

## REST API

**Autentisering**  
För att kunna utföra den här åtgärden måste du inkludera en giltig JWT-token i `Authorization`-headern. Skaffa token genom att skicka en POST-begäran till OAuth 2.0-tokenändpunkten med ditt klient-ID och klienthemlighet. Token måste inkludera scope:et `Cells.ReadWrite` och är giltig under den tid som token-tjänsten anger.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Namn                | Typ     | Plats  | Obligatoriskt | Standardvärde | Beskrivning                                            |
| ------------------- | ------- | ------ | ------------- | ------------- | ------------------------------------------------------ |
| **name**            | string  | path   | Ja            | –             | Namnet på Excel-filen.                                 |
| **sheetName**       | string  | path   | Ja            | –             | Namnet på arket som innehåller listobjektet.           |
| **listObjectIndex** | integer | path   | Ja            | –             | Nollbaserat index för listobjektet (tabellen) som ska konverteras. |
| **folder**          | string  | query  | Nej           | –             | Mappväg där filen lagras.                              |
| **storageName**     | string  | query  | Nej           | –             | Namn på lagringstjänsten.                              |

> **Obs!** Denna åtgärd fungerar endast med moderna Excel-format som **.xlsx** och **.xlsm**. Listobjektet får inte vara skyddat. Mer information om listobjekt finns i [Översikt över listobjekt](/list-objects/). För detaljer om hur du arbetar med intervall, se [intervall-dokumentationen](/ranges/).

### cURL-exempel (begäran)

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <ditt-jwt-token>"
```

{{< /tab >}}

#### Svarschema

API:t returnerar ett **200 OK**-svar med information om det nyskapade intervallet.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Fält            | Typ     | Beskrivning                                     |
| --------------- | ------- | ----------------------------------------------- |
| **Code**        | integer | HTTP-liknande statuskod (200 anger lyckad åtgärd). |
| **Status**      | string  | Textuell statusmeddelande.                      |
| **RangeName**   | string  | Det namn som tilldelats det skapade intervallet. |
| **Address**     | string  | Fullständig adress till intervallet, inklusive arknamn. |
| **FirstRow**    | integer | Nollbaserat index för första raden i intervallet. |
| **FirstColumn** | integer | Nollbaserat index för första kolumnen i intervallet. |
| **RowCount**    | integer | Antal rader i intervallet.                      |
| **ColumnCount** | integer | Antal kolumner i intervallet.                   |

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                            |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK                          | Filter har tillämpats korrekt; svaret innehåller åtgärdens information. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filformat som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.     |
| 500 | Internal Server Error       | Oväntat serverfel.                                     |

**Felsvarschema (exempel):**

```json
{
  "Code": 400,
  "Message": "Ogiltigt listObjectIndex. Index måste ligga mellan 0 och 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Titta in på [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}