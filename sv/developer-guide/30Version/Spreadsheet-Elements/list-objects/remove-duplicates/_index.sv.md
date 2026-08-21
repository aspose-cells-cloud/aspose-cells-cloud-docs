---
title: "Ta bort dubbletter från en ListObject – Aspose.Cells Cloud API-dokumentation"
second_title: "Dokument"
linktitle: "Ta bort dubbletter"
type: docs
keywords: "ta bort dubbletter, listobject, Aspose.Cells Cloud API, Excel, REST"
url: /list-objects/remove-duplicates/
description: "Lär dig hur du tar bort dubbletter från en ListObject i ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar endpoint, parametrar, autentisering samt exempel på begäranden och svar."
weight: 20
---

Denna REST API tar bort dubbletter från en **ListObject** i ett Excel-ark.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **Begärandeparametrar**

| Parameternamn       | Typ     | Plats  | Beskrivning                                               |
| ------------------- | ------- | ------ | --------------------------------------------------------- |
| **name**            | String  | Path   | Namnet på Excel-filen.                                    |
| **sheetName**       | String  | Path   | Namnet på arket som innehåller listobjektet.              |
| **listObjectIndex** | Integer | Path   | Det nollbaserade indexet för det listobjekt som ska bearbetas. |
| **folder**          | String  | Query  | (Valfritt) Sökvägen till mappen där filen lagras.         |
| **storageName**     | String  | Query  | (Valfritt) Namnet på lagringstjänsten.                    |

### Exempel på begäran (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
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
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "Dubbletterna togs framgångsrikt bort."
}
```

{{< /tab >}}
{{< /tabs >}}

### Svar

Vid lyckad begäran returnerar tjänsten ett JSON-objekt som liknar exemplet ovan. Fälten är:

- **Code** – HTTP-statuskod (`200` för lyckad åtgärd).
- **Status** – Textuell beskrivning av statusen.
- **DuplicateRowsRemoved** – Antal rader som togs bort.
- **Message** – Ytterligare information om åtgärden.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltigt eller saknat JWT-token.                      |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.     |
| 500 | Internal Server Error       | Oväntat serverfel.                                    |

## Cloud SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kontrollera GitHub-förrådet för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}