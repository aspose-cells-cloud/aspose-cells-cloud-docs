---
title: "Verschieben eines benannten Bereichs mit einer Excel-Arbeitsmappe"
second_title: "Dokument"
linktitle: "Verschieben"
type: docs
url: /de/ranges/move/
aliases: [  /de/move-a-named-range-with-an-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, benannter Bereich verschieben, Excel-Arbeitsmappe, REST-API, Bereich verschieben, SDK-Beispiele"
description: "Erfahren Sie, wie Sie einen benannten Bereich innerhalb einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API v3.0 verschieben – inklusive Endpunkt-Details, Authentifizierung, Beispielen und SDK-Codebeispielen."
weight: 20
ArticleTitle: "Verschieben eines benannten Bereichs mit einer Excel-Arbeitsmappe über die Aspose.Cells Cloud API"
---

Das Verschieben eines benannten Bereichs ist eine häufige Aufgabe, wenn Sie Daten programmgesteuert neu organisieren müssen. Dieser Abschnitt erläutert, wie Sie einen definierten Bereich auf derselben Arbeitsmappe an eine neue Position verschieben, mithilfe der Aspose.Cells Cloud REST API.

Diese REST-API verschiebt einen angegebenen Bereich an eine Zielposition innerhalb einer Excel-Arbeitsmappe.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Authentifizierung
Die API erfordert ein **Bearer JWT-Token**, das über den OAuth-Flow von Aspose Cloud abgerufen wird. Fügen Sie das Token in den `Authorization`-Header ein:

```
Authorization: Bearer <jwt token>
```

Das Token muss den Scope **Cells** besitzen.

### Voraussetzungen
- Die Arbeitsmappe muss im Aspose Cloud-Speicher gespeichert sein.  
- Geben Sie den Speichernamen (`storageName`) und den Ordnerpfad (`folder`) an, wenn sich die Datei nicht im Root-Verzeichnis befindet.  
- Verwenden Sie die neueste Version des Aspose.Cells Cloud SDK, die API-Version **v3.0** unterstützt.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter

| Name           | Typ    | Position | Beschreibung |
|----------------|--------|----------|-------------|
| **name**       | string | path     | Name der Arbeitsmappe |
| **sheetName**  | string | path     | Name des Arbeitsblatts |
| **destRow**    | integer| query    | Startzeilenindex des Zielbereichs (0-basiert) |
| **destColumn**| integer| query    | Startspaltenindex des Zielbereichs (0-basiert) |
| **range**      | object | body     | Definition des zu verschiebenden Quellbereichs |
| **folder**     | string | query    | Ordnerpfad, in dem die Arbeitsmappe gespeichert ist |
| **storageName**| string | query    | Name des Aspose Cloud-Speichers |

### Anforderungstext

| Feld           | Typ    | Erforderlich | Beschreibung |
|----------------|--------|--------------|-------------|
| **ColumnCount**| integer| Nein | Anzahl der Spalten im Quellbereich |
| **ColumnWidth**| integer| Nein | Breite jeder Spalte (in Punkten) |
| **FirstColumn**| integer| Nein | Nullbasierter Index der ersten Spalte des Quellbereichs |
| **FirstRow**   | integer| Nein | Nullbasierter Index der ersten Zeile des Quellbereichs |
| **Name**       | string | Nein | Name des Bereichs (falls es sich um einen benannten Bereich handelt) |
| **RefersTo**   | string | Nein | A1-Referenzstil, der den Bereich definiert |
| **RowCount**   | integer| Nein | Anzahl der Zeilen im Quellbereich |
| **RowHeight**  | integer| Nein | Höhe jeder Zeile (in Punkten) |
| **Worksheet**  | string | Nein | Arbeitsblatt, das den Quellbereich enthält |

### Arbeitsablauf

1. **Hochladen** der Arbeitsmappe in den Aspose Cloud-Speicher (sofern noch nicht vorhanden).  
2. **Erstellen** eines JWT-Tokens über den OAuth-Endpunkt.  
3. **Erstellen** des JSON-Payloads, der den Quellbereich beschreibt.  
4. **Aufrufen** des `moveto`-Endpunkts mit den erforderlichen Pfad- und Abfrageparametern sowie dem JSON-Body.  
5. **Überprüfen** der Antwort; bei erfolgreicher Ausführung wird ein Statuscode `200 OK` zurückgegeben.

### Beispielanfrage / -antwort

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
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

Im Fehlerfall enthält die Antwort ein optionales Feld `ErrorMessage`, das zusätzliche Details zum Fehler liefert.

**HTTP-Statuscodes**

| Code | Bedeutung                  | Beschreibung |
|------|----------------------------|--------------------------------------------------|
| 200  | OK                         | Filter erfolgreich angewendet; Antwort enthält Details zur Operation. |
| 400  | Bad Request                | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized               | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large          | Die hochgeladene Datei überschreitet die Größe. |
| 500  | Internal Server Error      | Unerwarteter Serverfehler. |

**Antwortschema**

| Feld | Typ | Beschreibung |
|------|-----|-------------|
| **Code** | integer | HTTP-ähnlicher Statuscode, der von der API zurückgegeben wird (z. B. 200) |
| **Status** | string | Textuelle Beschreibung des Ergebnisses (z. B. "OK") |
| **ErrorMessage** | string (optional) | Menschlich lesbare Fehlerdetails im Fehlerfall |

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektziele konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}