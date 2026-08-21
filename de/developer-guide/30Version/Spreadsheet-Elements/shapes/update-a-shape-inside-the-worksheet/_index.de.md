---
title: "Eine Form auf einem Excel-Arbeitsblatt aktualisieren"
second_title: "Dokument"
linktitle: "Aktualisieren"
type: docs
url: /de/shapes/update/
aliases: [  /de/update-a-shape-inside-the-worksheet/ ]
keywords: "Form in Excel aktualisieren, Aspose.Cells Cloud, Excel-Form-Aktualisierung, REST-API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Erfahren Sie, wie Sie eine Form in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API aktualisieren. Enthält HTTPS-Endpunkt, Authentifizierungsdetails, DTO-Schema, Schritt-für-Schritt-Anleitung, cURL-Beispiel und SDK-Codebeispiele für mehrere Sprachen."
ArticleTitle: "Eine Form auf einem Excel-Arbeitsblatt aktualisieren – Aspose.Cells Cloud API"
weight: 31
---

Diese REST-API aktualisiert eine Form in einem Excel-Arbeitsblatt.

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### Anforderungsparameter

| Parametername   | Typ     | Ort     | Beschreibung                                                                                  |
| --------------- | ------- | ------- | --------------------------------------------------------------------------------------------- |
| **name**        | string  | path    | Der Name der Arbeitsmappe.                                                                    |
| **sheetName**   | string  | path    | Der Name des Arbeitsblatts, das die Form enthält.                                             |
| **shapeindex**  | integer | path    | Der nullbasierte Index der Form innerhalb des Arbeitsblatts.                                  |
| **dto**         | object  | body    | Das Datenübertragungsobjekt für die Form, das die aktualisierten Eigenschaften enthält (siehe _DTO-Schema_ weiter unten). |
| **folder**      | string  | query   | Der Ordner, in dem die Arbeitsmappe gespeichert ist.                                          |
| **storageName** | string  | query   | Der Name des Aspose Cloud-Speichers.                                                          |

### DTO-Schema

Das `dto`-Objekt enthält die Eigenschaften, die aktualisiert werden können. Alle Felder sind optional, sofern nicht anders angegeben.

| Feld                | Typ     | Erforderlich | Beschreibung                                                                      |
| ------------------- | ------- | ------------ | --------------------------------------------------------------------------------- |
| **Name**            | string  | Nein         | Neuer Name für die Form.                                                          |
| **UpperLeftRow**    | integer | Nein         | Zeilenindex der oberen linken Ecke der Form.                                      |
| **UpperLeftColumn** | integer | Nein         | Spaltenindex der oberen linken Ecke der Form.                                     |
| **Width**           | integer | Nein         | Breite der Form (in Punkten).                                                     |
| **Height**          | integer | Nein         | Höhe der Form (in Punkten).                                                       |
| **RotationAngle**   | integer | Nein         | Drehwinkel in Grad.                                                               |
| **IsHidden**        | boolean | Nein         | `true`, um die Form auszublenden.                                                |
| **IsLocked**        | boolean | Nein         | `true`, um die Form zu sperren.                                                  |
| **Font**            | object  | Nein         | Schriftarteinstellungen (siehe OpenAPI-Spezifikation für Untereigenschaften).    |
| **...**             | …       | Nein         | Weitere Eigenschaften wie `HtmlText`, `AlternativeText`, `ZOrderPosition`, etc.  |

> Für eine vollständige Liste verweisen Sie bitte auf die offizielle OpenAPI-Spezifikation: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### Anforderungsheader

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(das JWT-Token aus dem _Authentifizierungsschritt_)_

### Anforderungstext (Beispiel)

```json
{
  "Name": "MeineForm",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## Beispiel mit cURL (Befehlszeilentool)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "AktualisierteForm",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Antwort

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Fehlerbehandlung** – Die API kann folgende Statuscodes zurückgeben:

| Code | Bedeutung             | Typische Ursache                                     |
| ---- | --------------------- | ---------------------------------------------------- |
| 400  | Bad Request           | Ungültiges JSON oder fehlende erforderliche Felder. |
| 401  | Unauthorized          | Fehlendes oder ungültiges JWT-Token.               |
| 404  | Not Found             | Arbeitsmappe, Arbeitsblatt oder Formindex existiert nicht. |
| 500  | Internal Server Error | Unerwartetes serverseitiges Problem.                |

**Beispiel für Fehlerantworten**

*400 – Bad Request*

```json
{
  "Code": 400,
  "Message": "Ungültige Anforderungsnutzlast. Feld 'Name' überschreitet maximale Länge."
}
```

*401 – Unauthorized*

```json
{
  "Code": 401,
  "Message": "Authentifizierung fehlgeschlagen. Ungültiges oder abgelaufenes JWT-Token."
}
```

*404 – Not Found*

```json
{
  "Code": 404,
  "Message": "Die angegebene Arbeitsmappe, das Arbeitsblatt oder der Formindex wurde nicht gefunden."
}
```

*500 – Internal Server Error*

```json
{
  "Code": 500,
  "Message": "Auf dem Server ist ein unerwarteter Fehler aufgetreten."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}