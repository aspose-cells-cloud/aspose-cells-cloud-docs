---
title: "Aspose.Cells Cloud Upload File API – Eine Schnittstelle zum schnellen Hochladen von Dateien in der Cloud"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Upload File API – Eine Schnittstelle zum schnellen Hochladen von Dateien in der Cloud"
linktype: "Upload File"
type: docs
url: /upload-file/
keywords: "Aspose.Cells, Datei-Upload, Excel-API, Cloud-Speicher, REST-API"
description: "Anleitung zum Hochladen von Dateien mit der Aspose.Cells Cloud API, einschließlich Anforderungsparameter, HTTP-Statuscodes, Fehlerbehandlung und Codebeispielen."
weight: 100
---

Die **uploadFile**-API ermöglicht es Entwicklern, Dateien direkt in den Cloud-Speicher hochzuladen, um sie anschließend mit Aspose Cells zu verarbeiten.

## **Aspose Cells API: Datei hochladen**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anforderungsparameter der **uploadFile**-API lauten:

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                           |
| :------------ | :---- | :--------------------------------- | :------------------------------------------------------------------------------------- |
| UploadFiles   | Datei | FormData                           | Dateien in den Cloud-Speicher hochladen.                                              |
| path          | String| Pfad                               | Der Zielpfad im Cloud-Speicher. Geben Sie den Pfad an, in den die Datei hochgeladen werden soll. |
| storageName   | String| Abfrage                            | Der Name des Speichers, in den die Datei hochgeladen werden soll.                     |

### **Antwort**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["Ergebnis des Datei-Uploads"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["Liste der hochgeladenen Dateinamen"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["Liste der Fehler."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

Die API gibt die folgenden HTTP-Statuscodes zurück:

| Statuscode                    | Beschreibung                                          |
| ----------------------------- | ----------------------------------------------------- |
| **200 OK**                    | Datei erfolgreich hochgeladen.                        |
| **400 Bad Request**           | Ungültige Parameter oder fehlerhafte Anforderung.    |
| **401 Unauthorized**          | Fehlender oder ungültiges Authentifizierungstoken.   |
| **403 Forbidden**             | Unzureichende Berechtigungen für den angegebenen Speicher. |
| **500 Internal Server Error** | Unerwarteter Serverfehler.                            |

## Wie verwendet man die Upload-Datei-API mit SDKs?

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/UploadFile) bietet eine detaillierte Beschreibung der API und ermöglicht es Entwicklern, direkt über einen Webbrowser mit ihr zu interagieren.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs verbessert die Entwicklungsproduktivität, indem sie sich um Low-Level-Details kümmert und Entwicklern so die Möglichkeit gibt, sich auf die eigentlichen Projektaufgaben zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**Siehe auch**

- [Download File API](/download-file/) – Abrufen einer Datei aus dem Cloud-Speicher.
- [Copy File API](/copy-file/) – Kopieren einer Datei innerhalb des Cloud-Speichers.
- [Delete File API](/delete-file/) – Entfernen einer Datei aus dem Cloud-Speicher.