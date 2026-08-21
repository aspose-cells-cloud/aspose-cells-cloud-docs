---
title: "Lägg till ett kalkylbladsvalidering till ett Excel-kalkylblad"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /validations/add/
keywords: "Lägg till kalkylbladsvalidering, Excel, Aspose.Cells Cloud, REST API, Kalkylark, Valideringsregel"
description: "Använd Aspose.Cells Cloud REST API för att lägga till en kalkylbladsvalidering till en Excel-fil. SDK:er finns tillgängliga för C#, Java, PHP, Ruby, Node.js, Python, Perl, Go och Swift."
weight: 10
---

Denna REST API lägger till en kalkylbladsvalidering till ett Excel-kalkylblad.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Parametrar för begäran**

| Parameter Namn | Typ    | Plats  | Beskrivning                                                |
| -------------- | ------ | ------ | ---------------------------------------------------------- |
| name           | string | path   | Namn på Excel-dokumentet.                                  |
| sheetName      | string | path   | Namn på kalkylbladet.                                      |
| range          | string | query  | Cellomfång till vilket valideringen tillämpas (t.ex. A1:B10). |
| validation     | object | body   | Definition av valideringsregel.                            |
| folder         | string | query  | Mapp som innehåller dokumentet.                            |
| storageName    | string | query  | Namn på lagringstjänsten.                                  |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation) definierar ett offentligt tillgängligt programmeringssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
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

## Molnsdk-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}