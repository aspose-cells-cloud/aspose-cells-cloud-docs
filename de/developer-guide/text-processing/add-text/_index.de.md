---
title: "Aspose.Cells Cloud Add Text API – Fügt Text zu mehreren Excel-Zellen gleichzeitig hinzu – Einfügen von Präfixen, Suffixen und Bezeichnungen"
second_title: "Dokument"
ArticleTitle: "Massenhafte Texteinbindung für Excel – Fügt Präfixe, Suffixe und benutzerdefinierten Text zu Zellen hinzu – Schritt-für-Schritt-Anleitung"
linktitle: "AddText"
type: docs
url: /de/add-text/
keywords: "Aspose Cells API, Text zu Excel hinzufügen, Massen-Texteinbindung, Präfix-Suffix-Excel, Textersetzung in Tabellenkalkulationen, Excel-Automatisierung, Cloud-Tabellenkalkulations-API"
description: "Fügen Sie mit Aspose.Cells Cloud Präfixe, Suffixe oder benutzerdefinierte Bezeichnungen in viele Excel-Zellen mit einem einzigen Aufruf hinzu. Wählen Sie zwischen Einfügen am Anfang, am Ende, vor oder nach einem bestimmten Text. Unterstützt Bereichs-, Arbeitsblatt- und Leerzellenbehandlung."
weight: 100
---

Fügen Sie Text in mehrere Excel-Zellen mit einem einzigen Vorgang hinzu. Fügen Sie Präfixe, Suffixe, Bezeichnungen oder benutzerdefinierte Zeichen am Anfang, am Ende oder vor/after einem bestimmten Text innerhalb der Zellen mithilfe der Aspose.Cells API ein.

## Übersicht

Einzelner Aufruf für Masseneinfügung von Präfixen, Suffixen oder positionsgesteuerten Zeichenketten in jede Zelle eines Zielbereichs – keine Formeln, keine Hilfsspalten erforderlich.

- Einfügen von benutzerdefiniertem Text an **beliebiger Position** innerhalb jeder Zelle

| Wert             | Beschreibung                                                                 |
| ---------------- | ---------------------------------------------------------------------------- |
| `None`           | Ersetzen des ursprünglichen Inhalts                                          |
| `AtTheBeginning` | Einfügen am Anfang (Präfix)                                                  |
| `AtTheEnd`       | Einfügen am Ende (Suffix)                                                    |
| `BeforeText`     | Einfügen **vor** dem ersten Vorkommen von `selectText`; überspringen, falls nicht gefunden |
| `AfterText`      | Einfügen **nach** dem ersten Vorkommen von `selectText`; überspringen, falls nicht gefunden |

- Vier Positionsmodi: Präfix, Suffix, vor/nach einem Teilstring.
- Leerzellen überspringen, um Unordnung zu vermeiden.
- Die API bearbeitet ausschließlich Werte vom Typ **String**; Zahlen, Boolesche Werte und Formeln werden vorher in Text konvertiert.
- **Leere Zellen**
  - `skipEmptyCells = true` → leere Zellen werden übersprungen.
  - `skipEmptyCells = false` → Text wird in leere Zellen eingefügt (Zelle wird zum Texttyp).

- **Anker nicht gefunden**: Wenn `position = BeforeText | AfterText` und `selectText` **nicht** vorhanden ist, bleibt der Zellwert unverändert.

### **Web-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anforderungsparameter der **AddText**-API lauten

| Parametername | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                     | Erforderlich |
| :------------ | :----- | :--------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- |
| Spreadsheet   | Datei  | FormData                           | Die zu verarbeitende Tabellendatei. Unterstützte Formate umfassen XLSX, XLS, ODS, CSV usw.                                                                     | Ja           |
| text          | String | Abfrage                            | Der Textinhalt, der in die angegebenen Zellen der Tabellendatei eingefügt werden soll.                                                                        | Ja           |
| position      | String | Abfrage                            | Gibt an, wo der Text relativ zum vorhandenen Zellinhalt eingefügt werden soll. Optionen: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`.     | Ja           |
| selectText    | String | Abfrage                            | _(Optional)_ Wenn angegeben, wird der Text nur in Zellen eingefügt, die diesen genauen Teilstring enthalten. Wird in Verbindung mit dem Parameter `position` verwendet. | Nein         |
| skipEmptyCells | Boolean | Abfrage                          | Wenn `true`, werden leere Zellen übersprungen; wenn `false`, wird Text in leere Zellen eingefügt.                                                               | Nein         |
| worksheet     | String | Abfrage                            | _(Optional)_ Der Name des Arbeitsblatts, in das der Text eingefügt werden soll. Wenn weggelassen, gilt der Vorgang standardmäßig für das erste Arbeitsblatt.    | Nein         |
| range         | String | Abfrage                            | _(Optional)_ Der Zellbereich, in den der Text eingefügt werden soll (z. B. `"A1:C10"`). Wenn weggelassen, gilt der Vorgang für alle genutzten Zellen im angegebenen Arbeitsblatt. | Nein         |
| outPath       | String | Abfrage                            | _(Optional)_ Der Ordnerpfad im Cloud-Speicher, in dem die verarbeitete Arbeitsmappe gespeichert wird. Wenn weggelassen, wird die Datei im Quellordner gespeichert. | Nein         |
| outStorageName | String | Abfrage                         | Der Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                        | Nein         |
| region        | String | Abfrage                            | _(Optional)_ Legt die Lokalisierung für die Formatierung von Zahlen, Datumsangaben und Währungen in der Ausgabedatei fest (z. B. `"en-US"`, `"zh-CN"`, `"de-DE"`). | Nein         |
| password      | String | Abfrage                            | _(Optional)_ Falls die hochgeladene Tabellendatei passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                   | Nein         |

**cURL-Beispiel**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Report&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
```

