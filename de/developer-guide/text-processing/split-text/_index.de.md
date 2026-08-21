---
title: "Split-Text-API – Excel-Zellen in Spalten segmentieren | Aspose.Cells Cloud"
second_title: "Dokument"
ArticleTitle: "Excel-Text-Splitter – Zellinhalte in mehrere Spalten segmentieren | Aspose.Cells Cloud"
linktitle: "Text teilen"
type: docs
url: /de/split-text/
keywords: "Aspose, Cells, Split-Text-API, Excel, Trennzeichen, Textsegmentierung, Cloud-API"
description: "Teilen Sie Excel-Zellentext problemlos in separate Spalten oder Zeilen mithilfe von Aspose.Cells Cloud. Unterstützt benutzerdefinierte Trennzeichen, Masken, Zeilenumbrüche und optionale Beibehaltung der Trennzeichen. Beginnen Sie in Minuten mit curl oder SDKs."
weight: 100
---

Teilen Sie Excel-Zellentext mithilfe benutzerdefinierter Segmentierungsregeln in mehrere Spalten auf. Trennen Sie den Inhalt anhand von Trennzeichen und geben Sie die Ergebnisse in festgelegte Bereiche aus – mithilfe der Aspose.Cells Cloud Web-API zur Textaufteilung.

## **Einführung**: Text teilen

Die Textsegmentierungs-API zerlegt Zellinhalte basierend auf festgelegten Trennzeichen, Mustern oder Zeilenumbrüchen in mehrere Zellen und schreibt die Ergebnisse in einen Zielbereich. Sie unterstützt flexible Aufteilungsmethoden, Richtungsoptionen für die Ausgabe (Spalten oder Zeilen) sowie die Möglichkeit, Trennzeichen beizubehalten – ideal zum Parsen verketteter Daten, CSV-ähnlicher Inhalte oder mehrzeiliger Texte in strukturierte Formate.

- **Zelle anhand eines bestimmten Zeichens teilen** – zerlegen Sie den Zellinhalt in mehrere Zellen, indem Sie beliebige Zeichen als Trennzeichen festlegen (Komma, Leerzeichen, Semikolon usw.).
- **Zellen anhand eines Zeichenfolgenmusters teilen** – trennen Sie Zellen anhand beliebiger Zeichenkombinationen, die Sie angeben.
- **Text anhand einer Maske teilen** – verwenden Sie Platzhalter, um Text anhand eines bestimmten Musters aufzuteilen; dies bietet eine noch flexiblere und leistungsfähigere Methode zur Textaufteilung.
- **Zellinhalte anhand von Zeilenumbrüchen teilen** – erstellen Sie eine übersichtlichere Darstellung, indem Sie an Zeilenumbrüchen trennen.
- **Zellen in Spalten oder Zeilen aufteilen** – wählen Sie aus, ob die Aufteilungsergebnisse in aufeinanderfolgende Spalten oder Zeilen geschrieben werden.
- **Trennzeichen entfernen oder beibehalten** – entscheiden Sie, ob die Trennzeichen entfernt oder am Anfang oder Ende der resultierenden Zellen beibehalten werden.

## **SplitText-API**

**Voraussetzungen**: Um diese API nutzen zu können, benötigen Sie einen gültigen Aspose Cloud-Zugriffstoken, und die zu verarbeitende Arbeitsmappe muss entweder in den Aspose Cloud-Speicher hochgeladen oder direkt in der Anfrage übermittelt werden. Die API unterstützt gängige Tabellenkalkulationsformate wie XLSX, XLS, ODS und CSV.

### Web-API

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anfrageparameter der **splitText**-API sind

