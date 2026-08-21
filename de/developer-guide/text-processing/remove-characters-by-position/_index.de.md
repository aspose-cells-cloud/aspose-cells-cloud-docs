---
title: "Aspose.Cells Cloud – Web-API zum Entfernen von Zeichen nach Position – Text aus spezifischen Positionen in Excel löschen"
second_title: "Dokument"
ArticleTitle: "Excel – Positionsbasiertes Zeichenentfernungstool – Text an spezifischen Positionen löschen – Online-Shortcode"
linktitle: "Zeichen nach Position entfernen"
type: docs
url: /remove-characters-by-position/
keywords: "Aspose.Cells Cloud, Zeichen nach Position entfernen, Excel-Textbereinigung, erste N Zeichen entfernen, letzte N Zeichen entfernen, Text vor Marker entfernen, Text nach Marker entfernen, Entfernen zwischen Werten"
description: "Verwenden Sie die Aspose.Cells Cloud Web-API, um Zeichen aus Excel-Zellen basierend auf ihrer Position zu löschen – entfernen Sie die ersten/letzten N Zeichen oder Text vor/nach bestimmten Markern mit hoher Präzision."
weight: 100
---

Entfernen Sie Zeichen aus Excel-Zellen nach Position: entfernen Sie die ersten/letzten N Zeichen oder löschen Sie Text vor/nach bestimmten Markern. Präzise Textbereinigung mit der Aspose.Cells Cloud Web-API.


## **Einführung**: Unerwünschte Zeichen nach Position entfernen

**Positionsmodi**

- `theFirstNCharacters` – entfernen Sie N Zeichen vom Anfang
- `theLastNCharacters` – entfernen Sie N Zeichen vom Ende
- `allCharactersBeforeText` – löschen Sie alles vor dem ersten Vorkommen des angegebenen Teilstrings
- `allCharactersAfterText` – löschen Sie alles nach dem ersten Vorkommen
- `BetweenValues` – entfernen Sie den Teilstring (und optional auch die Trennzeichen selbst) zwischen zwei benutzerdefinierten Werten

**Optionen**

- `caseSensitive` – legt fest, ob Suchvorgänge für `BeforeText`, `AfterText` und `BetweenValues` groß-/kleinschreibungssensitiv sind

## **RemoveCharactersByPosition API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anforderungsparameter der **RemoveCharactersByPosition** API sind

| Parametername           | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                            |
| ----------------------- | ------- | ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet             | Datei   | FormData                           | Die zu verarbeitende Tabellendatei. Unterstützte Formate sind unter anderem XLSX, XLS, ODS, CSV usw.                                                                  |
| Authorization           | String  | Header                             | Bearer-Token zur Authentifizierung (erforderlich).                                                                                                                      |
| theFirstNCharacters     | Integer | Query                              | Anzahl der Zeichen, die vom Anfang des Texts in jeder ausgewählten Zelle entfernt werden (z. B. entfernt `3` die ersten 3 Zeichen).                                   |
| theLastNCharacters      | Integer | Query                              | Anzahl der Zeichen, die vom Ende des Texts in jeder ausgewählten Zelle entfernt werden (z. B. entfernt `2` die letzten 2 Zeichen).                                    |
| allCharactersBeforeText | String  | Query                              | Entfernt alle Zeichen, die vor dem angegebenen Textstring in jeder Zelle stehen. Bei mehrfachen Vorkommen wird nur bis zum ersten Vorkommen entfernt.                  |
| allCharactersAfterText  | String  | Query                              | Entfernt alle Zeichen, die nach dem angegebenen Textstring in jeder Zelle stehen. Bei mehrfachen Vorkommen wird ab dem ersten Vorkommen entfernt.                      |
| worksheet               | String  | Query                              | _(Optional)_ Der Name des Arbeitsblatts, auf das die Zeichenentfernung angewendet werden soll. Falls weggelassen, wird das erste Arbeitsblatt verwendet.               |
| range                   | String  | Query                              | _(Optional)_ Der Zellbereich, auf den die Zeichenentfernung angewendet werden soll (z. B. `"A1:C10"`). Falls weggelassen, wird der Vorgang auf alle belegten Zellen im angegebenen Arbeitsblatt angewendet. |
| outPath                 | String  | Query                              | _(Optional)_ Der Pfad zum Cloud-Speicherordner, in dem die verarbeitete Arbeitsmappe gespeichert wird. Falls weggelassen, wird die Datei im Quellordner gespeichert.   |
| outStorageName          | String  | Query                              | Der Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                                |
| region                  | String  | Query                              | _(Optional)_ Legt das Gebietsschema für die Textverarbeitung fest, insbesondere relevant für sprachspezifische Zeichenpositionen und Kodierung (z. B. `"en-US"`, `"zh-CN"`). |
| password                | String  | Query                              | _(Optional)_ Falls die hochgeladene Tabellendatei passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                         |

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

- **200 OK** – Die Anfrage war erfolgreich, die verarbeitete Datei wird zurückgegeben.
- **400 Bad Request**: Ungültige Aspose.Cells Cloud API-URI.
- **401 Unauthorized**: Ungültiges Zugriffstoken oder ungültige Client-ID und -Geheimnis.
- **404 Not Found**: Die Tabellendatei ist nicht zugänglich.
- **500 Server Error**: Die Tabellendatei ist während des Abrufs von Berechnungsdaten auf einen Fehler gestoßen.

## Wofür sollte die API „Zeichen nach Position entfernen“ verwendet werden?

- **Datenstandardisierung**: Bereinigen von Produktcodes (Entfernen führender Nullen oder Suffixe), Telefonnummern (Entfernen von Ländervorwahlen)
- **Textextraktion**: Extrahieren wichtiger Informationen aus Protokolldateien (Entfernen von Zeitstempeln oder Präfixen)
- **Dateiverarbeitung**: Organisieren von Dateinamen (Entfernen einheitlicher Präfixe oder Datumsuffixe)
- **Datenparsung**: Verarbeiten strukturierter Texte (Extrahieren von Inhalten zwischen Klammern oder spezifischen Markern)
- **Datenbankverwaltung**: Bereinigen importierter Daten (Entfernen fester Header-/Trailerzeichen im festen Format)

## Warum sollten Sie die API „Zeichen nach Position entfernen“ verwenden?

- **Präzise und effizient**: Direkte Positionslöschung eliminiert die Notwendigkeit komplexer regulärer Ausdrücke.
- **Flexibel konfigurierbar**: Fünf Positionsmodi plus eine Option für Groß-/Kleinschreibung abdecken vielfältige Szenarien.
- **Batchverarbeitung**: Reinigen Sie ganze Spalten mit einem einzigen Aufruf und steigern Sie die Effizienz um bis zu 10×.
- **Intelligente Parsung**: Extrahieren Sie problemlos Inhalte zwischen zwei Trennzeichen.
- **Entwicklerfreundlich**: Aspose.Cells Cloud stellt SDKs für mehrere Sprachen zur Verfügung, wodurch die Entwicklung beschleunigt und umfassende Dokumentation bereitgestellt wird. Im Vergleich zur Erstellung eigener Textverarbeitungslogik reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient**: Zeichen können entfernt werden, ohne die Arbeitsmappe vorab hochzuladen – dies spart Speicherplatz und senkt Kosten.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrundeliegenden Details, sodass Sie die Zeichenentfernung nach Position für Zellen mit minimalem Codeaufwand implementieren können.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---