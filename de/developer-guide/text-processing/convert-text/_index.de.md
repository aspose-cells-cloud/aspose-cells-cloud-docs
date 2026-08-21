---
title: "Aspose.Cells Cloud Web-API – Konvertierung von Text in Zahlen in Excel & Bereinigung spezieller Zeichen"
second_title: "Dokument"
ArticleTitle: "Excel-Datenreiniger – Konvertierung von Text in Zahlen & Entfernung unerwünschter Zeichen"
linktitle: "Text konvertieren"
type: docs
url: /de/convert-text/
keywords: "Aspose.Cells Text konvertieren, Excel Text in Zahlen, spezielle Zeichen in Excel entfernen, Zeilenumbrüche in Excel ersetzen, akzentuierte Zeichen normalisieren, Excel-Datenreinigungs-API"
description: "Konvertieren Sie numerische Werte, die als Text formatiert sind, in echte Zahlen, ersetzen Sie unerwünschte Zeichen und Zeilenumbrüche sowie normalisieren Sie akzentuierte Zeichen in Excel-Dateien mithilfe der Aspose.Cells Cloud API."
weight: 100
---

Bereinigen Sie Excel-Daten, indem Sie Zahlen, die als Text formatiert sind, in numerische Werte umwandeln, unerwünschte Zeichen und Zeilenumbrüche ersetzen sowie akzentuierte Zeichen in normale Buchstaben normalisieren – alles mithilfe der Aspose.Cells API.

## Übersicht

**Zahlen als Text konvertieren, unnötige Zeichen entfernen, Akzente austauschen – ein Aufruf, keine Formeln.**

- **Konvertierung von als Text gespeicherten Zahlen in echte Zahlen**: Wandeln Sie numerische Daten, die als Text vorliegen, in echte Zahlen um, um genaue Berechnungen und eine korrekte Datendarstellung sicherzustellen.
- **Spezifische Zeichen ersetzen**: Ersetzen Sie alle Vorkommen bestimmter Zeichen in den ausgewählten Zellen auf einmal, um Ihre Daten zu standardisieren.
- **Konvertierung von Zeilenumbrüchen in Leerzeichen, Kommas oder Semikolons**: Verbessern Sie die Lesbarkeit, indem Sie Zeilenumbrüche durch Leerzeichen, Kommas oder Semikolons ersetzen – eine übersichtlichere und optisch ansprechendere Darstellung.
- **Ersetzen akzentuierter Zeichen**: Falls Ihre Daten in verschiedenen Sprachen vorliegen, können Sie akzentuierte Zeichen wie „é“ oder „ü“ durch ihre nicht-akzentuierten Gegenstücke ersetzen, was Konsistenz und Klarheit erhöht.

## **ConvertText API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter der **convertText**-API

| Parametername       | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                              |
| ------------------- | ------ | ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet         | Datei  | FormData                            | Die zu verarbeitende Tabellendatei. Unterstützte Formate sind unter anderem XLSX, XLS, ODS, CSV usw.                                                                     |
| convertTextType     | String | Abfrage                             | Gibt die Art der anzuwendenden Textkonvertierung an, z. B. Konvertierung von als Text formatierten Zahlen in numerische Werte oder Konvertierung akzentuierter Zeichen.     |
| sourceCharacters    | String | Abfrage                             | Gibt die Zeichen, Zeichenfolgen oder Muster an, die aus dem Text ersetzt oder entfernt werden sollen (z. B. `"é,è,ê"`, `"#N/A"`, `"\\n"` für Zeilenumbrüche).                |
| targetCharacters    | String | Abfrage                             | Gibt die Ersatzzeichen oder -zeichenfolgen an, die die Quellzeichen ersetzen (z. B. `"e"` für akzentuierte Buchstaben, `""` zum Entfernen, `" "` für Zeilenumbrüche).      |
| worksheet           | String | Abfrage                             | _(Optional)_ Der Name des Arbeitsblatts, auf das die Textkonvertierung angewendet werden soll. Falls nicht angegeben, wird das erste Arbeitsblatt verwendet.              |
| range               | String | Abfrage                             | _(Optional)_ Der Zellbereich, auf den die Textkonvertierung angewendet werden soll (z. B. `"A1:C10"`). Falls nicht angegeben, wird die Operation auf alle belegten Zellen angewendet. |
| outPath             | String | Abfrage                             | _(Optional)_ Der Pfad zum Cloud-Speicherordner, in dem die verarbeitete Arbeitsmappe gespeichert wird. Falls nicht angegeben, wird die Datei im Quellordner gespeichert.    |
| outStorageName      | String | Abfrage                             | Der Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                                   |
| region              | String | Abfrage                             | _(Optional)_ Legt die Locale für Textkonvertierungsregeln fest, insbesondere relevant für sprachspezifische Zeichenverarbeitung (z. B. `"en-US"`, `"fr-FR"`).             |
| password            | String | Abfrage                             | _(Optional)_ Falls die hochgeladene Tabellendatei passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                           |

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

- **400 Bad Request**: Ungültige Aspose.Cells Cloud API-URI.
- **401 Unauthorized**: Ungültiges Zugriffstoken oder ungültige Client-ID und -Geheimnis.
- **404 Not Found**: Die Tabellendatei ist nicht zugänglich.
- **500 Server Error**: Die Tabellendatei hat beim Abrufen von Berechnungsdaten einen Fehler festgestellt.

## Wann sollte die Convert Text API verwendet werden?

- **Korrektur des Zahlenformats**: Konvertieren Sie als Text gespeicherte Zahlen (z. B. „123,45“) in ein für Berechnungen geeignetes numerisches Format.
- **Bereinigung spezieller Zeichen**: Entfernen Sie unnötige Sonderzeichen, zusätzliche Leerzeichen oder unsichtbare Zeichen aus den Daten.
- **Behandlung von Zeilenumbrüchen**: Ersetzen Sie Zeilenumbrüche in Zellen durch Leerzeichen oder andere Trennzeichen.
- **Normalisierung akzentuierter Zeichen**: Konvertieren Sie akzentuierte Buchstaben (z. B. „é“, „ñ“) in Standardbuchstaben („e“, „n“).
- **CSV-Dateivorverarbeitung**: Standardisieren Sie das Textformat vor dem Import von CSV-Dateien in Excel.

## Warum sollte man die Convert Text API verwenden?

- **Automatische Formatumwandlung**: Konvertieren Sie als Text formatierte Zahlen mit einem einzigen Aufruf in berechenbare Werte in Stapelverarbeitung.
- **Zeichennormalisierung**: Einheitliche Behandlung spezieller Zeichen, Diakritika und Kodierungsprobleme.
- **Datenkonsistenz**: Sicherstellen, dass das Textformat vollständig einheitlich über den gesamten Datensatz hinweg ist.
- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung ermöglicht und umfassende Dokumentation bereitstellt. Im Vergleich zum Aufbau eigener Textverarbeitungslösungen wird der Entwicklungsaufwand deutlich reduziert.
- **Kosteneffizient**: Sie können Text konvertieren, ohne die Arbeitsmappe zunächst hochzuladen – dies spart Speicherplatz und Kosten.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Convert Text-Funktion für Zellen mit minimalem Codeaufwand implementieren können.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---