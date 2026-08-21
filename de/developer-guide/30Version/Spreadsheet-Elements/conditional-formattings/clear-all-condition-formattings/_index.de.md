---
title: "Bedingte Formatierungen löschen"
type: docs
url: /de/conditional-formattings/clear/
aliases: [  /de/clear-all-condition-formattings/ ]
keywords: "Aspose.Cells Cloud, REST API, bedingte Formatierung löschen, Excel, Arbeitsblätter, JWT, v3.2"
description: "Löschen Sie alle bedingten Formatierungsregeln aus einem Arbeitsblatt mithilfe der Aspose.Cells Cloud API (v3.2). Erfahren Sie mehr zur Anforderungssyntax, den erforderlichen Parametern, den Authentifizierungsschritten und sehen Sie Beispielcodes in verschiedenen SDKs."
weight: 80
---

Diese REST API löscht alle bedingten Formatierungsregeln aus einem Arbeitsblatt.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                                                         |
| --------------- | ------ | ------ | -------------------------------------------------------------------- |
| **name**        | string | path   | Der Name der Arbeitsmappe (z. B. `Book1.xlsx`).                     |
| **sheetName**   | string | path   | Der Name des Arbeitsblatts, aus dem die bedingte Formatierung entfernt werden soll. |
| **folder**      | string | query  | _(Optional)_ Pfad des Ordners im Speicher, in dem sich die Arbeitsmappe befindet. |
| **storageName** | string | query  | _(Optional)_ Name des Speicherdienstes.                             |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) definiert eine öffentlich zugängliche Programmierschnittstelle, und **die OpenAPI-Spezifikation** ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
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

### Fehlerantworten

| HTTP-Code | Grund                                              | Beispielinhalt                                                      |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – fehlende oder ungültige Parameter.  | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }`          |
| **401**   | Unauthorized – fehlender oder ungültiger JWT-Token. | `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code":"404", "Message":"Datei nicht gefunden." }`              |
| **500**   | Internal Server Error – unerwarteter Serverfehler. | `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

## SDK-Beispiele

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}