---
title: "Aspose.Cells Cloud Web API – Lokale Excel-Tabellendaten in eine JSON-Datei konvertieren"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie lokale Tabellendaten in einer Tabellenkalkulation in eine JSON-Datei: Schritt-für-Schritt-Anleitung"
linktype: "Convert Table to JSON"
type: docs
url: /de/convert-table-to-json/
keywords: "Excel, API, JSON, Konvertierung, Cloud, Datei, Tabellenkalkulation"
description: "Verwenden Sie die Aspose.Cells Cloud API, um eine lokale Excel-Tabelle in einer einzigen PUT-Anforderung in eine JSON-Datei umzuwandeln. Enthält cURL-Beispiel, Parameter und SDK-Snippets für C#, Java, Python und mehr."
weight: 100
---

Konvertieren Sie lokale Tabellenkalkulations-/Excel-Tabellendaten mit der Aspose.Cells Cloud Web API in eine **JSON**-Datei.

## **Convert Table to JSON API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername      | Typ    | Speicherort | Beschreibung                                                                                           |
| -------------------- | ------ | ----------- | ------------------------------------------------------------------------------------------------------ |
| **Spreadsheet**      | Datei  | FormData    | Die hochzuladende Excel-Datei.                                                                        |
| **worksheet**        | String | Query       | Name des Arbeitsblatts, das die Tabelle enthält.                                                     |
| **tableName**        | String | Query       | Name der zu konvertierenden Tabelle.                                                                  |
| **outPath**          | String | Query       | (Optional) Der Ordnerpfad, in dem die resultierende JSON-Datei gespeichert wird; Standardwert ist **null**. |
| **outStorageName**   | String | Query       | (Optional) Name des Speichers, in dem die Ausgabedatei abgelegt wird.                                |
| **fontsLocation**    | String | Query       | (Optional) Pfad zu benutzerdefinierten Schriftarten, die während der Konvertierung verwendet werden. |
| **region**           | String | Query       | (Optional) Regionale Einstellungen für die Arbeitsmappe.                                             |
| **password**         | String | Query       | (Optional) Passwort zum Öffnen einer geschützten Arbeitsmappe.                                       |

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

| Code | Bedeutung             | Beschreibung                                                             |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.     |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                                    |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                   |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                              |

## **Wofür sollten Sie die Convert Table to JSON API verwenden?**

- **Echtzeit-Dashboards** – Konvertieren Sie Live-Excel-Daten in JSON für Diagrammbibliotheken wie Chart.js oder D3.js.
- **Spreadsheet-as-a-Service** – Stellen Sie Excel-Tabellen als JSON-Endpunkte für andere Mikroservices bereit.
- **Webhook-Payloads** – Wandeln Sie Tabellendaten für Webhook-Benachrichtigungen in JSON um.
- **Schnelles Daten-Prototyping** – Konvertieren Sie bereinigte Excel-Daten schnell in JSON für Python- oder R-Analysen.
- **Machine-Learning-Pipelines** – Bereiten Sie Trainingsdaten aus Geschäfts-Tabellenkalkulationen vor.
- **E-Commerce-Operationen** – Synchronisieren Sie Produktkataloge oder Preislisten über JSON mit Webseiten.
- **Berichterstellungsautomatisierung** – Generieren Sie JSON-Feeds aus Finanzmodellen für automatisierte Berichte.
- **App-Konfiguration** – Verwalten Sie Feature-Flags, Einstellungen oder A/B-Testparameter in Excel → JSON.
- **Mehrsprachige Unterstützung** – Konvertieren Sie Lokalisierungs-Tabellenkalkulationen in JSON für i18n-Bibliotheken.
- **Dynamische Menüs/Navigation** – Speichern Sie Webseiten-Navigationsstrukturen in Excel und bereitstellen Sie sie als JSON.

## Warum sollten Sie die Convert Table to JSON API verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDKs für viele Sprachen, was den Entwicklungsaufwand reduziert und eine umfassende Dokumentation bereitstellt.
- **Kosteneffizient** – Konvertieren Sie Tabellendaten, ohne die Arbeitsmappe zuvor hochzuladen, wodurch Speicherplatz gespart und Kosten gesenkt werden.
- **Moderne Web- und Mobile-Kompatibilität** – JSON ist die native Datensprache des Webs; die API ermöglicht es Ihnen, Live-Tabellendaten direkt in React, Vue, Angular, Mobile-Apps oder Single-Page-Anwendungen einzuspeisen, ohne komplexe Parsing-Vorgänge.
- **Breite Sprachunterstützung** – JSON funktioniert mit praktisch jeder Programmiersprache, Datenbank und Webdienst.
- **Erhalt strukturierter Daten**
  - **Intelligente Strukturerkennung** – Wandelt Tabellendaten automatisch in korrekte JSON-Arrays/Objekte um.
  - **Header-Mapping** – Verwendet die erste Zeile als JSON-Schlüssel für saubere Objektstrukturen.
  - **Datentyp-Erhaltung** – Behält Zahlen, Datumsangaben und Boolesche Werte bei (nicht nur Text).

_Versionsverlauf:_ Der Convert Table to JSON-Endpunkt wurde mit API-Version **v4.0** (2024) eingeführt und ist die aktuelle stabile Version. Ältere v3.x-Endpunkte sind veraltet.

## Wie verwenden Sie die Convert Table to JSON API mit SDKs?

### Convert Table to JSON API-Spezifikation

Die [Convert Table to JSON API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} stellt eine öffentlich zugängliche Programmierschnittstelle bereit, die REST-Interaktionen direkt aus einem Webbrowser ermöglicht.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-codiert)",
  "contentType": "MIME-Type",
  "fileDownloadName": "optionaler Dateiname"
}
```

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs abstractisiert Low-Level-Details, sodass Sie Tabellendaten einer Tabellenkalkulation mit minimalem Code in eine JSON-Datei konvertieren können. Besuchen Sie das offizielle GitHub-Repository für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs auf Aspose.Cells-Webdienste zugreifen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}