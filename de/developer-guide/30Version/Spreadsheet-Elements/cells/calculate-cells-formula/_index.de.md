---
title: "Zellenformel berechnen – Aspose.Cells Cloud API"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, Zellenformel berechnen, Excel-API, REST-API, SDK"
description: "Berechnen Sie eine Excel-Zellenformel über die Aspose.Cells Cloud REST-API (v3.0). Enthält Endpunkt, Parameter, cURL-Beispiel und SDK-Snippets."
ArticleTitle: "Zellenformel berechnen – Aspose.Cells Cloud API-Dokumentation"
---

## REST API

Diese REST-API berechnet die **Zellenformel** in einer Excel-Arbeitsmappe.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Anforderungsparameter

| Parametername | Typ   | Parameterposition (Pfad/Abfrage/Textkörper) | Beschreibung                                                                 |
| ------------- | ----- | -------------------------------------------- | ---------------------------------------------------------------------------- |
| name          | string | Pfad                                        | Name der Excel-Datei (z. B. `Book1.xlsx`).                                   |
| sheetName     | string | Pfad                                        | Name des Arbeitsblatts, das die Zelle enthält.                               |
| cellName      | string | Pfad                                        | Adresse der zu berechnenden Zelle (z. B. `A1`).                              |
| options       | object | Textkörper                                  | JSON-Objekt mit Berechnungsoptionen (siehe Tabelle **Options-Objekt**).     |
| folder        | string | Abfrage                                     | Ordner im Speicher, in dem sich die Datei befindet.                          |
| storageName   | string | Abfrage                                     | Name des Aspose Cloud-Speichers.                                             |

#### Options-Objekt

| Feld          | Typ     | Beschreibung                                                                      | Standardwert |
| ------------- | ------- | --------------------------------------------------------------------------------- | ------------ |
| CalcStackSize | string  | Maximale Größe des Berechnungsstapels.                                            | `"1"`        |
| IgnoreError   | boolean | Wenn `true`, werden Berechnungsfehler ignoriert und der Zellwert wird auf `#N/A` gesetzt. | `false`      |
| Recursive     | boolean | Aktiviert die rekursive Berechnung abhängiger Zellen.                             | `false`      |
| Precision     | string  | Anzahl der Dezimalstellen für numerische Ergebnisse.                              | `"15"`       |
| UseThreading  | boolean | Aktiviert die mehrthreadsige Berechnung.                                          | `false`      |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                         |
|------|-----------------------------|----------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größeinschränkung.             |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                          |

## Verwendung der PostCellCalculate API mit SDKs

### PostCellCalculate API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird. **Holen Sie sich zuerst ein JWT-Token**, indem Sie sich beim Endpunkt `/connect/token` authentifizieren, und ersetzen Sie `<jwt token>` durch den Tokenwert.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK abstractiert Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}