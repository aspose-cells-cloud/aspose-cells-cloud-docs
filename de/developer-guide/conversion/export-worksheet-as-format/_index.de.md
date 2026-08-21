---
title: "Arbeitsblatt exportieren – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
second_title: "Dokument"
ArticleTitle: "So exportieren Sie ein entferntes Tabellendarstellungs-Blatt in ein anderes Format: Schritt-für-Schritt-Anleitung"
linktitle: "Arbeitsblatt exportieren"
type: docs
url: /de/export-worksheet-as-format/
keywords: "Aspose Cells, Arbeitsblatt exportieren, Cloud-API, PDF, PNG, CSV, Excel-Konvertierung"
description: "Konvertieren Sie ein in Aspose.Cells Cloud gespeichertes Arbeitsblatt mithilfe eines einzigen GET-Aufrufs in PDF, PNG, SVG, CSV oder andere Formate. Enthält Codebeispiele für C#, Java, Python und mehr."
weight: 100
---

Exportieren Sie ein Cloud-Tabellendarstellungs- oder Excel-Arbeitsblatt in eine andere Formatdatei mithilfe der Aspose.Cells Cloud Web-API.

## **API zum Exportieren eines Arbeitsblatts in ein anderes Format**

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anfrageparameter**

| Parametername      | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                         |
| :----------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Pfad                       | (Erforderlich) Der Name der abzurufenden Arbeitsmappe.                                                                                             |
| **worksheet**      | String | Pfad                       | (Erforderlich) Das spezifische Arbeitsblatt, das konvertiert werden soll.                                                                          |
| **format**         | String | Abfrage                    | (Erforderlich) Das gewünschte Ausgabeformat (z. B. `png`, `pdf`, `svg`).                                                                           |
| **folder**         | String | Abfrage                    | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist `null`.                                                       |
| **storageName**    | String | Abfrage                    | (Optional) Der Name des benutzerdefinierten Cloud-Speichers. Bei Weglassung wird der Standardspeicher verwendet.                                  |
| **outPath**        | String | Abfrage                    | (Optional) Der Ausgabeordnerpfad. Standardwert ist `null`.                                                                                         |
| **outStorageName** | String | Abfrage                    | (Optional) Speichername für die Ausgabedatei.                                                                                                      |
| **fontsLocation**  | String | Abfrage                    | (Optional) Gibt benutzerdefinierte Schriftarten an, falls erforderlich.                                                                            |
| **region**         | String | Abfrage                    | (Optional) Regionale/Spracheinstellung der Tabellendarstellung (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| **password**       | String | Abfrage                    | (Optional) Das Passwort zum Zugriff auf die Tabellendarstellungsdatei.                                                                             |

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

| Code | Bedeutung             | Beschreibung                                                    |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## **Wann sollten Sie die API zum Exportieren eines Arbeitsblatts in ein anderes Format verwenden?**

- **Migration veralteter Systeme** – Konvertieren Sie Tausende veralteter XLS-Dateien in XLSX für moderne Systeme.  
- **Archivstandardisierung** – Normalisieren Sie verschiedene Tabellendarstellungsformate (XLS, XLSM, ODS, CSV) in ein einheitliches Format für Archivzwecke.  
- **Interoperabilität mit Office-Suiten** – Konvertieren Sie Excel-Dateien in Formate, die mit LibreOffice, Google Sheets oder Apple Numbers kompatibel sind.  
- **Datenquellennormalisierung** – Konvertieren Sie verschiedene Tabellendarstellungsformate in CSV oder JSON für die Einspeisung in Datenbanken.  
- **Veröffentlichung im Web** – Konvertieren Sie Finanzmodelle in HTML für die Webdarstellung.

## **Warum sollten Sie die API zum Exportieren eines Arbeitsblatts in ein anderes Format verwenden?**

- **Multi-Sprach-SDK-Unterstützung** – Bietet Client-Bibliotheken für verschiedene Programmiersprachen, sodass Entwickler die API direkt aus ihrer bevorzugten Umgebung aufrufen können.  
- **Direkte Konvertierung ohne Zwischenspeicherung** – Ermöglicht die Konvertierung eines in Cloud-Speicher gespeicherten Arbeitsblatts in das angeforderte Format, ohne die Datei herunterladen und erneut hochzuladen.  
- **Daten-only-Extraktion** – Gibt den Arbeitsblatinhalt im gewählten Format zurück, ohne visuelle Formatierungen beizubehalten.

## **Wie verwendet man die API zum Exportieren eines Tabellendarstellungsblatts in ein anderes Format mit SDKs?**

### Spezifikation der API zum Exportieren eines Arbeitsblatts in ein anderes Format

Die [Spezifikation der API zum Exportieren eines Arbeitsblatts in ein anderes Format](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) bietet eine öffentlich zugängliche Programmierschnittstelle, um REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Im folgenden Beispiel wird gezeigt, wie Aufrufe an die Cloud-API mit cURL erfolgen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Details auf niedriger Ebene abstrahiert und es ermöglicht, ein Tabellendarstellungsblatt mit kurzem Code in eine Formatdatei zu exportieren.  
Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs erfolgen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}