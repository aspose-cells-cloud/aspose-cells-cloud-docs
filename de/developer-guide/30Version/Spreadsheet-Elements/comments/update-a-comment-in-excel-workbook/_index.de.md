---
title: "Aktualisieren eines Zellenkommentars in einem Arbeitsblatt"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, Arbeitsblatt, Zellenkommentar, Aktualisieren eines Arbeitsblatt-Kommentars, Kommentarobjekt"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um einen Zellenkommentar in einem Excel-Arbeitsblatt zu aktualisieren, einschließlich Anforderungsdetails, Antwortcodes und SDK-Beispielen."
weight: 30
ArticleTitle: "Arbeitsblatt-Zellenkommentar aktualisieren – Aspose.Cells Cloud API"
---

Diese REST API aktualisiert einen Kommentar in einer Zelle eines Arbeitsblatts. Verwenden Sie diesen Endpunkt, um **einen Arbeitsblatt-Kommentar** in einer Excel-Datei zu aktualisieren.

**Voraussetzungen:**
- Ein gültiges OAuth/JWT-Zugriffstoken muss im `Authorization`-Header enthalten sein.
- Die Arbeitsmappe muss an einem unterstützten Speicherort in der Cloud gespeichert sein (geben Sie `folder` und optional `storageName` an).

## PostWorksheetComment API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                                                                 |
|-----------------|--------|--------|------------------------------------------------------------------------------|
| name            | string | path   | Der Name der Excel-Datei.                                                   |
| sheetName       | string | path   | Der Name des Arbeitsblatts, das die Zelle enthält.                          |
| cellName        | string | path   | Die Adresse der Zelle (z. B. **A1**).                                       |
| comment         | object | body   | Ein **Comment**-Objekt, das den hinzuzufügenden oder zu aktualisierenden Kommentar definiert. |
| folder          | string | query  | Der Ordner, in dem das Dokument gespeichert ist.                            |
| storageName     | string | query  | Der Name des Speicherdiensts.                                                |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Mögliche Antwortstatuscodes:

| Code | Beschreibung                                     |
|------|--------------------------------------------------|
| 200  | Kommentar erfolgreich aktualisiert.             |
| 400  | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert – Authentifizierung fehlgeschlagen. |
| 404  | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Kommentar existiert nicht. |
| 500  | Interner Serverfehler.                          |

**Hinweise / Tipps:**
- Die maximale Länge eines Kommentars beträgt 1024 Zeichen.
- Unterstützte Zeichen sind UTF-8; steuernde Zeichen sollten vermieden werden.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, mit Aspose.Cells Cloud zu entwickeln. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihr Projekt konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

Verwandte Vorgänge:
- [Arbeitsblatt-Kommentar abrufen](/comments/get/)
- [Arbeitsblatt-Kommentar hinzufügen](/comments/add/)
- [Arbeitsblatt-Kommentar löschen](/comments/delete/)