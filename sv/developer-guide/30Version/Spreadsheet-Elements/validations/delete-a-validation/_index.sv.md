---
title: "Ta bort kalkylbladsvalidering – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Ta bort"
type: docs
url: /validations/delete/
keywords: "Ta bort, kalkylbladsvalidering, Aspose.Cells Cloud, Excel-API"
description: "Lär dig hur du tar bort en kalkylbladsvalidering från en Excel-fil med Aspose.Cells Cloud REST API. Inkluderar slutpunkt, parametrar, autentiseringsuppgifter, cURL-exempel, felhantering och SDK-kodavsnitt."
weight: 10
---

Denna REST API tar bort en kalkylbladsvalidering med dess nollbaserade index från ett kalkylblad i en Excel-fil.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Begärparametrar**

| ParameterName    | Typ     | Plats  | Beskrivning                                         |
| ---------------- | ------- | ------ | --------------------------------------------------- |
| name             | string  | path   | Namnet på Excel-filen.                              |
| sheetName        | string  | path   | Namnet på kalkylbladet.                             |
| validationIndex  | integer | path   | Det nollbaserade indexet för valideringen som ska tas bort. |
| folder           | string  | query  | Mappen som innehåller dokumentet.                   |
| storageName      | string  | query  | Namnet på lagringstjänsten.                         |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att anropa Aspose.Cells-webbtjänsten. Exemplet nedan visar hur du tar bort en validering med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request (Felaktig begäran) | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized (Obehörig)     | Ogiltigt eller saknat JWT-token.                   |
| 413 | Payload Too Large (För stor payload) | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error (Internt serverfel) | Oväntat serverfel. |

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att integrera den här åtgärden i din applikation. SDK:er hanterar detaljer på lågnivå så att du kan fokusera på affärslogik. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du tar bort en kalkylbladsvalidering med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}