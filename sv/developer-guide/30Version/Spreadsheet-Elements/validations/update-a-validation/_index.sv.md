---
title: "Uppdatera en validering på ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Uppdatera"
type: docs
url: /sv/validations/update/
keywords: "Aspose.Cells Cloud, uppdatering av Excel-validering, REST API, validering av arbetsblad, Excel API"
description: "Hur man uppdaterar en validering på ett Excel-arbetsblad med Aspose.Cells Cloud REST API, med cURL-exempel och SDK-kodsnuttar för flera programmeringsspråk."
weight: 10
ArticleTitle: "Uppdatera validering på arbetsblad med Aspose.Cells Cloud API"
---

Denna REST API uppdaterar en validering på ett Excel-arbetsblad med dess index.

Innan du anropar denna endpoint, skaffa ett JWT-åtkomsttoken med lämpliga omfattningar (t.ex. `Cells.ReadWrite`). Inkludera token i `Authorization`-huvudet enligt exemplen.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Begäringsparametrar**

| Parametername   | Typ     | Plats  | Beskrivning                                                    |
| --------------- | ------- | ------ | -------------------------------------------------------------- |
| name            | string  | path   | Namnet på arbetsboksfilen.                                     |
| sheetName       | string  | path   | Namnet på arbetsbladet som innehåller valideringen.            |
| validationIndex | integer | path   | Det nollbaserade indexet för den validering som ska uppdateras.|
| validation      | object  | body   | Ett JSON-objekt som definierar de uppdaterade valideringsinställningarna. |
| folder          | string  | query  | Mappen i molnlagring där arbetsboken finns.                    |
| storageName     | string  | query  | Namnet på lagringstjänsten (om en anpassad lagring används).   |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att anropa Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**Möjliga HTTP-statuskoder**

| Kod | Betydelse                               | Beskrivning |
|-----|-----------------------------------------|-------------|
| 200 | OK                                      | Valideringen uppdaterades framgångsrikt. |
| 400 | Felaktig begäran                        | Begäran är felaktigt formaterad eller saknar nödvändiga parametrar. |
| 401 | Oautentiserad                           | Ogiltig eller saknad JWT-token. |
| 403 | Förbjuden                               | Token har inte tillräckliga omfattningar. |
| 404 | Hittades inte                           | Den angivna arbetsboken, arbetsbladet eller valideringsindexet finns inte. |
| 500 | Internt serverfel                       | Ett oväntat fel inträffade på servern. |

För mer information om felhantering, se <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud-feldokumentationen</a>.

Du kanske också vill utforska relaterade åtgärder, såsom att lägga till en ny validering eller ta bort en befintlig:

- [Lägg till en validering på ett arbetsblad](https://docs.aspose.cloud/cells/validations/add/)
- [Ta bort en validering på ett arbetsblad](https://docs.aspose.cloud/cells/validations/delete/)

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på lågnivå och låter dig fokusera på din affärslogik. Kolla in <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}