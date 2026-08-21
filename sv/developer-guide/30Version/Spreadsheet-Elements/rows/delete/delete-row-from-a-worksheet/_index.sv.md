---
title: "Ta bort en rad i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Rad"
type: docs
url: /sv/rows/delete/row/
aliases: [  /sv/delete-row-from-a-worksheet/ ]
description: "Använd slutpunkten DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} för att ta bort en specifik rad från ett Excel-arbetsblad via Aspose.Cells Cloud REST API. Innehåller cURL-kommando, SDK-exempel och fullständig parameterreferens."
keywords: "Aspose.Cells, ta bort rad, Excel, API, REST, moln, SDK"
weight: 80
ArticleTitle: "Ta bort en rad i ett Excel-arbetsblad – Aspose.Cells Cloud API-guide"
---

Denna REST API tar bort en rad från ett Excel-arbetsblad.

**Förutsättningar**  
- En giltig JWT-**auktoriserings**token.  
- Arbetshandboken måste lagras i ett stödt Aspose-molnlagringsutrymme (standard eller anpassat).  
- Målmappen (om angiven) måste finnas i det valda lagringsutrymmet.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Förfrågningsparametrar**

| Parameter namn      | Typ     | Sökväg / fråga | Obligatorisk | Beskrivning                                                                                          |
| ------------------- | ------- | -------------- | ------------ | ---------------------------------------------------------------------------------------------------- |
| **name**            | sträng  | sökväg         | Ja           | Namnet på arbetshandboken.                                                                           |
| **sheetName**       | sträng  | sökväg         | Ja           | Namnet på arbetsbladet.                                                                              |
| **rowIndex**        | heltal  | sökväg         | Ja           | Nollbaserat index för den rad som ska tas bort.                                                      |
| **startrow**        | heltal  | fråga          | Nej          | Index för den första raden som ska tas bort (normalt samma som `rowIndex`).                          |
| **totalRows**       | heltal  | fråga          | Nej          | Antal på varandra följande rader som ska tas bort.                                                   |
| **updateReference** | boolean | fråga          | Nej          | När `true` (standard) uppdateras formler, namngivna intervall och andra referenser efter borttagandet. |
| **folder**          | sträng  | fråga          | Nej          | Mapp som innehåller arbetshandboken.                                                                 |
| **storageName**     | sträng  | fråga          | Nej          | Namn på lagringstjänsten.                                                                            |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) definierar ett offentligt tillgängligt programmeringssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar ett komplett, körbart anrop.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

**Möjliga HTTP-svarskoder**

| Kod | Betydelse                            | Beskrivning                                                               |
|-----|--------------------------------------|---------------------------------------------------------------------------|
| 200 | OK                                   | Raden togs framgångsrikt bort.                                            |
| 400 | Felaktig förfrågan                   | Saknade eller ogiltiga parametrar (t.ex. icke-numeriskt `rowIndex`).     |
| 401 | Auktorisering nekades                | Ogiltig eller saknad JWT-token.                                           |
| 404 | Hittades inte                        | Angiven arbetshandbok, arbetsblad eller rad finns inte.                  |
| 500 | Internt serverfel                    | Oväntat serverfel; se svarsmeddelandet för detaljer.                      |

**Exempel på felmeddelande**

```json
{
  "Code": 400,
  "Message": "Ogiltigt radindex angavs."
}
```

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
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

**Relaterade åtgärder**  
- [Lägg till en rad](/sv/cells/rows/add/row/)  
- [Ta bort flera rader](/sv/cells/rows/delete/rows/)  
- [Hämta radinformation](/sv/cells/rows/get/row/)  
---