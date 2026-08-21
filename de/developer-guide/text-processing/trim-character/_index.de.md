---
title: "Aspose.Cells Cloud Text-Trimming-Web-API – Entfernen von zusätzlichen Leerzeichen und Zeilenumbrüchen"
second_title: "Dokument"
ArticleTitle: "Excel-Datenreiniger – Zeichen, Leerzeichen und Zeilenumbrüche automatisch trimmen – Online, Shortcode"
linktype: "Trim-Zeichen"
type: docs
url: /de/trim-character/
keywords: "Excel, Texttrimming, Leerzeichen entfernen, Zeilenumbrüche, Aspose.Cells, Datenbereinigung, Tabellenkalkulation, Zellformatierung normalisieren"
description: "Entfernen Sie zusätzliche Leerzeichen, Zeilenumbrüche und unerwünschte Zeichen aus Excel-Zellen mit der Aspose.Cells Cloud-API. Stellen Sie saubere und konsistente Tabellendaten sicher."
weight: 100
---

Trimmen Sie automatisch unnötige Zeichen, überflüssige Leerzeichen und Zeilenumbrüche aus Excel-Zellen mit der Aspose.Cells Trim-Zeichen-API. Bereinigen Sie Dateneinträge und gewährleisten Sie eine konsistente Formatierung Ihrer Tabellenkalkulationen.

## **Übersicht**

- **Trimmen der Leerzeichen am Anfang und Ende**
  - Entfernen Sie überflüssige Leerzeichen am Anfang und Ende von Texten
  - Verbessern Sie die übersichtliche Darstellung und Lesbarkeit der Daten
- **Bearbeitung von überflüssigen Leerzeichen zwischen Wörtern**
  - Entfernen Sie überflüssige Leerzeichen zwischen Wörtern
  - Vermeiden Sie Formatierungsprobleme, die durch Daten aus mehreren Quellen entstehen

- **Spezielle Leerzeichen entfernen**
  - Entfernen Sie gezielt geschützte Leerzeichen (nicht umbruchfähige Leerzeichen)
  - Sicherstellen der Datengenauigkeit und -konsistenz

- **Verwaltung von Zeilenumbrüchen**
  - Entfernen Sie überflüssige oder alle Zeilenumbrüche
  - Halten Sie den Zellinhalt organisiert und professionell gestaltet

## **TrimCharacter-API**

Vor dem Aufruf der API stellen Sie sicher, dass Sie über ein gültiges Aspose-Cloud-Konto, eine `client_id`/`client_secret` sowie ein Zugriffstoken mit dem Scope **Cells** verfügen.

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anforderungsparameter der **trimCharacter**-API sind:

