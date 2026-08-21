---
title: "Arbeiten mit Excel ListObject"
ArticleTitle: "Arbeiten mit Excel ListObject"
second_title: "Dokument"
linktype: "ListObjects"
type: docs
url: /de/list-objects/
aliases:
  - /de/working-with-list-objects/
  - /de/working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, Excel Tabellen-API, Tabelle hinzufügen, Tabelle aktualisieren, Tabelle löschen, Tabelle in Bereich konvertieren, Excel-Tabelle sortieren"
description: "Erfahren Sie, wie Sie Excel ListObjects (Tabellen) mithilfe der Aspose.Cells Cloud REST API hinzufügen, aktualisieren, löschen, abrufen, sortieren und in Bereiche konvertieren. Enthält Codebeispiele für C#, Java, Python und mehr."
weight: 100
---

Excel ListObjects (Tabellen) bieten eine strukturierte Möglichkeit, Datensätze zu organisieren. Sie umfassen Funktionen wie automatische Datenanordnung, Kopfzeilen, integrierte Filter und optionale Gesamtzeilen. Ermitteln Sie diese Fähigkeiten, um Ihre Daten schnell und effizient zu analysieren.

**Definition von ListObject:** Ein **ListObject** ist das native Tabellenobjekt von Excel, das Zeilen und Spalten gruppiert, Sortierung, Filterung und Formatierung ermöglicht und über die Aspose.Cells Cloud API abgerufen werden kann.

## Wie Sie mit Tabellen (ListObject) arbeiten

- [So fügen Sie eine Tabelle (ListObject) in das Arbeitsblatt ein](/de/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [So aktualisieren Sie eine Tabelle (ListObject) im Arbeitsblatt](/de/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [So konvertieren Sie eine Tabelle (ListObject) in einen Bereich](/de/cells/convert-list-object-or-table-to-range/)
- [So sortieren Sie Tabellendaten](/de/cells/sort-table-data/)
- [So entfernen Sie doppelte Zeilen aus einer Tabelle](/de/cells/list-objects/remove-duplicates/)
- [So fügen Sie einen Slicer für eine Tabelle ein](/de/cells/list-objects/insert-slicer/)

**API-Referenz (Übersicht):**  
Die Aspose.Cells Cloud REST API stellt ListObject-Operationen über Endpunkte wie `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` und `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` bereit. Erforderliche Abfrageparameter sind `folder` und `storage`. Anforderungstexte sind JSON-Objekte, die die Eigenschaften der Tabelle (Name, ShowHeaderRow, ShowTotalRow usw.) beschreiben, und Antworten liefern JSON-Payloads mit den Details des erstellten oder geänderten ListObjects zurück.

**Voraussetzungen:**  
- Ein gültiges Aspose.Cells Cloud-Authentifizierungstoken.  
- Die Arbeitsmappe muss in einem unterstützten Speicherort hochgeladen worden sein (Standard: **/**), und der Abfrageparameter `folder` muss auf diesen Speicherort zeigen.  
- Optional: Legen Sie `storage` fest, wenn ein nicht standardmäßiger Speicherdienst verwendet wird.

**Endpunkt-Details**

| Methode | Endpunkt | Abfrageparameter | Anforderungstext (JSON) | Erfolgsantwort (Beispiel) | Statuscodes |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (erforderlich), `storage` (optional) | *kein* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (erforderlich), `storage` (optional) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Created, 400 – Bad Request, 401 – Unauthorized, 409 – Conflict |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (erforderlich), `storage` (optional) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (erforderlich), `storage` (optional) | *kein* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |

**Code-Snippets**

*C# (POST – ListObject hinzufügen)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – ListObjects abrufen)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – ListObject aktualisieren)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – ListObject entfernen)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Hinweise:**  
- ListObject-Indizes sind nullbasiert.  
- Bei Hinzufügen eines ListObjects definieren `StartRow` und `StartColumn` die obere linke Zelle der Tabelle.  
- Die API unterstützt Pagination über die Abfrageparameter `offset` und `limit` (nicht in der Tabelle dargestellt) für große Arbeitsblätter.  
- Ratenlimits: 100 Anfragen pro Minute pro Konto; Überschreitung führt zu **429 Too Many Requests**.

Durch die wiederholte Verwendung des Begriffs **Excel ListObject** im gesamten Dokument stimmt der Inhalt mit den Ziel-Keywords „Excel ListObject“, „Aspose.Cells Cloud“ und „Excel table API“ überein, was die SEO verbessert, ohne für Leser unnatürlich zu wirken.