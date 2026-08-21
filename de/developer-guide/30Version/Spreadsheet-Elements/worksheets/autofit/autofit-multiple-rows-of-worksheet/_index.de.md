---
title: "Mehrere Zeilen in einem Excel-Arbeitsblatt automatisch anpassen"
second_title: "Dokument"
linktitle: "Zeilen"
type: docs
url: /worksheets/autofit/rows/
aliases: [/autofit-multiple-rows-of-worksheet/]
keywords: "Zeilen automatisch anpassen, Excel, Aspose.Cells Cloud, REST API, Arbeitsblatt, Tabellenkalkulation"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST API mehrere Zeilen in einem Excel-Arbeitsblatt automatisch anpassen können. Enthält Anforderungssyntax, Parameter, cURL-Beispiel, SDK-Snippets und Fehlerbehandlung."
weight: 40
ArticleTitle: "Mehrere Zeilen in einem Excel-Arbeitsblatt automatisch anpassen – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST API passt die Höhe der Zeilen in einem Excel-Arbeitsblatt automatisch an.

## Sicherheit und Authentifizierung  
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **Anforderungsparameter**

| Parametername         | Typ     | Ort    | Beschreibung                                                                                                                          | Erforderlich |
| --------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------ |
| **name**              | string  | path   | Der Name der Excel-Datei.                                                                                                           | ✔            |
| **sheetName**         | string  | path   | Der Name des Arbeitsblatts.                                                                                                         | ✔            |
| **autoFitterOptions** | object  | body   | Optionen zur Steuerung der automatischen Anpassung von Zeilen (z. B. ignorierte ausgeblendete Zeilen). Siehe die kurze Feldbeschreibung unten. | ✖            |
| **startRow**          | integer | query  | Die erste anzupassende Zeile (1-basierter Index).                                                                                  | ✔            |
| **endRow**            | integer | query  | Die letzte anzupassende Zeile (inklusiv).                                                                                          | ✔            |
| **onlyAuto**          | boolean | query  | Wenn `true`, passt die API nur Zeilen an, deren Höhe von Excel automatisch berechnet wird. Wenn `false`, wird eine vollständige Anpassung durchgeführt. | ✖            |
| **folder**            | string  | query  | Der Ordner, der das Dokument enthält.                                                                                              | ✖            |
| **storageName**       | string  | query  | Der Name des Speicherdienstes.                                                                                                      | ✖            |

**autoFitterOptions**-Felder (alle optional):

- `AutoFitMergedCells` _(boolean)_ – Wenn `true`, werden zusammengeführte Zellen bei der Berechnung der Zeilenhöhe berücksichtigt.
- `IgnoreHidden` _(boolean)_ – Wenn `true`, werden ausgeblendete Zeilen während des Anpassungsvorgangs ignoriert.
- `OnlyAuto` _(boolean)_ – Spiegelt den Abfrageparameter `onlyAuto`; bei Festlegung überschreibt dieser Wert den Abfragewert.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um bequem auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Typische Fehlerantworten umfassen:

- **400 Bad Request** – Ungültige Parameterwerte oder fehlerhaftes JSON-Body.
- **401 Unauthorized** – Fehlender oder ungültiger JWT-Token.
- **404 Not Found** – Die angegebene Datei oder das angegebene Arbeitsblatt existiert nicht.
- **500 Internal Server Error** – Ein unerwarteter Serverfehler ist aufgetreten.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                     |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; die Antwort enthält Operationsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.            |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                       |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie  
Die Verwendung eines SDKs ist die schnellste Methode zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}