| Parametername          | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                         |
| :--------------------- | :------ | :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet            | Datei   | FormData                            | Die zu verarbeitende Tabellendatei. Unterstützte Formate sind unter anderem XLSX, XLS, ODS, CSV usw.                                                                |
| trimContent            | Zeichenkette | Query                           | Gibt die spezifischen Zeichen oder Zeichenfolgen an, die aus dem Zellinhalt entfernt werden sollen. Kann ein einzelnes Zeichen, mehrere Zeichen oder ein benutzerdefiniertes Muster sein. |
| trimLeading            | Boolean | Query                               | Wenn `true`, werden die angegebenen Zeichen vom Anfang des Zellinhalts entfernt.                                                                                   |
| trimTrailing           | Boolean | Query                               | Wenn `true`, werden die angegebenen Zeichen vom Ende des Zellinhalts entfernt.                                                                                     |
| trimSpaceBetweenWordTo1| Boolean | Query                               | Wenn `true`, werden mehrere aufeinanderfolgende Leerzeichen zwischen Wörtern innerhalb jeder Zelle auf ein einzelnes Leerzeichen reduziert.                       |
| trimNonBreakingSpaces  | Boolean | Query                               | Wenn `true`, entfernt geschützte Leerzeichen (Unicode U+00A0) aus dem Zellinhalt.                                                                                 |
| removeExtraLineBreaks  | Boolean | Query                               | Wenn `true`, reduziert mehrere aufeinanderfolgende Zeilenumbrüche innerhalb jeder Zelle auf einen einzigen Zeilenumbruch.                                         |
| removeAllLineBreaks    | Boolean | Query                               | Wenn `true`, entfernt alle Zeilenumbruchzeichen aus dem Zellinhalt.                                                                                                |
| worksheet              | Zeichenkette | Query                         | _(Optional)_ Der Name des Arbeitsblatts, auf das die Texttrimming-Operation angewendet werden soll. Falls ausgelassen, wird das erste Arbeitsblatt verwendet.      |
| range                  | Zeichenkette | Query                         | _(Optional)_ Der Zellbereich, auf den die Texttrimming-Operation angewendet werden soll (z. B. `"A1:C10"`). Falls ausgelassen, wird die Operation auf alle verwendeten Zellen im angegebenen Arbeitsblatt angewendet. |
| outPath                | Zeichenkette | Query                         | _(Optional)_ Der Cloud-Speicherordnerpfad, in dem die verarbeitete Arbeitsmappe gespeichert wird. Falls ausgelassen, wird die Datei im Quellordner gespeichert.     |
| outStorageName         | Zeichenkette | Query                         | Der Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                             |
| region                 | Zeichenkette | Query                         | _(Optional)_ Legt das Gebietsschema für die Textverarbeitung fest, was die Handhabung von Leerzeichen und Zeilenumbrüchen für bestimmte Sprachen beeinflussen kann (z. B. `"de-DE"`, `"ar-SA"`). |
| password               | Zeichenkette | Query                         | _(Optional)_ Falls die hochgeladene Tabellendatei passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                      |

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

**Erfolgsbeispiel (HTTP 200):** Die API gibt einen Dateistream zurück, der die getrimmte Arbeitsmappe enthält.

### Fehlercodes

- **400 Bad Request**: Ungültige Aspose.Cells Cloud-API-URI.
- **401 Unauthorized**: Ungültiges Zugriffstoken. Oder ungültige client_id und client_secret.
- **404 Not Found**: Die Tabellendatei ist nicht zugänglich.
- **500 Server Error**: Bei der Tabellendatei ist beim Abrufen von Berechnungsdaten ein Fehler aufgetreten.

## Wofür sollte die Trim-Zeichen-API verwendet werden?

- **Normalisierung von Benutzereingaben**: Bereinigen Sie manuell eingegebene Tabellendaten, indem überflüssige Leerzeichen und Zeilenumbrüche entfernt werden.
- **Pflege von Kundendatenbanken**: Bereinigen Sie überflüssige Leerzeichen und Formatierungsprobleme in Kundennamen, Adressen und Kontaktdaten.
- **Automatisierte Berichtsbereinigung**: Bereinigt das Datenquellenformat vor der Erstellung automatisierter Berichte.
- **Vorbereitung für Datenmigration**: Bereinigt Formatierungsprobleme vor der Migration der Daten in das neue System.

## Warum sollte die Trim-Zeichen-API verwendet werden?

- **Reduzierte Arbeitskosten**: Eliminieren Sie zeitaufwändige manuelle Datenbereinigungsarbeiten
- **Reduzierte Fehlerkosten**: Vermeiden Sie Analysefehler aufgrund von Formatierungsproblemen
- **Pay-per-Use**: Keine festen Gebühren, es werden nur die tatsächlich genutzte Leistung fakturiert
- **Keine Infrastrukturinvestitionen**: Keine Notwendigkeit, Server oder Software zu warten
- **Unterstützung mehrerer Formate**: Unterstützt die Verarbeitung mehrerer Formate wie XLSX, XLS, CSV, ODS usw.
- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, die eine schnelle Entwicklung ermöglichen, und wird mit umfangreicher Dokumentation geliefert. Im Vergleich zum Aufbau eigener Diagramm-Renderingslösungen wird der Entwicklungsaufwand erheblich reduziert.
- **Kosteneffizient**: Sie können doppelte Zeichen entfernen, ohne zuerst die Arbeitsmappe hochzuladen, wodurch Speicherplatz gespart und Kosten reduziert werden.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie das Trimmen von Zeichen für Zellen mit minimalem Codeaufwand implementieren können.
Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}