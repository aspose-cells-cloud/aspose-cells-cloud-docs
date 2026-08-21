---
title: "Tabellenkalkulationsinhalt durchsuchen – Aspose.Cells Cloud API (Text in Excel finden)"
second_title: "Dokument"
ArticleTitle: "Text in lokalen Excel-Tabellenkalkulationen suchen – Spezifische Daten finden"
linktitle: "Tabellenkalkulationsinhalt durchsuchen"
type: docs
url: /de/search-spreadsheet-content/
keywords: "Aspose.Cells, Excel-Such-API, Tabellenkalkulationsinhalt durchsuchen, Cloud-Tabellenkalkulations-API, Textsuche"
description: "Verwenden Sie die Aspose.Cells Cloud API, um Text, Zahlen oder Formeln in lokalen Excel-Dateien zu durchsuchen. Unterstützt groß-/kleinschreibungunabhängige Abfragen, worksheetbezogenen Suchbereich und sichere Authentifizierung."
weight: 100
---

## **API zum Durchsuchen von Tabellenkalkulationsinhalten**

Durchsuchen Sie programmgesteuert beliebige Excel-Tabellenkalkulationen nach spezifischem Text mithilfe der Aspose.Cells Cloud API. Die API kann Text, Zahlen oder Formeln in lokal gespeicherten Dateien finden, die in der Cloud abgelegt sind, und ermöglicht so automatisierte Datenerschließung, Inhaltsanalyse sowie Auditierungs-Workflows für Tabellenkalkulationen.


### **Web-API**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

Falls Sie lieber mit rohem HTTP arbeiten möchten, zeigt das folgende cURL-Beispiel dieselbe Anfrage:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Rechnung&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter**

| Parameter    | Typ     | Ort        | Beschreibung                                                                                      |
| ------------ | ------- | ---------- | ------------------------------------------------------------------------------------------------- |
| spreadsheet  | Datei   | FormData   | Die zu durchsuchende Excel-Datei.                                                                |
| searchText   | String  | Abfrage    | Der Text (oder numerische Wert), der in der Arbeitsmappe gesucht werden soll.                    |
| ignoringCase | Boolean | Abfrage    | Auf `true` setzen, um eine groß-/kleinschreibungunabhängige Suche durchzuführen.                 |
| worksheet    | String  | Abfrage    | Name des Arbeitsblatts, auf das die Suche beschränkt werden soll. Falls weggelassen, werden alle Arbeitsblätter durchsucht. |
| cellArea     | String  | Abfrage    | Bereich im A-1-Stil (z. B. `A1:C10`), der den Suchbereich eingrenzt.                             |
| region       | String  | Abfrage    | Geografische Region des Diensts (z. B. `us-east-1`).                                             |
| password     | String  | Abfrage    | Passwort, das zum Öffnen einer geschützten Arbeitsmappe erforderlich ist.                        |


### **Antwort**

Die API gibt ein `SearchResult`-Objekt zurück, das ein Array mit übereinstimmenden Zellen enthält. Jedes Element enthält den Namen des Arbeitsblatts, die Zellenadresse und den übereinstimmenden Text.

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Gesamt",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Gesamt",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### Fehlercodes

- **400 Bad Request** – Die Anforderungs-URI oder -Parameter sind ungültig.
- **401 Unauthorized** – Fehlender oder ungültiger Zugriffstoken oder falsche Client-Anmeldeinformationen.
- **404 Not Found** – Die angegebene Tabellenkalkulation kann nicht zugegriffen werden.
- **500 Internal Server Error** – Beim Verarbeiten der Arbeitsmappe ist ein unerwarteter Serverfehler aufgetreten.

## Wofür sollte die API zum Durchsuchen von Inhalten in Tabellenkalkulationen verwendet werden?

- **Umfassender Prüfung der Arbeitsmappe auf Konformität** – Scannen Sie die gesamte Arbeitsmappe, um sensible Begriffe (z. B. „Vertrauliche Klausel“, „Interne Daten“) für Sicherheits- und Konformitätsprüfungen zu finden.
- **Datenzuordnung über Arbeitsblätter hinweg** – Finden Sie eine Projektnummer oder einen Kundennamen, der auf mehreren Arbeitsblättern vorkommt, um eine schnelle Querintegration zu ermöglichen.
- **Batch-Verifizierung von Vorlageninhalten** – Nach der Erstellung von Berichten überprüfen Sie, ob alle Platzhalter wie `{{Datum}}` in einer Gruppe von Excel-Dateien korrekt ersetzt wurden.
- **Historische Datenarchivierung und -auswertung** – Durchsuchen Sie alte Excel-Dateien nach spezifischen Ereigniscodes oder Geschäftsbedingungen, um Datenarchäologie und Analyse zu beschleunigen.

## Warum sollten Sie die API zum Durchsuchen von Inhalten in Tabellenkalkulationen verwenden?

- **Entwicklerfreundlich** – SDKs sind für viele Sprachen verfügbar und reduzieren den Entwicklungsaufwand im Vergleich zu einem benutzerdefinierten Lösungsansatz.
- **Geringere Arbeitskosten** – Automatisiert Aufgaben, die andernfalls manuelle Überprüfung der Tabellenkalkulationen erfordern würden.
- **Pay-per-Use** – Sie zahlen nur für die API-Aufrufe, die Sie tatsächlich tätigen.
- **Kein Wartungsaufwand** – Keine Server zu verwalten, keine Software-Updates und keine Kompatibilitätsprobleme.
- **Beibehaltung komplexer Formatierungen** – Ergebnisse können als PDF exportiert werden, wobei das ursprüngliche Excel-Layout beibehalten wird.

## Wie Sie mit SDKs nach defekten Links in der API zum Durchsuchen von Inhalten in Tabellenkalkulationen suchen

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Suchfunktion zu integrieren. Das SDK abstrahiert die HTTP-Ebene, sodass Sie die API mit minimalem Codeaufruf verwenden können. Die vollständige Liste der SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie die Operation „Tabellenkalkulationsinhalt durchsuchen“ mit verschiedenen SDKs aufgerufen wird:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}