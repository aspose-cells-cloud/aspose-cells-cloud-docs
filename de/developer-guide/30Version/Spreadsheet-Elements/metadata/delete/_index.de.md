---
title: "Metadaten aus Excel-Dateien entfernen"
second_title: "Dokument"
linktitle: "Entfernen ohne Speicherung"
type: docs
url: /de/metadata/delete/
keywords: "Aspose.Cells, Metadaten entfernen, Excel-API, Arbeitsmappen-Eigenschaften"
description: "Entfernen Sie Arbeitsmappen-Metadaten (Autor, Titel, benutzerdefiniert) über die Aspose.Cells Cloud API. Enthält Endpunkt, Authentifizierung, Parameter sowie cURL- und SDK-Beispiele."
weight: 55
ArticleTitle: "Metadaten aus Excel-Dateien entfernen – Aspose.Cells Cloud-Dokumentation"
---

**Übersicht**  
Der Vorgang „Metadaten entfernen“ löscht dauerhaft alle Arbeitsmappen-Eigenschaften (standardmäßig und benutzerdefiniert) aus den hochgeladenen Excel-Dateien und gibt die verarbeiteten Dateien in der Antwort zurück.

**Voraussetzungen**  
- Ein gültiges Aspose.Cells Cloud JWT-Token (erhältlich über den OAuth 2.0-Authentifizierungsflow).  
- API-Version **v3.0** (der in diesem Beispiel verwendete Endpunkt).  
- Für die SDK-Nutzung: Installieren Sie das passende Aspose.Cells Cloud SDK für Ihre Sprache (z. B. über NuGet, Maven, npm, pip, CPAN oder Go-Module).

Diese REST-API entfernt **Metadaten** aus einer oder mehreren Excel-Dateien. Sie löscht Arbeitsmappen-Eigenschaften wie Autor, Titel und benutzerdefinierte Daten und gibt die bereinigten Dateien zurück.

## a API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername | Typ    | Ort      | Beschreibung                                           |
|---------------|--------|----------|--------------------------------------------------------|
| file          | Datei  | formData | Excel-Datei zum Hochladen zum Entfernen von **Metadaten** |
| type          | string | query    | Vorgangstyp; setzen Sie auf **all**, um alle **Metadaten** zu entfernen |

Die <a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
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
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Fehlerantworten** können folgende enthalten:

- **400 Bad Request** – fehlende Datei oder ungültiger `type`-Wert.
- **401 Unauthorized** – ungültiges oder fehlendes JWT-Token.
- **500 Internal Server Error** – serverseitiger Verarbeitungsfehler.

Die API gibt ein JSON-Objekt zurück, das ein `Error`-Feld mit Details für jeden Fall enthält.

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Metadaten entfernt, Datei zurückgegeben |
| 400 | Bad Request | Fehlende Datei oder ungültiger `type`-Wert |
| 401 | Unauthorized | Ungültiges oder fehlendes JWT-Token |
| 500 | Internal Server Error | Serverseitiger Verarbeitungsfehler |

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}