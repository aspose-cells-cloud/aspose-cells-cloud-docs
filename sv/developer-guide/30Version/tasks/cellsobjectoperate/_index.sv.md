---
title: "Aspose.Cells Cloud API – Arbeta med CellsObjectOperate-uppgift (REST)"
second_title: "Dokument"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Lär dig hur du använder CellsObjectOperate-uppgiften i Aspose.Cells Cloud API med referens till parametrar, exempel på begäran/svar och bästa praxis för kalkylblad, diagram och pivot-tabeller."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – Arbeta med CellsObjectOperate-uppgift (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "CellsObjectOperate-uppgift"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "diagramåtgärd"
  - "pivot-tabell-API"
  - "sidbrytnings-API"
---

**Översikt**  
**CellsObjectOperate**-uppgiften låter dig utföra skapa, läsa, uppdatera och ta bort (CRUD)-åtgärder på Excel-objekt såsom arbetsböcker, kalkylblad, diagram, pivot-tabeller, former, sidbrytningar och mer via ett enda REST-anrop. Ange objekttypen med `OperateObjectType` och tillhandahåll motsvarande parameterblock (t.ex. `ChartOperateParameter` för diagramrelaterade åtgärder).

---

**OperateObject**

| Parameter Name          | Typ    | Beskrivning |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | Typen av Excel-objekt att arbeta med. Tillåtna värden: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition   | objekt | Behållare som identifierar målobjektets plats (t.ex. arbetsbokens namn, kalkylbladsnamn, diagramindex). Krävs för de flesta åtgärder. |

**OperateObjectPosition**

| Parameter Name | Typ    | Beskrivning |
| -------------- | ------ | ----------- |
| Workbook       | objekt | Arbetsboken som innehåller målobjektet. Måste innehålla antingen `FileName` (molnlagring) eller `FileContent` (base‑64‑kodad data). |
| SheetName      | string | Namn på kalkylbladet där åtgärden ska utföras. Krävs för objekt på kalkylbladsnivå (diagram, former etc.). |
| ChartIndex     | heltal | Nollbaserat index för diagrammet inom kalkylbladet (används när `OperateObjectType` är `Chart`). |
| ShapeIndex     | heltal | Nollbaserat index för formen inom kalkylbladet (används när `OperateObjectType` är `Shape`). |
| CellName       | string | A1‑stilad cellreferens (t.ex. `A1`). Används för cellnivååtgärder. |
| ListObjectIndex| heltal | Nollbaserat index för listobjektet (används när `OperateObjectType` är `ListObject`). |

**ChartOperateParameter**

