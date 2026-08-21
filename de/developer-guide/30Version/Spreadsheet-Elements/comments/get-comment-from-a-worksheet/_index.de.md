---
title: "Arbeitsblattkommentar abrufen – Aspose.Cells Cloud API-Dokumentation"
type: docs
url: /comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: "Aspose.Cells, Arbeitsblattkommentar, API, GET, Excel"
description: "Erfahren Sie, wie Sie einen Arbeitsblattkommentar anhand des Zellnamens mit der Aspose.Cells Cloud API (v3.0) abrufen. Enthält die Anforderungs-URL, Parameter, ein cURL-Beispiel, Antwortdetails und SDK-Codebeispiele."
weight: 10
ArticleTitle: "Arbeitsblattkommentar abrufen – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST-API ruft einen Arbeitsblattkommentar anhand des Zellnamens mithilfe von **Aspose.Cells Cloud** ab.

**Voraussetzungen:** Um diesen Vorgang aufzurufen, müssen Sie ein gültiges JWT-Zugriffstoken im `Authorization`-Header (`Bearer <jwt token>`) angeben. Tokens können über den in der [Authentifizierungsanleitung](/cells/authentication/) beschriebenen Authentifizierungsfluss von Aspose.Cells Cloud abgerufen werden.

## GetWorksheetComment API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Position (URL-Pfad / Abfragezeichenfolge) | Beschreibung                                                               |
|-----------------|--------|-------------------------------------------|----------------------------------------------------------------------------|
| name            | string | URL-Pfad                                  | Der Name der Excel-Datei.                                                  |
| sheetName       | string | URL-Pfad                                  | Der Name des Arbeitsblatts, das den Kommentar enthält.                    |
| cellName        | string | URL-Pfad                                  | Die Zelladresse (z. B. **A1**), deren Kommentar abgerufen werden soll.    |
| folder          | string | Abfragezeichenfolge                       | Der Ordnerpfad, in dem das Dokument gespeichert ist.                      |
| storageName     | string | Abfragezeichenfolge                       | Der Name des Speicherdiensts.                                              |

Die <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Antwort:** Die API gibt ein JSON-Objekt zurück, das ein `Comment`-Objekt mit den folgenden Feldern enthält:

| Feld                        | Typ     | Beschreibung                                              |
|----------------------------|---------|-----------------------------------------------------------|
| `CellName`                 | string  | Adresse der Zelle (z. B. **A1**).                         |
| `Author`                   | string  | Name des Kommentarautors.                                 |
| `HtmlNote`                 | string  | Kommentarinhalt im HTML-Format (sofern vorhanden).       |
| `Note`                     | string  | Klartextversion des Kommentars.                           |
| `AutoSize`                 | boolean | Gibt an, ob die Kommentarbox automatisch skaliert wird.  |
| `IsVisible`                | boolean | Bestimmt, ob der Kommentar sichtbar ist.                 |
| `Width`                    | integer | Breite der Kommentarbox (in Zeichen).                     |
| `Height`                   | integer | Höhe der Kommentarbox (in Zeichen).                       |
| `TextHorizontalAlignment`  | string  | Horizontale Ausrichtung des Textes (z. B. **Bottom**).   |
| `TextOrientationType`      | string  | Ausrichtung des Textes (z. B. **TopToBottom**).          |
| `TextVerticalAlignment`    | string  | Vertikale Ausrichtung des Textes (z. B. **Bottom**).     |

## Häufige Fehler

- **401 Unauthorized** – Stellen Sie sicher, dass das JWT-Token gültig, nicht abgelaufen und korrekt im `Authorization`-Header platziert ist.
- **404 Not Found** – Überprüfen Sie, ob Dateiname, Arbeitsblattname und Zelladresse korrekt sind und ob die Datei im angegebenen Ordner/Speicher vorhanden ist.
- **500 Internal Server Error** – Prüfen Sie die Anforderungsnutzdaten auf fehlerhafte Daten und bestätigen Sie, dass der Dienst ordnungsgemäß funktioniert.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                               |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                      |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.     |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}