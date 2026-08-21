---
title: "Aspose.Cells Cloud – Erkennen defekter Verknüpfungen im Excel-Bereich (API)"
second_title: "Dokument"
ArticleTitle: "Defekte Verknüpfungen im entfernten Excel-Bereich finden und beheben – Cloud-basierte Prüfung von Tabellenverknüpfungen"
linktype: "Suche defekter Verknüpfungen im entfernten Bereich"
type: docs
url: /search-broken-links-in-remote-range/
keywords: "Aspose, Cells, defekte Verknüpfungen, API, Excel-Bereich, Validierung, Cloud, Tabellenkalkulation, externer Verweis, Prüfprogramm"
description: "Verwenden Sie die Aspose.Cells Cloud API, um einen bestimmten Excel-Bereich auf defekte externe Verknüpfungen, ungültige Formeln oder fehlende Datenquellen zu überprüfen. Sicher, schnell und cloudbasiert."
weight: 100
---

## **Suche defekter Verknüpfungen im entfernten Bereich – API**

Automatische Erkennung defekter Verknüpfungen in Bereichsdaten von Excel-Dateien, die in der Cloud gespeichert sind. Unsere API durchsucht definierte Bereiche auf defekte externe Verweise, ungültige Formeln und fehlende Datenquellen. Unterstützt die remote-Prüfung von Tabellenkalkulationen, automatisierte Qualitätsprüfungen und Integration in Cloud-Speicherdienste. RESTful API für die Automatisierung von Unternehmens-Workflows.


### **Web-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter

| Parametername | Typ   | Speicherort | Beschreibung                                                                                                                                                          |
| -------------- | ------ | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path     | **Erforderlich.** Der Name der Excel-Arbeitsmappe (z. B. `financial_report.xlsx`), die in der Cloud gespeichert ist und auf defekte Verknüpfungen hin untersucht werden soll. |
| worksheet      | String | Path     | **Erforderlich.** Der Name des spezifischen Arbeitsblatts (z. B. `Sheet1`, `Q4_Data`) innerhalb der Arbeitsmappe, in dem nach defekten Verknüpfungen gesucht werden soll. |
| cellArea       | String | Path     | **Erforderlich.** Die Zielbereichsadresse (z. B. `A1:F100`) innerhalb des angegebenen Arbeitsblatts, die auf defekte externe Verweise, Formeln oder Verknüpfungen hin untersucht werden soll. |
| folder         | String | Query    | **Optional.** Der Verzeichnispfad im Cloud-Speicher, in dem sich die Zielarbeitsmappe befindet. Falls nicht angegeben, wird das Stammverzeichnis verwendet.              |
| storageName    | String | Query    | **Optional.** Der Name des konfigurierten Cloud-Speicherdiensts (z. B. `DropboxBusiness`, `S3Bucket`). Falls nicht angegeben, wird der Standard-Speicher des Kontos verwendet. |
| region         | String | Query    | **Optional.** Die Gebietsschemaeinstellung (z. B. `en-GB`, `de-DE`) zur Anwendung bei der regionalsspezifischen Dateninterpretation während der Untersuchung.        |
| password       | String | Query    | **Optional.** Das Entschlüsselungspasswort, das für den Zugriff auf eine passwortgeschützte Arbeitsmappe erforderlich ist. Leer lassen, wenn die Datei nicht verschlüsselt ist. |

**Beispiel für Anforderungstext**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### Antwort

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

Die Auflistung `BrokenLinks` enthält Objekte des Typs **BrokenLink**. Jedes Objekt bietet folgende Eigenschaften:

- **CellName** – Die Zelladresse mit dem defekten Verweis (z. B. `B12`).
- **LinkType** – Der Typ der defekten Verknüpfung (z. B. `ExternalReference`, `Formula`).
- **ErrorMessage** – Eine Beschreibung, warum die Verknüpfung als defekt eingestuft wird.

**Hinweis:** Die API unterliegt Rate-Limits. Details finden Sie auf der Seite [Preise und Rate Limits](https://www.aspose.cloud/pricing).

### Fehlercodes

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API-URI.
- **401 Unauthorized** – Ungültiges Zugriffstoken, Client-ID oder Client-Secret.
- **404 Not Found** – Die Tabellenkalkulationsdatei ist nicht zugänglich.
- **500 Server Error** – Die Tabellenkalkulation stieß beim Abrufen von Berechnungsdaten auf eine Anomalie.

## Wann sollte die Suche nach defekten Verknüpfungen im Bereich der Tabellenkalkulation-API verwendet werden?

- **Regelmäßige Prüfung großer Finanzmodelle** – Vor der Veröffentlichung monatlicher oder quartalsweise Berichte automatisch Schlüsselbereiche mit vielen externen Datenverweisen (z. B. `Dashboard!B5:K50`) prüfen, um sicherzustellen, dass alle Verknüpfungen auf gültige Quelldateien verweisen.
- **Datenintegration bei Fusionen und Übernahmen** – Nach dem Zusammenführen mehrerer Tabellenkalkulationsdateien, die Geschäftsbereiche darstellen, das Arbeitsblatt „Übersicht“ darauf prüfen, ob durch geänderte Dateipfade oder Berechtigungsprobleme Verknüpfungen ungültig geworden sind.
- **Vorbereitung von Investordatenpaketen** – Vor der Fertigstellung von Präsentationsunterlagen mit Diagrammen und Tabellen, die an externe Datenbanken oder Marktdatenquellen gebunden sind, die Gültigkeit aller Verknüpfungen überprüfen.

## Warum sollte die Suche nach defekten Verknüpfungen im Bereich der Tabellenkalkulation-API verwendet werden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen und ermöglicht so eine schnelle Entwicklung mit umfassender Dokumentation. Im Vergleich zur Entwicklung einer individuellen Lösung reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Arbeitskosten** – Entfällt der Bedarf an dediziertem Personal für manuelles Zusammenführen von Dokumenten.
- **Pay-per-Use** – Keine Anfangsinvestition; Sie zahlen nur für tatsächlich getätigte API-Aufrufe.
- **Keine Wartungskosten** – Keine Serverpflege, keine Software-Updates, keine Kompatibilitätsprobleme.
- **Beibehaltung komplexer Excel-Formatierungen** – Ergebnisse können im universell zugänglichen PDF-Format exportiert werden, ohne Formatierungen zu verlieren.

## Wie verwendet man die Suche nach defekten Verknüpfungen im Bereich der Tabellenkalkulation-API mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Methode zur Beschleunigung der Entwicklung. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie „Suche defekter Verknüpfungen in einem Bereich“ mit minimalem Codeaufwand implementieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}