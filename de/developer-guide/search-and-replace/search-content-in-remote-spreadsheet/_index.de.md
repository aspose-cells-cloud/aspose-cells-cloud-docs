---
title: "Text in Remote Excel-Tabellenkalkulationen suchen – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "Text in Remote Excel-Tabellenkalkulationen suchen – Spezifische Daten finden"
linktype: "Suchen von Remote-Tabelleninhalten"
type: docs
url: /de/search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, Excel-Such-API, Cloud-Tabellenkalkulation, Textsuche, REST"
description: "Suchen Sie nach Text, Zahlen oder Formeln in Excel-Dateien, die in der Cloud-Speicherung gespeichert sind, mithilfe von Aspose.Cells Cloud. Unterstützt Groß-/Kleinschreibung-unabhängige Abfragen, Ordnerauswahl und passwortgeschützte Arbeitsmappen."
weight: 100
---

### **Inhalte in Remote-Tabellenkalkulation per API durchsuchen**

Suchen Sie programmgesteuert nach spezifischem Text in beliebigen Excel-Tabellenkalkulationen mithilfe der Aspose.Cells Cloud API. Finden Sie Text, Zahlen oder Formeln in Dateien, die in der Cloud-Speicherung abgelegt sind. Diese RESTful API ermöglicht automatisierte Datenerschließungs-, Inhaltsanalyse- und Auditierungsworkflows für Tabellenkalkulationen.

### **Web-API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername    | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                      |
| :--------------- | :------ | :--------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String  | Pfad                               | **Erforderlich**. Der Dateiname der Excel-Arbeitsmappe (einschließlich Erweiterung), in der die Textsuche durchgeführt werden soll, z. B. `verkaufsdaten.xlsx`. |
| searchText       | String  | Abfrage                            | **Erforderlich**. Der exakte String, die Zahl oder Teilinhalt, der/m die in der gesamten Arbeitsmappe oder den Arbeitsblättern gesucht werden soll.           |
| ignoringCase     | Boolean | Abfrage                            | **Optional**. Legt fest, ob die Groß-/Kleinschreibung beachtet wird. Setzen Sie auf `true`, um groß-/kleinschreibungsunabhängig zu suchen (z. B. „Bericht“ findet „BERICHT“); Standard ist `false`. |
| folder           | String  | Abfrage                            | **Optional**. Der Verzeichnispfad innerhalb Ihres Cloud-Speichers, der die Zielarbeitsmappe enthält. Falls weggelassen, wird der Root-Ordner angenommen.        |
| storageName      | String  | Abfrage                            | **Optional**. Der Name-Bezeichner für einen benutzerdefiniert konfigurierten Cloud-Speicherdienst. Falls nicht angegeben, nutzt die API den Standardspeicher des Kontos. |
| region           | String  | Abfrage                            | **Optional**. Die Gebietsschema-Einstellung (z. B. `de-DE`), die während der Suche angewendet wird und die Textnormalisierung oder Sortierregeln beeinflussen kann. |
| password         | String  | Abfrage                            | **Optional**. Das Entschlüsselungspasswort, das für den Zugriff auf eine passwortgeschützte Excel-Datei erforderlich ist. Weglassen, wenn die Datei nicht verschlüsselt ist. |

**Glossar**

- **searchText** – Der exakte Suchstring; kann ein Teilstring sein.
- **ignoringCase** – `true` macht die Suche groß-/kleinschreibungsunabhängig; `false` erzwingt Groß-/Kleinschreibungsbetontung.
- **folder** – Pfad zum Verzeichnis, das die Arbeitsmappe enthält.
- **storageName** – Bezeichner einer benutzerdefinierten Speicherkonfiguration.
- **region** – Gebietsschemacode, der die Regeln für Textvergleiche beeinflusst.
- **password** – Entschlüsselungspasswort für geschützte Arbeitsmappen.

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

Die Antwort enthält eine Liste von Zellen (`CellName`), in denen der gesuchte Text gefunden wurde, zusammen mit dem Namen des Arbeitsblatts und dem passenden Text. Falls keine Übereinstimmungen gefunden werden, ist das Array `TextItems` leer, und die Anforderung gibt den HTTP-Status 200 OK zurück.

### Fehlercodes

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API-URI.  
  ```json
  {"code":400,"message":"Ungültige Anforderungs-URI"}
  ```
- **401 Unauthorized** – Ungültiges Zugriffstoken, Client-ID oder Client-Secret.  
  ```json
  {"code":401,"message":"Ungültiges Zugriffstoken"}
  ```
- **404 Not Found** – Die Tabellenkalkulationsdatei ist nicht zugänglich.  
  ```json
  {"code":404,"message":"Datei nicht gefunden"}
  ```
- **500 Server Error** – Eine unerwartete Bedingung verhinderte die vollständige Ausführung der API-Anforderung.  
  ```json
  {"code":500,"message":"Interner Serverfehler"}
  ```

## Wofür sollte die Suche nach Inhalten in der Tabellenkalkulation-API verwendet werden?

- **Umfassender Compliance-Audit der Arbeitsmappe** – Scannen Sie schnell die gesamte Excel-Datei, um alle sensiblen Begriffe (z. B. „Vertrauliche Klausel“, „Interne Daten“) für Unternehmensdatensicherheits- und Compliance-Prüfungen zu identifizieren.
- **Überblattübergreifende Datenassoziationsabfrage** – Wenn Projektinformationen über mehrere Arbeitsblätter verteilt sind, suchen Sie nach einer bestimmten Projektnummer oder Kundennamen und finden Sie sofort alle zugehörigen Daten.
- **Batch-Überprüfung von Vorlageninhalten** – Nach automatisierter Berichtserstellung scannen Sie mehrere Excel-Dateien in Stapeln, um sicherzustellen, dass alle voreingestellten Platzhalter (wie `{{Date}}`) korrekt ersetzt wurden, und so die Vollständigkeit und Genauigkeit der Berichte zu gewährleisten.
- **Archivierung und Mining historischer Daten** – Analysieren Sie alte Dateien, suchen Sie nach bestimmten Ereigniscodes oder Geschäftsbegriffen und erfassen Sie schnell historische Geschäftslogik für Datenarchäologie.

## Warum sollten Sie die Suche nach Inhalten in der Tabellenkalkulation-API verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen und ermöglicht eine schnelle Entwicklung mit umfassender Dokumentation. Im Vergleich zur Erstellung eigener Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Arbeitskosten** – Automatisiert wiederholte Suchaufgaben und befreit Entwickler von manueller Datenextraktion.
- **Pay-per-Use** – Keine Vorabinvestition; Sie zahlen nur für die tatsächlich genutzten API-Aufrufe.
- **Kein Wartungsaufwand** – Aspose verwaltet Server, Updates und Kompatibilität, sodass Sie sich auf Ihre Anwendungslogik konzentrieren können.
- **Beibehaltung komplexer Excel-Formatierung** – Ergebnisse können im universell lesbaren PDF-Format exportiert werden, wobei die ursprüngliche Formatierung erhalten bleibt.

## So verwenden Sie die Suche nach defekten Links im Bereich der Tabellenkalkulation-API mit SDKs

### OpenAPI-Spezifikation

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung des SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrundeliegenden Details, sodass Sie die Suche nach Inhalten in Tabellenkalkulationen mit minimalem Codeaufwand implementieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---