---
title: "Uppdatera stil för pivotdiagram"
second_title: "Dokument"
linktitle: "Formatera alla"
type: docs
url: /pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: "pivotdiagram, uppdatera stil, Aspose.Cells Cloud, REST API, Excel, kalkylark, API, pivotdiagramstil, formatera alla"
description: "Lär dig hur du uppdaterar stilen för hela ett pivotdiagram med Aspose.Cells Cloud REST API. Inkluderar begärandedetaljer, ett cURL-exempel och SDK-utdrag för flera programmeringsspråk."
weight: 100
ArticleTitle: "Uppdatera stil för pivotdiagram - Aspose.Cells Cloud API"
---

Denna REST API uppdaterar stilen för ett pivotdiagram.

## PostPivotTableStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**Förutsättningar / Autentisering**  
En giltig JWT-åtkomsttoken måste anges i `Authorization`-headern (t.ex. `Bearer <jwt token>`). Se till att token har behörighet att komma åt det angivna arbetsboken och kalkylarket.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärandeparametrar**

| Parameter_name  | Typ     | Plats  | Beskrivning                                                                              |
| --------------- | ------- | ------ | ---------------------------------------------------------------------------------------- |
| name            | sträng  | path   | Namnet på arbetsbokens fil.                                                              |
| sheetName       | sträng  | path   | Kalkylarket som innehåller pivotdiagrammet.                                              |
| pivotTableIndex | heltal  | path   | Nollbaserat index för pivotdiagrammet som ska formateras.                                |
| style           | objekt  | body   | En stil-DTO som definierar formateringen som ska tillämpas.                              |
| needReCalculate | boolean | query  | Ställ in på **true** för att omberäkna pivotdiagrammet efter formatering; standard är **false**. |
| folder          | sträng  | query  | Mappen där arbetsboken lagras.                                                           |
| storageName     | sträng  | query  | Namnet på lagringstjänsten.                                                              |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör en anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Formatering lyckades; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla mot API:et. SDK:n abstraher bort detaljer på låg nivå så att du kan fokusera på din affärslogik. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar API:et med Go SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
---