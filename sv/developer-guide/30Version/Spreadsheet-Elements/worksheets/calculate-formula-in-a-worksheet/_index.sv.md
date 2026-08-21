---
title: "Beräkna en formel i ett Excel-ark"
second_title: "Dokument"
linktitle: "Beräkna"
type: docs
url: /sv/worksheets/calculate-formula/
aliases: [  /sv/calculate-formula-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, formelberäkning, REST API, SDK:er, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Beräkna formler i ett Excel-ark med Aspose.Cells Cloud REST API. Stöder flera SDK:er (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) med klara, direktanvändbara exempel."
weight: 20
ArticleTitle: "Beräkna en formel i ett Excel-ark – Aspose.Cells Cloud-dokumentation"
---

Detta REST API returnerar **det beräknade värdet av en formel** i ett ark. Det kan användas för att **evaluera en Excel-formel** direkt från din applikation.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **Förfrågningsparametrar**

| Parameternamn | Typ   | Plats  | Beskrivning                                           |
| ------------- | ----- | ------ | ----------------------------------------------------- |
| name          | string | path   | Namn på Excel-filen.                                  |
| sheetName     | string | path   | Namn på arket som innehåller formeln.                |
| formula       | string | query  | Formeln som ska evalueras (t.ex. `SUM(A5:A10)`).     |
| folder        | string | query  | Mapp där dokumentet lagras.                           |
| storageName   | string | query  | Namn på lagringstjänsten (om tillämpligt).           |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Autentisering

Alla förfrågningar måste innehålla en giltig **Bearer JWT-token** i `Authorization`-headern:

```
Authorization: Bearer <din_jwt_token>
```

Du kan erhålla en token genom att följa OAuth 2.0-flödet som beskrivs i Aspose.Cells Cloud:s autentiseringsguide.

### Möjliga svarsstatuskoder

| Kod | Beskrivning                                         |
|-----|-----------------------------------------------------|
| 200 | Förfrågan lyckades; formelvärdet returneras.        |
| 400 | Felaktig förfrågan – saknade eller ogiltiga parametrar. |
| 401 | Ej auktoriserad – ogiltig eller saknad JWT-token.   |
| 404 | Ej hittad – den angivna filen eller arket finns inte. |
| 500 | Internt serverfel – oväntat tillstånd på servern.   |

Du kan använda kommandoradsverktyget **cURL** för enkelt anropa Aspose.Cells Cloud:s webbtjänster. Exemplet nedan visar hur du begär ett formelresultat med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Molnsdk-familj

Att använda en SDK är det snabbaste sättet att integrera API:et. En SDK hanterar detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud:s SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**Se även:**  
- [Hämta ark](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [Uppdatera ark](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [Beräkna alla formler](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---