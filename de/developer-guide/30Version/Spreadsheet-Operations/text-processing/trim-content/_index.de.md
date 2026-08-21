---
title: "Aspose.Cells Trim Content API – Leerzeichen und Zeilenumbrüche aus Excel entfernen"
second_title: "Dokument"
linktitle: "Inhalt kürzen"
type: docs
url: /spreadsheet-trim-content/
keywords: "Aspose.Cells, Trim Content API, Excel-Daten bereinigen, Leerzeichen in Excel entfernen, Zeilenumbrüche entfernen, Datenbereinigung für Tabellenkalkulationen"
description: "Verwenden Sie die Aspose.Cells Cloud PostTrimContent API, um automatisch zusätzliche Leerzeichen, Zeilenumbrüche und unerwünschte Zeichen aus Excel-Zellen zu entfernen. Erfahren Sie mehr über den Endpunkt, das Anforderungsformat, Beispielcode und Fehlerbehandlung."
weight: 100
---

## **Excel-Web-API: PostTrimContent**

Die **PostTrimContent** API verarbeitet und kürzt den Inhalt innerhalb eines angegebenen Bereichs in einer Tabellenkalkulation. Sie entfernt überflüssige Leerzeichen, Zeilenumbrüche und andere unnötige Zeichen aus dem Inhalt ausgewählter Zellen, was sie besonders nützlich für die Bereinigung von Dateneinträgen und die Sicherstellung einer konsistenten Formatierung von Tabellenkalkulationen macht.

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### **Funktionsbeschreibung**

- **Effizienz** – Kürzt den Inhalt ausschließlich innerhalb des festgelegten Bereichs und spart Zeit sowie Ressourcen, indem unnötige Vorgänge am gesamten Arbeitsblatt vermieden werden.
- **Flexibilität** – Ermöglicht es Benutzern, den genauen Zellbereich festzulegen, der verarbeitet werden soll, und passt sich so verschiedenen Datensätzen und Anforderungen an.
- **Datenintegrität** – Entfernt überflüssige Leerzeichen und Zeilenumbrüche und hilft so, konsistente und zuverlässige Daten für Analysen und Berichte zu gewährleisten.
- **Benutzerfreundlichkeit** – Einfache Integration mit minimalem Konfigurationsaufwand, geeignet für Entwickler sowie Endbenutzer.

### **Anforderungsparameter**

| Parametername         | Typ   | Ort   | Beschreibung                                                                 |
| --------------------- | ----- | ----- | ---------------------------------------------------------------------------- |
| trimContentOptions    | Klasse | Body  | Optionen, die festlegen, wie der Inhalt gekürzt werden soll (z. B. Zielbereich, Kürzungsmodus). |

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[zusammengeführter Dateiname]",
    "Filesize" : [Dateigröße],
    "FileContent" : "[Base64-Zeichenfolge]"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |
## So verwenden Sie die PostRemoveCharacters API mit SDKs

### PostRemoveCharacters API-Spezifikation


Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Aspose.Cells Cloud SDKs verwenden

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_Zuletzt aktualisiert: 2026-03-30_