| Parametername                  | Typ     | Position | Erforderlich? | Standardwert   | Beschreibung                                                                                                                                         |
| ------------------------------ | ------- | -------- | ------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | Datei   | FormData | Ja            | —              | Die zu verarbeitende Tabellenkalkulationsdatei. Unterstützte Formate umfassen XLSX, XLS, ODS, CSV usw.                                              |
| delimiters                     | String  | Query    | Nein          | —              | Ein oder mehrere Trennzeichen, die zum Aufteilen von Text innerhalb von Zellen verwendet werden (z. B. `","`, `";"`, `Leerzeichen`, `Zeilenumbruch`, `Tab`, `Pipe`, `Benutzerdefiniert`). |
| keepDelimitersInResultingCells | Boolean | Query    | Nein          | false          | Wenn `true`, bleiben die Trennzeichen in den resultierenden aufgeteilten Zellen erhalten.                                                           |
| keepDelimitersPosition         | String  | Query    | Nein          | None           | Position, an der Trennzeichen beibehalten werden sollen, sofern `keepDelimitersInResultingCells` auf `true` steht. Optionen: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| howToSplit                     | String  | Query    | Nein          | SplitToColumns | Methode zur Textsegmentierung. Optionen: `None`, `SplitToColumns`, `SplitToRows`.                                                                   |
| outPositionRange               | String  | Query    | Ja            | —              | Zielbereich, in den die Aufteilungsergebnisse geschrieben werden (z. B. `"D1:F10"`).                                                                 |
| worksheet                      | String  | Query    | Nein          | —              | Name des Arbeitsblatts, auf das die Textaufteilung angewendet wird. Falls weggelassen, wird das erste Arbeitsblatt verwendet.                      |
| range                          | String  | Query    | Nein          | —              | Quellzellenbereich, auf den die Aufteilungsoperation angewendet wird (z. B. `"A1:A10"`). Falls weggelassen, werden alle genutzten Zellen im Arbeitsblatt verarbeitet. |
| outPath                        | String  | Query    | Nein          | —              | Pfad zum Cloud-Speicherordner, in dem die verarbeitete Arbeitsmappe gespeichert wird. Falls weggelassen, wird die Datei im Quellordner gespeichert. |
| outStorageName                 | String  | Query    | Nein          | —              | Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                 |
| region                         | String  | Query    | Nein          | —              | Lokalisierung für die Textsegmentierung, die die Interpretation von Trennzeichen und die Zeichenkodierung beeinflussen kann (z. B. `"de-DE"`, `"ja-JP"`). |
| password                       | String  | Query    | Nein          | —              | Passwort zum Öffnen einer passwortgeschützten Tabellenkalkulation.                                                                                  |

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

- **400 Bad Request** – Ungültige Aspose.Cells Cloud-API-URI oder fehlerhafte Parameter.
- **401 Unauthorized** – Fehlender oder ungültiger Zugriffstoken (oder client-id/secret).
- **404 Not Found** – Die angegebene Tabellenkalkulationsdatei konnte nicht zugegriffen werden.
- **500 Server Error** – Ein interner Verarbeitungsfehler trat bei der Tabellenkalkulation auf.

## Wofür sollte die Split-Text-API verwendet werden?

### **Bereinigung beim Import von CSV- und Textdateien**

Beim Importieren von Daten aus externen Systemen werden Felder häufig in einzelne Zellen verkettet:

- **ERP-/CRM-Datenimporte** – teilen Sie `"Max Mustermann;max@example.com;030-123456"` in separate Spalten für Name, E-Mail und Telefonnummer auf.
- **Datenbank-Exports** – parsen Sie kombinierte Schlüssel wie `"ORD-2024-001|Premium|Express"` in Auftrags-ID, Tarif und Versandart.
- **Protokollanalyse** – zerlegen Sie halbstrukturierte Protokolle wie `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` zur Filterung.

### **Migration alter Systeme**

- Alte Systeme speichern mehrwertige Felder in einzelnen Zellen; teilen Sie diese auf, um neue Datenbankschemata abzubilden.
- Wandeln Sie Flat-File-Exports in normalisierte Excel-Tabellen um, die sofort für Power BI oder Tableau nutzbar sind.

### **Datenbereinigung und -standardisierung**

- **Trennzeichen-Standardisierung** – wandeln Sie gemischte Trennzeichen (`"A,B;C|D"`) mithilfe einer Multitrennzeichen-Aufteilung in ein einheitliches Format um.
- **Leerzeichenbereinigung** – teilen Sie an Leerzeichen, um übermäßige Leerzeichen zwischen Wörtern zu identifizieren und zu entfernen.
- **Finanzdaten** – teilen Sie kombinierte Transaktionscodes wie `"EIN-CHK-3847"` in Transaktionstyp, Quelle und Referenz auf.
- **Medizinische Aufzeichnungen** – parsen Sie Patientendaten wie `"Müller,Maria_F_1985"` in Nachname, Vorname, Geschlecht und Geburtsjahr.

## Warum sollten Sie die Split-Text-API verwenden?

- **Spezifische Zeichen** – teilen Sie an einem beliebigen einzelnen Zeichen (Komma, Semikolon, Tabulator, Leerzeichen).
- **Zeichenfolgenkombinationen** – verwenden Sie mehrzeilige Trennzeichen wie `||`, `->` oder benutzerdefinierte Trenner.
- **Zeilenumbrüche** – parsen Sie mehrzeilige Zellen sofort in separate Zeilen (Adressen, Kommentare, Beschreibungen).
- **Benutzerdefinierte Trennzeichen** – definieren Sie beliebige Zeichenkombinationen als Trennzeichen für proprietäre Datenformate.
- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, die eine schnelle Entwicklung ermöglichen, und wird mit umfassender Dokumentation geliefert. Im Vergleich zum Aufbau eigener Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient** – Sie können doppelte Zeichen entfernen, ohne die Arbeitsmappe zuvor hochzuladen, was Speicherplatz spart und Kosten senkt.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Textaufteilung für Zellen mit minimalem Codeaufwand implementieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs einzusehen.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}