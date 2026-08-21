---
title: "Aspose.Cells Cloud Remove Characters Web API – Löschen benutzerdefinierter Zeichen & Teilzeichenfolgen aus Excel (Online Short‑Code)"
second_title: "Dokument"
ArticleTitle: "Excel Text Cleaner – Zeichen & Teilzeichenfolgen aus ausgewähltem Bereich entfernen"
linktype: "docs"
url: /de/remove-characters/
keywords: "Aspose.Cells, Zeichen entfernen, Excel API, Textbereinigung, Tabellenkalkulation"
description: "Entfernen Sie benutzerdefinierte Zeichen, Zeichensätze und Teilzeichenfolgen aus Excel-Zellen im ausgewählten Bereich. Löschen Sie Text an spezifischen Positionen mithilfe der Aspose.Cells API für präzise Datenbereinigung."
weight: 100
---

Bereinigen Sie Excel-Daten durch Entfernen benutzerdefinierter Zeichen, Zeichensätze oder Teilzeichenfolgen aus einem ausgewählten Zellbereich. Entfernen Sie Text an spezifischen Positionen mit der Aspose.Cells API für genaue Datenformatierung.

## Einführung

Bereinigen und standardisieren Sie Ihre Excel-Daten mühelos durch Entfernen spezifischer, unerwünschter Zeichen. Unser Add-in bietet mehrere zielgerichtete Methoden zur Bereinigung Ihrer Zellen:

- **Benutzerdefinierte Zeichen entfernen**  
  Löschen Sie alle spezifischen Symbole, die Sie definieren. Geben Sie einfach jedes Zeichen in das Feld ein, und das Add-in entfernt sofort alle Vorkommen aus den ausgewählten Zellen. Ideal zum Entfernen eindeutiger Trennzeichen, Tippfehler oder Sonderzeichen.

- **Zeichensätze entfernen (Bulk-Bereinigung)**
  - **Nicht druckbare Zeichen** – Bereinigen Sie Ihre Daten von unsichtbaren Zeichen, die Analysen und Formatierungen stören (Zeilenumbrüche, Wagenrückläufe, Tabulatoren und andere Steuerzeichen wie ASCII 0‑31, 127, 129, 141, 143, 144, 157).
  - **Textzeichen (alle Buchstaben)** – Isolieren Sie Zahlen und Symbole, indem Sie alle Buchstaben (A‑Z, a‑z) aus dem ausgewählten Bereich entfernen.
  - **Numerische Zeichen (alle Ziffern)** – Extrahieren Sie reinen Text, indem Sie alle Ziffern (0‑9) entfernen; ideal zur Bereinigung von Produktbezeichnungen oder Textbeschreibungen.
  - **Symbole** – Entfernen Sie eine Vielzahl symbolischer Störelemente, darunter mathematische (z. B. ±, √), geometrische (z. B. ∆, °), technische, Währungszeichen (z. B. £, ¢) und buchstabenähnliche Symbole (z. B. ™, ®, ©).
  - **Satzzeichen** – Erzeugen Sie sauberen, satzzeichenfreien Text durch Entfernen aller Satzzeichen wie Punkte, Kommas, Anführungszeichen und Bindestriche.

- **Spezifische Teilzeichenfolge entfernen**  
  Gehen Sie über einzelne Zeichen hinaus und entfernen Sie ganze Wörter oder spezifische Zeichenfolgen. Entfernen Sie mühelos gängige Präfixe, Suffixe oder überflüssige Textphrasen aus Ihren Datensätzen.

**Version 4.0 – Aktualisiert am 2024‑11‑15**

## RemoveCharacters API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter

