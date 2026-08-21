---
title: "Aspose.Cells Cloud – Excel-API zur Erkennung defekter Links – Prüfen und Validieren von Verknüpfungen in entfernten Arbeitsblättern"
second_title: "Dokument"
ArticleTitle: "Defekte Links in entfernten Excel-Arbeitsblättern finden und beheben – Cloud-basierte Link-Prüfung für Tabellenkalkulationen"
linktitle: "Suche nach defekten Links in entfernten Arbeitsblättern"
type: docs
url: /de/search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, defekte Links, Excel-API, Cloud-Tabellenkalkulation, Link-Validierung"
description: "Erkennen und Beheben von defekten externen Verknüpfungen in Excel-Arbeitsblättern, die in der Cloud gespeichert sind. Nutzen Sie die Aspose.Cells Cloud-API, um Bereiche zu scannen, Link-Details zurückzugeben und Qualitätsprüfungen zu automatisieren."
weight: 100
---

## **Suche nach defekten Links in entfernten Arbeitsblättern über die API**

Automatisches Erkennen defekter Links in einem Excel-Arbeitsblatt, das in einem Cloud-Speicher abgelegt ist. Unsere API scannt angegebene Bereiche, um defekte externe Verweise, ungültige Formeln und fehlende Datenquellen zu finden. Unterstützt die Überprüfung entfernter Tabellenkalkulationen, automatisierte Qualitätsprüfungen und die Integration mit Cloud-Speicheranbietern. REST-basierte API zur Automatisierung unternehmensweiter Workflows.

### **Web-API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                                                                                      |
| :-------------- | :----- | :---------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String | Pfad                                | **Erforderlich.** Der Dateiname (mit Erweiterung) der Excel-Arbeitsmappe, in der nach defekten Links gesucht werden soll (z. B. `Jahresbericht.xlsx`).                                                                         |
| worksheet       | String | Pfad                                | **Erforderlich.** Der exakte Name des Arbeitsblatts, in dem der Link-Scan durchgeführt werden soll (z. B. `Datenblatt1`).                                                                                                       |
| folder          | String | Abfrage                             | **Optional.** Der Verzeichnispfad innerhalb Ihres Cloud-Speichers, in dem sich die Zielarbeitsmappe befindet. Falls nicht angegeben, wird der Stammordner verwendet.                                                             |
| storageName     | String | Abfrage                             | **Optional.** Der Bezeichner Ihrer benutzerdefinierten Cloud-Speicherkonfiguration. Falls nicht angegeben, wird der Standard-Speicher des Kontos verwendet.                                                                    |
| region          | String | Abfrage                             | **Optional.** Die zu verwendende Gebietsschema-Einstellung während der Suche (z. B. `de-DE`). Dies kann die Interpretation bestimmter Formeln oder regionaler Datumsformate beeinflussen. _Unterstützte Gebietsschema-Codes sind z. B. `en-US`, `fr-FR`, `de-DE`, `es-ES` usw._ |
| password        | String | Abfrage                             | **Optional.** Das Entschlüsselungspasswort für eine passwortgeschützte Tabellenkalkulation. Weglassen, wenn die Datei nicht verschlüsselt ist.                                                                                 |

**Beispiel-cURL-Anfrage**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Jahresbericht.xlsx/worksheets/Datenblatt1/search/broken-links?folder=Berichte&storageName=MeinSpeicher" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Daten\\Quelle.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Quelldatei nicht gefunden"
    }
  ]
}
```

Das Antwortobjekt ist vom Typ **BrokenLinksResponse** und enthält:

- **BrokenLinks** – eine Sammlung von `BrokenLink`-Objekten, wobei jedes Objekt den problematischen Verweis (Adresse, Fehlercode und Meldung) beschreibt.
- **Code** – numerischer Statuscode, der vom Dienst zurückgegeben wird.
- **Status** – textuelle Beschreibung des Ergebnisses.

**Hinweise**: Die API paginiert die Ergebnisse nicht. Pro Anfrage können bis zu 10.000 defekte Links zurückgegeben werden. Das Rate-Limit beträgt 100 Anfragen pro Minute pro Konto.

### Fehlercodes

- **400 Bad Request** – Ungültige Aspose.Cells Cloud-API-URI.
- **401 Unauthorized** – Ungültiges oder fehlendes Zugriffstoken.
- **404 Not Found** – Die Tabellenkalkulationsdatei ist nicht zugänglich.
- **500 Server Error** – Beim Abrufen von Berechnungsdaten ist ein Fehler aufgetreten.

## Wann sollte die Suche nach defekten Links in Arbeitsblättern der Tabellenkalkulation über die API verwendet werden?

- **Regelmäßige Prüfung großer Finanzmodelle**: Vor der Veröffentlichung monatlicher oder quartalsweise Berichte automatisch die wichtigsten Bereiche mit Berechnungen (z. B. `Dashboard!B5:K50`) scannen, in denen viele externe Datenverweise enthalten sind, um sicherzustellen, dass alle Links auf gültige Quelldateien zeigen.
- **Datenintegration bei Fusionen und Übernahmen**: Nach dem Integrationsprozess das Arbeitsblatt „Übersicht“ scannen, um Verknüpfungen zu identifizieren, die aufgrund geänderter Dateipfade oder Berechtigungsprobleme ungültig geworden sind.
- **Vorbereitung von Investordatenpaketen**: Vor der endgültigen Erstellung von Präsentationsunterlagen mit Diagrammen und Tabellen, die mit externen Datenbanken oder Marktdatenquellen verknüpft sind, die Gültigkeit aller Links überprüfen.

## Warum sollte man die Suche nach defekten Links in Arbeitsblättern der Tabellenkalkulation über die API verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Programmiersprachen, was eine schnelle Entwicklung ermöglicht, und comes mit umfassender Dokumentation. Im Vergleich zum Aufbau eigener Lösungen zur Diagrammerstellung wird der Entwicklungsaufwand deutlich reduziert.
- **Reduziert Personalkosten**: Vermeidet den Bedarf an Mitarbeitern, die für manuelle Dokumentenkonsolidierung und Linkprüfung zuständig sind.
- **Pay-per-Use**: Keine Vorabinvestition; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Keine Wartungskosten**: Keine Server zu warten, keine Softwareupdates und keine Kompatibilitätsprobleme zu verwalten.
- **Erhält komplexe Excel-Formatierungen** im universell zugänglichen PDF-Format.

## Wie verwendet man die Suche nach defekten Links in Arbeitsblättern der Tabellenkalkulation über die API mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die effizienteste Methode, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Suche nach defekten Links in Arbeitsblättern mit minimalem Codeaufwand umsetzen können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---