---
title: "Excel-Arbeitsmappe speichern – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Speichern als"
type: docs
url: /de/save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, Speichern als, PDF, CSV, JSON, Markdown, REST API"
description: "Speichern Sie Excel-Arbeitsmappen in PDF, CSV, JSON, Markdown und anderen Formaten mithilfe der Aspose.Cells Cloud REST API."
weight: 30
---

Diese REST API ermöglicht es Ihnen, **eine Excel-Datei in verschiedenen Formaten zu speichern**.  
Bevor Sie diesen Endpunkt aufrufen, stellen Sie sicher, dass Sie über ein gültiges OAuth 2.0-Access-Token verfügen und sich die Quell-Arbeitsmappe in Ihrem Aspose Cloud-Speicher befindet.

**Voraussetzungen**  
1. Beschaffen Sie ein JWT-Access-Token und fügen Sie es in den `Authorization: Bearer <token>`-Header jeder Anfrage ein.  
2. Laden Sie die Quell-Arbeitsmappe in den Aspose Cloud-Speicher hoch (oder bestätigen Sie, dass sie bereits vorhanden ist).  
3. Kennen Sie den Speichernamen und den Ordnerpfad, in dem sich die Arbeitsmappe befindet.

## PostWorkbookSaveAs API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Pfadparameter**

| Parametername | Typ    | Beschreibung                        |
| ------------- | ------ | ----------------------------------- |
| name          | string | Der Name der Excel-Datei.           |

### **Abfrageparameter**

| Parametername         | Typ    | Beschreibung                                                                                     |
| --------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| newfilename           | string | Neuer Dateiname für das gespeicherte Dokument.                                                  |
| isAutoFitRows         | string | Wenn `true`, werden alle Zeilen in der Arbeitsmappe automatisch angepasst. Standard ist `false`. |
| isAutoFitColumns      | string | Wenn `true`, werden die Spaltenbreiten in der Arbeitsmappe automatisch angepasst. Standard ist `false`. |
| folder                | string | Ordner, der die ursprüngliche Arbeitsmappe enthält.                                             |
| storageName           | string | Name des Speichers, in dem sich die Quelldatei befindet.                                        |
| outStorageName        | string | Name des Speichers, in dem die Ausgabedatei gespeichert wird.                                   |
| checkExcelRestriction | bool   | Gibt an, ob Excel-Einschränkungen beim Ändern von Zellen oder zugehörigen Objekten erzwungen werden sollen. |
| region                | string | Regionale Einstellungen, die auf die Arbeitsmappe angewendet werden.                            |
| pageWideFitOnPerSheet | bool   | Passt die Seitenbreite an jedes Arbeitsblatt an, wenn konvertiert wird.                         |
| pageTallFitOnPerSheet | bool   | Passt die Seitenhöhe an jedes Arbeitsblatt an, wenn konvertiert wird.                           |
| sheetName             | string | Name des Arbeitsblatts, das konvertiert werden soll.                                            |
| pageIndex             | string | Index der Seite, die innerhalb des angegebenen Arbeitsblatts konvertiert werden soll (erfordert `sheetName`). |
| onePagePerSheet       | bool   | Generiert beim Konvertieren in PDF eine Seite pro Arbeitsblatt.                                 |

### **Anforderungstextparameter**

| Parametername | Typ    | Beschreibung                                                       |
| ------------- | ------ | ------------------------------------------------------------------ |
| SaveOptions   | Object | Speicheroptionen, die im zweiten Teil der Multipart-Anfrage übergeben werden. |

**Beispiel für Anforderungstext (JSON-Teil der Multipart-Anfrage)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Antwort

Die API gibt ein `SaveResponse`-Objekt zurück.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.        |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Verwendung der PostWorkbookSaveAs API mit SDKs

### PostWorkbookSaveAs API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können **cURL** verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Schauen Sie sich das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

Weitere Konvertierungsszenarien finden Sie in den Anleitungen [Konvertieren von Excel in PDF](/convert-excel-to-pdf/) und [Exportieren von Excel in CSV](/export-excel-to-csv/).