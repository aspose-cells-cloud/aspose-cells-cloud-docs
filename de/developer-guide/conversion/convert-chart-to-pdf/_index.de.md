---
title: "Aspose.Cells Cloud API – Excel-Diagramm in PDF konvertieren"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie ein lokales Tabellenkalkulationsdiagramm in eine PDF-Datei: Schritt-für-Schritt-Anleitung"
linktitle: "Diagramm in PDF konvertieren"
type: docs
url: /convert-chart-to-pdf/
keywords: "Aspose Cells, Diagramm, PDF, Excel, Konvertierung, Cloud API"
description: "Exportieren Sie Diagramme aus lokalen Excel-Dateien in das PDF-Format mithilfe der Aspose.Cells Cloud REST API. Unterstützt XLSX- und XLS-Dateien."
weight: 100
---

Exportieren Sie Diagramme aus einer lokalen Excel-Datei in das [PDF](https://docs.fileformat.com/pdf/)-Format mithilfe der Cloud API.

## **Diagramm in PDF konvertieren – Web-API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername      | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                      |
|--------------------|--------|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Spreadsheet        | Datei  | FormData                            | Laden Sie die Tabellenkalkulationsdatei hoch.                                                    |
| worksheet          | String | Abfrage                             | Der Name des Arbeitsblatts, das das Diagramm enthält.                                            |
| chartIndex         | Integer| Abfrage                             | Der Index des zu konvertierenden Diagramms.                                                       |
| outPath            | String | Abfrage                             | (Optional) Der Ordnerpfad, in dem die konvertierte Datei gespeichert wird. Standardwert ist null. |
| outStorageName     | String | Abfrage                             | Name des Speichers für die Ausgabedatei.                                                         |
| fontsLocation      | String | Abfrage                             | Verwenden Sie benutzerdefinierte Schriftarten, falls erforderlich.                               |
| region           | String | Abfrage                             | Die Regionseinstellung der Tabellenkalkulation.                                                  |
| password           | String | Abfrage                             | Das Passwort zum Öffnen der Tabellenkalkulationsdatei.                                           |

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

| Code | Bedeutung               | Beschreibung                                                           |
|------|-------------------------|------------------------------------------------------------------------|
| 200  | OK                      | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.       |
| 400  | Bad Request             | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized            | Ungültiges oder fehlendes JWT-Token.                                  |
| 413  | Payload Too Large       | Die hochgeladene Datei überschreitet die Größenbeschränkung.          |
| 500  | Internal Server Error   | Unerwarteter Serverfehler.                                            |

## Wo sollten Sie die API „Diagramm in PDF konvertieren“ verwenden?

### **1. Geschäftliche Berichterstellung und Automatisierung**

- **Finanzabteilungen**: Monatliche Finanzberichtsdiagramme → PDF-Archivierung  
- **Vertriebsteams**: Leistungstrenddiagramme → PDF-Kundenberichte  
- **Marketing-Analytik**: Kampagnenleistungsdiagramme → PDF-Executive-Briefings  
- **Operationsmanagement**: Produktionsüberwachungsdiagramme → PDF-Conformance-Dokumente  

### **2. Softwareentwicklung und Integration**

- **SaaS-Anwendungen**: Vom Benutzer generierte Diagrammdaten → herunterladbare PDF-Berichte  
- **Unternehmenssysteme**: ERP/CRM-Systemdiagramme → PDF-Prüfungsunterlagen  
- **Mobile Anwendungen**: In-App-Analysediagramme → weitergabe-fähige PDF-Dateien  
- **Webanwendungen**: Dashboard-Diagramme → PDF-Export-Funktionalität  

### **3. Dokumentenverarbeitungs-Workflows**

- **Batchverarbeitung**: Mehrere Excel-Dateidiagramme gleichzeitig in PDF konvertieren  
- **Geplante Aufgaben**: Automatisierte tägliche/wöchentliche Diagrammberichtsgenerierung  
- **Vorlagenbasierte Ausgaben**: Standard-Diagrammformate → PDF-Dokumente  
- **Dokumentenzusammenstellung**: Diagramme mit anderen Inhalten im PDF-Format kombinieren  

### **4. Branchenspezifische Anwendungen**

- **Forschungseinrichtungen**: Experimentelle Datencharts → PDF-Figuren für Forschungsarbeiten  
- **Bildungsbereich**: Bildungsmaterialien-Diagramme → PDF-Kursunterlagen  
- **Beratungsunternehmen**: Analysecharts → PDF-Kundenlieferungen  
- **Fertigung**: Qualitätskontrollcharts → PDF-Prüfberichte  
- **Gesundheitswesen**: Patientendatencharts → PDF-medizinische Aufzeichnungen  
- **Öffentlicher Sektor**: Statistikcharts → PDF-offizielle Veröffentlichungen  

### **5. Inhaltmanagement und Verteilung**

- **Digital Asset Management**: Diagrammarchivierung im standardisierten PDF-Format  
- **Wissensdatenbanken**: Technische Dokumentation mit eingebetteten PDF-Diagrammen  
- **Kundenportale**: Sichere PDF-Berichtszustellung an Stakeholder  
- **Regulatorische Konformität**: Prüfungsbereite PDF-Dokumentenerstellung  

## Warum sollten Sie die API „Diagramm in PDF konvertieren“ verwenden?

- Sie können Diagramme **ohne vorheriges Hochladen der Arbeitsmappe** konvertieren, was Speicherplatz spart und Kosten senkt.  
- Die Entwicklung kann schnell über die vorhandenen Aspose.Cells Cloud SDKs abgeschlossen werden.  
- **Einfache Integration**: REST API mit klarer Dokumentation.  
- **Skalierbare Architektur**: Verarbeitet Workloads von kleinen bis unternehmensweiten Anwendungen.  

## Wie verwenden Sie die API „Diagramm in PDF konvertieren“ mit SDKs?

### API-Spezifikation für „Diagramm in PDF konvertieren“

Die [API-Spezifikation „Diagramm in PDF konvertieren“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen REST-Interaktionen direkt aus einem Webbrowser.

## Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahieren und Ihnen so die Konvertierung eines Diagramms in eine PDF-Datei mit minimalem Code ermöglichen.  
Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}