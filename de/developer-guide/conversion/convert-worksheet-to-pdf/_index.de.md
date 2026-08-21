---
title: "Aspose.Cells Cloud Web API – Konvertieren einer lokalen Excel-Arbeitsmappe in eine PDF-Datei – Kostenlose Online-Tool"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie ein lokales Tabellenkalkulationsblatt in eine PDF-Datei: Schritt-für-Schritt-Anleitung"
linktype: "Konvertieren von Arbeitsblatt in PDF"
type: docs
url: /convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel zu PDF, Arbeitsblatt-Konvertierung, REST API, Cloud-Konvertierung, Tabellenkalkulation PDF, API-Endpunkt, PDF-Erstellung"
description: "Nutzen Sie die Aspose.Cells Cloud API, um ein Arbeitsblatt aus einer lokalen Excel-Datei schnell und sicher in ein PDF-Dokument zu konvertieren."
weight: 100
---

Exportieren Sie ein Arbeitsblatt aus einer lokalen Excel-Datei in eine [PDF](https://docs.fileformat.com/pdf/)-Datei mithilfe der Cloud API.

## **Konvertieren von Arbeitsblatt in PDF – API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                 |
| ----------------- | ------ | ---------------------------------- | ---------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData                           | Laden Sie die Tabellenkalkulationsdatei hoch.                               |
| worksheet         | String | Abfrage                            | Name des Arbeitsblatts in der Tabellenkalkulation.                          |
| outPath           | String | Abfrage                            | (Optional) Der Ordnerpfad zum Speichern der Arbeitsmappe; Standard ist null.|
| outStorageName    | String | Abfrage                            | Der Speichername für die Ausgabedatei.                                      |
| fontsLocation     | String | Abfrage                            | Verwenden Sie benutzerdefinierte Schriftarten für das PDF.                  |
| region            | String | Abfrage                            | Definieren Sie die Regionseinstellung der Tabellenkalkulation.              |
| password          | String | Abfrage                            | Das Passwort zum Öffnen der Tabellenkalkulationsdatei.                      |

### **Antwort**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                            |
| ---- | --------------------- | ----------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.        |
| 400  | Ungültige Anfrage     | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).|
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes JWT-Token.                                    |
| 413  | Anforderung zu groß   | Die hochgeladene Datei überschreitet die Dateigrößenbeschränkung.      |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler.                                              |

## **Wann sollten Sie die Konvertieren-von-Arbeitsblatt-in-PDF-API verwenden?**

- **Finanzaussagen**: Konvertieren Sie Bilanzen, Gewinn-und-Verlust-Rechnungen (spezifische Tabellen) in PDF für prüfungsreife Dokumentationen.
- **Verkaufsberichte**: Wandeln Sie Verkaufs-Dashboards oder Provisionsberechnungen in verteilbare PDFs um.
- **Betriebskennzahlen**: Exportieren Sie KPI-Tabellen und Leistungsmetriken als formelle PDF-Berichte.
- **Vertragsdaten**: Exportieren Sie Preislisten und Service-Level-Vereinbarungen aus Tabellenkalkulationen als PDF-Anhänge.
- **Audit-Protokolle**: Bewahren Sie Finanzarbeitsblätter als unveränderbare PDF-Beweise auf.
- **Portfoliountersuchungen**: Exportieren Sie Anlageperformancetabellen als kundenfertige PDF-Auszüge.
- **Qualitätskontrollberichte**: Exportieren Sie Prüfarbeitsblätter in PDF für Compliance-Aufzeichnungen.
- **Inventarübersichten**: Wandeln Sie Lagerarbeitsblätter in PDF für Management-Reviews um.

## **Warum sollten Sie die Konvertieren-von-Arbeitsblatt-in-PDF-API verwenden?**

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Programmiersprachen an, die eine schnelle Entwicklung ermöglichen, und wird mit umfangreicher Dokumentation geliefert. Im Vergleich zum Aufbau eigener Diagramm-Renderlösungen reduziert dies die Entwicklungsaufwände erheblich.
- **Kosteneffizient**: Sie können Tabellendaten konvertieren, ohne die Arbeitsmappe zuvor hochzuladen, wodurch Speicherplatz gespart und Kosten reduziert werden.
- **Formatbeibehaltung**: Beibehaltung komplexer Excel-Formatierungen im universell lesbaren PDF-Format.

## **Wie verwenden Sie die Konvertieren-von-Arbeitsblatt-in-PDF-API mit SDKs?**

### Spezifikation der Konvertieren-von-Arbeitsblatt-in-PDF-API

Die [Spezifikation der Konvertieren-von-Arbeitsblatt-in-PDF-API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) stellt eine öffentlich zugängliche Programmierschnittstelle bereit und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da dabei die Low-Level-Details abstrahiert werden, sodass Sie Tabellenkalkulationsdaten mit minimalem Code in eine PDF-Datei konvertieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie Aspose.Cells-Webservices mit verschiedenen SDKs aufrufen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}