---
title: "Aspose.Cells Cloud Web API – Arbeitsblatt in JSON konvertieren"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie ein Tabellenkalkulationsarbeitsblatt mithilfe der Aspose.Cells Cloud API in JSON"
linktitle: "Arbeitsblatt in JSON konvertieren"
type: docs
url: /de/convert-worksheet-to-json/
keywords: "Aspose.Cells, Arbeitsblatt in JSON, Excel-Konvertierung, Cloud-API, API v4, Datenexport"
description: "Schritt-für-Schritt-Anleitung zur Konvertierung eines Excel-Arbeitsblatts in JSON mithilfe der Aspose.Cells Cloud API, einschließlich Anforderungsparameter, Antwortbehandlung, Fehlercodes und SDK-Beispielen."
weight: 100
---

Der **ConvertWorksheetToJson**-Endpunkt liest eine Tabellenkalkulationsdatei aus dem lokalen Dateisystem, extrahiert das angegebene Arbeitsblatt und gibt dessen Inhalt als JSON-Datei zurück. Die Konvertierung erfolgt vollständig auf den Aspose.Cells Cloud-Servern, sodass kein vorheriger Upload oder Zwischenspeicherung erforderlich ist. Die API unterstützt passwortgeschützte Arbeitsmappen, benutzerdefinierte Schriftartenstandorte und regionale Einstellungen und bietet eine schnelle, cloudbasierte Lösung zum Exportieren von Arbeitsblattdaten in JSON für weitere Verarbeitungsschritte.

## **Convert Worksheet to JSON API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Ort        | Erforderlich/Optional | Beschreibung                                                                                                                                                                             |
| :---------------- | :----- | :--------- | :-------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData   | Erforderlich          | Die zu verarbeitende Excel-Arbeitsmappe. Muss ein unterstütztes Format sein (xls, xlsx, csv usw.). Wird als multipart/form-data übertragen. Beispiel: `Spreadsheet=@C:\Docs\Sample.xlsx`. |
| worksheet         | String | Query      | Erforderlich          | Exakter Name des zu konvertierenden Arbeitsblatts (Groß-/Kleinschreibung beachten). Wird dieses weggelassen oder nicht gefunden, gibt die API einen Fehler zurück. Beispiel: `worksheet=Sheet1`. |
| outPath           | String | Query      | Optional              | Zielordner im konfigurierten Cloud-Speicher, in dem die erzeugte JSON-Datei gespeichert wird. Wenn nicht angegeben, wird die JSON-Datei direkt im Antwortstream zurückgegeben. Beispiel: `outPath=/converted/`. |
| outStorageName    | String | Query      | Optional              | Name des Ziel-Speichers (z. B. „MyStorage“), der den `outPath` enthält. Bei Weglassung wird der Standardspeicher verwendet.                                                             |
| fontsLocation     | String | Query      | Optional              | Serverseitiger Ordner, der benutzerdefinierte Schriftarten für die präzise Wiedergabe von Text im Arbeitsblatt enthält. Beispiel: `fontsLocation=/fonts/custom/`.                       |
| region            | String | Query      | Optional              | Kultur-/Regionsbezeichner, der die Formatierung von Zahlen, Datumsangaben und Währungen in der erzeugten JSON-Datei beeinflusst (z. B. `de-DE`, `fr-FR`).                                |
| password          | String | Query      | Optional              | Passwort zum Öffnen einer verschlüsselten Arbeitsmappe. Wird dieses Feld weggelassen, sofern die Arbeitsmappe nicht passwortgeschützt ist.                                              |

### **Antwort**

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
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wann sollte die Convert Worksheet to JSON API verwendet werden?

- **Web-Dashboards** – Exportieren Sie Arbeitsblattdaten in JSON für clientseitige Diagrammbibliotheken (z. B. Chart.js, D3.js).
- **Datenmigration** – Übertragen Sie veraltete Excel-Daten in NoSQL-Datenbanken oder REST-Dienste, die JSON verarbeiten.
- **Mobile oder Offline-Apps** – Konvertieren Sie Arbeitsblatinhalte serverseitig in JSON und synchronisieren Sie das kompakte Ergebnis mit mobilen Geräten.
- **Reporting-Pipelines** – Führen Sie Arbeitsblattdaten direkt in Analyse-Engines ein, die JSON-Eingaben ohne zusätzliche CSV-Zwischenschritte akzeptieren.

## Warum sollte man die Convert Worksheet to JSON API verwenden?

- **Upload-freier Workflow** – Verarbeiten Sie lokale Dateien in der Cloud, ohne sie zuvor in den Speicher hochzuladen. Dies spart Bandbreite und Speicherkosten.
- **Vollständige Konvertierungsfunktionen** – Unterstützt passwortgeschützte Arbeitsmappen, benutzerdefinierte Schriftarten und regionale Formatierungen für präzise Datenrepräsentation.
- **Schnelle, skalierbare Ausführung** – Nutzt die leistungsstarke Engine von Aspose.Cells in Cloud-Infrastrukturen und verarbeitet große Arbeitsblätter effizient.
- **Vereinfachte Integration** – Ein einziger PUT-Aufruf liefert eine sofort verwendbare JSON-Datei oder speichert sie direkt, was den Codeaufwand in Clientanwendungen reduziert.

## Wie verwendet man die Convert Worksheet to JSON API mit SDKs?

### API-Spezifikation für Convert Worksheet to JSON

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">API-Spezifikation für Convert Worksheet to JSON</a> bietet eine öffentlich zugängliche Programmierschnittstelle, um REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie mit cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-codiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie detaillierte Low-Level-Details abstrahieren und Ihnen die Arbeit mit Tabellenkalkulationen mittels präzisem Code ermöglichen. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.  
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs auf Aspose.Cells-Webdienste zugreifen können:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}