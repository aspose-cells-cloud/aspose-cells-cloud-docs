---
title: "Infoga en filterpanel i en Excel ListObject – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Infoga filterpanel"
type: docs
keywords: "Aspose.Cells, Excel-filterpanel, ListObject, REST API, molntjänst"
description: "Lär dig hur du lägger till en filterpanel i en Excel ListObject med Aspose.Cells Cloud REST API (v3.0). Inkludera endpoint, parametrar, autentisering, exempel på cURL-förfrågan och JSON-svar."
weight: 20
ArticleTitle: "Infoga en filterpanel i en Excel ListObject – Aspose.Cells Cloud API"
---

Denna REST API infogar en filterpanel för en listobjekt på ett Excel-arbetsblad.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### Förfrågningsparametrar

| Parameternamn   | Typ     | Plats  | Beskrivning                                                                 |
| --------------- | ------- | ------ | --------------------------------------------------------------------------- |
| name            | String  | Path   | Namnet på Excel-filen.                                                      |
| sheetName       | String  | Path   | Namnet på arbetsbladet som innehåller listobjektet.                         |
| listObjectIndex | Integer | Path   | Det nollbaserade indexet för det listobjekt som filterpanelen ska läggas till i. |
| columnIndex     | Integer | Query  | Det nollbaserade indexet för den kolumn som filterpanelen baseras på.       |
| destCellName    | String  | Query  | Cellreferensen (t.ex. **A1**) där filterpanelen ska placeras.               |
| folder          | String  | Query  | Mappen i lagringen som innehåller Excel-filen.                              |
| storageName     | String  | Query  | Namnet på Aspose Cloud-lagrings tjänsten.                                   |

Du kan använda kommandoradsverktyget cURL för att anropa API:t:

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Obs:** Förfrågan kräver en giltig JWT-bärartoken som erhållits från Aspose Cloud-autentiseringstjänsten. Denna endpoint kräver inte en förfrågningskropp; skicka ett tomt JSON-objekt `{}` om ditt klientbibliotek kräver en payload.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **Svarshuvud:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                    |
|-----|-----------------------------|----------------------------------------------------------------|
| 200 | OK                          | Filter har tillämpats korrekt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering nekad         | Ogiltig eller saknad JWT-token.                               |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.             |
| 500 | Internt serverfel           | Oväntat serverfel.                                             |

### Felhantering

När ett fel uppstår returnerar API:t ett JSON-objekt med ett fält `ErrorMessage` som beskriver problemet. Granska HTTP-statuskoden och `ErrorMessage` för att fastställa åtgärd.

## Molntjänstfamilj för SDK

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se GitHub-arkivet för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}