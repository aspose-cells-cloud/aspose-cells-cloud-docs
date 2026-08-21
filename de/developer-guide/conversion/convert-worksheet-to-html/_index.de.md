---
title: "Aspose.Cells Cloud Web API – Arbeitsblatt in HTML konvertieren"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie ein Arbeitsblatt mit der Aspose.Cells Cloud API in HTML"
linktype: "Convert Worksheet To Html"
type: docs
url: /convert-worksheet-to-html/
description: "Erfahren Sie, wie Sie ein Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API in HTML konvertieren – ohne Upload, mit benutzerdefinierten Schriftarten, Regionsunterstützung und Fehlerbehandlung."
keywords: "Aspose.Cells, Excel zu HTML, Arbeitsblattkonvertierung, Cloud-API"
weight: 100
---

Der Endpunkt **ConvertWorksheetToHtml** liest eine Excel-Arbeitsmappe aus dem lokalen Dateisystem, extrahiert das angegebene Arbeitsblatt und gibt den Inhalt als HTML-Datei zurück. Die Konvertierung erfolgt vollständig auf den Cloud-Servern von Aspose, sodass kein Zwischen-Upload oder Speicherung erforderlich ist. Ideal zur Erstellung webfähiger Ansichten von Tabellendaten unterstützt die API optionale Ausgabepfade, benutzerdefinierte Schriftarten, Regions-Einstellungen und passwortgeschützte Arbeitsmappen.

## Konvertieren eines Arbeitsblatts in HTML über die API

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Ort      | Erforderlich/Optional | Beschreibung                                                                                                                                                                                              |
| :------------ | :----- | :------- | :------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | Datei  | Erforderlich | FormData             | Binäre Excel-Datei, die verarbeitet werden soll. Muss eine gültige .xlsx-, .xls-, .xlsb-Datei usw. sein. Beispiel: `myWorkbook.xlsx`. Die Excel-Datei wird direkt aus dem Anforderungstext gelesen; kein vorheriger Upload in den Cloud-Speicher erforderlich. |
| worksheet     | String | Erforderlich | Query                | Name des zu konvertierenden Arbeitsblatts (Groß-/Kleinschreibung beachten). Muss in der bereitgestellten Arbeitsmappe vorhanden sein. Beispiel: `Sheet1`.                                                 |
| outPath       | String | Optional     | Query                | Zielordnerpfad (im Cloud-Speicher), in dem die generierte HTML-Datei gespeichert wird. Falls weggelassen, wird die Datei direkt in der Antwort zurückgegeben. Beispiel: `/output/html/`.                    |
| outStorageName| String | Optional     | Query                | Name des zu verwendenden Cloud-Speicherdienstes für `outPath`. Erforderlich, wenn `outPath` auf einen nicht Standard-Speicher verweist.                                                                    |
| fontsLocation | String | Optional     | Query                | Absoluter Pfad zu einem Ordner mit benutzerdefinierten TrueType/OpenType-Schriftarten, die während der Konvertierung verwendet werden sollen. Ermöglicht die korrekte Darstellung nicht-standardmäßiger Zeichen. |
| region        | String | Optional     | Query                | Gebietsschema-Bezeichner, der die Formatierung von Zahlen/Daten beeinflusst (z. B. `de-DE`, `fr-FR`). Standardmäßig wird die interne Regions-Einstellung der Arbeitsmappe verwendet.                       |
| password      | String | Optional     | Query                | Passwort zum Öffnen einer geschützten Arbeitsmappe. Weglassen bei ungeschützten Dateien.                                                                                                                  |

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
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Hochgeladene Datei überschreitet die Größeinschränkung.         |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wofür sollte die Convert worksheet to HTML API verwendet werden?

- **Eingebettete Live-Tabellendaten in einem Web-Portal** – Konvertieren Sie ein Finanzberichtsarbeitsblatt in HTML, um es direkt im Browser anzuzeigen, ohne Excel-Plugins zu benötigen.
- **Druckfähige HTML-Rechnungen aus einer Excel-Vorlage generieren** – Automatisieren Sie die Erstellung webfähiger Rechnungsseiten aus einem vordefinierten Arbeitsblatt.
- **Dokumentationsausschnitte erstellen** – Konvertieren Sie Design-Spezifikationsblätter in HTML-Fragmente, die in technischen Handbüchern oder Wikis eingefügt werden können.
- **Low-Code-BI-Dashboards entwickeln** – Holen Sie sich Arbeitsblattdaten, konvertieren Sie sie in HTML und stellen Sie sie in benutzerdefinierten Dashboard-Widgets dar.

## Warum sollte man die Convert worksheet to HTML API verwenden?

- **Zero-Upload-Workflow** – Konvertieren Sie lokale Dateien direkt in der Cloud, sodass große Arbeitsmappen nicht erst in den Speicher übertragen werden müssen.
- **Hochleistungs-Rendern** – Die serverseitige Konvertierung nutzt die optimierte Engine von Aspose und liefert schnelle und präzise HTML-Ausgaben.
- **Vollständige Kontrolle über die Ausgabe** – Optionale Parameter (benutzerdefinierte Schriftarten, Region, Passwort) ermöglichen es Ihnen, das HTML an lokale Anforderungen und Branding-Vorgaben anzupassen.
- **Nahtlose Integration** – Eine einfache PUT-Anforderung mit multipart/form‑data passt natürlicherweise in CI/CD-Pipelines, Microservices oder serverlose Funktionen.

## Wie Sie die Convert worksheet to HTML API mit SDKs verwenden

### API-Spezifikation für „Convert worksheet to HTML“

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">API-Spezifikation für „Convert Worksheet to HTML“</a> stellt eine öffentlich zugängliche Programmierschnittstelle für die direkte Ausführung von REST-Interaktionen aus einem Webbrowser bereit.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Low-Level-Details abstrahieren und Ihnen ermöglichen, Arbeitsblätter mit knapper, übersichtlicher Code zu verschmelzen.  
Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud SDK GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.  
Die folgenden Codebeispiele zeigen, wie Sie mit Aspose.Cells-Webdiensten über verschiedene SDKs interagieren:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}