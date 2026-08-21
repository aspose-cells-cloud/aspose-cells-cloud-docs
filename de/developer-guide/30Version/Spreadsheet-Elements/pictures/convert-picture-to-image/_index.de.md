---
title: "Aspose.Cells Cloud API – Bild aus Arbeitsblatt abrufen"
second_title: "Dokument"
linktitle: "Abrufen"
type: docs
url: /de/pictures/get/
aliases: [  /de/convert-picture-to-image/ ]
keywords: "Aspose.Cells, Bild abrufen, API, Excel, Cloud, REST"
description: "Rufen Sie ein bestimmtes Bild aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API ab. Enthält Endpunkt, Parameter, Authentifizierungsschritte, Antwortcodes und Codebeispiele."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Bild aus Arbeitsblatt abrufen"
---

Diese REST API ruft ein Bild anhand seines nullbasierten Indexes aus einem Excel-Arbeitsblatt ab.

## REST API

Um diesen Endpunkt aufzurufen, müssen Sie ein gültiges JWT-Access-Token im **Authorization**-Header angeben. Tokens werden über den Aspose.Cells Cloud-Authentifizierungsfluss erhalten und erfordern die entsprechenden Scopes für den Dateizugriff. Einzelheiten zum Erwerb eines Tokens finden Sie im allgemeinen Leitfaden zur **Authentifizierung**.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Anforderungsparameter

| Parametername  | Typ     | Position | Beschreibung                                                                                                         |
| -------------- | ------- | -------- | -------------------------------------------------------------------------------------------------------------------- |
| name           | string  | path     | Name der Excel-Datei.                                                                                                |
| sheetName      | string  | path     | Name des Arbeitsblatts.                                                                                              |
| pictureIndex   | integer | path     | Nullbasierter Index des Bildes.                                                                                      |
| format         | string  | query    | Gewünschtes Exportformat (z. B. png, jpg, bmp, gif, tiff). Wenn weggelassen, wird das Bild im ursprünglichen Format zurückgegeben. |
| folder         | string  | query    | Ordner, der das Dokument enthält.                                                                                    |
| storageName    | string  | query    | Name des Speicherorts.                                                                                               |

### Fehlerantworten

| HTTP-Code | Beschreibung                                                                     |
| --------- | -------------------------------------------------------------------------------- |
| 401       | Nicht autorisiert – fehlendes oder ungültiges Token.                            |
| 404       | Nicht gefunden – die angegebene Datei, das Arbeitsblatt oder der Seitenumbruchindex existiert nicht. |
| 400       | Ungültige Anforderung – fehlerhafte Anforderungssyntax oder ungültige Parameter. |
| 500       | Interner Serverfehler – ein unerwarteter Zustand ist aufgetreten.               |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# Binäre Bilddaten (PNG) werden im Antworttext zurückgegeben.
# Beispiel: base64-kodiertes Snippet
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}