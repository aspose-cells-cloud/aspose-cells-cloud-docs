---
title: "Aspose.Cells Cloud Excel Textsuch-API – Text in Remote-Tabellenblattbereichen suchen"
second_title: "Dokument"
ArticleTitle: "Text in Remote-Excel-Tabellenblättern suchen – Daten in spezifischen Bereichen finden"
linktitle: "Inhalte in Remote-Bereichen durchsuchen"
type: docs
url: /search-content-in-remote-range/
keywords: "Aspose.Cells, Excel-API, Textsuche, Remote-Bereich, Cloud-Tabellenblatt, REST-API, Datenerschließung"
description: "Suchen Sie nach Text, Zahlen oder Formeln in einem bestimmten Bereich einer Excel-Arbeitsmappe, die in Aspose Cloud gespeichert ist."
weight: 100
---

## **Inhalte in Remote-Bereichen suchen**

Suchen Sie programmgesteuert nach bestimmtem Text in beliebigen Bereichen von Excel-Tabellenblättern mithilfe der Aspose.Cells Cloud API. Finden Sie Text, Zahlen oder Formeln in Remote-Dateien, die in der Cloud-Speicherung abgelegt sind. Eine RESTful API für automatisierte Datenerschließung, Inhaltsanalyse und Auditierungsworkflows für Tabellenblätter.


### **Web-API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


**cURL-Beispiel**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### Anforderungsparameter

| Parametername   | Typ     | Path/Query/String/HTTPBody | Beschreibung                                                                                                                                         |
| :-------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String  | Path                       | **Erforderlich**. Der Dateiname (einschließlich Erweiterung) der zu durchsuchenden Excel-Arbeitsmappe, z. B. `customer_data.xlsx`.                |
| worksheet       | String  | Path                       | **Erforderlich**. Der exakte Name des Tabellenblatts innerhalb der Arbeitsmappe, in dem gesucht werden soll, z. B. `Orders_2024`.                 |
| cellArea        | String  | Path                       | **Erforderlich**. Der Ziel-Zellbereich für die Suche, angegeben in A1-Notation (z. B. `B2:H100`). Die Suche ist auf diesen Bereich beschränkt.      |
| searchText      | String  | Query                      | **Erforderlich**. Der spezifische Textstring, die Zahl oder der Teilinhalt, der im definierten Zellbereich gefunden werden soll.                    |
| ignoreCase      | Boolean | Query                      | **Optional**. Wenn auf `true` gesetzt, ignoriert die Suche Groß-/Kleinschreibung (z. B. stimmt „Report“ mit „report“ überein). Standard ist `false` (Groß-/Kleinschreibung beachten). |
| folder          | String  | Query                      | **Optional**. Der Verzeichnispfad im Cloud-Speicher, in dem sich die Arbeitsmappe befindet. Falls weggelassen, wird das Stammverzeichnis verwendet. |
| storageName     | String  | Query                      | **Optional**. Der Bezeichner für eine benutzerdefinierte Cloud-Speicherkonfiguration. Falls nicht angegeben, wird der Standard-Speicher des Kontos verwendet. |
| region          | String  | Query                      | **Optional**. Die Kultur-/Regionseinstellung (z. B. `de-DE`), die die Interpretation regionspezifischer Zeichen oder Formate während der Suche beeinflussen kann. |
| password        | String  | Query                      | **Optional**. Das Passwort zur Entschlüsselung und zum Zugriff auf eine passwortgeschützte Tabellenblattdatei. Weglassen, wenn die Datei nicht verschlüsselt ist. |

### Antwort

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

### Fehlercodes

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API-URI.  
- **401 Unauthorized** – Ungültiges Zugriffstoken, Client-ID oder Client-Secret.  
- **404 Not Found** – Die Tabellenblattdatei ist nicht zugänglich.  
- **500 Server Error** – Eine unerwartete Bedingung verhinderte, dass der Server die Anforderung erfüllen konnte.

## Wann sollte die Suchfunktion „Inhalte im Bereich des Tabellenblatts“ verwendet werden?

- **Großflächige Datenqualitätsprüfung** – Während der Akzeptanzphase des ETL-Prozesses im Data-Warehouse-Szenario suchen Sie nach fehlenden Feldbeschreibungen, undefinierten Abkürzungen oder Platzhaltertexten (z. B. `„TBD“` oder `„NULL“`) in der Datenzuordnungstabelle (`DataDictionary!B2:F1000`), um unvollständige Datendefinitionen zu identifizieren.  
- **Dynamische Berichtsgenerierung und Inhaltsextraktion** – In automatisierten Berichtssystemen intelligent nach aktuellen Datenblöcken suchen und diese extrahieren, die mit spezifischen Kennzeichen (z. B. `„[KPI]“`) gekennzeichnet sind, aus Vorlagen-Tabellenblättern mit gemischten Daten (`Monthly_Metrics!C10:G50`), um den endgültigen Bericht zusammenzustellen.  
- **Vertrags- und Rechtsdokumentenanalyse** – Beim Überprüfen von Tabellenblattanlagen mit vielen Klauseln effizient spezifische Rechtsbegriffe (z. B. `„Haftungsgrenze“`), Parteinamen oder Daten in einem definierten Bereich (`Contract_Terms!A:A`) lokalisieren, um den Überprüfungsprozess zu beschleunigen.

## Warum sollten Sie die Suchfunktion „Inhalte im Bereich des Tabellenblatts“ verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung und umfassende Dokumentation ermöglicht und den Entwicklungsaufwand im Vergleich zur Erstellung eigener Lösungen erheblich reduziert.  
- **Verringerte Personalkosten** – Entfällt die Notwendigkeit für dedizierte Positionen für die Dokumentenkonsolidierung.  
- **Pay-per-use** – Keine Anfangsinvestition; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.  
- **Keine Wartungskosten** – Keine Server zu warten, keine Softwareaktualisierungen und keine Kompatibilitätsprobleme.

## So verwenden Sie die Suchfunktion „Inhalte im Bereich des Tabellenblatts“ mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Suche nach Inhalten in Bereichen von Tabellenblättern mit minimalem Codeaufwand implementieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}