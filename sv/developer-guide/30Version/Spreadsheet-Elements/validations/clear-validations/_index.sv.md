---
title: "Ta bort alla kalkylbladsvalideringar – Aspose.Cells Cloud API"
second_title: "Dokumentation"
linktitle: "Ta bort"
type: docs
url: /sv/validations/clear/
keywords: "Aspose.Cells Cloud, Ta bort kalkylbladsvalideringar, Excel, REST API, Validering av kalkylark, API"
description: "Ta bort alla regler för datavalidering från ett kalkylblad i en Excel-fil med Aspose.Cells Cloud REST API. Inkluderar autentiseringsssteg, begärandebeskrivning, cURL-exempel, svarschema, felhantering och SDK-utdrag."
weight: 10
---

**Förutsättningar**

- Ett giltigt Aspose Cloud-konto.
- En JWT-åtkomsttoken som har erhållits via Aspose Clouds autentiserings-API (`/connect/token`).
- Arbetsboken måste lagras i din Aspose Cloud-lagring (eller så måste lämpliga frågeparametrar `folder`/`storageName` anges).

Denna REST API tar bort alla kalkylbladsvalideringar från ett Excel-kalkylblad.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Begärparametrar**

| Parameternamn | Typ   | Plats  | Beskrivning                                            |
| ------------- | ----- | ------ | ------------------------------------------------------ |
| name          | string | path   | Namnet på Excel-dokumentet.                            |
| sheetName     | string | path   | Namnet på kalkylbladet som innehåller valideringarna. |
| folder        | string | query  | Mappen där dokumentet är lagrat.                       |
| storageName   | string | query  | Namnet på lagringstjänsten.                            |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man anropar API:et med cURL efter att ha erhållit en JWT-token.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
  -X DELETE \
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

### Felhantering

| HTTP-status | Betydelse             | Beskrivning                                                |
| ----------- | --------------------- | ---------------------------------------------------------- |
| 400         | Felaktig begäran      | Begäran är felaktigt formaterad eller saknar nödvändiga parametrar. |
| 401         | Auktorisering saknas  | JWT-token saknas, är ogiltig eller har gått ut.            |
| 404         | Hittades inte         | Den angivna arbetsboken eller kalkylbladet finns inte.     |
| 500         | Internt serverfel     | Ett oväntat fel uppstod på serversidan.                    |

Felsvaret följer samma JSON-struktur med fälten `Code` och `Message`, till exempel:

```json
{
  "Code": 401,
  "Message": "Ogiltig eller utgången token."
}
```

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på affärslogik. Se [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}