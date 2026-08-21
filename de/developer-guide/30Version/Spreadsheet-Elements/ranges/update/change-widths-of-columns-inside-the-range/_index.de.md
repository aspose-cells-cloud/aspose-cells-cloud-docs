---
title: "Spaltenbreiten innerhalb eines Bereichs ändern"
ArticleTitle: "Spaltenbreiten innerhalb eines Bereichs ändern – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Spaltenbreite"
type: docs
url: /de/ranges/update/column-width/
aliases: [  /de/change-widths-of-columns-inside-the-range/ ]
keywords: "Aspose.Cells, Spaltenbreite, REST API, Excel, SDK, Bereich, Cloud"
description: "Erfahren Sie, wie Sie Spaltenbreiten innerhalb eines Bereichs mithilfe der Aspose.Cells Cloud REST API oder SDKs (C#, Java, Python usw.) ändern. Enthält cURL-Beispiele, Anforderungs-/Antwortdetails und Authentifizierungsschritte."
weight: 74
---

Dieser REST-Dienst legt die Spaltenbreite eines Bereichs fest.

## Sicherheit und Authentifizierung  
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Voraussetzungen** – Vor dem Aufruf des Endpunkts müssen Sie Folgendes tun:

1. Einen Aspose Cloud-Account erstellen und eine *Client-ID* sowie einen *Client-Secret* erhalten.  
2. Ein JWT-Token durch Aufruf des OAuth-Endpunkts (`/connect/token`) anfordern. Das Token wird im Feld `access_token` zurückgegeben.  
3. Die Zielarbeitsmappe in Ihren Aspose Cloud-Speicher hochladen (oder sicherstellen, dass sie bereits im angegebenen Ordner vorhanden ist).  

Die Anforderungsparameter lauten:

| Parametername | Typ    | Ort     | Beschreibung |
|---------------|--------|---------|--------------|
| name          | string | path    | Name der Arbeitsmappendatei |
| sheetName     | string | path    | Name des Arbeitsblatts |
| value         | number | query   | Gewünschter Spaltenbreitenwert |
| range         | object | body    | Bereichsobjekt, das die Zielzellen definiert |
| folder        | string | query   | Ordnerpfad, in dem die Arbeitsmappe gespeichert ist |
| storageName   | string | query   | Name des Speicherdiensts |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

<h3 id="request">Anforderung</h3>

```bash
# Aufruf des Spaltenbreiten-Endpunkts für die Arbeitsmappe *test.xlsx*,
# Arbeitsblatt *Sheet1*, Festlegen der Breite der ausgewählten Spalten auf 20 Punkte.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">Antwort</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Mögliche Fehlerantworten*  

| HTTP-Code | Beschreibung                              |
|-----------|-------------------------------------------|
| 400       | Bad Request – ungültiges JSON oder Parameter |
| 401       | Unauthorized – fehlendes oder ungültiges Token |
| 404       | Not Found – Arbeitsmappe oder Arbeitsblatt nicht vorhanden |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie  

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q:** *Welcher Endpunkt muss aufgerufen werden, um die Spaltenbreite eines Bereichs in einer Excel-Arbeitsmappe festzulegen?*  
**A:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth`, wobei `{name}` der Name der Arbeitsmappendatei und `{sheetName}` das Zielarbeitsblatt ist.

**Q:** *Wie wird die Anforderung bei Verwendung der Spaltenbreiten-API authentifiziert?*  
**A:** Fügen Sie den Header `Authorization: Bearer <jwt token>` hinzu. Holen Sie sich das JWT-Token über den Aspose Cloud OAuth-Flow (`/connect/token`) unter Verwendung Ihrer Client-ID und Client-Secret.

**Q:** *Welcher JSON-Body muss gesendet werden, um die Breite der Spalten A–C auf 25 Punkte zu ändern?*  
**A:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

Fügen Sie dem Anforderungs-URL den Abfrageparameter `value=25` hinzu.