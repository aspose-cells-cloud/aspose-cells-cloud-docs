---
title: "Aspose.Cells Cloud API – Arbeiten mit der CellsObjectOperate-Aufgabe (REST)"
second_title: "Dokument"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Erfahren Sie, wie Sie die CellsObjectOperate-Aufgabe in der Aspose.Cells Cloud API nutzen können – inklusive Parameterreferenz, Anforderungs-/Antwortbeispielen und bewährten Tipps für Arbeitsblätter, Diagramme und Pivot-Tabellen."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – Arbeiten mit der CellsObjectOperate-Aufgabe (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "CellsObjectOperate-Aufgabe"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "Diagrammvorgang"
  - "Pivot-Tabellen-API"
  - "Seitenumbruch-API"
---

**Übersicht**  
Die **CellsObjectOperate**-Aufgabe ermöglicht das Ausführen von Erstellen, Lesen, Aktualisieren und Löschen (CRUD) von Excel-Objekten wie Arbeitsmappen, Arbeitsblättern, Diagrammen, Pivot-Tabellen, Formen, Seitenumbrüchen und weiteren über einen einzigen REST-Aufruf. Geben Sie den Objekttyp mit `OperateObjectType` an und stellen Sie den zugehörigen Parameterblock bereit (z. B. `ChartOperateParameter` für diagrammspezifische Aktionen).

---

**OperateObject**

| Parametername             | Typ    | Beschreibung |
| ------------------------- | ------ | ------------ |
| OperateObjectType         | string | Der Typ des zu bearbeitenden Excel-Objekts. Zulässige Werte: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition     | object | Container, der den Speicherort des Zielobjekts identifiziert (z. B. Name der Arbeitsmappe, Name des Arbeitsblatts, Diagrammindex). Erforderlich für die meisten Vorgänge. |

**OperateObjectPosition**

| Parametername     | Typ    | Beschreibung |
| ----------------- | ------ | ------------ |
| Workbook          | object | Die Arbeitsmappe, die das Zielobjekt enthält. Muss entweder `FileName` (Cloud-Speicher) oder `FileContent` (Base64-kodiert) enthalten. |
| SheetName         | string | Name des Arbeitsblatts, auf dem der Vorgang ausgeführt wird. Erforderlich für objektebene Arbeitsblattobjekte (Diagramme, Formen usw.). |
| ChartIndex        | integer| Nullbasierter Index des Diagramms innerhalb des Arbeitsblatts (wird verwendet, wenn `OperateObjectType` = `Chart` ist). |
| ShapeIndex        | integer| Nullbasierter Index der Form innerhalb des Arbeitsblatts (wird verwendet, wenn `OperateObjectType` = `Shape` ist). |
| CellName          | string | Zellreferenz im A1-Stil (z. B. `A1`). Wird für zellbasierte Vorgänge verwendet. |
| ListObjectIndex   | integer| Nullbasierter Index des Listenobjekts (wird verwendet, wenn `OperateObjectType` = `ListObject` ist). |

**ChartOperateParameter**

