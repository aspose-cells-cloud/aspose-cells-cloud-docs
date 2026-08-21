---
title: "Aspose.Cells Cloud Excel-Komprimierungs-Web-API – Reduzieren Sie die Dateigröße von Tabellenkalkulationen programmgesteuert"
second_title: "Dokument"
ArticleTitle: "So komprimieren Sie Excel-Dateien – Reduzieren Sie die Größe von Tabellenkalkulationen und optimieren Sie die Leistung"
linktitle: "Tabellenkalkulation komprimieren"
type: docs
url: /compress-spreadsheet/
keywords: "Excel-Komprimierung, Aspose.Cells Cloud, Reduzierung der Tabellengröße, API, Optimierung der Arbeitsmappe"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mit der Aspose.Cells Cloud-API komprimieren können. Holen Sie sich schrittweise Beispiele, Parameter, Authentifizierung und bewährte Verfahren."
weight: 100
---

Komprimieren Sie Excel-Tabellenkalkulationen programmgesteuert und reduzieren Sie die Dateigröße mit der Aspose.Cells Cloud-API. Optimieren Sie die Leistung der Arbeitsmappe, indem Sie ungenutzte Daten entfernen, eingebettete Objekte komprimieren und Formatierungen bereinigen. Diese RESTful API ermöglicht automatisierte Excel-Dateikomprimierungs- und Optimierungsläufe.

## **Tabellenkalkulation komprimieren API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter

| Parametername   | Typ     | Pfad/Abfrage/Zeichenkette/HTTP-Body | Beschreibung                                                                                                                         |
|-----------------|---------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet     | Datei   | FormData                            | **Erforderlich.** Die zu komprimierende Quell-Excel-Arbeitsmappendatei (`.xlsx`, `.xls`, usw.).                                   |
| level           | Integer | Abfrage                             | **Optional.** Komprimierungsintensität (0 = schnellste/niedrigste, 9 = langsamste/höchste). Wenn weggelassen, wird ein ausgewogener Standardwert (5) verwendet. |
| outPath         | String  | Abfrage                             | **Optional.** Zielordnerpfad in Ihrem Cloud-Speicher. Wenn weggelassen, wird die Datei im gleichen Ordner wie die Quell-Arbeitsmappe gespeichert. |
| outStorageName  | String  | Abfrage                             | **Erforderlich.** Bezeichner des konfigurierten Cloud-Speicherdienstes (z. B. `CorporateDrive`).                                 |
| region          | String  | Abfrage                             | **Optional.** Locale-Einstellung (z. B. `de-DE`), die die regionsabhängige Datenverarbeitung beeinflussen kann.                   |
| password        | String  | Abfrage                             | **Optional.** Passwort zur Entschlüsselung einer geschützten Tabellenkalkulation. Leer lassen, wenn die Datei nicht verschlüsselt ist. |

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
|------|-----------------------|------------------------------------------------------------------|
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large     | Hochgeladene Datei überschreitet das Größenlimit.                |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## Wo sollte die API „Tabellenkalkulation komprimieren“ verwendet werden?

- **Automatisierte Berichtsverteilung** – Komprimieren Sie monatliche Finanzaussagen vor dem Versand per E-Mail, um eine erfolgreiche Zustellung sicherzustellen und die Erfahrung des Empfängers zu verbessern.
- **Optimierung hochgeladener Dateien durch Benutzer** – Komprimieren Sie hochgeladene Excel-Dateien im Hintergrund, um Cloud-Speicherplatz zu sparen und die Speicherkosten zu senken.
- **Datenpipelineverarbeitung und Migration** – Komprimieren Sie Zwischendateien im Excel-Format, die während ETL-Prozessen erstellt werden, um die Netzwerkübertragung zu beschleunigen und die Belastung des temporären Speichers zu verringern.

## Warum sollte man die API „Tabellenkalkulation komprimieren“ verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, sodass eine schnelle Entwicklung mit umfassender Dokumentation möglich ist.
- **Geringere Arbeitskosten** – Entfällt der Bedarf an dediziertem Personal zum manuellen Zusammenführen von Dokumenten.
- **Pay-per-Use-Preismodell** – Keine Vorabinvestition; Sie zahlen nur für die tatsächlich getätigten API-Aufrufe.
- **Kein Server-Management erforderlich** – Keine zu wartenden Server, keine Softwareaktualisierungen und keine Kompatibilitätsprobleme.

## Wie verwendet man die API „Tabellenkalkulation komprimieren“ mit SDKs

### Spezifikation der API „Tabellenkalkulation komprimieren“

Die [Spezifikation der API „Tabellenkalkulation komprimieren“](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) stellt eine öffentlich zugängliche Schnittstelle für REST-Interaktionen bereit, sodass direkte API-Aufrufe aus einem Webbrowser möglich sind.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
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

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie detaillierte Low-Level-Details abstrahiert und es Ihnen ermöglicht, eine Tabellenkalkulation mit nur wenigen Codezeilen zu komprimieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs einzusehen.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs auf Aspose.Cells-Webdienste zugreifen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}