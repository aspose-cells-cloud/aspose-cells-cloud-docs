---
title: "Aspose.Cells Cloud – Text in lokalen Excel-Dateien ersetzen (Finden & Ersetzen API)"
second_title: "Dokument"
ArticleTitle: "Massen-Textersatz in lokalen Excel-Dateien – Finden & Ersetzen API"
linktitle: "Inhalt von Tabellenkalkulationen ersetzen"
type: docs
url: /replace-spreadsheet-content/
keywords: "Text in Excel ersetzen, Aspose.Cells Finden & Ersetzen, lokale Tabellenkalkulations-API, Excel-Datei ersetzen, API-Inhalt ersetzen"
description: "Ersetzen Sie Text in lokalen Excel-Arbeitsmappen, ohne diese in die Cloud hochzuladen. Verwenden Sie die Aspose.Cells Cloud Finden & Ersetzen API, um spezifische Bereiche, Arbeitsblätter oder ganze Dateien mit einem einzigen Aufruf zu aktualisieren."
weight: 100
---

Ersetzen Sie angegebenen Text in lokalen Excel-Tabellenkalkulationsdateien, ohne diese in die Cloud hochzuladen. Aktualisieren Sie den Inhalt in Arbeitsmappen effizient mithilfe der Aspose.Cells Finden & Ersetzen API für Offline-Bearbeitung.

## **API zum Ersetzen von Tabellenkalkulationsinhalt**

### **Web-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                                     |
| :-------------- | :----- | :--------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Datei  | FormData                           | Die lokale Tabellenkalkulationsdatei, die verarbeitet werden soll. Unterstützte Formate sind u. a. XLSX, XLS, ODS, CSV usw.                                                      |
| searchText      | String | Abfrage                            | Der Suchtext innerhalb des angegebenen Arbeitsblatts und Zellbereichs.                                                                                                          |
| replaceText     | String | Abfrage                            | Der Text, der alle Vorkommen von `searchText` im angegebenen Bereich ersetzen soll.                                                                                             |
| worksheet       | String | Abfrage                            | _(Optional)_ Der Name des Arbeitsblatts, auf dem die Finden & Ersetzen-Operation ausgeführt wird. Falls weggelassen, wird das erste Arbeitsblatt verwendet.                     |
| cellArea        | String | Abfrage                            | _(Optional)_ Der spezifische Zellbereich (z. B. `"A1:D20"`, `"B5:F15"`), in dem die Textsuche und -ersatz erfolgt. Falls weggelassen, wird der Vorgang auf alle genutzten Zellen im angegebenen Arbeitsblatt angewendet. |
| region          | String | Abfrage                            | _(Optional)_ Legt das Gebietsschema für die Textverarbeitung fest, was sich auf die Groß-/Kleinschreibung und Zeichencodierung bei Suchvorgängen auswirken kann (z. B. `"de-DE"`, `"fr-FR"`). |
| password        | String | Abfrage                            | _(Optional)_ Falls die hochgeladene Tabellenkalkulation passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                             |

### **Antwort**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Die Antwort ist ein Binärstream, der die aktualisierte Arbeitsmappe enthält. Speichern Sie ihn mit der entsprechenden Dateierweiterung (z. B. `.xlsx`).

### **Fehlercodes**

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API URI oder fehlerhafte Parameter.
- **401 Unauthorized** – Ungültiges oder fehlendes Zugriffstoken; holen Sie sich ein neues Token.
- **404 Not Found** – Die Tabellenkalkulationsdatei ist nicht zugänglich oder das angegebene Arbeitsblatt existiert nicht.
- **500 Server Error** – Bei der Verarbeitung der Tabellenkalkulation ist ein interner Fehler aufgetreten; kontaktieren Sie den Support, falls das Problem weiterhin besteht.

## Wofür sollte die API zum Ersetzen von Inhalten in Tabellenkalkulationen verwendet werden?

- **Batchverarbeitung lokaler Excel-Dateien** – Automatisieren Sie Finden & Ersetzen über viele lokal gespeicherte Arbeitsmappen hinweg.
- **Lokale Datenpipelines** – Integrieren Sie die API in geplante Aufträge, die Berichte modifizieren, bevor sie archiviert oder verteilt werden.
- **Lokale Berichtsgenerierung** – Fügen Sie dynamisch Werte in Vorlagenarbeitsmappen ein, ohne diese in die Cloud hochzuladen.

## Warum sollten Sie die API zum Ersetzen von Inhalten in Tabellenkalkulationen verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung und umfassende Dokumentation ermöglicht. Im Vergleich zum Aufbau eigener Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Arbeitskosten** – Verringert den Bedarf an Fachkräften für manuelle Dokumentenkonsolidierung.
- **Pay-per-Use** – Keine Vorabinvestition; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Keine Wartungskosten** – Keine Server zu warten, keine Softwareupdates und keine Kompatibilitätsprobleme.
- **Beibehaltung komplexer Excel-Formatierungen** – Die ursprüngliche Formatierung, Formeln und Diagramme der Arbeitsmappe bleiben nach dem Ersetzen erhalten.

## Verwendung der API zum Ersetzen von Inhalten in Tabellenkalkulationen mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie Ersetzungsoperationen mit minimalem Codeaufwand implementieren können. Weitere Informationen finden Sie im offiziellen **Aspose.Cells Cloud SDK GitHub**-Repository mit einer vollständigen Liste unterstützter Sprachen.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs mit Aspose.Cells-Webdiensten interagieren:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}