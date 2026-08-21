---
title: "So verschmelzen Sie Zellen in einer Excel-Arbeitsmappe – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /de/merge-cells-in-excel-worksheet/
weight: 110
keywords: "Zellen verschmelzen, Aspose.Cells, Cloud API, Excel"
description: "Anleitung zum Verschmelzen von Zellen in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API mit cURL- und SDK-Beispielen."
ArticleTitle: "So verschmelzen Sie Zellen in einer Excel-Arbeitsmappe – Aspose.Cells Cloud API (v3.0)"
---

Die Aspose.Cells Cloud REST API verschmilzt ein rechteckiges Zellblock in eine einzelne Zelle, die sich über die angegebenen Zeilen und Spalten erstreckt.

**Voraussetzungen**  
- Ein gültiges JWT-Token zur Authentifizierung.  
- Die Arbeitsmappe muss bereits im angegebenen Speicherordner vorhanden sein.  
- Die Speicherkonfiguration (Ordner und Speichername) muss in Ihrem Aspose.Cloud-Konto eingerichtet sein.

## PostWorksheetMerge API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Name          | Typ     | Ort     | Beschreibung                                     |
|---------------|---------|---------|--------------------------------------------------|
| name          | string  | path    | Der Name der Arbeitsmappe.                       |
| sheetName     | string  | path    | Der Name des Arbeitsblatts.                      |
| startRow      | integer | query   | Nullbasierter Index der ersten Zeile (0 = erste Zeile). |
| startColumn   | integer | query   | Nullbasierter Index der ersten Spalte (0 = erste Spalte). |
| totalRows     | integer | query   | Anzahl der zu verschmelzenden Zeilen.            |
| totalColumns  | integer | query   | Anzahl der zu verschmelzenden Spalten.           |
| folder        | string  | query   | Der Ordner, der die Arbeitsmappe enthält.        |
| storageName   | string  | query   | Der Speichername.                                |

*Für diesen Vorgang ist kein Anforderungstext erforderlich.*

## **Antwort**

Gibt CellsCloudResponse zurück.

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## So verwenden Sie die PostWorksheetMerge API mit SDKs

### PostWorksheetMerge API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das **cURL-Befehlszeilentool** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
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

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Bitte überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}