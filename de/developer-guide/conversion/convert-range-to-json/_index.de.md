---
title: "Aspose.Cells Cloud Web-API – Lokale Excel-Bereichsdaten in eine JSON-Datei konvertieren – Kostenloses Online-Tool"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie Bereichsdaten lokaler Tabellendateien in eine JSON-Datei: Schritt-für-Schritt-Anleitung"
linktitle: "Bereich in JSON konvertieren"
type: docs
url: /de/convert-range-to-json/
keywords: "Bereich in JSON konvertieren, Aspose.Cells Cloud, Excel zu JSON, Tabellenkonvertierung, API"
description: "Konvertieren Sie einen bestimmten Bereich aus einer lokalen Excel-Tabellendatei in JSON mithilfe der Aspose.Cells Cloud API."
weight: 100
---

Exportieren Sie Bereichsdaten aus einer lokalen Excel-Datei in eine JSON-Datei mithilfe der Cloud-API.

## **API zum Konvertieren eines Bereichs in JSON**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                 |
| ----------------- | ------ | ---------------------------------- | ---------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData                           | Laden Sie die Tabellendatei hoch.                                            |
| worksheet         | String | Abfrage                            | Name des Arbeitsblatts in der Tabellendatei.                                |
| range             | String | Abfrage                            | Zellbereich zur Konvertierung, z. B. A1:C10.                                 |
| outPath           | String | Abfrage                            | (Optional) Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; Standardwert ist null. |
| outStorageName    | String | Abfrage                            | Name des Ausgabedatenspeichers.                                              |
| fontsLocation     | String | Abfrage                            | Speicherort für benutzerdefinierte Schriftarten für den privaten Gebrauch.  |
| region            | String | Abfrage                            | Regionaleinstellung der Tabellendatei.                                       |
| password          | String | Abfrage                            | Passwort zum Öffnen der Tabellendatei.                                       |

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

| Code | Bedeutung             | Beschreibung                                                             |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.     |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                     |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                   |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                               |

## **Wann sollten Sie die API zum Konvertieren eines Bereichs in JSON verwenden?**

- Echtzeit-Dashboards: Konvertieren Sie Live-Excel-Daten in JSON für Diagrammbibliotheken wie Chart.js oder D3.js.
- Tabellenkalkulation als Dienst: Stellen Sie Excel-Bereiche als JSON-Endpunkte für andere Dienste bereit.
- Webhook-Payloads: Wandeln Sie Tabellendaten in JSON für Webhook-Benachrichtigungen um.
- Schnelles Datenprototyping: Konvertieren Sie bereinigte Excel-Daten schnell in JSON für die Analyse mit Python oder R.
- Machine-Learning-Pipelines: Vorverarbeiten Sie Trainingsdaten aus von Geschäftsabteilungen gepflegten Tabellen.
- E-Commerce-Operationen: Synchronisieren Sie Produktkataloge oder Preislisten über JSON mit Webseiten.
- Berichterstattungsautomatisierung: Generieren Sie JSON-Datenströme aus Finanzmodellen für automatisierte Berichte.
- Anwendungskonfiguration: Verwalten Sie Feature-Flags, Einstellungen oder A/B-Testparameter in Excel → JSON.
- Multilingualer Support: Konvertieren Sie Lokalisierungstabellen in JSON für i18n-Bibliotheken.
- Dynamische Menüs/Navigation: Speichern Sie Webseiten-Navigationsstrukturen in Excel und bereitstellen als JSON.

_Für weitere Konvertierungsoptionen siehe die [Konvertieren von Bereich in CSV](/convert-range-to-csv/) Anleitung._

## Warum sollten Sie die API zum Konvertieren eines Bereichs in JSON verwenden?

- **SDK-Unterstützung**: Aspose.Cells Cloud stellt Bibliotheken für mehrere Programmiersprachen bereit, wodurch der Aufwand für benutzerdefinierten Code verringert wird.
- **Geringere Speicherkosten**: Der Bereich kann konvertiert werden, ohne zuerst die gesamte Arbeitsmappe hochzuladen, wodurch Speicherplatz gespart wird.
- **Kompatibilität mit Web- und Mobile-Apps**: JSON ist das native Datenformat moderner JavaScript-Frameworks wie React, Vue und Angular.
- **Breite Sprachunterstützung**: praktisch jede Programmiersprache und Datenbank kann JSON verarbeiten.
- **Erhalt strukturierter Daten**
  - **Intelligente Strukturerkennung**: Wandelt tabellarische Daten automatisch in geeignete JSON-Arrays oder -Objekte um.
  - **Header-Zuordnung**: Verwendet die erste Zeile als JSON-Schlüssel für saubere Objektstrukturen.
  - **Datentyp-Erhaltung**: Behält Zahlen-, Datums- und Boolean-Typen bei statt in reinen Text umzuwandeln.

## Wie verwenden Sie die API zum Konvertieren eines Bereichs in JSON mit SDKs?

### API-Spezifikation zum Konvertieren eines Bereichs in JSON

Die [API-Spezifikation zum Konvertieren eines Bereichs in JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da dabei detaillierte Low-Level-Details abstrahiert werden, sodass Sie mit wenig Code einen Datenbereich in eine JSON-Datei konvertieren können.  
Schauen Sie sich das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}

---