### **Antwort**

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

### Fehlercodes

| Code | Beschreibung |
| ---- | ----------- |
| **400** Bad Request | Ungültige Aspose.Cells Cloud API-URI oder fehlende erforderliche Parameter. |
| **401** Unauthorized | Ungültiges Zugriffstoken oder ungültige Client-ID und -Geheimnis. |
| **404** Not Found | Die Tabellendatei ist nicht zugänglich. |
| **500** Server Error | Bei der Tabellendatei trat beim Abrufen von Berechnungsdaten eine Abweichung auf. |

## Wo sollte die Add Text für Tabellenkalkulation API verwendet werden?

- **Dynamische Berichtsbezeichnung**: Dynamische Titel, Datumsangaben oder Anmerkungen zu automatisch generierten Finanzberichten und Verkaufsberichten hinzufügen.
- **Batch-Dateiwassermarkierung**: Firmenlogos, Vertraulichkeits-Wasserzeichen oder Versionsinformationen zu einer Gruppe von Excel-Dateien hinzufügen.
- **Vorlagen-Datenerfassung**: Automatisches Einfügen von Kundennamen, Beträgen und anderen Texten an festgelegten Positionen in Vertrags- oder Rechnungsvorlagen.
- **Datenklassifizierungsbezeichnung**: Automatisches Hinzufügen von Klassifizierungsbezeichnungen oder Statusbezeichnungen (z. B. „Zur Überprüfung ausstehend“, „Genehmigt“) zu Datenzeilen basierend auf Analyseergebnissen.
- **Datenqualitätsanmerkung**: Anmerkungen für problematische Daten während der Datenbereinigung hinzufügen.
- **Massentextformatierung**: Einheitliches Hinzufügen von Präfixen oder Suffixen zu Produkt- oder Kundenbezeichnungen.

## Warum sollten Sie die Add Text für Tabellenkalkulation API verwenden?

- **Massen-Texteinbindung**: Fügen Sie Text gleichzeitig in Hunderte von Zellen oder Dateien ein und sparen Sie bis zu 95 % der Zeit im Vergleich zur manuellen Arbeit.
- **Präzise Positionssteuerung**: Unterstützt das Einfügen von Text an sechs Positionen präzise, einschließlich am Anfang, am Ende oder vor/nach einem bestimmten Text innerhalb einer Zelle.
- **Intelligente bedingte Handhabung**: Entscheiden Sie, ob Text basierend darauf eingefügt werden soll, ob eine Zelle leer ist oder bestimmten Text enthält.
- **Unterstützung mehrerer Positionsstrategien**:
  - `AtTheBeginning`: Fügt denselben Text vor dem Inhalt aller ausgewählten Zellen ein.
  - `AtTheEnd`: Fügt Text nach dem Inhalt aller ausgewählten Zellen ein.
  - `BeforeText` / `AfterText`: Fügt Text nur vor oder nach Zellen ein, die bestimmten Text enthalten.
  - `None`: Ersetzt den ursprünglichen Inhalt.
- **Präzise Bereichssteuerung**: Ermöglicht die Angabe bestimmter Arbeitsblätter oder Zellbereiche für Vorgänge.
- **Bedingte Überspringoption**: Unterstützt das Überspringen leerer Zellen, um unnötige Texteinblendungen zu vermeiden.
- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, die eine schnelle Entwicklung ermöglichen und umfangreiche Dokumentation bereitstellen. Im Vergleich zum Aufbau eigener Diagramm-Renderlösungen wird die Entwicklungsarbeit erheblich reduziert.
- **Kosteneffizient**: Sie können Text in einer Zelle anhängen, ohne die Arbeitsmappe zuvor hochzuladen, was Speicherplatz spart und Kosten senkt.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie Add Text für Zellen mit minimalem Codeaufwand implementieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---