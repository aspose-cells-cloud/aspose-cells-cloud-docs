---
title: "Aspose.Cells Cloud Web-API – Exportieren entfernter Excel-Arbeitsblätter in andere Formate – Kostenloses Online-Tool"
second_title: "Dokument"
ArticleTitle: "So exportieren Sie das entfernte Tabellenkalkulationsarbeitsblatt in andere Formate: Schritt-für-Schritt-Anleitung"
linktype: "Exportieren Sie Tabellenkalkulation als Format"
type: docs
url: /de/export-spreadsheet-as-format/
keywords: "Aspose.Cells, Tabellenkalkulationskonvertierung, API, Export, PDF, CSV, JSON, XLSX"
description: "Konvertieren Sie Excel-Arbeitsmappen, die in Aspose Cloud gespeichert sind, über einen einzigen REST-Endpunkt in PDF, XLSX, CSV, JSON oder HTML. Erfahren Sie die Anfrage-Syntax, Parameter und sehen Sie SDK-Beispiele in C#, Java, Python und mehr."
weight: 100
---

Exportieren Sie eine Cloud-Tabellenkalkulation (Excel) in ein anderes Dateiformat.

## **Exportieren Sie Tabellenkalkulation als Format-API**

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anfrageparameter:**

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                        |
| :------------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Pfad                        | (Erforderlich) Der Name der abzurufenden Arbeitsmappendatei.                                                                                          |
| format         | String | Abfrage                     | (Erforderlich) Das gewünschte Ausgabeformat (z. B. „Xlsx“, „PDF“, „CSV“).                                                                                 |
| folder         | String | Abfrage                     | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null.                                                                      |
| storageName    | String | Abfrage                     | (Optional) Der Name des Speichers bei Verwendung einer benutzerdefinierten Cloud-Speicherlösung. Verwenden Sie den Standardspeicher, wenn dies weggelassen wird.                                                  |
| outPath        | String | Abfrage                     | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert wird. Standardwert ist null.                                                                 |
| outStorageName | String | Abfrage                     | (Optional) Speichername für die Ausgabedatei.                                                                                                               |
| fontsLocation  | String | Abfrage                     | (Optional) Benutzerdefinierter Speicherort für Schriftarten.                                                                                                                  |
| region         | String | Abfrage                     | (Optional) Regionale/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Nummernformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password       | String | Abfrage                     | (Optional) Das Passwort zum Öffnen der Tabellenkalkulationsdatei.                                                                                          |

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

Die Antwort enthält ein einzelnes Objekt, das den konvertierten Dateistream darstellt.

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).      |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                     |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größe.                                 |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                          |

## Wofür sollten Sie die API zum Exportieren von Tabellenkalkulationen in andere Formate verwenden?

- **Migration veralteter Systeme**: Konvertieren Sie Tausende veralteter XLS-Dateien in XLSX für moderne Systeme.
- **Standardisierung der Archivierung**: Normalisieren Sie verschiedene Tabellenkalkulationsformate (XLS, XLSM, ODS, CSV) auf ein einziges Format für Archivzwecke.
- **Interoperabilität mit Office-Suiten**: Konvertieren Sie Excel-Dateien in Formate, die mit LibreOffice, Google Sheets oder Apple Numbers kompatibel sind.
- **Datenquellen-Standardisierung**: Konvertieren Sie verschiedene Tabellenkalkulationsformate in CSV oder JSON für die Datenbankverarbeitung.
- **Veröffentlichung im Web**: Konvertieren Sie Finanzmodelle in HTML für die Webanzeige.

## Warum sollten Sie die API zum Exportieren von Tabellenkalkulationen in andere Formate verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, was eine schnelle Entwicklung ermöglicht und von umfassender Dokumentation begleitet wird. Im Vergleich zum Aufbau eigener Diagramm-Rendering-Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Personalkosten**: Reduziert die Notwendigkeit, Stellen für die Dokumentenkonsolidierung bereitzustellen.
- **Pay-per-use**: Keine Anfangsinvestition; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Kein serverseitiger Wartungsaufwand**: Keine Notwendigkeit, Server zu warten, Software zu aktualisieren oder Kompatibilitätsprobleme zu lösen.
- **Umfassende Formatunterstützung**: Konvertieren Sie zwischen mehr als 20 Tabellenkalkulationsformaten.
- **Beibehaltung von Datenintegrität und Formatierung**: Behält das ursprüngliche Layout, die Formeln und das Styling während der Konvertierung bei.

## Wie verwenden Sie die API zum Exportieren von Tabellenkalkulationen als Format mit SDKs?

### API-Spezifikation „Exportieren Sie Tabellenkalkulation als Format“

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">API-Spezifikation „Exportieren Sie Tabellenkalkulation als Format“</a> bietet eine öffentlich zugängliche Programmierschnittstelle, um REST-Interaktionen nahtlos durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MeineArbeitsmappe.xlsx/worksheets?format=pdf" \
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

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung, da sie niedrigere Details abstrahiert und es Ihnen ermöglicht, eine Tabellenkalkulation mit wenig Code in eine Datei zu exportieren.  
Bevor Sie die API aufrufen, holen Sie sich ein OAuth 2.0-Zugriffstoken und fügen Sie es in den Header `Authorization: Bearer <token>` ein.

Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie über verschiedene SDKs mit Aspose.Cells-Webdiensten interagieren:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}