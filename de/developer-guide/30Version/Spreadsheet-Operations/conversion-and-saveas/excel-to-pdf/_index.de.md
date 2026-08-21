---
title: "Excel in PDF konvertieren – Aspose.Cells Cloud API"
ArticleTitle: "Excel in PDF konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Excel in PDF konvertieren"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, Konvertierung, Cloud API"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mit der Aspose.Cells Cloud REST API in PDF konvertieren. Enthält cURL-Beispiele, SDK-Beispiele (C#, Java, Python) und eine Anleitung zur Authentifizierung."
weight: 80
---

Diese REST API konvertiert eine Tabellendatei in eine PDF-Datei. **Voraussetzungen:** Holen Sie sich ein gültiges JWT-Access-Token, stellen Sie sicher, dass die Quell-Excel-Datei in einem unterstützten Speicher abgelegt ist, und verfügen Sie über die erforderlichen Berechtigungen, um die Konvertierungs-Endpunkt aufzurufen.

## PostConvertWorkbookToPDF API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Abfrageparameter**

| Parametername         | Typ    | Beschreibung                                                                     |
| :-------------------- | :----- | :------------------------------------------------------------------------------ |
| password              | string | Passwort zum Öffnen der Excel-Datei.                                            |
| storageName           | string | Der Name des Speichers, in dem sich die Datei befindet.                         |
| checkExcelRestriction | bool   | Ob Excel-Dateieinschränkungen beim Ändern zellbezogener Objekte erzwungen werden sollen. |

`checkExcelRestriction` ist standardmäßig `false`, falls weggelassen.

### **Anforderungstextparameter**

| Parametername | Typ  | Beschreibung                                                    |
| :------------ | :--- | :-------------------------------------------------------------- |
| datafile      | file | Die Datendatei, die als erster Teil des multipart-Inhalts gespeichert wird. |

### **Antwort**

[FileInfo](/cells/file-info/)

Die Antwort gibt ein JSON-Objekt mit Dateimetadaten zurück. Die PDF-Datei selbst kann mithilfe des bereitgestellten `FileContent` (base64-kodiert) oder über den `FileInfo`-Link heruntergeladen werden. Die API gibt ein JSON-Objekt des Typs **FileInfo** zurück:

- **FileInfo** – Objekt, das Name, Größe und base64-kodierten Inhalt der erzeugten **PDF**-Datei enthält.

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                              |
|------|-----------------------------|---------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.      |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).  |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                     |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                    |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                |

## Verwendung der PostConvertWorkbookToPDF API mit SDKs

### PostConvertWorkbookToPDF API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

**Anforderungsheader**

| Header          | Typ    | Beschreibung                                           |
| :-------------- | :----- | :----------------------------------------------------- |
| Authorization   | string | Bearer-Token, das über JWT-Authentifizierung erhalten wurde. |
| Content-Type    | string | Muss `multipart/form-data` für den Datei-Upload sein. |
| Accept          | string | `application/json`, um die Antwortmetadaten zu erhalten. |

Sie können das **cURL**-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Fügen Sie ein Access-Token in den `Authorization`-Header ein und führen Sie dann die folgende Anforderung aus.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### Verwendung der Aspose.Cells Cloud SDKs


Die Verwendung eines SDKs kann die Entwicklung vereinfachen, indem Low-Level-Details gehandhabt werden. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Weitere APIs, die diese Funktion implementieren

| **API**        | **Typ** | **Beschreibung**                                                                 | **Swagger-Link**                                                                            |
| :------------- | :------ | :------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT     | Konvertiert eine Arbeitsmappe aus dem Anforderungstext in ein angegebenes Format. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

Die [POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API ermöglicht es, eine MS-Excel-Datei mit zusätzlichen Einstellungen als PDF zu speichern und das Ergebnis im Speicher abzulegen.

Diese REST API konvertiert eine Excel-Datei in PDF.

Die [PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API ermöglicht es, eine MS-Excel-Datei mit zusätzlichen Einstellungen in PDF zu konvertieren und das Ergebnis in der Antwort zurückzugeben.

Die [GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API ermöglicht es, eine MS-Excel-Datei mit zusätzlichen Einstellungen in PDF zu konvertieren und das Ergebnis in der Antwort zurückzugeben.

Diese [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) und [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) APIs definieren eine öffentlich zugängliche Programmierschnittstelle und ermöglichen REST-Interaktionen direkt aus einem Webbrowser.

Weitere Konvertierungsoptionen finden Sie auf der Seite [Save Options](/cells/save-options/).