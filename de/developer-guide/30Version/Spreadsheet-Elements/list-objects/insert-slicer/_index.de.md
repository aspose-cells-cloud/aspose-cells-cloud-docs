---
title: "Einfügen eines Slicers in ein Excel ListObject – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Slicer einfügen"
type: docs
keywords: "Aspose.Cells, Excel-Slicer, ListObject, REST-API, Cloud-SDK"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API (v3.0) einen Slicer einem Excel ListObject hinzufügen. Enthält Endpunkt, Parameter, Authentifizierung, Beispiel-cURL-Anfrage und Antwort-JSON."
weight: 20
ArticleTitle: "Einfügen eines Slicers in ein Excel ListObject – Aspose.Cells Cloud API"
---

Diese REST-API fügt einen Slicer für ein ListObject in einem Excel-Arbeitsblatt ein.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### Anforderungsparameter

| Parametername   | Typ     | Ort     | Beschreibung                                                                          |
| --------------- | ------- | ------- | ------------------------------------------------------------------------------------- |
| name            | String  | Pfad    | Der Name der Excel-Datei.                                                             |
| sheetName       | String  | Pfad    | Der Name des Arbeitsblatts, das das ListObject enthält.                              |
| listObjectIndex | Integer | Pfad    | Der nullbasierte Index des ListObjects, dem der Slicer hinzugefügt werden soll.      |
| columnIndex     | Integer | Query   | Der nullbasierte Index der Spalte, auf der der Slicer basiert.                        |
| destCellName    | String  | Query   | Die Zellreferenz (z. B. **A1**), an der der Slicer platziert wird.                   |
| folder          | String  | Query   | Der Ordner im Speicher, der die Excel-Datei enthält.                                 |
| storageName     | String  | Query   | Der Name des Aspose Cloud-Speicherdiensts.                                            |

Sie können das cURL-Befehlszeilentool verwenden, um die API aufzurufen:

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Hinweis:** Die Anfrage erfordert ein gültiges JWT-Bearer-Token, das vom Aspose Cloud-Authentifizierungsdienst abgerufen wurde. Dieser Endpunkt erfordert keinen Anforderungstext; senden Sie ein leeres JSON-Objekt `{}`, sofern Ihre Client-Bibliothek einen Payload vorschreibt.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **Antwortheader:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

### Fehlerbehandlung

Bei einem Fehler gibt die API ein JSON-Objekt mit einem Feld `ErrorMessage` zurück, das das Problem beschreibt. Prüfen Sie den HTTP-Statuscode und den `ErrorMessage`, um die erforderliche Korrekturmaßnahme zu ermitteln.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Low-Level-Details und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Besuchen Sie das GitHub-Repository für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}