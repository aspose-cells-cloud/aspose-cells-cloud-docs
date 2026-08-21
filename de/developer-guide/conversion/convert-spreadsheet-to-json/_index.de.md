---
title: "Aspose.Cells Cloud Web-API – Konvertieren Sie Tabellenkalkulation in JSON"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie eine lokale Tabellenkalkulation mithilfe der Aspose.Cells Cloud API in JSON"
linktype: "Konvertieren Sie Tabellenkalkulation in JSON"
type: docs
url: /convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, Konvertieren Sie Tabellenkalkulation in JSON, Excel zu JSON API, Aspose.Cells Cloud API, REST API, Tabellenkalkulationskonvertierung"
description: "Erfahren Sie, wie Sie lokale Excel-Dateien mit der Aspose.Cells Cloud API in JSON konvertieren. Enthält Endpunkt, Parameter, Beispielcode und Fehlerbehandlung für nahtlose Integration."
weight: 100
---

Der **ConvertSpreadsheetToJson**-Endpunkt konvertiert eine auf einem lokalen Laufwerk gespeicherte Tabellenkalkulation vollständig auf dem Aspose.Cells Cloud-Server in eine JSON-Datei. Durch das Senden der Tabellenkalkulation als `multipart/form-data` gibt der Dienst einen JSON-Stream zurück, der sofort zum Herunterladen oder zur weiteren Verarbeitung verwendet werden kann. Diese cloudnative Konvertierung eliminiert die Notwendigkeit, die Datei zuerst in den Speicher hochzuladen, reduziert die Speicherkosten und vereinfacht den Arbeitsablauf für Anwendungen, die Tabellenkalkulationsdaten im JSON-Format für Analyse, Berichtserstellung oder Datenaustausch benötigen.

**Voraussetzungen**: Sie müssen über ein Aspose Cloud-Konto, ein gültiges JWT-Zugriffstoken sowie das Aspose.Cells Cloud SDK oder den API-Schlüssel verfügen, der konfiguriert ist.

**Hintergrund**: Die Konvertierung von Tabellenkalkulationen in JSON ist ein gängiger Schritt bei der Integration von Excel-Daten mit Webdiensten, NoSQL-Datenbanken oder clientseitigen JavaScript-Anwendungen. Die API „Tabellenkalkulation in JSON konvertieren“ bietet eine schnelle serverseitige Konvertierung, ohne die Originaldatei speichern zu müssen.

## API: Tabellenkalkulation in JSON konvertieren

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ                        | Standort | Erforderlich/Optional | Beschreibung                                                                                                                                                                       |
| :---------------- | :------------------------- | :------- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei (multipart/form-data)| FormData | Erforderlich         | Die Quell-Tabellenkalkulationsdatei (z. B. .xls, .xlsx, .xlsm). Beispiel: `curl -F "Spreadsheet=@myfile.xlsx"`                                                                    |
| outPath           | Zeichenkette               | Query    | Optional             | Zielordnerpfad im Cloud-Speicher, in dem die konvertierte JSON-Datei gespeichert wird. Falls weggelassen, wird das JSON direkt im Antwortstream zurückgegeben. Beispiel: `outPath=/output/`. |
| outStorageName    | Zeichenkette               | Query    | Optional             | Name des Cloud-Speichers (z. B. Amazon S3, Azure Blob), in den die Ausgabedatei geschrieben werden soll. Erforderlich nur, wenn `outPath` mit einem nicht standardmäßigen Speicher verwendet wird. |
| fontsLocation     | Zeichenkette               | Query    | Optional             | Pfad zu einem benutzerdefinierten Schriftartenordner auf dem Server. Dieser Parameter ist zu verwenden, wenn die Tabellenkalkulation Schriftarten verwendet, die nicht in der Standardbibliothek verfügbar sind. |
| region            | Zeichenkette               | Query    | Optional             | Regionale/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Formatierung von Zahlen, Daten und Währungen während der Konvertierung.     |
| password          | Zeichenkette               | Query    | Optional             | Passwort zum Öffnen einer passwortgeschützten Tabellenkalkulation. Weglassen bei ungeschützten Dateien.                                                                            |

### Antwort

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

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Anforderungstext zu groß | Hochgeladene Datei überschreitet das Größenlimit.              |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler.                                       |

## Wann sollte die API „Tabellenkalkulation in JSON konvertieren“ verwendet werden?

- **Daten-Migrationspipelines** – Konvertieren Sie veraltete Excel-Berichte in JSON zur Einspeisung in moderne NoSQL-Datenbanken oder Data Lakes.
- **Mobile oder Webanwendungen** – Transformieren Sie schnell per Benutzer hochgeladene Tabellenkalkulationen in JSON für clientseitige Darstellung, ohne die Originaldatei im Cloud-Speicher zu speichern.
- **Automatisierte Berichterstellung** – Generieren Sie JSON-Payloads für nachgelagerte Analyse-Dienste (z. B. Power BI, Tableau) direkt aus Tabellenkalkulations-Eingaben.
- **Serverlose Funktionen** – Verwenden Sie die API innerhalb von AWS Lambda oder Azure Functions, um sofortige Konvertierungen durchzuführen, ohne temporären Speicher verwalten zu müssen.

## Warum sollten Sie die API „Tabellenkalkulation in JSON konvertieren“ verwenden?

- Cloudnative Konvertierung entfernt die Notwendigkeit, große Dateien vor der Verarbeitung in den Speicher hochzuladen, wodurch Latenz und Speicherkosten reduziert werden.
- Einzelner Anforderungs-Workflow: Laden Sie die Tabellenkalkulation hoch und erhalten Sie JSON im gleichen HTTP-Aufruf, was die Integrationslogik vereinfacht.
- Unterstützt passwortgeschützte und regions-spezifische Tabellenkalkulationen, um eine genaue Datendarstellung über verschiedene Regionen hinweg sicherzustellen.
- Skalierbar auf der Infrastruktur von Aspose – verarbeitet große Arbeitsmappen und komplexe Formeln, ohne die eigenen Serverressourcen zu beeinträchtigen.

## So verwenden Sie die API „Tabellenkalkulation in JSON konvertieren“ mit SDKs

### API-Spezifikation: Tabellenkalkulation in JSON konvertieren

Die [API-Spezifikation „Tabellenkalkulation in JSON konvertieren“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) stellt eine öffentlich zugängliche Programmierschnittstelle bereit, um REST-Interaktionen direkt aus einem Webbrowser auszuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung des SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahiert und Ihnen die Konvertierung einer Tabellenkalkulation in JSON mit nur wenigen Codezeilen ermöglicht.  
Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.  
Die folgenden Codebeispiele zeigen, wie mit Aspose.Cells-Webdiensten mithilfe verschiedener SDKs interagiert wird:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}