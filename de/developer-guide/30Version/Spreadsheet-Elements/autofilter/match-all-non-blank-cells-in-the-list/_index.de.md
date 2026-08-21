---
title: "Alle nicht leeren Zellen in einem Excel-Arbeitsblatt abgleichen"
second_title: "Dokument"
linktitle: "Alle nicht leeren Zellen abgleichen"
type: docs
url: /de/autofilter/match-all-non-blank/
aliases: [  /de/match-all-non-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells Cloud, nicht leere Zellen abgleichen, AutoFilter, Excel-API"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST-API nutzen, um alle nicht leeren Zellen in einer AutoFilter-Liste eines Excel-Arbeitsblatts abzugleichen. Enthält Endpunkt, Parameter, Authentifizierung, Antwort-Schema, Fehlercodes und SDK-Beispiele."
ArticleTitle: "Alle nicht leeren Zellen in einem Excel-Arbeitsblatt mit der Aspose.Cells Cloud API abgleichen"
weight: 100
---

**Übersicht**  
Der Vorgang *Alle nicht leeren Zellen abgleichen* wendet einen AutoFilter auf ein Arbeitsblatt an und gibt nur die Zeilen zurück, in denen die angegebene Spalte Daten enthält, wobei leere Zellen ignoriert werden. Dies ist nützlich für die Bereinigung von Datensätzen, die Erstellung von Berichten oder die Vorbereitung von Daten für eine weitere Analyse.

**Voraussetzungen**  
- Ein gültiges JWT-Token für die Authentifizierung bei Aspose.Cells Cloud.  
- Die Arbeitsmappe muss in den Aspose Cloud-Speicher hochgeladen sein.  
- Sie benötigen den Dateinamen, den Arbeitsblattnamen und den nullbasierten Spaltenindex (`fieldIndex`), den Sie filtern möchten.

Diese REST-API gleicht alle nicht leeren Zellen in der AutoFilter-Liste eines Excel-Arbeitsblatts ab.

## PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter

| Parametername | Typ    | Ort    | Beschreibung                                                     |
| ------------- | ------ | ------ | ---------------------------------------------------------------- |
| name          | string | path   | Der Name der Excel-Datei.                                        |
| sheetName     | string | path   | Der Name des Arbeitsblatts, das den AutoFilter enthält.         |
| fieldIndex    | integer | query | Nullbasierter Index der Spalte, auf die der Filter angewendet wird. |
| folder        | string | query  | _(Optional)_ Pfad zum Ordner, in dem die Datei gespeichert ist.  |
| storageName   | string | query  | _(Optional)_ Name des zu verwendenden Speicherdienstes.          |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; die Antwort enthält Details zum Vorgang.     |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.               |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

*Beispiel für eine Fehlerantwort (400)*  

```json
{
  "Code": 400,
  "Message": "Ungültiger Parameter: fieldIndex muss eine nicht-negative Ganzzahl sein."
}
```

## Verwendung der PostWorksheetMatchNonBlanks API mit SDKs

### Spezifikation der PostWorksheetMatchNonBlanks API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}