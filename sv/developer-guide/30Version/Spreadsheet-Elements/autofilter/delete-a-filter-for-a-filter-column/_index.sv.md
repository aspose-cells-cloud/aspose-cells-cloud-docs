---
title: "Ta bort ett filter från ett Excel-ark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Ta bort filter"
type: docs
url: /sv/delete-filter/
aliases: [/sv/delete-a-filter-for-a-filter-column/, /sv/delete-auto-filter/]
keywords: "Aspose.Cells Cloud ta bort filter, Excel, REST API, SDK"
description: "Lär dig hur du tar bort ett autofilter från ett Excel-ark med Aspose.Cells Cloud REST API, cURL och SDK:er (t.ex. C#, Java, Python etc.). Inkluderar slutpunkt, parametrar, autentisering och exempelkod."
weight: 100
---

## REST API

Detta REST API tar bort ett **autofilter** från ett Excel-ark.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärans parametrar

| Parametername            | Typ     | Plats  | Obligatorisk? | Beskrivning                                                                                     |
| ------------------------ | ------- | ------ | ------------- | ----------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path   | Ja            | Namnet på arbetsboken.                                                                          |
| **sheetName**            | string  | Path   | Ja            | Namnet på arket.                                                                                |
| **range**                | string  | Query  | Nej           | Cellintervallet som filtret gäller (t.ex. `A1:C10`).                                          |
| **fieldIndex**           | integer | Query  | Ja            | Nollbaserat index för kolumnen som filtret tillämpas på.                                       |
| **dateTimeGroupingType** | string  | Query  | Nej           | Hur datum-/tidsvärden grupperas: `Day`, `Hour`, `Minute`, `Month`, `Second` eller `Year`.     |
| **year**                 | integer | Query  | Nej           | Årskomponent för datumgruppering.                                                               |
| **month**                | integer | Query  | Nej           | Månadskomponent för datumgruppering.                                                            |
| **day**                  | integer | Query  | Nej           | Dagkomponent för datumgruppering.                                                               |
| **hour**                 | integer | Query  | Nej           | Timkomponent för datumgruppering.                                                               |
| **minute**               | integer | Query  | Nej           | Minutkomponent för datumgruppering.                                                             |
| **second**               | integer | Query  | Nej           | Sekundkomponent för datumgruppering.                                                            |
| **matchBlanks**          | boolean | Query  | Nej           | `true` / `false` – om tomma celler ska inkluderas i filtret.                                   |
| **refresh**              | boolean | Query  | Nej           | `true` / `false` – om arket ska uppdateras efter borttagning.                                 |
| **folder**               | string  | Query  | Nej           | ursprunglig mapp för arbetsboken.                                                               |
| **storageName**          | string  | Query  | Nej           | Lagringsnamn.                                                                                   |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades korrekt; svaret innehåller åtgärdens detaljer.          |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).            |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                                             |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.                           |
| 500 | Internal Server Error       | Oväntat serverfel.                                                          |

## Hur du använder DeleteWorksheetFilter API med SDK:er

### DeleteWorksheetFilter API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
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

Att använda en SDK är det mest effektiva sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektoppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}