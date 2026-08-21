---
title: "Aspose.Cells Cloud – Excel API zur Erkennung defekter Verknüpfungen – Scan & Validierung von Tabellenverknüpfungen in entfernten Arbeitsmappen"
second_title: "Dokumentation"
ArticleTitle: "Defekte Verknüpfungen in entfernten Excel-Dateien finden und beheben – Cloud-basierte Verknüpfungsprüfung für Tabellenkalkulationen"
linktitle: "Suche nach defekten Verknüpfungen in entfernten Tabellenkalkulationen"
type: docs
url: /de/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, defekte Verknüpfungen, API, Cloud, Tabellenkalkulation, Validierung, Aspose.Cells"
description: "Nutzen Sie die Aspose.Cells Cloud API, um entfernte Excel-Arbeitsmappen auf defekte externe Verknüpfungen, ungültige Formeln und fehlende Datenquellen zu überprüfen."
weight: 100
---

## **Suche nach defekten Verknüpfungen in entfernten Tabellenkalkulationen per API**

Erkennen Sie automatisch defekte Verknüpfungen in Excel-Dateien, die in einer Cloud-Speicherlösung gespeichert sind. Unsere API prüft angegebene Zellbereiche auf defekte externe Verweise, ungültige Formeln und fehlende Datenquellen. Sie unterstützt die Remote-Auditing-Funktion für Tabellenkalkulationen, automatisierte Qualitätsprüfungen sowie die Integration mit Cloud-Speicheranbietern. Nutzen Sie die RESTful API, um unternehmensübergreifende Workflows zu automatisieren.

### **Web-API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anfrageparameter:**

| Parametername | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                             |
| :------------ | :----- | :----------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | Pfad                           | **Erforderlich.** Der Name der zu prüfenden Excel-Arbeitsmappendatei auf defekte Verknüpfungen (z. B. `Quarterly_Report.xlsx`).                         |
| worksheet     | String | Abfrage                        | **Erforderlich.** Der Name des Arbeitsblatts, in dem die Suche durchgeführt werden soll. Geben Sie den genauen Blattnamen wie in der Arbeitsmappe angezeigt an. |
| cellArea      | String | Abfrage                        | **Erforderlich.** Der Zellbereich, der auf defekte Verknüpfungen geprüft werden soll, in A1-Notation (z. B. `C5:J50`). Die API durchsucht nur diesen Bereich. |
| folder        | String | Abfrage                        | **Optional.** Der Pfad zum Verzeichnis mit der Arbeitsmappe in Ihrem Cloud-Speicher. Falls weggelassen, wird das Stammverzeichnis angenommen.             |
| storageName   | String | Abfrage                        | **Optional.** Der Name Ihrer benutzerdefinierten Cloud-Speicherkonfiguration. Falls weggelassen, wird die Standard-Speicherkonfiguration verwendet.    |
| region        | String | Abfrage                        | **Optional.** Gebietsschemaeinstellung, die während der Verarbeitung angewendet wird (z. B. `de-DE`). Kann die Interpretation regionspezifischer Formelsyntax oder -verweise beeinflussen. |
| password      | String | Abfrage                        | **Optional.** Passwort zum Öffnen einer verschlüsselten Tabellenkalkulation. Weglassen, falls die Datei nicht passwortgeschützt ist.                  |

**Beispiel-cURL-Anfrage**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Antwort**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**Beispiel-JSON-Antwort**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "Datei nicht gefunden"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "Externer Verweis im Cloud-Modus nicht unterstützt"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Fehlercodes

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API-URI.  
- **401 Unauthorized** – Ungültiges Zugriffstoken, Client-ID oder Client-Geheimnis.  
- **404 Not Found** – Die Tabellenkalkulationsdatei ist nicht zugänglich.  
- **500 Server Error** – Beim Abrufen von Berechnungsdaten ist ein Fehler aufgetreten.

## Wofür sollte die Suche nach defekten Verknüpfungen in der Tabellenkalkulations-API verwendet werden?

- **Regelmäßige Prüfung großer Finanzmodelle** – Scannen Sie vor der Veröffentlichung monatlicher oder quartalsweise Berichte die wichtigsten Bereiche für Berechnungen (z. B. `Dashboard!B5:K50`), die viele externe Datenverweise enthalten, um sicherzustellen, dass alle Verknüpfungen auf gültige Quelldateien verweisen.  
- **Datenintegration bei Fusionen und Übernahmen** – Scannen Sie nach der Integration mehrerer Tabellenkalkulationen, die Geschäftsabteilungen repräsentieren, das Arbeitsblatt „Übersicht“, um Verknüpfungen zu identifizieren, die aufgrund geänderter Dateipfade oder Berechtigungsprobleme ungültig geworden sind.  
- **Vorbereitung von Investorendatenpaketen** – Überprüfen Sie vor der Fertigstellung von Präsentationsunterlagen, die Diagramme und Tabellen mit externen Datenbanken oder Marktdatenquellen enthalten, die Gültigkeit aller Verknüpfungen.

## Warum sollte man die Suche nach defekten Verknüpfungen in der Tabellenkalkulations-API verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, sodass eine schnelle Entwicklung mit umfassender Dokumentation möglich ist. Im Vergleich zum Aufbau einer benutzerdefinierten Lösung wird der Entwicklungsaufwand deutlich reduziert.  
- **Geringere Personalkosten** – Automatisiert die Verknüpfungsvalidierung und eliminiert die Notwendigkeit, dass Mitarbeiter Dokumente manuell konsolidieren müssen.  
- **Pay-per-Use** – Keine Vorab-Investition; Sie zahlen nur für die tatsächlich genutzten API-Aufrufe.  
- **Keine Wartungskosten** – Keine Server zu warten, keine Software-Updates und keine Kompatibilitätsprobleme.

## Wie verwendet man die Suche nach defekten Verknüpfungen in der Tabellenkalkulations-API mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist der effizienteste Weg, um die Entwicklung zu beschleunigen. Das SDK abstrahiert die zugrunde liegenden HTTP-Details, sodass Sie die Erkennung defekter Verknüpfungen mit minimalem Codeaufwand implementieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs auf Aspose.Cells-Webservices zugreifen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}