---
title: "Aspose.Cells Cloud – Excel-Bereich in HTML konvertieren"
description: "Konvertieren Sie einen bestimmten Bereich einer Excel-Datei (z. B. A1:C10) mit der Aspose.Cells Cloud REST API in eine HTML-Datei. Enthält Authentifizierung, Anforderungsbeispiele, Antwortverarbeitung, SDK-Snippets und Fehlercodes."
keywords: "Aspose.Cells, Excel zu HTML, Bereichskonvertierung, Cloud-API, Tabellenkalkulation"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Konvertieren Sie einen ausgewählten Bereich einer lokalen Excel-Arbeitsmappe direkt über Aspose.Cells Cloud in eine HTML-Datei. Die Konvertierung erfolgt vollständig auf dem Cloud-Server, sodass Sie weder die gesamte Arbeitsmappe hochladen noch Excel lokal installieren müssen.

## Convert Range to HTML API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

Der Anforderungstext ist `multipart/form-data` und enthält die Tabellendatei. Alle weiteren Optionen werden als Abfrageparameter übergeben.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Name               | Typ     | Speicherort | Erforderlich | Beschreibung                                                              |
| ------------------ | ------- | ----------- | ------------ | ------------------------------------------------------------------------- |
| **Spreadsheet**    | Datei   | FormData    | Ja           | Die zu konvertierende Excel-Arbeitsmappe.                                 |
| **worksheet**      | String  | Query       | Ja           | Name des Arbeitsblatts, das den Bereich enthält.                          |
| **range**          | String  | Query       | Ja           | Umzuwandelnder Zellbereich, z. B. `A1:C10`.                               |
| **outPath**        | String  | Query       | Nein         | Ordnerpfad, in dem die resultierende HTML-Datei gespeichert werden soll (Standard: `null`). |
| **outStorageName** | String  | Query       | Nein         | Name des Speicherdienstes für die Ausgabedatei.                           |
| **fontsLocation**  | String  | Query       | Nein         | Pfad zu einem benutzerdefinierten Schriftartenordner.                     |
| **AutoRowsFit**    | Boolean | Query       | Nein         | Alle Zeilen im Arbeitsblatt automatisch anpassen.                         |
| **AutoColumnsFit** | Boolean | Query       | Nein         | Alle Spalten im Arbeitsblatt automatisch anpassen.                        |
| **region**         | String  | Query       | Nein         | Gebietsschemabezeichner (z. B. `de-DE`, `fr-FR`). Beeinflusst Zahlen-/Datumsformatierung. |
| **password**       | String  | Query       | Nein         | Passwort zum Öffnen einer geschützten Arbeitsmappe.                       |

## Antwort

Die API gibt die konvertierte HTML-Datei als **Binärstream** (`application/octet-stream`) zurück.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Beispiel für erfolgreiche Antwort (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="bericht.html"
Content-Length: 8423

<table>
  <tr><th>Produkt</th><th>Preis</th></tr>
  <tr><td>Widget A</td><td>10 €</td></tr>
  <tr><td>Widget B</td><td>15 €</td></tr>
</table>
```

Speichern Sie den Antworttext in einer Datei (z. B. `bericht.html`), um die gerenderte Tabelle in einem Browser anzuzeigen.

---

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                            |
| 413  | Payload Too Large     | Hochgeladene Datei überschreitet die Größe.                     |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## Wie verwendet man die Convert Range to HTML API mit SDKs?

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) beschreibt eine öffentlich zugängliche API, die REST-basierte Interaktionen direkt aus einem Webbrowser ermöglicht.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie mit cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Tabelle1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Bericht.xlsx" \
     -F "outPath=output/bericht.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="bericht.html"
Content-Length: 8423

<table>
  <tr><th>Produkt</th><th>Preis</th></tr>
  <tr><td>Widget A</td><td>10 €</td></tr>
  <tr><td>Widget B</td><td>15 €</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Low-Level-Details abstrahiert und Ihnen so die Konvertierung eines Datenbereichs in eine HTML-Datei mit minimalem Code ermöglicht.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie in unserem [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden. Falls das Laden aus Gist blockiert ist, können Sie die Beispiele direkt aus dem Repository herunterladen.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}