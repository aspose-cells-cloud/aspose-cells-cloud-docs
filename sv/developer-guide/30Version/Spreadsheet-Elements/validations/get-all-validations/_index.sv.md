---
title: "Hämta alla valideringar från ett Excel-kalkylblad"
second_title: "Document"
linktitle: "Hämta alla"
type: docs
url: /sv/validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, kalkylbladsvalideringar, REST API, hämta alla valideringar, SDK:er"
description: "Hämta alla kalkylbladsvalideringar från ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Stöder flera SDK:er (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) för snabb integration."
weight: 10
---

Kalkylbladsvalideringar låter dig definiera regler som begränsar vilken typ eller vilket intervall av data som får anges i celler. De används ofta för att säkerställa datointegritet, till exempel genom att begränsa inmatningar till en lista med värden, datum inom ett visst intervall eller numeriska gränser.

Denna REST API hämtar alla kalkylbladsvalideringar från ett Excel-kalkylblad.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Begärparametrar**

| Parameter Name | Typ    | Plats  | Beskrivning                                  |
| -------------- | ------ | ------ | -------------------------------------------- |
| name           | string | path   | Namn på Excel-dokumentet.                    |
| sheetName      | string | path   | Namn på kalkylbladet.                        |
| folder         | string | query  | Mappväg där dokumentet lagras.               |
| storageName    | string | query  | Namn på lagringstjänsten.                    |

**Svarsstatuskoder**

| Kod | Beskrivning                                   |
|-----|-----------------------------------------------|
| 200 | Lyckad begäran – lista med valideringar       |
| 401 | Auktorisering fel – ogiltigt eller saknat token |
| 404 | Ej hittad – dokument eller kalkylblad saknas  |
| 500 | Internt serverfel                             |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells Cloud-webbtjänster. **Förutsättning:** du måste inkludera en giltig JWT-token i `Authorization`-headern.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "Värdet måste vara mellan 1 och 100."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Alternativ1,Alternativ2,Alternativ3\"",
      "showErrorMessage": true,
      "errorMessage": "Välj ett värde från listan."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Moln SDK-familj

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}