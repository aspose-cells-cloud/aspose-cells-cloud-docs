---
title: "Importera bild till Excel-arket"
ArticleTitle: "Importera bild till Excel-ark – Aspose.Cells Cloud API-guide"
second_title: "Dokument"
linktitle: "Importera bild"
type: docs
url: /sv/import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "Importera bild, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "Lär dig hur du importerar bilder till Excel-ark med Aspose.Cells Cloud REST API v3.0. Inkluderar exempel på multipart-förfrågningar, SDK-kodexempel och råd om felhantering. Kom igång snabbt med tydliga steg."
weight: 19
---

Att importera en bild till ett Excel-ark gör det möjligt att berika kalkylark med visuellt innehåll såsom logotyper, diagram eller scheman. Denna guide visar hur du använder Aspose.Cells Clouds **ImportPicture**-åtgärd, det nödvändiga förfrågningsformatet och hur du hanterar svar.

**Förutsättningar:** Du måste ha ett giltigt JWT-autentiseringstoken och en redan existerande arbetsbok lagrad i Aspose Cloud-lagring innan du utför importåtgärden.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar**

Förfrågan är en HTTP **POST** med innehållstypen **multipart/related** (se [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- Den **första delen** innehåller ett JSON-objekt med namnet **ImportPictureOption** som beskriver var och hur bilden ska placeras.
- Den **andra delen** innehåller bildfilen (eller dess Base64-kodade data).

### ImportPictureOption – definition

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` är en **boolesk** parameter – `true` infogar en ny bild, `false` ersätter en befintlig._

### Viktiga parametrar

**ImportPictureOption**

| Parameternamn        | Typ         | Beskrivning                                                                                                                                                                                    |
| -------------------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UpperLeftRow         | int         | Radindex för övre vänstra hörnet där bilden ska placeras.                                                                                                                                      |
| UpperLeftColumn      | int         | Kolumnindex för övre vänstra hörnet där bilden ska placeras.                                                                                                                                   |
| LowerRightRow        | int         | Radindex för nedre högra hörnet som definierar bildens gränser.                                                                                                                                |
| LowerRightColumn     | int         | Kolumnindex för nedre högra hörnet som definierar bildens gränser.                                                                                                                             |
| Filename             | string      | Namn på bildfilen.                                                                                                                                                                             |
| Data                 | string      | Base64-kodad binärdata för bilden (valfritt om filen skickas som den andra delen).                                                                                                             |
| DestinationWorksheet | string      | Namn på arket där bilden ska infogas.                                                                                                                                                          |
| **IsInsert**         | **boolean** | `true` för att infoga en ny bild; `false` för att ersätta en befintlig.                                                                                                                        |
| ImportDataType       | string      | Typ av data som importeras (t.ex. `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource  | Anger var datafilen finns när parametern `BatchData` är null.                                                                                                                                  |

### Svar

En framgångsrik förfrågan returnerar **HTTP 200** med ett JSON-svar liknande detta:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Möjliga statuskoder:

| Kod | Betydelse                               |
| --- | --------------------------------------- |
| 200 | Importen lyckades                       |
| 400 | Felaktig förfrågan – saknad eller ogiltig data |
| 401 | Obehörig – ogiltig eller saknad token   |
| 500 | Internt serverfel                       |


## Hur du använder PostImportData API med SDK:er

### PostImportData API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er


Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---