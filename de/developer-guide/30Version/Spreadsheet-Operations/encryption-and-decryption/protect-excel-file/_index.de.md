---
title: "Schützen einer Excel-Arbeitsmappe mit der Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Schützen einer Excel-Datei"
type: docs
url: /protect-excel-file/
aliases: [/protect-excel-workbooks/, /workbook/protect/]
keywords: "Aspose.Cells, Excel-Schutz, API, REST, SDK"
description: "Erfahren Sie, wie Sie eine Excel-Arbeitsmappe über die Aspose.Cells Cloud REST API schützen können. Enthält Authentifizierungsschritte, Abfrage- und Body-Parameter, cURL-Anforderung und SDK-Codebeispiele für C#, Java, PHP, Ruby, Node.js, Python, Perl und Go."
weight: 30
ArticleTitle: "Schützen einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud API"
---

Diese REST API **schützt** eine Excel-Arbeitsmappe und ermöglicht es Ihnen, eine Excel-Arbeitsmappe sicher mit Passwort und Schutzeinstellungen über die Aspose.Cells Cloud zu schützen.

## PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Abfrageparameter

| Parametername     | Typ    | Beschreibung                                                         |
| ----------------- | ------ | -------------------------------------------------------------------- |
| folder            | string | Ordner, der die Quell-Arbeitsmappe enthält. _(optional)_            |
| storageName       | string | Name des Speicherorts. _(optional; Standard = "Default")_           |

### Body-Parameter der Anforderung

| Parametername | Typ                       | Beschreibung                                              |
| ------------- | ------------------------- | --------------------------------------------------------- |
| protection    | WorkbookProtectionRequest | Objekt, das die Schutzeinstellungen für die Arbeitsmappe definiert. |

#### WorkbookProtectionRequest

| Parametername   | Typ    | Beschreibung                                                                                                                                             |
| --------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType  | string | Art des anzuwendenden Schutzes. Zulässige Werte (Groß-/Kleinschreibung wird ignoriert): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password        | string |OPTIONALES Passwort zur Festlegung des Schutzes.                                                                                                         |

### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.                |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Verwendung der PostProtectDocument API mit SDKs

### Voraussetzungen

Bevor Sie die API aufrufen, stellen Sie sicher, dass Sie die folgenden Schritte ausgeführt haben:

- **Holen Sie sich ein JWT-Zugriffstoken** mithilfe des in der Sicherheitssection beschriebenen Authentifizierungsflusses.  
- **Laden Sie die Arbeitsmappe** in Ihren Aspose Cloud-Speicher hoch oder bestätigen Sie, dass sie bereits im Zielordner vorhanden ist.  
- **Kennen Sie den Speichernamen** (Standard ist `"Default"`, sofern nicht angegeben) und den genauen Dateinamen, den Sie schützen möchten.

### Spezifikation der PostProtectDocument API

Die <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Beispiel: Schützen einer Arbeitsmappe mit cURL

1. Holen Sie sich ein Zugriffstoken wie in **Voraussetzungen / Authentifizierung** beschrieben.  
2. Führen Sie die Anforderung aus:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   Die Antwort enthält ein Statusobjekt, das bestätigt, dass der Schutz erfolgreich war.

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um mit Aspose.Cells Cloud zu entwickeln. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> finden Sie eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufrufen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Beispiel für vollständige Antwort

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```