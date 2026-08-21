---
title: "Aspose.Cells Cloud Web-API – Konvertieren einer Tabellendatei in PDF"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie eine lokale Tabellendatei mithilfe der Aspose.Cells Cloud API in PDF"
linktitle: "Tabellendatei in PDF konvertieren"
type: docs
url: /de/convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, Tabellendatei zu PDF, Excel-Konvertierung, Cloud-API, PDF-Erstellung, REST-API, v4.0"
description: "Schritt-für-Schritt-Anleitung zur Konvertierung einer lokalen Tabellendatei in PDF mithilfe der Aspose.Cells Cloud API. Enthält Anforderungssyntax, Parameter, Antwortdetails, Fehlerbehandlung und praktische Anwendungsfälle."
weight: 100
---

Der Endpunkt **ConvertSpreadsheetToPdf** liest eine Tabellendatei ein, die vom lokalen Laufwerk hochgeladen wurde, verarbeitet sie auf dem Aspose.Cells Cloud-Server und gibt das resultierende PDF-Dokument als Binärstream zurück. Diese cloudbasierte Konvertierung beseitigt die Notwendigkeit, die Quelldatei in den Speicher hochzuladen, reduziert den Ressourcenverbrauch und vereinfacht Workflows, da das PDF direkt an den Client geliefert wird. Unterstützte Formate hängen von den zugrunde liegenden Bibliotheken ab; die API überprüft die Dateiexistenz, die Berechtigungen und die Integrität der Konvertierung und löst geeignete HTTP-Fehler für ungültige Eingaben oder Verarbeitungsfehler aus.

## **Convert Spreadsheet To Pdf API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Ort       | Erforderlich/Optional | Beschreibung                                                                                                                                                                                    |
| :---------------- | :----- | :-------- | :-------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData  | Erforderlich          | Die zu konvertierende Quell-Tabellendatei (XLS, XLSX, CSV usw.). Muss eine gültige, lesbare Datei sein; maximale Größe beträgt 100 MB. Beispiel: `myWorkbook.xlsx`.                             |
| outPath           | String | Query     | Optional              | Zielordnerpfad, in dem die konvertierte PDF-Datei auf dem Server gespeichert wird (sofern gewünscht). Falls weggelassen, wird die Datei direkt in der Antwort zurückgegeben. Beispiel: `/output/reports/`. |
| outStorageName    | String | Query     | Optional              | Name des Ziel-Speicherdienstes (z. B. `MyCloudStorage`). Erforderlich, nur wenn `outPath` verwendet wird und der Speicher nicht der Standardspeicher ist.                                      |
| fontsLocation     | String | Query     | Optional              | Pfad zu einem benutzerdefinierten Schriftartenordner auf dem Server, um eine korrekte Textdarstellung im PDF sicherzustellen. Beispiel: `/fonts/custom/`.                                       |
| region            | String | Query     | Optional              | Regionale/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten.                                    |
| password          | String | Query     | Optional              | Passwort, das zum Öffnen einer geschützten Tabellendatei erforderlich ist. Weglassen, wenn die Datei nicht verschlüsselt ist.                                                                  |

### **Antwort**

Erfolgreiche Antwort (200 OK)  
Content-Type: application/pdf  
Content-Disposition: attachment; filename="converted.pdf"  
Content-Length: `<Größe in Bytes>`

Body: Binärstream der generierten PDF-Datei

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                      |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Vorgang erfolgreich abgeschlossen; Antwort enthält Details.      |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.            |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## Wo sollte die Convert Spreadsheet To Pdf API verwendet werden?

- **Automatisierte Berichtspipelines** – Konvertieren Sie tägliche Excel-Berichte, die automatisch generiert werden, in PDF zum Archivieren oder Versenden per E-Mail, ohne manuelle Schritte.
- **Dokumentenverwaltungssysteme (DMS)** – Speichern Sie PDFs direkt im DMS nach der Konvertierung; die ursprüngliche Tabellendatei verbleibt ausschließlich auf Clientseite.
- **Webanwendungen mit dynamischem Export** – Ermöglichen Sie Endbenutzern das Herunterladen einer PDF-Version einer Tabellendatei, die sie im Browser bearbeiten, wobei die Cloud-Konvertierung das Layout beibehält.
- **Regulatorische Compliance** – Erstellen Sie unveränderliche PDF-Snapshots von Finanz-Tabellendateien für Prüfungsprotokolle, ohne dass die Quelldatei die Clientumgebung verlässt.
- **Konvertierungsworkflows für mehrere Formate** – Kombinieren Sie mit anderen Konvertierungs-Endpunkten wie der [Convert Spreadsheet to CSV](/convert-spreadsheet-to-csv/) API, um Archive in mehreren Formaten zu erstellen.

## Warum sollte man die Convert Spreadsheet To Pdf API verwenden?

- **Upload-freier Workflow** – Kein Upload der Quelldatei in den Cloud-Speicher erforderlich; die Konvertierung erfolgt direkt aus dem hochgeladenen Stream, was Bandbreite und Speicherkosten spart.
- **Hochwertige Wiedergabe** – Aspose.Cells bewahrt komplexe Formeln, Diagramme und Formatierungen bei der Konvertierung in PDF und entspricht damit der Ausgabe von Excel auf dem Desktop.
- **Skalierbare Cloud-Ausführung** – Nutzt die Cloud-Infrastruktur von Aspose für schnelle, zuverlässige Konvertierungen, unabhängig von der Client-Hardware.
- **Einfache REST-Schnittstelle** – Eine einzelne `PUT`-Anfrage mit optionalen Query-Parametern; liefert einen sofort herunterladbaren PDF-Stream, was die Integration in jede Sprache vereinfacht.

## So verwenden Sie die Convert Spreadsheet To Pdf API mit SDKs

### API-Spezifikation für Convert Spreadsheet To Pdf

Die [API-Spezifikation für Convert Spreadsheet To Pdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) stellt eine öffentlich zugängliche Programmierschnittstelle zur Verfügung, mit der REST-Interaktionen direkt aus einem Webbrowser ausgeführt werden können.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie mit cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da die SDKs die Low-Level-Details abstrahieren und es ermöglichen, Tabellendateien mit wenig Code zusammenzuführen. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs einzusehen. Die folgenden Codebeispiele zeigen, wie mit Aspose.Cells-Webdiensten über verschiedene SDKs interagiert wird:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}