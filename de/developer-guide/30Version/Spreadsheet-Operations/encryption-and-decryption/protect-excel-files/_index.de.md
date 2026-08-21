---
title: "Excel-Dateien schützen"
second_title: "Dokument"
linktitle: "Excel-Dateien verschlüsseln"
type: docs
url: /protect-excel-files/
aliases:
  [
    /protect/without-storage/,
    /protect/without-using-storage/,
    /protect/without-using-storage/,
  ]
keywords: "Aspose.Cells, Excel-Schutz-API, Excel-Arbeitsmappe verschlüsseln, Cloud-Tabellensicherheit, REST-API"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um Excel-Dateien zu schützen. Dieser Leitfaden zeigt, wie Arbeitsmappen über HTTP POST, cURL und SDKs für mehrere Programmiersprachen verschlüsselt werden können (Stand 2026)."
weight: 40
---

Diese REST-API schützt Excel-Dateien.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Anforderungsparameter

| Parametername | Typ   | Speicherort                  | Beschreibung                                |
| -------------- | ------ | ------------------------- | ------------------------------------- |
| file           | Datei  | formData (body)           | Hochzuladende Datei                        |
| password       | Zeichenfolge | Abfragezeichenfolge (`password`) | Passwort zum Schutz der Arbeitsmappe |

### Antwort


```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "geschützter Dateiname: smaple1.xlsx",
      "FileSize": Größe,
      "FileContent": "-----Base64-Zeichenfolge von sample1-----"
    },
    {
      "Filename": "geschützter Dateiname: sample2.xlsx",
      "FileSize": Größe,
      "FileContent": "-----Base64-Zeichenfolge von sample2-----"
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                     | Beschreibung                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zur Operation. |
| 400  | Ungültige Anforderung                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Anforderungstext zu groß           | Hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Interner Serverfehler       | Unerwarteter Serverfehler. |
## Verwendung der PostProtect-API mit SDKs

### PostProtect-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-Zeichenfolge von sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-Zeichenfolge von sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Fehlerbehandlung**

– Die API kann die folgenden Statuscodes zurückgeben:

| HTTP-Code | Bedeutung                                 | Beispiel-JSON-Fehlerpayload                          |
| --------- | --------------------------------------- | --------------------------------------------------- |
| 400       | Ungültige Anforderung (z. B. fehlende Datei)        | `{"Code":400,"Message":"Datei ist erforderlich."}`        |
| 401       | Nicht autorisiert (ungültiges oder fehlendes Token) | `{"Code":401,"Message":"Ungültiges Zugriffstoken."}`    |
| 403       | Verboten (unzureichende Berechtigungen)    | `{"Code":403,"Message":"Zugriff verweigert."}`           |
| 500       | Interner Serverfehler                   | `{"Code":500,"Message":"Unerwarteter Serverfehler."}` |

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Details der unteren Schicht, sodass Sie sich auf Ihre Projektziele konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}