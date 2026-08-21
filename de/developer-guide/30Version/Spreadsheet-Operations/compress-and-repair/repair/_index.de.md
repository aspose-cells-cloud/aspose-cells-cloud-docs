---
title: "Excel-Dateien reparieren"
second_title: "Dokument"
type: docs
linktitle: "Excel-Dateien reparieren"
url: /repair-excel-files/
keywords: "Aspose Cells, Excel-Reparatur-API, beschädigte XLSX, Wiederherstellung von Tabellenkalkulationen, Cloud-API"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um beschädigte Excel-Dateien (XLS, XLSX, XLSM, XLSB, ODS) zu reparieren. Laden Sie eine oder mehrere Dateien hoch, wählen Sie das Ausgabeformat aus und erhalten Sie die reparierten Dateien als Base64-codierten String. Keine Installation erforderlich."
weight: 39
---

Diese REST-API ermöglicht es Ihnen, **Excel-Dateien zu reparieren**.

- Reparieren Sie XLS-, XLSX-, XLSM-, XLSB-, ODS- und weitere Tabellenkalkulationsformate.  
- Unterstützt das Hochladen mehrerer Dateien in einer einzigen Anfrage.

Aspose.Cells Cloud Excel-Reparatur stellt Daten aus beschädigten Excel-Dateien online wieder her, ohne dass eine Installation erforderlich ist. Beschädigte Excel-Dateien sind problematisch, da sie nicht geöffnet werden können. Sie können die Aspose.Cells Cloud Excel-Reparatur-Anwendung ausprobieren, um Daten aus solchen Dateien wiederherzustellen.

## REST-API

Der Endpunkt **Excel-Dateien reparieren** repariert beschädigte Tabellenkalkulationsdateien und gibt den reparierten Inhalt zurück.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter

| Parametername | Typ   | Standort                     | Beschreibung |
|---------------|-------|------------------------------|--------------|
| file          | Datei | formData (multipart)         | Hochzuladende Datei |
| format        | string | query                       | Gewünschtes Ausgabeformat. Falls weggelassen (null), wird das Ausgabeformat standardmäßig dem Format der Eingabedatei entsprechen. |

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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                             |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größeinschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## So verwenden Sie die PostRepair-API mit SDKs

### PostRepair-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

Bei Erfolg gibt der Dienst HTTP 200 mit einer JSON-Payload zurück, die ein `Files`-Array enthält. Bei Fehlersituationen verwendet die API standardmäßige HTTP-Statuscodes:

- **400 Bad Request** – Ungültige Parameter oder nicht reparierbare Datei.  
- **401 Unauthorized** – Fehlendes oder ungültiges JWT-Token.  
- **413 Payload Too Large** – Die hochgeladene Datei überschreitet die zulässige Größe.  
- **500 Internal Server Error** – Unerwarteter serverseitiger Fehler.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Methode, um die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf die Aufgaben Ihres Projekts zu konzentrieren. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) mit einer vollständigen Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}