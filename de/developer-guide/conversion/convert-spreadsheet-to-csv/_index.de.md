---
title: "Aspose.Cells Cloud Web-API – Konvertieren Sie Tabellenkalkulation in CSV"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie eine Tabellenkalkulation mithilfe der Aspose.Cells Cloud API in CSV"
linktype: "docs"
url: /convert-spreadsheet-to-csv/
keywords: "Aspose Cells, CSV-Konvertierung, Excel-API, Cloud-Konvertierung"
description: "Erfahren Sie, wie Sie Excel-Dateien (XLS, XLSX, XLSM usw.) mithilfe der Aspose.Cells Cloud API in CSV konvertieren. Enthält Authentifizierungsschritte, cURL-Beispiel, SDK-Code-Snippets und Fehlerbehandlung."
weight: 100
---

Der **ConvertSpreadsheetToCsv**-Endpunkt liest eine Tabellenkalkulationsdatei ein, die von einem lokalen Laufwerk hochgeladen wurde, führt die Konvertierung vollständig auf den Aspose.Cells Cloud-Servern durch und gibt die resultierende CSV-Datei als Binärstream zurück. Dies cloudnative Vorgehen eliminiert die Notwendigkeit, die Quelldatei in den Cloud-Speicher hochzuladen, reduziert die Speicherkosten und vereinfacht den Workflow für Entwickler, die schnelle Tabellenkalkulations-zu-CSV-Transformationen benötigen. Die unterstützten Formate hängen von den zugrunde liegenden Bibliotheken ab, und für das Lesen der Quelldatei sind entsprechende Berechtigungen erforderlich. Fehler wie fehlende Dateien, ungültige Anfragen oder Konvertierungsfehler werden mit standardmäßigen HTTP-Statuscodes zurückgegeben.

## **Convert Spreadsheet To CSV API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Speicherort | Erforderlich | Beschreibung                                                                                                                                                      |
| :---------------- | :----- | :---------- | :----------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData    | Erforderlich | Die zu konvertierende Tabellenkalkulationsdatei. Akzeptiert gängige Formate wie .xls, .xlsx, .xlsm. Muss als multipart/form-data bereitgestellt werden. Beispiel: `myWorkbook.xlsx`. |
| outPath           | String | Query       | Optional     | Zielordnerpfad, in dem die konvertierte CSV gespeichert werden soll. Falls weggelassen, wird die CSV direkt im Antworttext zurückgegeben. Beispiel: `/output/reports/`. |
| outStorageName    | String | Query       | Optional     | Name des Cloud-Speicherdienstes, in dem die Ausgabedatei gespeichert werden soll. Falls nicht angegeben, wird der für das Aspose.Cells-Konto konfigurierte Standardspeicher verwendet. |
| fontsLocation     | String | Query       | Optional     | Pfad zu einem Ordner mit benutzerdefinierten Schriftarten, die von der Tabellenkalkulation benötigt werden. Ermöglicht die korrekte Darstellung von Zellen mit nicht-standardmäßigen Schriftarten. |
| region            | String | Query       | Optional     | Regionale/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst Zahlenformatierung, Datumsauswertung und länderspezifisches Verhalten. |
| password          | String | Query       | Optional     | Passwort zum Öffnen passwortgeschützter Tabellenkalkulationen. Wenn die Datei verschlüsselt ist und das Passwort fehlt oder falsch ist, wird ein Fehler 400/401 zurückgegeben. |

### **Antwort**

Im Erfolgsfall gibt die API **HTTP 200** (oder **202** bei asynchroner Verarbeitung) mit dem Header `Content-Type: application/octet-stream` zurück. Der Antworttext enthält die generierte CSV-Datei als Binärstream.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                           |
| ---- | --------------------- | ---------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails.     |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                  |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                 |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                             |

## Wann sollten Sie die Convert Spreadsheet To CSV API verwenden?

- **Datenexport für Berichtssysteme** – Generieren Sie CSV-Exporte aus Excel-basierten Berichten, um BI-Tools oder Data-Warehouses ohne manuellen Dateiaufwand zu versorgen.
- **Automatisierte Batchverarbeitung** – Konvertieren Sie große Mengen lokal gespeicherter Tabellenkalkulationen in CSV in einem serverseitigen Job und streamen Sie die Ergebnisse direkt an nachgelagerte Dienste weiter.
- **Webanwendungen mit Datei-Uploads** – Ermöglichen Sie Endbenutzern das Hochladen einer Excel-Datei und erhalten Sie sofort eine CSV-Version für weitere Analysen oder den Import in andere Plattformen.
- **Integration veralteter Systeme** – Übersetzen Sie veraltete Tabellenkalkulationsformate in CSV für Systeme, die nur einfache, durch Trennzeichen getrennte Textdateien akzeptieren.

## Warum die Convert Spreadsheet To CSV API verwenden?

- **Zero-Upload-Architektur** – Keine Notwendigkeit, die Quelldatei im Cloud-Speicher zu speichern; die Konvertierung erfolgt direkt aus dem hochgeladenen Stream, was Zeit und Speicherkosten spart.
- **Hochleistungs-Cloudverarbeitung** – Nutzt die optimierte Konvertierungs-Engine von Aspose.Cells auf skalierbaren Cloud-Servern und liefert schnelle CSV-Ausgaben, auch bei großen Arbeitsmappen.
- **Einfache Integration** – Einzelner PUT-Request mit optionalen Abfrageparametern; gibt die CSV als sofort herunterladbaren Binärstream zurück, wodurch Nachbearbeitungsschritte entfallen.
- **Vollständige Funktionsunterstützung** – Verarbeitet passwortgeschützte Dateien, benutzerdefinierte Schriftarten und länderspezifische Einstellungen und gewährleistet so eine präzise Konvertierung auch für komplexe Tabellenkalkulationen.

## Wie Sie die Convert Spreadsheet To CSV API mit SDKs verwenden

### Convert Spreadsheet To CSV API-Spezifikation

Die [Convert Spreadsheet To CSV API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv) bietet eine öffentlich zugängliche Programmierschnittstelle zur Durchführung von REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Details der niedrigen Ebene abstrahiert und es Ihnen ermöglicht, mit Tabellenkalkulationen über prägnanten Code zu arbeiten. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs. Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs auf die Aspose.Cells-Webdienste zugreifen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}