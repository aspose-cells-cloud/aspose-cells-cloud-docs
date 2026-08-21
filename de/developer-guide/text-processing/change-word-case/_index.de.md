---
title: "Aspose.Cells Cloud – Wortgroße ändern (Groß, Klein, Titel- und Satzschreibung)"
ArticleTitle: "Excel-Wortgroßenkonverter – Großschreibung, Kleinschreibung, Titelschreibung & Satzschreibung"
linktype: "Wortgroße"
type: docs
url: /change-word-case/
keywords: "Wortgroße ändern API, Aspose.Cells, Excel-Wortgroßenkonvertierung, Großschreibung, Kleinschreibung, Titelschreibung, Satzschreibung, Textformatierung"
description: "Konvertieren Sie die Wortgroße in Excel-Dateien mithilfe der Aspose.Cells Cloud API ganz einfach. Unterstützt Großschreibung, Kleinschreibung, Titelschreibung und Satzschreibung. Holen Sie sich Codebeispiele in C#, Java, Python u. a."
weight: 100
---

## **Wortgroße ändern**

Verwenden Sie die Aspose.Cells Cloud Web-API, um die Wortgroße in Ihrer Tabellendatei sofort zu ändern – wechseln Sie zwischen Großschreibung, Kleinschreibung, Titelschreibung (jedes Wort großschreiben) oder Satzschreibung (ersten Buchstaben jedes Satzes großschreiben) innerhalb eines ausgewählten Bereichs. Nur Zellen mit Textinhalten werden beeinflusst; Zahlen, Boolesche Werte, Fehler und leere Zellen bleiben unberührt. Formeln, Formatierungen und Datenvalidierungen bleiben unverändert.

- **UpperCase (Großschreibung)** – Alle Zeichen werden großgeschrieben.
- **LowerCase (Klein schreiben)** – Alle Zeichen werden kleingeschrieben.
- **ProperCase (Titelschreibung)** – Der erste Buchstabe jedes Wortes wird großgeschrieben, der Rest kleingeschrieben.
- **SentenceCase (Satzschreibung)** – Der erste Buchstabe jedes Satzes wird großgeschrieben, der Rest kleingeschrieben.

<img src="images/result.png" alt="Vergleichsbild vor/nach der Wortgroßenänderung" width="800" height="450" />

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```
### Anfrageparameter für die **UpdateWordCase** API

| Parametername     | Typ    | Ort       | Beschreibung                                                                                                                                                        |
| :---------------- | :----- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| spreadsheet       | File   | FormData  | Die zu verarbeitende Tabellendatei. Unterstützte Formate sind unter anderem XLSX, XLS, ODS, CSV usw.                                                               |
| wordCaseType      | String | Query     | Gibt den Typ der Textgroßenkonvertierung an: `UpperCase`, `LowerCase`, `ProperCase` oder `SentenceCase`.                                                         |
| worksheet         | String | Query     | _(Optional)_ Der Name des Arbeitsblatts, auf das die Wortgroßenänderung angewendet werden soll. Falls weggelassen, wird die Operation auf das erste Arbeitsblatt des Arbeitsbooks angewendet. |
| range             | String | Query     | _(Optional)_ Der Zellbereich, auf den die Wortgroßenänderung angewendet werden soll (z. B. `"A1:C10"`). Falls weggelassen, wird die Operation auf alle genutzten Zellen des angegebenen Arbeitsblatts angewendet. |
| outPath           | String | Query     | _(Optional)_ Der Pfad zum Cloud-Speicherordner, in dem das verarbeitete Arbeitsbuch gespeichert werden soll. Falls weggelassen, wird die Datei im Quellordner gespeichert. |
| outStorageName    | String | Query     | Der Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert werden soll.                                                                                     |
| region            | String | Query     | _(Optional)_ Legt das Gebietsschema für die Textgroßenregeln fest, insbesondere relevant für sprachspezifische Großschreibungsregeln (z. B. `"en-US"`, `"tr-TR"`). |
| password          | String | Query     | _(Optional)_ Falls die hochgeladene Tabellendatei passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                    |

### Antwort

Im Erfolgsfall gibt der Dienst **200 OK** (oder **202 Accepted**) mit einer JSON-Payload zurück, die den Binärstream der verarbeiteten Arbeitsmappe enthält.

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

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API-URI.
- **401 Unauthorized** – Ungültiges Zugriffstoken oder falsche Clientanmeldedaten.
- **404 Not Found** – Die Tabellendatei ist nicht zugänglich.
- **500 Server Error** – Bei der Verarbeitung der Tabellendatei ist ein interner Fehler aufgetreten.

## Wo sollte die API zur Wortgroßenänderung verwendet werden?

### Datenbereinigung und -standardisierung

- **Kundendatenverwaltung** – Standardisierung der Großschreibung von Kundennamen und Adressinformationen (z. B. `max mustermann` → `Max Mustermann`).
- **Produktkatalogverarbeitung** – Standardisierung von Produkttiteln und Beschreibungstexten (z. B. `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **Erstellung von Finanzberichten** – Normalisierung von Artikelbezeichnungen und Beschreibungsfeldern in Finanzberichten.

