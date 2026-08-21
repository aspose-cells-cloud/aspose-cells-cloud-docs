---
title: "Suche nach defekten Links in Tabellenkalkulationen – Aspose.Cells Cloud API"
second_title: "Dokumentation"
ArticleTitle: "Defekte Links in Excel finden und beheben – Cloud-basierte Link-Prüfung für Tabellenkalkulationen"
linktitle: "Suche nach defekten Links in Tabellenkalkulationen"
type: docs
url: /de/search-spreadsheet-broken-links/
keywords: "Aspose Cells, defekte Links, Audit von Tabellenkalkulationen, Excel API, Cloud-Tabellenkalkulation, Link-Checker"
description: "Erkennen und Beheben defekter Links in Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud API. Scannen Sie Bereiche, erhalten Sie detaillierte JSON-Ergebnisse und integrieren Sie die API in jede Sprache per SDK."
weight: 100
---

## **API zur Suche nach defekten Links in Tabellenkalkulationen**

Automatische Erkennung defekter Links in Excel-Dateien. Unsere API scannt angegebene Bereiche auf defekte externe Verweise, ungültige Formeln und fehlende Datenquellen. Unterstützt die Remote-Auditierung von Tabellenkalkulationen, automatisierte Qualitätsprüfungen und die Integration mit Cloud-Speicheranbietern. RESTful API für die Automatisierung von Unternehmens-Workflows.

**Zusammenfassung:** Verwenden Sie diesen Endpunkt, um ungültige Links in Arbeitsmappen schnell zu identifizieren und zu reparieren, um die Datenintegrität in Finanzmodellen, M&A-Datensätzen und investorengerechten Präsentationsunterlagen sicherzustellen.

### **Web-API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anfrageparameter

| Parametername | Typ   | Speicherort              | Beschreibung                                                                                                           |
|---------------|-------|--------------------------|------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet   | Datei | FormData (multipart)     | **Erforderlich.** Die zu analysierende Excel-Arbeitsmappe (`.xlsx`, `.xls` usw.).                                   |
| worksheet     | String | Query                    | **Optional.** Der Name des zu analysierenden Arbeitsblatts. Falls weggelassen, wird das erste Arbeitsblatt verwendet.|
| cellArea      | String | Query                    | **Optional.** Ziel-Zellbereich in A1-Notation (z. B. `B2:D10`). Falls nicht angegeben, wird der gesamte genutzte Bereich analysiert. |
| region        | String | Query                    | **Optional.** Gebietsschema-Einstellung (z. B. `de-DE`), die die Interpretation von Datums-, Zahlen- oder Währungsformaten beeinflussen kann. |
| password      | String | Query                    | **Optional.** Passwort für verschlüsselte Arbeitsmappen. Leer lassen, falls die Datei nicht geschützt ist.            |

### Antwort

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "Datei nicht gefunden",
      "Status": "Defekt"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Not Found",
      "Status": "Defekt"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Fehlercodes

| Code | Beschreibung |
|------|--------------|
| **400 Bad Request** | Ungültige Aspose.Cells Cloud API URI. |
| **401 Unauthorized** | Ungültiges Zugriffstoken, Client-ID oder Client-Secret. |
| **404 Not Found** | Die Tabellenkalkulationsdatei ist nicht erreichbar. |
| **429 Too Many Requests** | Rate-Limit überschritten (60 Aufrufe / Minute). |
| **500 Server Error** | Die Tabellenkalkulation ist beim Abruf von Berechnungsdaten auf eine Anomalie gestoßen. |


## Wann sollte die API zur Suche nach defekten Links in Tabellenkalkulationen verwendet werden?

- **Regelmäßige Prüfung großer Finanzmodelle**: Vor der Veröffentlichung monatlicher oder quartalsweiser Berichte automatisch Schlüsselbereiche mit vielen externen Datenverweisen (z. B. `Dashboard!B5:K50`) scannen, um sicherzustellen, dass alle Links auf gültige Quelldateien zeigen.  
- **Datenintegration bei Fusionen und Übernahmen (M&A)**: Nach dem Zusammenführen mehrerer Tabellenkalkulationsdateien, die Geschäftsbereiche repräsentieren, das Arbeitsblatt „Übersicht“ scannen, um Links zu identifizieren, die aufgrund geänderter Dateipfade oder Berechtigungsprobleme ungültig geworden sind.  
- **Vorbereitung von Investordatenpaketen**: Vor der Fertigstellung von Präsentationsunterlagen mit Diagrammen und Tabellen, die auf externe Datenbanken oder Marktdatenquellen verweisen, die Gültigkeit aller Links überprüfen.

## Warum sollte die API zur Suche nach defekten Links in Tabellenkalkulationen verwendet werden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung und umfassende Dokumentation ermöglicht. Im Vergleich zur Erstellung eigener Lösungen wird der Entwicklungsaufwand erheblich reduziert.  
- **Geringere Arbeitskosten** – Entfällt die Notwendigkeit, Mitarbeiter für die manuelle Verifizierung von Dokumentenlinks einzusetzen.  
- **Pay-per-Use** – Keine Anschaffungskosten; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.  
- **Keine Wartungskosten** – Keine Serverpflege, keine Softwareupdates und keine Kompatibilitätsprobleme.  
- **Beibehaltung komplexer Excel-Formatierung** – Ergebnisse werden in einem universell lesbaren JSON-Format zurückgegeben, wobei das ursprüngliche Layout der Arbeitsmappe erhalten bleibt.

## Wie verwendet man die API zur Suche nach defekten Links in Tabellenkalkulationen mit SDKs?

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Funktion zur Suche nach defekten Links mit minimalem Codeaufwand implementieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}