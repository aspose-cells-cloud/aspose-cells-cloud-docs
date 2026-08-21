---
title: "Excel zu TIFF"
second_title: "Dokument"
linketitle: "Excel zu TIFF"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/, /convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud, Excel-zu-TIFF-Konvertierung, REST API, cURL, SDK, .NET, Java, Python, Bildexport"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud API in hochwertige TIFF-Bilder konvertieren können. Detaillierte cURL-Befehle, SDK-Beispiele (C#, Java, Python, …), Authentifizierungsschritte und Fehlerbehandlung."
weight: 90
---

Die **Convert**-, **SaveAs**- und **Export**-Endpunkte von Aspose.Cells Cloud ermöglichen es Ihnen, eine Excel-Arbeitsmappe in ein TIFF-Bild umzuwandeln.  
Sie können diese Endpunkte direkt mit **cURL** oder über eines der unterstützten SDKs aufrufen.

## REST API

| **API**                | **Methode** | **Zweck**                                                                                                      | **Swagger-Link**                                                                            |
| ---------------------- | ----------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT         | Wandelt die in der Anforderungsnachricht übergebene Arbeitsmappe in das angegebene Format (TIFF) um.           | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET         | Exportiert die benannte Arbeitsmappe in ein anderes Format (TIFF) und gibt das Ergebnis in der Antwort zurück. | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST        | Speichert die Arbeitsmappe in einem gewählten Format (TIFF) und speichert das Ergebnis im Cloud-Speicher.      | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

Diese Endpunkte sind öffentlich zugänglich und können direkt aus einem Webbrowser oder beliebigen HTTP-Clients aufgerufen werden.

### cURL-Beispiele

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑content>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **Hinweis:**
>
> - Der **Convert**-Anforderungstext muss die Datei (oder einen Verweis auf eine gespeicherte Datei) sowie das gewünschte `SaveFormat` enthalten.
> - Bei der **Export**-Anforderung ist kein Anforderungstext erforderlich; das Format wird über die Abfragezeichenfolge (`format=tiff`) übergeben.

## Fehlerbehandlung

| **Statuscode** | **Bedeutung**         | **Typische Ursache**                        |
| -------------- | --------------------- | ------------------------------------------- |
| 200            | Erfolg                | Das TIFF-Bild wird zurückgegeben (Binärstream). |
| 400            | Ungültige Anfrage     | Fehlende oder fehlerhafte Parameter.        |
| 401            | Nicht autorisiert     | Ungültiges oder fehlendes JWT-Token.        |
| 404            | Nicht gefunden        | Die angegebene Arbeitsmappe existiert nicht. |
| 500            | Interner Serverfehler | Unerwarteter Serverzustand.                 |

Im Fehlerfall gibt die API eine JSON-Nutzlast mit den Feldern `Code`, `Message` und optional `Description` zurück.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die niederwertigen Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}