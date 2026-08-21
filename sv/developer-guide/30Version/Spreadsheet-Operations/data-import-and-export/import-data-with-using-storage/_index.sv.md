---
title: "Importera data med hjälp av lagring"
second_title: "Dokument"
linktype: "dokumentation"
type: docs
url: /sv/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Importera data med hjälp av lagring: Importera data till ett Excel-arbetsblad med Aspose.Cells Cloud API från olika lagringskällor. Stöder JSON, CSV och andra format via HTTPS."
keywords: "Aspose.Cells Cloud, Excel, importera data, REST API, molnlagring, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Importera data med hjälp av lagring – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API importerar data till en Excel-fil.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärans parametrar är

| Parameternamn   | Typ    | Plats  | Beskrivning                                               |
| --------------- | ------ | ------ | --------------------------------------------------------- |
| name            | string | path   | Namnet på Excel-filen.                                    |
| folder          | string | query  | Mappens sökväg i lagringen där filen finns.              |
| storageName     | string | query  | Namnet på lagringstjänsten.                               |
| importData      | object | body   | JSON-objekt som innehåller de data som ska importeras.   |

**Parametrarna för importdataalternativen** beskrivs i [referenslänken](/cells/import/#import-data-option-parameter).

**Förutsättningar:** Du måste ange en giltig JWT-token i `Authorization`-headern och säkerställa att målarbetsboken redan finns på den angivna lagringsplatsen.

### Respons

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod  | Betydelse                    | Beskrivning                                                   |
|------|------------------------------|---------------------------------------------------------------|
| 200  | OK                           | Filtrering lyckades; responsen innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran             | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Inte auktoriserad            | Ogiltig eller saknad JWT-token.                               |
| 413  | För stor nyttolast           | Den uppladdade filen överskrider storleksgränsen.             |
| 500  | Internt serverfel            | Oväntat serverfel.                                            |

## Hur du använder PostImportData API med SDK:er

### PostImportData API-specifikation

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänsten med PHP SDK:
---