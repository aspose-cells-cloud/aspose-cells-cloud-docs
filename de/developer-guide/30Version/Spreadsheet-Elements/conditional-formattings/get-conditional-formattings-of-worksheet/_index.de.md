---
title: "Abrufen bedingter Formatierungsregeln"
type: docs
url: /de/conditional-formattings/get-all/
aliases: [  /de/get-conditional-formattings-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, Bedingte Formatierung, Arbeitsblatt, Conditional Formatting API"
description: "Rufen Sie alle bedingten Formatierungsregeln ab, die auf ein Arbeitsblatt angewendet werden, mithilfe der Aspose.Cells Cloud REST API. Enthält Syntaxanforderung, Authentifizierungsschritte, Parameter, prägnante Antwortbeispiele und Fehlerbehandlung."
weight: 20
---

Diese REST API ruft die bedingten Formatierungsregeln ab, die auf ein Arbeitsblatt angewendet werden.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                                       |
| --------------- | ------ | ------ | -------------------------------------------------- |
| name            | string | path   | Der Name der Excel-Datei.                         |
| sheetName       | string | path   | Der Name des Arbeitsblatts.                       |
| folder          | string | query  | Der Pfad des Ordners, in dem die Datei gespeichert ist. |
| storageName     | string | query  | Der Name des Speicherdienstes (optional).        |

### Fehlerantworten

| HTTP-Code | Grund                                              | Beispielinhalt                                                      |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – fehlende oder ungültige Parameter. | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }`          |
| **401**   | Unauthorized – fehlender oder ungültiger JWT-Token. | `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code":"404", "Message":"Datei nicht gefunden." }`             |
| **500**   | Internal Server Error – unerwarteter Serverfehler. | `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

Die <a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_Das obige Beispiel zeigt nur die relevantesten Felder, um die Nutzlast knapp zu halten._

**Antwortparameter**

| Parameter                              | Typ    | Beschreibung                                                    |
|----------------------------------------|--------|-----------------------------------------------------------------|
| Status                                 | string | Ergebnisstatus der Anforderung (z. B. **OK**).                 |
| ConditionalFormattings                 | object | Container für bedingte Formatierungsdaten.                     |
| ConditionalFormattings.Count           | integer| Anzahl der zurückgegebenen bedingten Formatierungsregeln.      |
| ConditionalFormattings.ConditionalFormattingList | array  | Liste der bedingten Formatierungsobjekte.                      |
| ConditionalFormattingList[].sqref      | string | Zellbereich, auf den die Formatierung angewendet wird (z. B. **A1:B10**). |
| ConditionalFormattingList[].FormatConditions | array  | Sammlung von Formatbedingungsobjekten für den Bereich.         |
| FormatConditions[].Priority            | integer| Evaluationspriorität der Bedingung.                            |
| FormatConditions[].Type                | string | Typ der Bedingung (z. B. **CellValue**).                       |
| FormatConditions[].Operator            | string | Für die Bedingung verwendeter Operator (z. B. **GreaterThan**). |
| FormatConditions[].Formula1            | string | Erste Formel oder der erste Wert für die Bedingung.            |
| FormatConditions[].Style               | object | Formatierung, die angewendet wird, wenn die Bedingung erfüllt ist. |
| Style.Font.Color                       | object | RGBA-Farbangabe für die Schriftart.                             |
| Style.Font.IsBold                      | boolean| Gibt an, ob die Schriftart fett ist.                            |

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                     |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größenbeschränkung.        |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                       |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Bitte schauen Sie in das <a href="https://github.com/aspose-cells-cloud" target="_blank">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}