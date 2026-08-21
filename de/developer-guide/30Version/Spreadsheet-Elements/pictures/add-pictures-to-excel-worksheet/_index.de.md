---
title: "Ein Bild in einer Excel-Datei hinzufügen"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /pictures/add/
aliases: [/add-pictures-to-excel-worksheet/]
keywords: "Aspose.Cells, Excel, Bild hinzufügen, REST API"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um ein Bild zu einem Excel-Arbeitsblatt hinzuzufügen. SDKs für Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift vereinfachen die plattformübergreifende Integration."
weight: 20
ArticleTitle: "Ein Bild zu einem Excel-Arbeitsblatt hinzufügen – Aspose.Cells Cloud API"
---

Diese REST API fügt ein neues Bild zu einem Excel-Arbeitsblatt hinzu.  
**Voraussetzungen:** Sie benötigen einen gültigen Aspose Cloud-Authentifizierungstoken, eine bestehende Arbeitsmappe, die in einem unterstützten Speicher gespeichert ist, sowie entsprechende Berechtigungen zum Bearbeiten des Arbeitsblatts.

## PutWorksheetAddPicture API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ    | Ort    | Beschreibung                                                                                   |
| ----------------- | ------ | ------ | ---------------------------------------------------------------------------------------------- |
| name              | string | path   | Der Name der Arbeitsmappe.                                                                     |
| sheetName         | string | path   | Der Name des Arbeitsblatts.                                                                    |
| picture           | object | body   | Bildobjekt (binäre Daten).                                                                     |
| upperLeftRow      | integer| query  | Nullbasierter Index der oberen linken Zeile, an der das Bild platziert wird.                  |
| upperLeftColumn   | integer| query  | Nullbasierter Index der oberen linken Spalte, an der das Bild platziert wird.                 |
| lowerRightRow     | integer| query  | Nullbasierter Index der unteren rechten Zeile des Bildbereichs.                               |
| lowerRightColumn  | integer| query  | Nullbasierter Index der unteren rechten Spalte des Bildbereichs.                              |
| picturePath       | string | query  | Pfad zur Bilddatei; falls weggelassen, müssen die Bilddaten im Anforderungstext übergeben werden. |
| folder            | string | query  | Der Ordner, der die Arbeitsmappe enthält.                                                      |
| storageName       | string | query  | Der Name des Speicherdienstes.                                                                 |

**Hinweis zum Anforderungstext:** Wenn `picturePath` weggelassen wird, senden Sie die binären Bilddaten im Anforderungstext im Format `multipart/form-data`.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zur Operation.       |
| 400  | Ungültige Anforderung       | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Nicht autorisiert           | Ungültiger oder fehlender JWT-Token.                                         |
| 413  | Anforderungstext zu groß    | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Interner Serverfehler       | Unerwarteter Serverfehler.                                                   |

**Beispiel für 200-Antwortschema**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**Hinweis:** Die maximale Bildgröße beträgt 10 MB; größere Dateien werden mit einer `400 Bad Request`-Antwort abgelehnt.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Hinweis:** Unterstützte Bildformate sind PNG, JPEG, BMP und GIF. Die maximale Bildgröße beträgt 10 MB; größere Dateien werden mit einer `400 Bad Request`-Antwort abgelehnt.