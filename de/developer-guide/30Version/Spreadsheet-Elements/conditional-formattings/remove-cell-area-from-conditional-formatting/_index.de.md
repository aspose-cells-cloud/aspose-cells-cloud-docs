---
title: "Zellbereich löschen – Aspose.Cells Cloud API-Dokumentation"
type: docs
url: /conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: "Aspose.Cells Cloud, Zellbereich löschen, Conditional Formatting API, Excel REST API"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um einen bestimmten Zellbereich aus einer bedingten Formatierung in einem Excel-Arbeitsblatt zu entfernen. Enthält Beispiele für ASP.NET, Java und Python."
ArticleTitle: "Zellbereich löschen – Aspose.Cells Cloud API-Dokumentation"
weight: 70
---

Diese REST API entfernt einen Zellbereich aus einer bedingten Formatierungsregel.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Anforderungsparameter

| Parametername     | Typ     | Ort    | Beschreibung                                                                 |
| ----------------- | ------- | ------ | ---------------------------------------------------------------------------- |
| `name`            | string  | path   | Der Name der Excel-Datei.                                                    |
| `sheetName`       | string  | path   | Der Name des Arbeitsblatts, das die bedingte Formatierung enthält.          |
| `startRow`        | integer | query  | Nullbasierter Index der ersten Zeile des zu entfernenden Bereichs.          |
| `startColumn`     | integer | query  | Nullbasierter Index der ersten Spalte des zu entfernenden Bereichs.         |
| `totalRows`       | integer | query  | Anzahl der Zeilen im zu entfernenden Bereich.                                |
| `totalColumns`    | integer | query  | Anzahl der Spalten im zu entfernenden Bereich.                               |
| `folder`          | string  | query  | Ordner im Cloud-Speicher, in dem sich die Datei befindet (optional).        |
| `storageName`     | string  | query  | Name des Speicherdiensts (optional).                                         |

### Fehlerantworten

| HTTP-Status | Code            | Beschreibung                                                     | Beispiel-JSON                                                  |
|-------------|-----------------|------------------------------------------------------------------|----------------------------------------------------------------|
| 400         | `BadRequest`    | Fehlende oder ungültige Parameter.                              | `{ "Code": "400", "Message": "Ungültige Anforderungsparameter." }` |
| 401         | `Unauthorized`  | Fehlender oder ungültiger JWT-Token.                            | `{ "Code": "401", "Message": "Authentifizierung fehlgeschlagen." }` |
| 404         | `NotFound`      | Datei, Arbeitsblatt oder bedingte Formatierung nicht gefunden.  | `{ "Code": "404", "Message": "Ressource nicht gefunden." }`   |
| 500         | `InternalError` | Unerwarteter Serverfehler.                                      | `{ "Code": "500", "Message": "Interner Serverfehler." }`      |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells Cloud-Dienste zuzugreifen. Das folgende Beispiel zeigt, wie der Endpunkt **Zellbereich löschen** mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}