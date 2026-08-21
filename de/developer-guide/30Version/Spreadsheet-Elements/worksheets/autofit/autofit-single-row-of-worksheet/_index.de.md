---
title: "Zeile in einem Excel-Arbeitsblatt automatisch anpassen"
second_title: "Dokument"
linktitle: "Zeile"
type: docs
url: /de/worksheets/autofit/row/
aliases: [  /de/autofit-single-row-of-worksheet/ ]
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST API verwenden, um eine Zeile in einem Excel-Arbeitsblatt automatisch anzupassen. Enthält Endpunkt, Parameter, Authentifizierung, Fehlerbehandlung, cURL-Anforderung und SDK-Beispiele."
keywords: "Zeile automatisch anpassen, Aspose.Cells Cloud, Excel-API, REST, Arbeitsblatt, SDK, Tabellenkalkulation, Cloud-API"
weight: 30
ArticleTitle: "Zeile in Excel-Arbeitsblatt mit Aspose.Cells Cloud API automatisch anpassen"
---

Diese REST API **passt eine Zeile in einem Excel-Arbeitsblatt automatisch an**.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Anforderungsparameter**

| Parametername     | Typ     | Ort    | Beschreibung                                                                                                                                                                                                  |
| ----------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name              | string  | path   | Der Name der Excel-Datei.                                                                                                                                                                                     |
| sheetName         | string  | path   | Der Name des Arbeitsblatts.                                                                                                                                                                                   |
| rowIndex          | integer | query  | Nullbasierter Index der Zeile, die automatisch angepasst werden soll.                                                                                                                                        |
| firstColumn       | integer | query  | Index der ersten Spalte, die in den Vorgang einbezogen wird.                                                                                                                                                 |
| lastColumn        | integer | query  | Index der letzten Spalte, die in den Vorgang einbezogen wird.                                                                                                                                                |
| autoFitterOptions | object  | body   | Objekt, das das Verhalten der automatischen Anpassung steuert (z. B. ob zusammengeführte Zellen oder Textumbrüche berücksichtigt werden sollen). Siehe [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="Steuert das Verhalten der automatischen Anpassung"}. |
| folder            | string  | query  | Ordner, in dem die Datei gespeichert ist.                                                                                                                                                                    |
| storageName       | string  | query  | Name des Speichers.                                                                                                                                                                                           |

**Beispiel-`autoFitterOptions` JSON-Body**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### Entitätsdefinitionen

| Entität               | Beschreibung                                                                 |
| --------------------- | ---------------------------------------------------------------------------- |
| `rowIndex`            | Nullbasierter Index der Zielzeile.                                           |
| `firstColumn`         | Startspalte für den Vorgang der automatischen Anpassung.                     |
| `lastColumn`          | Endspalte für den Vorgang der automatischen Anpassung.                       |
| `autoFitterOptions`   | optionale Einstellungen, die beeinflussen, wie die Zeile automatisch angepasst wird (zusammengeführte Zellen, Textumbruch usw.). |

Die [OpenAPI-Spezifikation](/cells/#/Worksheets/PostAutofitWorksheetRow) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Feld  | Beschreibung                                     |
| ----- | ----------------------------------------------- |
| Code  | `200` – Anforderung erfolgreich.                |
| Status | `"OK"` – die Zeile wurde erfolgreich angepasst. |

{{< /tab >}}

{{< /tabs >}}

## Fehlerbehandlung

Die API gibt standardmäßige HTTP-Statuscodes zurück. Häufige Fehlerantworten für diesen Endpunkt sind:

| HTTP-Code | Beispiel-Payload                                          | Bedeutung                                                                              |
| --------- | --------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 400       | `{ "Code": 400, "Message": "Row index out of range." }`   | Der übergebene `rowIndex` existiert nicht im Arbeitsblatt.                             |
| 401       | `{ "Code": 401, "Message": "Invalid or expired token." }` | Authentifizierung fehlgeschlagen – prüfen Sie das JWT-Token und stellen Sie sicher, dass die Anforderung über HTTPS erfolgt. |
| 404       | `{ "Code": 404, "Message": "File not found." }`           | Die angegebene Excel-Datei oder das Arbeitsblatt kann nicht gefunden werden.           |
| 500       | `{ "Code": 500, "Message": "Internal server error." }`    | Ein unerwartetes Serverproblem ist aufgetreten.                                        |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**Siehe auch:** [Spalte automatisch anpassen](/worksheets/autofit/column/), [Zeilen automatisch anpassen](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).