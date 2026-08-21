---
title: "Zellen in Excel-Arbeitsblatt entgruppen"
type: docs
url: /de/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, Zellen entgruppen, REST API, Cloud SDK"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST API Zellen in einem Excel-Arbeitsblatt entgruppen, einschließlich Beispielanfragen, Antwortformat und SDK-Codebeispielen für mehrere Programmiersprachen."
ArticleTitle: "Zellen in Excel-Arbeitsblatt entgruppen"
---

Diese REST API gruppiert Zellen in einer Excel-Datei wieder auf.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Anforderungsparameter**

| Parametername | Typ    | Ort    | Beschreibung                                             |
|---------------|--------|--------|----------------------------------------------------------|
| name          | string | path   | Name der Arbeitsmappen-Datei.                            |
| sheetName     | string | path   | Name des Arbeitsblatts.                                  |
| startRow      | integer | query | Nullbasierter Index der ersten Zeile, die entgruppt werden soll. |
| startColumn   | integer | query | Nullbasierter Index der ersten Spalte, die entgruppt werden soll. |
| totalRows     | integer | query | Anzahl der Zeilen, die in den Entgruppierungsvorgang einbezogen werden sollen. |
| totalColumns  | integer | query | Anzahl der Spalten, die in den Entgruppierungsvorgang einbezogen werden sollen. |
| folder        | string | query | Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.     |
| storageName   | string | query | Name des Speicherdienstes.                               |

## **Antwort**

Gibt CellCloudResponse zurück.

- **Übersicht der Antwortfelder**

| Feld           | Typ    | Beschreibung                                           |
| --------------- | ------ | ------------------------------------------------------ |
| `Status`        | string |                                                        |
| `Code`          | integer | 200,400,401,500,...                                   |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                      |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                       |

## Verwendung der PostWorksheetUnmerge API mit SDKs

### Spezifikation der PostWorksheetUnmerge API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach anzusprechen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene und lässt Sie sich auf Ihre ProjektAufgaben konzentrieren. Bitte überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}