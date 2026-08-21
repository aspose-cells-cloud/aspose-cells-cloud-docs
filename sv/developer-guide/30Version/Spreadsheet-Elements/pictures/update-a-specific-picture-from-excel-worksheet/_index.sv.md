---
title: "Uppdatera bild i en Excel-fil"
second_title: "Dokument"
linktitle: "Uppdatera"
type: docs
url: /sv/pictures/update/
aliases: [  /sv/update-a-specific-picture-from-excel-workshee/ ]
keywords: "Aspose.Cells Cloud, Excel, Uppdatera bild, REST API, SDK"
description: "Lär dig hur du uppdaterar en bild i ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Innehåller begärandedetaljer, ett cURL-exempel och SDK-utdrag för flera språk."
ArticleTitle: "Uppdatera bild i en Excel-fil med Aspose.Cells Cloud REST API"
weight: 70
---

Denna REST API uppdaterar en bild, identifierad med dess index, i ett Excel-arbetsblad.

**Förutsättningar:** Du måste ha ett giltigt Aspose Cloud JWT-token, målfilen lagrad i din Aspose Cloud-lagring och använda API-version 3.0 eller senare.

## PostWorksheetPicture API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäran parametrar**

| Parameternamn | Typ     | Plats  | Beskrivning                                                   |
| ------------- | ------- | ------ | ------------------------------------------------------------- |
| name          | string  | path   | Namnet på Excel-dokumentet.                                   |
| sheetName     | string  | path   | Namnet på arbetsbladet som innehåller bilden.                 |
| pictureIndex  | integer | path   | Nollbaserat index för den bild som ska uppdateras.            |
| picture       | object  | body   | JSON-objekt som beskriver de bildegenskaper som ska uppdateras. |
| folder        | string  | query  | Mappen där dokumentet är lagrat.                              |
| storageName   | string  | query  | Namnet på lagringstjänsten.                                   |

**Obs:** Bildindexet är nollbaserat. Stödda bildformat inkluderar JPEG, PNG, BMP och GIF. Den maximala bildstorleken är 10 MB.

### Felresponser

| HTTP-kod | Beskrivning                                                 |
| -------- | ----------------------------------------------------------- |
| 401      | Oauktoriserad – token saknas eller är ogiltig.              |
| 404      | Inte hittad – den angivna filen, arbetsbladet eller bildindexet finns inte. |
| 400      | Felaktig begäran – felaktig begäransyntax eller ogiltiga parametrar. |
| 500      | Internt serverfel – ett oväntat tillstånd uppstod.          |

<a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör en anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*Se även:* Lägg till bild, Ta bort bild, Hämta bild, Rensa bilder – andra bildrelaterade operationer i Aspose.Cells Cloud API.