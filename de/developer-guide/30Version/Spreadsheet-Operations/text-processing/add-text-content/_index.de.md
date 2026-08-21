---
title: "Text in Excel hinzufügen: Effizientes Einfügen von Daten mit der Tabellenkalkulations-Web-API"
second_title: "Dokument"
linktitle: "Text hinzufügen"
type: docs
url: /de/excel-add-text/
keywords: "Excel, Aspose.Cells, Text hinzufügen, Tabellenkalkulations-API, REST-API, Office Cloud, Text-Einfügung, Excel-API"
description: "Fügt Text an einer angegebenen Position in einer Excel-Tabellenkalkulation über die Aspose.Cells Cloud API hinzu."
weight: 100
---

Fügt Textinhalt an einer angegebenen Position innerhalb einer Tabellenkalkulation hinzu. Dazu ist ein Objekt erforderlich, das den hinzuzufügenden Text sowie die Position für die Einfügung definiert.

## **Excel-API: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### **Funktionsbeschreibung**

Diese Methode hängt sicher neuen Text an angegebene Zellen an und unterstützt mehrere Einfügemodi sowie Formatbehandlung.

- **Text am Anfang ausgewählter Zellen hinzufügen**  
  Fügt Text am Anfang aller ausgewählten Zellen hinzu und gewährleistet so Konsistenz bei der Datenerfassung. Ideal zum Hinzufügen allgemeiner Bezeichnungen oder Kennungen wie Produktnummern, Kategorien oder Präfixen.

- **Zeichen vor oder nach einem bestimmten Text einfügen**  
  Fügt Zeichen vor oder nach dem Zieltext in den ausgewählten Zellen ein, sodass Sie strukturierte und gut organisierte Inhalte einfach erstellen können.

- **Den gleichen Text am Ende jeder ausgewählten Zelle anhängen**  
  Fügt denselben Text in einem Vorgang am Ende mehrerer Zellen hinzu und vereinfacht so die Datenerfassung sowie die einheitliche Darstellung.

- **Text nach einer bestimmten Anzahl von Zeichen einfügen**  
  Fügt Text nach einer definierten Anzahl von Zeichen entweder vom Anfang oder vom Ende jeder Zelle im Zielbereich ein. Typische Anwendungsfälle sind die Formatierung von Codes, Zeitstempeln oder benutzerdefinierten Trennern.

### **Anfrageparameter**

| Parametername | Typ   | Ort     | Beschreibung                                                         |
|---------------|-------|---------|----------------------------------------------------------------------|
| addTextOptions| Klasse| Body    | Gibt den Textinhalt sowie die Position an, an der der Text eingefügt werden soll. |

### **Antwort**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_kodierter_String"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                       |
|------|-----------------------------|--------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## Wie Sie die PostAddTextContent-API mit SDKs verwenden

### PostAddTextContent-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die effizienteste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

---