| Parameter Name        | Typ     | Beskrivning |
| --------------------- | ------- | ----------- |
| ChartIndex            | heltal  | Index för diagrammet som ska ändras. Krävs vid uppdatering av ett befintligt diagram. |
| ChartType             | string  | Typ av diagram att skapa (t.ex. `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | heltal  | Radnummer för diagrammets övre vänstra hörn (nollbaserat). |
| UpperLeftColumn       | heltal  | Kolumnnummer för diagrammets övre vänstra hörn (nollbaserat). |
| LowerRightRow         | heltal  | Radnummer för diagrammets nedre högra hörn. |
| LowerRightColumn      | heltal  | Kolumnnummer för diagrammets nedre högra hörn. |
| Area                  | string  | Datointervall för diagrammet (t.ex. `A1:B5`). |
| IsVertical            | string  | `true` om diagrammets orientering är vertikal; annars `false`. |
| CategoryData          | string  | Intervall som tillhandahåller kategorier (x-axel) etiketter. |
| IsAutoGetSerialName   | string  | `true` för att automatiskt generera serienamn; `false` för att använda anpassade namn. |
| Title                 | string  | Titeltext som visas på diagrammet. |

**ListObjectOperateParameter**

| Parameter Name | Typ    | Beskrivning |
| -------------- | ------ | ----------- |
| ListObject     | objekt | Konfigurationsobjekt för en list‑/tabellåtgärd. Inkluderar egenskaper såsom `ShowHeader`, `ShowTotal` och `Style`. |

**PageBreakOperateParameter**

| Parameter Name | Typ     | Beskrivning |
| -------------- | ------- | ----------- |
| PageBreakType  | string  | Typ av sidbrytning (`Horizontal` eller `Vertical`). |
| Index          | heltal  | Nollbaserat index för den sidbrytning som ska tas bort eller ändras. |
| Row            | heltal  | Radnummer där en horisontell sidbrytning placeras. |
| Column         | heltal  | Kolumnnummer där en vertikal sidbrytning placeras. |
| StartIndex     | heltal  | Startindex för en intervallbaserad sidbrytningsåtgärd. |
| EndIndex       | heltal  | Slutindex för en intervallbaserad sidbrytningsåtgärd. |

**PageSetupOperateParameter**

| Parameter Name | Typ    | Beskrivning |
| -------------- | ------ | ----------- |
| PageSetup      | objekt | Inställningar för sidlayout (marginaler, orientering, pappersstorlek etc.). |

**PivotTableOperateParameter**

| Parameter Name   | Typ         | Beskrivning |
| ---------------- | ----------- | ----------- |
| DestCellName     | string      | Övre vänstra cellen i målintervallet för pivot-tabellen (t.ex. `C5`). |
| SourceData       | string      | Källintervall för pivot-tabellen (t.ex. `A1:D100`). |
| TableName        | string      | Namn som tilldelas den skapade pivot-tabellen. |
| UseSameSource    | string      | `true` för att återanvända ett befintligt källintervall; `false` för att skapa ett nytt. |
| PivotTableIndex  | heltal      | Index för pivot-tabellen som ska uppdateras (krävs för ändra/tar bort-åtgärder). |
| PivotFieldRows   | heltal[]    | Samling av fältindex som ska visas i radområdet. |
| PivotFieldColumns| heltal[]    | Samling av fältindex som ska visas i kolumnområdet. |
| PivotFieldData   | heltal[]    | Samling av fältindex som ska visas i dataområdet. |

**ShapeOperateParameter**

| Parameter Name | Typ    | Beskrivning |
| -------------- | ------ | ----------- |
| Shape          | objekt | Definition av formen (typ, position, storlek, text etc.). |

**WorkbookSettingsOperateParameter**

| Parameter Name   | Typ    | Beskrivning |
| ---------------- | ------ | ----------- |
| WorkbookSettings | objekt | Inställningar som påverkar hela arbetsboken (t.ex. beräkningsläge, precision). |

**WorksheetOperateParameter**

| Parameter Name | Typ    | Beskrivning |
| -------------- | ------ | ----------- |
| Name           | string | Nuvarande namn på det kalkylblad som ska bearbetas. |
| SheetType      | string | Typ av kalkylblad (`Worksheet`, `Chart` etc.). |
| NewName        | string | Nytt namn för kalkylbladet vid namnändring. |
| MovingRequest  | objekt | Parametrar för att flytta ett kalkylblad (t.ex. `FromIndex`, `ToIndex`). |

## REST API

| API                | Typ  | Beskrivning | Resurslänk |
| ------------------ | ---- | ----------- | ---------- |
| /cells/task/runtask| POST | Kör uppgift  | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definierar ett offentligt tillgängligt programmeringssnitt som låter dig utföra REST-interaktioner direkt från en webbläsare.

### Förutsättningar
- **Autentisering** – Inkludera ett giltigt `Authorization: Bearer <access_token>`-huvud.  
- **Lagring** – Källarbetsboken måste lagras i Aspose Cloud Storage eller levereras som base‑64‑kodat innehåll i begärandetexten.  
- **API-version** – Denna dokumentation riktar sig till **v3.0** av Aspose.Cells Cloud API.

### Exempel på begäran (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

Begärandetexten följer **CellsObjectOperateRequest**-schemat som definieras nedan:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* Ytterligare definitioner utelämnade för kortare text */
  }
}
```

### Exempel på svar (lyckad begäran – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Diagram skapat framgångsrikt."
  }
}
```

Svaret innehåller följande fält:

| Fält   | Typ    | Beskrivning |
| ------ | ------ | ----------- |
| Code   | heltal | HTTP-liknande statuskod som returneras av uppgiftsmotorn. |
| Status | string | Läsbar status (t.ex. `OK`). |
| TaskId | string | Identifierare för den asynkrona uppgiften. |
| Result | objekt | Objekt som innehåller åtgärdspecifika resultat. |
| Result.ChartId | heltal | Identifierare för det skapade eller ändrade diagrammet. |
| Result.Message | string | Kort meddelande som beskriver resultatet. |

### Felhantering

| HTTP-status | Felkod | Beskrivning | Rekommenderad åtgärd |
| ----------- | ------ | ----------- | ------------------- |
| 400         | InvalidParameter | En eller flera begärandeparametrar saknas eller är felaktigt formaterade. | Verifiera obligatoriska fält och datatyper. |
| 401         | Unauthorized | Ogiltig eller saknad autentiseringstoken. | Uppdatera åtkomsttoken och inkludera den i `Authorization`-huvudet. |
| 404         | NotFound | Angiven arbetsbok, kalkylblad eller objekt finns inte. | Kontrollera `FileName`, `SheetName` och objektindex. |
| 500         | ServerError | Ett oväntat fel inträffade på servern. | Försök igen; om problemet kvarstår, kontakta support. |

### Vanliga användningsfall
- **Lägg till ett nytt diagram** till ett kalkylblad.  
- **Byt namn på ett kalkylblad** (`OperateObjectType = "Worksheet"` med `WorksheetOperateParameter.NewName`).  
- **Infoga en sidbrytning** (`OperateObjectType = "PageBreak"` med `PageBreakOperateParameter`).  
- **Uppdatera källdata för pivot-tabell** (`OperateObjectType = "PivotTable"` med `PivotTableOperateParameter.SourceData`).  
- **Ändra arbetsboksuppdrag** såsom beräkningsläge (`OperateObjectType = "WorkbookSettings"`).  

---  

*Alla beskrivningar är hämtade från den officiella Aspose.Cells Cloud OpenAPI-specifikationen.*  
---