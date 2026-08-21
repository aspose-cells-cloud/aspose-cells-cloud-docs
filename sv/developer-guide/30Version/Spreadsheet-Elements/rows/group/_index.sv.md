---
title: "Gruppera rader i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Gruppera"
type: docs
url: /rows/group/
aliases: [/group-rows-in-excel-worksheet/]
keywords: "gruppera rader, Excel, Aspose.Cells Cloud, REST API, SDK, arbetsblad, Excel API"
description: "Gruppera rader i ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Stöder flera SDK:er (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) för enkel integration."
weight: 60
ArticleTitle: "Gruppera rader i Excel-arbetsblad med Aspose.Cells Cloud API"
---

Denna REST API grupperar rader i ett Excel-arbetsblad.

**Förutsättningar:**  
- Ett giltigt OAuth 2.0-åtkomsttoken (Bearer JWT) måste anges i `Authorization`-headern.  
- Arbetsboken måste redan finnas i den angivna `folder` för den valda `storageName` (eller standardlagringen) innan begäran skickas.

## PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäran parametrar**

| Parameter Name | Typ     | Plats  | Beskrivning                                                              |
| -------------- | ------- | ------ | ------------------------------------------------------------------------ |
| name           | string  | path   | Namnet på arbetsboksfilen.                                               |
| sheetName      | string  | path   | Namnet på arbetsbladet.                                                  |
| firstIndex     | integer | query  | Nollbaserat index för den första rad som ska grupperas.                 |
| lastIndex      | integer | query  | Nollbaserat index för den sista rad som ska grupperas.                  |
| hide           | boolean | query  | Anger om de grupperade raderna ska döljas (`true` eller `false`).       |
| folder         | string  | query  | Sökvägen till mappen som innehåller arbetsboken.                        |
| storageName    | string  | query  | Namnet på lagringen där arbetsboken finns.                              |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltigt eller saknat JWT-token.                        |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internal Server Error       | Oväntat serverfel.                                      |

Typiska felmeddelanden:

- **400 Bad Request** – kontrollera att `firstIndex` och `lastIndex` är giltiga heltal och att `firstIndex` ≤ `lastIndex`.  
- **401 Unauthorized** – verifiera att `Authorization`-headern innehåller ett giltigt JWT-token.  
- **404 Not Found** – se till att arbetsboken (`name`) och arbetsbladet (`sheetName`) finns i den angivna `folder`/`storageName`.

{{< /tab >}}

{{< /tabs >}}

**Se även:** [Avgruppera rader i ett Excel-arbetsblad](../rows/ungroup/ "Avgruppera rader i ett Excel-arbetsblad"), [Dölj rader i ett Excel-arbetsblad](../rows/hide/ "Dölj rader i ett Excel-arbetsblad"), [Visa rader i ett Excel-arbetsblad](../rows/unhide/ "Visa rader i ett Excel-arbetsblad").

## Cloud SDK-familj

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}