---
title: "Formatbedingung hinzufügen"
type: docs
url: /de/conditional-formattings/add-format-condition/
aliases: [  /de/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, Conditional Formatting API, Formatbedingung hinzufügen, Excel REST API, Cells API"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API (v3.0) eine Formatbedingung zu einem Excel-Arbeitsblatt hinzufügen. Enthält die Anforderungssyntax, Parameter, ein sicheres cURL-Beispiel und SDK-Snippets."
ArticleTitle: "Formatbedingung hinzufügen – Aspose.Cells Cloud API-Dokumentation"
weight: 50
---

Diese REST API fügt eine Formatbedingung zu einem Arbeitsblatt hinzu.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Anforderungsparameter

| Parametername   | Typ     | Ort    | Beschreibung                                                               |
| --------------- | ------- | ------ | -------------------------------------------------------------------------- |
| name            | string  | path   | Der Name der Excel-Arbeitsmappe.                                           |
| sheetName       | string  | path   | Der Name des Arbeitsblatts, das den zu formatierenden Bereich enthält.    |
| index           | integer | path   | Der nullbasierte Index der hinzuzufügenden oder zu ersetzenden Bedingung. |
| cellArea        | string  | query  | Der Zellbereich (z. B. `A1:C3`), auf den die Bedingung angewendet wird.   |
| type            | string  | query  | Der Typ der Bedingung (z. B. `Expression`, `CellValue`).                  |
| operatorType    | string  | query  | Der Operator für die Bedingung (z. B. `Between`, `Equal`).                |
| formula1        | string  | query  | Die erste Formel oder der erste Wert, der von der Bedingung verwendet wird.|
| formula2        | string  | query  | Die zweite Formel oder der zweite Wert (für einige Operatoren wie `Between` erforderlich). |
| folder          | string  | query  | Der Ordner im Speicher, in dem sich die Arbeitsmappe befindet.            |
| storageName     | string  | query  | Der Name des Speicherdienstes (z. B. `Default`).                          |

### Fehlerantworten

| HTTP-Code | Grund                                              | Beispiel-Body                                                       |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – fehlende oder ungültige Parameter.  | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }`          |
| **401**   | Unauthorized – fehlender oder ungültiger JWT-Token.| `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code":"404", "Message":"Datei nicht gefunden." }`          |
| **500**   | Internal Server Error – unerwarteter Serverfehler.| `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

### Erfolgsantwort

| HTTP-Code | Grund                                             | Beispiel-Body                             |
| --------- | ------------------------------------------------- | ------------------------------------------ |
| **200**   | OK – Bedingung erfolgreich hinzugefügt oder aktualisiert. | `{ "Code": "200", "Status": "OK" }` |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können **cURL** verwenden, um die Aspose.Cells API aufzurufen. Das folgende Beispiel zeigt eine vollständige Anforderung, einschließlich eines leeren JSON-Körpers.

### cURL-Beispiel

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
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

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektziele konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}