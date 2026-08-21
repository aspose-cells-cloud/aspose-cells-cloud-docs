---
title: "Aspose.Cells – Update Word Case API"
second_title: "Dokumentation"
linktype: "de"
linktitle: "Wort Groß-/Kleinschreibung"
type: docs
url: /de/post-update-word-case/
keywords: "Aspose.Cells, Update Word Case API, Textgroßschreibung, Excel, CSV, Google Sheets, REST API"
description: "Konvertieren Sie die Textgroßschreibung in Excel-, CSV- oder Google Sheets-Dateien mit der Update Word Case API von Aspose.Cells Cloud. Unterstützt Großschreibung, Kleinbuchstaben, Titelschreibung und Erstbuchstaben-Großschreibung."
weight: 100
ArticleTitle: "Aspose.Cells – Update Word Case API-Dokumentation"
---

**API-Version:** 3.0

Die Verwaltung inkonsistenter Textgroßschreibungen in Tabellenkalkulationen (Excel, Google Sheets, CSV) kann frustrierend sein, besonders bei großen Datensätzen. Die **PostUpdateWordCase-Web-API** automatisiert die Konvertierung der Textgroßschreibung und sorgt so für saubere und standardisierte Daten mit minimalem Aufwand.


## **Excel-Web-API – Update Word Case API**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Funktionsbeschreibung**

Die PostUpdateWordCase-Web-API löst das häufige Problem inkonsistenter Textgroßschreibungen in Tabellenkalkulationen, was die Datenanalyse und -verarbeitung erheblich beeinträchtigen kann. Diese API automatisiert die Großschreibungskonvertierung und sorgt dafür, dass Ihre Daten sauber, standardisiert und für weitere Bearbeitung oder Analyse bereit sind.

- **Automatisierte Textgroßschreibungskonvertierung**
  - **Großschreibung in Kleinbuchstaben** – Wandelt alle Großbuchstaben in Kleinbuchstaben um.
  - **Kleinbuchstaben in Großschreibung** – Wandelt alle Kleinbuchstaben in Großbuchstaben um.
  - **Erstbuchstaben groß schreiben** – Schreibt den ersten Buchstaben jedes Wortes groß.
  - **Titelschreibung** – Wandelt Text in Titelschreibung um, wobei der erste Buchstabe jeder Hauptwortart großgeschrieben wird.

- **Unterstützung für mehrere Formate** – Die API funktioniert mit einer breiten Palette an Tabellenkalkulationsformaten, darunter Excel, OpenOffice, JSON, CSV und andere. Diese Vielseitigkeit macht sie für verschiedene Datenverarbeitungsanforderungen geeignet.

### **Anforderungsparameter**

| Parametername         | Typ    | Speicherort     | Beschreibung                                                                                                               |
| --------------------- | ------ | --------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions`     | Objekt | Anforderungstext | Optionen, die die gewünschte Großschreibumwandlung definieren, z. B. den Quellbereich, den Zielgroßschreibungstyp und zusätzliche Einstellungen. |

**Schema für `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // Bereich im Excel-Stil zur Verarbeitung (erforderlich)
  "CaseType": "Upper", // Enum: Upper, Lower, Capitalize, Title (erforderlich)
  "IgnoreBlank": true // Boolean, optional – wenn true, bleiben leere Zellen unverändert
}
```

**Beispiel für Anforderungstext**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – Der Zellbereich, auf den die Großschreibungsumwandlung angewendet wird (z. B. `A1:C5`).
- **CaseType** – Der Typ der Großschreibungsumwandlung. Zulässige Werte sind `Upper`, `Lower`, `Capitalize` und `Title`.
- **IgnoreBlank** – Wenn `true`, werden leere Zellen ignoriert; Standardwert ist `false`.

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[zusammengeführter Dateiname]",
    "Filesize" : [Dateigröße],
    "FileContent" : "[Base64String]"
}
```

- **Filename** – Name der verarbeiteten Datei.
- **FileSize** – Größe der Datei in Bytes.
- **FileContent** – Base64-kodierter Inhalt der transformierten Datei.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                         |
|------|-----------------------------|----------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.     |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.               |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                           |

## So verwenden Sie die PostUpdateWordCase API mit SDKs

### PostUpdateWordCase API-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektanforderungen zu konzentrieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---