### Datenintegration aus mehreren Quellen

- **ETL für Data Warehouse** – Standardisierung des Textformats beim Laden von Daten aus verschiedenen Systemen.
- **API-Datenempfang** – Verarbeitung inkonsistenter Großschreibungen von externen APIs.
- **Datenfusion zwischen Abteilungen** – Standardisierung des Textformats in Excel-Berichten verschiedener Abteilungen.

### Content-Management-System

- **Automatisierte Pressemitteilungen** – Automatische Formatierung von Nachrichtentiteln und Inhalten (Großschreibungsregeln für Überschriften).
- **Erstellung von Produktdokumentationen** – Sicherstellung der Konsistenz bei der Formatierung technischer Dokumentationsbegriffe.
- **Wissensdatenbankpflege** – Standardisierung des Textformats von FAQ und Hilfedokumenten.

### Unternehmensanwendungskonnektivität

- **CRM-Systemintegration** – Automatische Formatierung von Namen und Firmeninformationen beim Import/Export von Kundendaten.
- **ERP-Datenverarbeitung** – Standardisierung von Schlüsselfeldern wie Materialbeschreibungen und Lieferantenbezeichnungen.
- **HR-Management-System** – Standardisierung von Mitarbeiterinformationen und Berufsbezeichnungen.

### Stapelverarbeitung von Dokumenten

- **Vorbereitung rechtlicher Dokumente** – Stapelverarbeitung von Klauselformaten in Verträgen und Vereinbarungen.
- **Erstellung von Marketingmaterialien** – Standardisierung des Textformats von Werbetexten und E-Mail-Vorlagen.
- **Formatierung wissenschaftlicher Arbeiten** – Standardisierung von Formatierungsanforderungen für Referenzen und Titel.

### Echtzeit-Datenverarbeitung

- **Benutzereingabevalidierung** – Echtzeit-Formatierung von Formulardaten, die von Benutzern eingereicht werden.
- **Chatbot-Antworten** – Standardisierung des Textformats für automatisch generierte Antworten.
- **Sofortige Berichtserstellung** – Dynamische Erstellung einheitlich formatierter Geschäftsberichte.

### Internationalisierung und Lokalisierung

- **Mehrsprachige Datenverarbeitung** – Berücksichtigung unterschiedlicher Großschreibungsregeln für Texte in verschiedenen Sprachen.
- **Vorbereitung lokalisierten Inhalts** – Erstellung formatiertem Inhalt für verschiedene Regionen.
- **Verwaltung von Übersetzungsprojekten** – Sicherstellung der Konsistenz des Textformats vor und nach der Übersetzung.

## Warum sollten Sie die API zur Wortgroßenänderung verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, sodass eine schnelle Entwicklung und umfassende Dokumentation gewährleistet sind. Im Vergleich zur Erstellung eigener Lösungen reduziert dies erheblich den Entwicklungsaufwand.
- **Kosteneffizient** – Sie können die Wortgroßenänderung durchführen, ohne zuerst die Arbeitsmappe hochzuladen, wodurch Speicherplatz gespart und Kosten reduziert werden.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrundeliegenden Details, sodass Sie **UpdateWordCase** für Zellen mit minimalem Codeaufwand einfach implementieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---