| Parametername         | Typ    | Beschreibung |
| --------------------- | ------ | ------------ |
| ChartIndex            | integer| Index des zu ändernden Diagramms. Erforderlich bei Aktualisierung eines bestehenden Diagramms. |
| ChartType             | string | Typ des zu erstellenden Diagramms (z. B. `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | integer| Zeilennummer der oberen linken Ecke des Diagramms (nullbasiert). |
| UpperLeftColumn       | integer| Spaltennummer der oberen linken Ecke des Diagramms (nullbasiert). |
| LowerRightRow         | integer| Zeilennummer der unteren rechten Ecke des Diagramms. |
| LowerRightColumn      | integer| Spaltennummer der unteren rechten Ecke des Diagramms. |
| Area                  | string | Datenbereich für das Diagramm (z. B. `A1:B5`). |
| IsVertical            | string | `true`, wenn die Diagrammausrichtung vertikal ist; andernfalls `false`. |
| CategoryData          | string | Bereich, der die Kategorie- (X-Achsen-)Beschriftungen bereitstellt. |
| IsAutoGetSerialName   | string | `true`, um Seriennamen automatisch zu generieren; `false`, um benutzerdefinierte Namen zu verwenden. |
| Title                 | string | Titeltext, der im Diagramm angezeigt wird. |

**ListObjectOperateParameter**

| Parametername | Typ    | Beschreibung |
| ------------- | ------ | ------------ |
| ListObject    | object | Konfigurationsobjekt für eine Listen-(Tabellen-)Operation. Enthält Eigenschaften wie `ShowHeader`, `ShowTotal` und `Style`. |

**PageBreakOperateParameter**

| Parametername | Typ    | Beschreibung |
| ------------- | ------ | ------------ |
| PageBreakType | string | Typ des Seitenumbruchs (`Horizontal` oder `Vertical`). |
| Index         | integer| Nullbasierter Index des zu löschenden oder zu ändernden Seitenumbruchs. |
| Row           | integer| Zeilennummer, an der ein horizontaler Seitenumbruch platziert wird. |
| Column        | integer| Spaltennummer, an der ein vertikaler Seitenumbruch platziert wird. |
| StartIndex    | integer| Startindex für eine bereichsbasierte Seitenumbruchoperation. |
| EndIndex      | integer| Endindex für eine bereichsbasierte Seitenumbruchoperation. |

**PageSetupOperateParameter**

| Parametername | Typ    | Beschreibung |
| ------------- | ------ | ------------ |
| PageSetup     | object | Einstellungen für das Seitenlayout (Ränder, Ausrichtung, Papierformat usw.). |

**PivotTableOperateParameter**

| Parametername      | Typ         | Beschreibung |
| ------------------ | ----------- | ------------ |
| DestCellName       | string      | Obere linke Zelle des Zielbereichs für die Pivot-Tabelle (z. B. `C5`). |
| SourceData         | string      | Quellbereich für die Pivot-Tabelle (z. B. `A1:D100`). |
| TableName          | string      | Name, der der erstellten Pivot-Tabelle zugewiesen wird. |
| UseSameSource      | string      | `true`, um einen vorhandenen Quellbereich wiederzuverwenden; `false`, um einen neuen zu erstellen. |
| PivotTableIndex    | integer     | Index der zu aktualisierenden Pivot-Tabelle (erforderlich für Änderungs-/Löschaktionen). |
| PivotFieldRows     | integer[]   | Sammlung von Feldindizes, die im Zeilenbereich angezeigt werden sollen. |
| PivotFieldColumns  | integer[]   | Sammlung von Feldindizes, die im Spaltenbereich angezeigt werden sollen. |
| PivotFieldData     | integer[]   | Sammlung von Feldindizes, die im Datenbereich angezeigt werden sollen. |

**ShapeOperateParameter**

| Parametername | Typ    | Beschreibung |
| ------------- | ------ | ------------ |
| Shape         | object | Definition der Form (Typ, Position, Größe, Text usw.). |

**WorkbookSettingsOperateParameter**

| Parametername      | Typ    | Beschreibung |
| ------------------ | ------ | ------------ |
| WorkbookSettings   | object | Einstellungen, die die gesamte Arbeitsmappe betreffen (z. B. Berechnungsmodus, Genauigkeit). |

**WorksheetOperateParameter**

| Parametername  | Typ    | Beschreibung |
| -------------- | ------ | ------------ |
| Name           | string | Aktueller Name des zu bearbeitenden Arbeitsblatts. |
| SheetType      | string | Typ des Arbeitsblatts (`Worksheet`, `Chart` usw.). |
| NewName        | string | Neuer Name des Arbeitsblatts bei einer Umbenennung. |
| MovingRequest  | object | Parameter zum Verschieben eines Arbeitsblatts (z. B. `FromIndex`, `ToIndex`). |

## REST API

| API                       | Typ  | Beschreibung     | Ressourcenlink |
| ------------------------- | ---- | ---------------- | -------------- |
| /cells/task/runtask       | POST | Aufgabe ausführen | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

### Voraussetzungen
- **Authentifizierung** – Fügen Sie einen gültigen Header `Authorization: Bearer <access_token>` hinzu.  
- **Speicher** – Die Quellarbeitsmappe muss im Aspose Cloud Storage gespeichert sein oder als base64-kodierter Inhalt im Anforderungstext übermittelt werden.  
- **API-Version** – Diese Dokumentation zielt auf **v3.0** der Aspose.Cells Cloud API ab.

### Beispielanforderung (cURL)

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

Der Anforderungstext folgt dem unten definierten Schema **CellsObjectOperateRequest**:

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
    /* Weitere Definitionen zur Kürze ausgelassen */
  }
}
```

### Beispielantwort (Erfolg – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Chart created successfully."
  }
}
```

Die Antwort enthält die folgenden Felder:

| Feld     | Typ    | Beschreibung |
| -------- | ------ | ------------ |
| Code     | integer| HTTP-ähnlicher Statuscode, der von der Task-Engine zurückgegeben wird. |
| Status   | string | Menschenlesbarer Status (z. B. `OK`). |
| TaskId   | string | Bezeichner der asynchronen Aufgabe. |
| Result   | object | Objekt mit aufgabenspezifischen Ergebnissen. |
| Result.ChartId | integer | Bezeichner des erstellten oder geänderten Diagramms. |
| Result.Message | string | Kurze Nachricht zur Beschreibung des Ergebnisses. |

### Fehlerbehandlung

| HTTP-Status | Fehlercode        | Beschreibung | Empfohlene Lösung |
| ----------- | ----------------- | ------------ | ----------------- |
| 400         | InvalidParameter  | Ein oder mehrere Anforderungsparameter fehlen oder sind ungültig formatiert. | Überprüfen Sie erforderliche Felder und Datentypen. |
| 401         | Unauthorized      | Ungültiger oder fehlender Authentifizierungstoken. | Aktualisieren Sie den Zugriffstoken und fügen Sie ihn in den `Authorization`-Header ein. |
| 404         | NotFound          | Angegebene Arbeitsmappe, Arbeitsblatt oder Objekt existiert nicht. | Überprüfen Sie `FileName`, `SheetName` und Objektindizes. |
| 500         | ServerError       | Ein unerwarteter Fehler ist auf dem Server aufgetreten. | Wiederholen Sie die Anforderung; falls das Problem bestehen bleibt, wenden Sie sich an den Support. |

### Häufige Anwendungsfälle
- **Hinzufügen eines neuen Diagramms** zu einem Arbeitsblatt.  
- **Umbenennen eines Arbeitsblatts** (`OperateObjectType = "Worksheet"` mit `WorksheetOperateParameter.NewName`).  
- **Einfügen eines Seitenumbruchs** (`OperateObjectType = "PageBreak"` mit `PageBreakOperateParameter`).  
- **Aktualisieren der Quelldaten einer Pivot-Tabelle** (`OperateObjectType = "PivotTable"` mit `PivotTableOperateParameter.SourceData`).  
- **Ändern von Arbeitsmappeneinstellungen** wie dem Berechnungsmodus (`OperateObjectType = "WorkbookSettings"`).  

---  

*Alle Beschreibungen basieren auf der offiziellen Aspose.Cells Cloud OpenAPI-Spezifikation.*