| Parametername       | Typ    | Speicherort              | Beschreibung                                                                                                                                                                                                                      |
| ------------------- | ------ | ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet         | File   | FormData                 | Die zu verarbeitende Tabellendatei. Unterstützte Formate sind unter anderem XLSX, XLS, ODS, CSV usw.                                                                                                                             |
| removeTextMethod    | String | Query                    | Gibt die Textentfernungs-Methode an. Optionen: `None`, `RemoveCustomCharacter`, `RemoveCharacterSets`, `RemoveSubString`. Standardwert ist `None`.                                                                             |
| characterSets       | String | Query                    | Vordefinierte Zeichensätze zum Entfernen, wenn `RemoveCharacterSets` ausgewählt ist. Optionen: `NonPrintingCharacters`, `TextCharacters`, `NumericCharacters`, `Symbols`, `PunctuationMarks`. Mehrere Sets können durch Kommas kombiniert werden. |
| removeCustomValue   | String | Query                    | Benutzerdefinierte Zeichen oder Teilzeichenfolgen zum Entfernen bei Verwendung von `RemoveCustomCharacter` oder `RemoveSubString`.                                                                                           |
| worksheet           | String | Query _(optional)_       | Der Name des Arbeitsblatts, auf dem die Textentfernung angewendet wird. **Bei Weglassung wird das erste Arbeitsblatt der Arbeitsmappe verarbeitet.**                                                                            |
| range               | String | Query _(optional)_       | Der Zellbereich, auf dem die Textentfernung angewendet wird (z. B. `"A1:C10"`). **Bei Weglassung wird die Operation auf alle genutzten Zellen im angegebenen Arbeitsblatt angewendet.**                                         |
| outPath             | String | Query _(optional)_       | Cloud-Speicherordnerpfad, in dem die verarbeitete Arbeitsmappe gespeichert wird. Bei Weglassung wird die Datei im Quellordner gespeichert.                                                                                     |
| outStorageName      | String | Query _(optional)_       | Der Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                                                                                         |
| region              | String | Query _(optional)_       | Legt die Locale für Zeichensatzdefinitionen fest (z. B. `"de-DE"`, `"en-US"`, `"ja-JP"`).                                                                                                                                         |
| password            | String | Query _(optional)_       | Passwort für eine geschützte Arbeitsmappe, sofern erforderlich.                                                                                                                                                                 |

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

### Fehlercodes

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Ungültiges Zugriffstoken oder falsche Client-ID und -Geheimnis.
- **404 Not Found** – Die Tabellendatei ist nicht zugänglich.
- **500 Server Error** – Die Tabellendatei hat bei der Ermittlung von Berechnungsdaten eine Anomalie aufgewiesen.

## Wo sollten Sie die Remove Characters API verwenden?

- **Datenimport/-export** – Bereinigen Sie importierte CSV-/Daten durch Entfernen unsichtbarer Zeichen und Formatierungsfehlern.
- **Datenbankverwaltung** – Standardisieren Sie Produktnummern, IDs und Namen durch Entfernen unerwünschter Symbole oder Satzzeichen.
- **Finanzanalyse** – Extrahieren Sie reine Zahlen durch Entfernen von Währungssymbolen und Textzeichen.
- **Textverarbeitung** – Entfernen Sie Zeilenumbrüche und Tabulatoren für saubere Textanalyse und Berichterstellung.
- **Inventarverwaltung** – Bereinigen Sie Produktbezeichnungen durch Entfernen überflüssiger Präfixe oder Suffixe.

## Warum die Remove Characters API verwenden?

- **Zeit sparen** – Entfernen Sie sofort in Massen mehrere Zeichentypen im Vergleich zur manuellen Bereinigung.
- **Genauigkeit gewährleisten** – Beseitigen Sie verborgene Zeichen, die Analysedefekte und Formatierungsprobleme verursachen.
- **Daten standardisieren** – Erzielen Sie konsistente Formatierungen über Datensätze und Systeme hinweg.
- **Analyse verbessern** – Erhalten Sie saubere, analysenbereite Daten durch Isolierung von Zahlen oder Text nach Bedarf.
- **Importfehler beheben** – Entfernen Sie problematische Zeichen, die Datenbanken und Formeln stören.
- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen und ermöglicht eine schnelle Entwicklung mit umfassender Dokumentation. Im Vergleich zum Aufbau eigener Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffektiv** – Entfernen Sie Zeichen, ohne die Arbeitsmappe zuvor hochzuladen, wodurch Speicherplatz gespart und Kosten gesenkt werden.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie **Remove Characters** für Zellen mit minimalem Codeaufwand implementieren können. Ein vollständiges Listing der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}