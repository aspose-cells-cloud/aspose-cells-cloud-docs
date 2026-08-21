---
title: "Einfügen eines vertikalen Seitenumbruchs"
second_title: "Dokument"
linktitle: "Einfügen eines vertikalen Seitenumbruchs"
type: docs
url: /de/page-breaks/add-vertical-page-break/
aliases: [  /de/insert-vertical-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, vertikaler Seitenumbruch, REST-API, Excel, SDK, cURL"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST-API (v3.0) einen vertikalen Seitenumbruch in ein Excel-Arbeitsblatt einfügen. Enthält die Anforderungssyntax, ein cURL-Beispiel, SDK-Beispiele, eine Anleitung zur Authentifizierung sowie Details zur Fehlerbehandlung."
weight: 40
ArticleTitle: "Einfügen eines vertikalen Seitenumbruchs – Aspose.Cells Cloud API"
---

Diese REST-API fügt einen vertikalen Seitenumbruch in ein Arbeitsblatt ein.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST-API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Anforderungsparameter

| Parametername   | Typ     | Speicherort | Beschreibung                                                                 |
|-----------------|---------|-------------|------------------------------------------------------------------------------|
| name            | string  | path        | Der Name der Excel-Arbeitsmappe.                                            |
| sheetName       | string  | path        | Der Name des Arbeitsblatts, in das der Seitenumbruch eingefügt wird.       |
| cellname        | string  | query       | Die Zellreferenz (z. B. **A1**), die die Position des Seitenumbruchs definiert. |
| column          | integer | query       | Der nullbasierte Index der Spalte, in der der Seitenumbruch beginnt.       |
| row             | integer | query       | Der nullbasierte Index der Zeile, in der der Seitenumbruch beginnt.        |
| startRow        | integer | query       | Die erste Zeile des Bereichs des Seitenumbruchs.                            |
| endRow          | integer | query       | Die letzte Zeile des Bereichs des Seitenumbruchs.                           |
| folder          | string  | query       | Der Ordnerpfad im Speicher, in dem sich die Arbeitsmappe befindet.         |
| storageName     | string  | query       | Der Name des Speicherdienstes.                                              |

**Pflichtparameter** – Entweder `cellname` **oder** `column` muss angegeben werden. Bei Verwendung von `column` können Sie zusätzlich `row`, `startRow` und `endRow` angeben, um einen Bereich zu definieren. Alle anderen Felder sind optional.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### cURL-Beispiel

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Antwort

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größeinschränkung.                 |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene und ermöglicht es Ihnen, sich auf die Aufgaben Ihres Projekts zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}
---