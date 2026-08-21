---
---
title: "Arbeiten mit Excel-Zeilen – Aspose.Cells Cloud API"
ArticleTitle: "Arbeiten mit Excel-Zeilen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /rows/
aliases: [/working-with-rows/]
keywords: "Aspose.Cells, Excel-Zeilen, REST API, Tabellenkalkulationsbearbeitung"
description: "Bearbeiten Sie Zeilen in Excel-Dateien mithilfe der Aspose.Cells Cloud REST API. Unterstützt Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift."
weight: 100
---

## Arbeiten mit Zeilen in einer Excel-Datei

**Zuletzt aktualisiert: Juli 2026**

- [So erhalten Sie Zeileninformationen in einem Excel-Arbeitsblatt.](/cells/rows/get/row/)
- [So fügen Sie eine leere Zeile in ein Excel-Arbeitsblatt ein.](/cells/rows/add/row/)
- [So kopieren Sie Zeilen in einem Excel-Arbeitsblatt.](/cells/rows/copy/)
- [So verbergen Sie Zeilen in einem Excel-Arbeitsblatt.](/cells/rows/hide/)
- [So zeigen Sie versteckte Zeilen in einem Excel-Arbeitsblatt wieder an.](/cells/rows/unhide/)
- [So gruppieren Sie Zeilen in einem Excel-Arbeitsblatt.](/cells/rows/group/)
- [So heben Sie die Gruppierung von Zeilen in einem Excel-Arbeitsblatt auf.](/cells/rows/ungroup/)
- [So löschen Sie eine Zeile aus einem Arbeitsblatt](/cells/rows/delete/)

Schnelle API-Referenz für häufige Zeilenoperationen:

| Operation        | HTTP-Methode | Endpunkt                                                               | Schlüsselparameter                           |
|------------------|--------------|------------------------------------------------------------------------|---------------------------------------------|
| [Zeile abrufen](https://docs.aspose.cloud/cells/rows/get/row/)     | GET          | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`        |
| [Zeile hinzufügen](https://docs.aspose.cloud/cells/rows/add/row/)     | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                        |
| [Zeilen kopieren](https://docs.aspose.cloud/cells/rows/copy/)      | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Zeile löschen](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE       | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`        |
| [Zeilen verbergen](https://docs.aspose.cloud/cells/rows/hide/)      | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`                   |
| [Zeilen anzeigen](https://docs.aspose.cloud/cells/rows/unhide/)  | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`                   |
| [Zeilen gruppieren](https://docs.aspose.cloud/cells/rows/group/)    | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`                   |
| [Gruppierung aufheben](https://docs.aspose.cloud/cells/rows/ungroup/)| POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`                   |

**Details zu Anfrage / Antwort**

- **Zeile abrufen**  
  *Anfrage*: Kein Body erforderlich.  
  *Antwort (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Fehler*: 400 Bad Request (ungültiger Index), 404 Not Found (Datei oder Arbeitsblatt fehlt).

- **Zeile hinzufügen**  
  *Anfragebody (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Antwort (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Fehler*: 400 Bad Request (fehlende/ungültige Parameter), 401 Unauthorized.

- **Zeilen kopieren**  
  *Anfragebody (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Antwort (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Fehler*: 400 Bad Request, 404 Not Found.

- **Zeile löschen**  
  *Anfrage*: Kein Body.  
  *Antwort (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Fehler*: 400 Bad Request, 404 Not Found.

- **Zeilen verbergen**  
  *Anfragebody (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Antwort (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Fehler*: 400 Bad Request.

- **Zeilen anzeigen** – gleicher Payload wie *Zeilen verbergen*; Antwort identisch, Status „Rows unhidden“.

- **Zeilen gruppieren** – gleicher Payload wie *Zeilen verbergen*; Antwortstatus „Rows grouped“.

- **Gruppierung aufheben** – gleicher Payload wie *Zeilen verbergen*; Antwortstatus „Rows ungrouped“.

Alle Operationen erfordern ein gültiges OAuth 2.0/JWT-Zugriffstoken und die entsprechende SDK-Version.  

---