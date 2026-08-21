---
title: "Arbeitsblatt-Konvertierung – Aspose.Cells Cloud API-Dokumentation"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie lokales Arbeitsblatt-Daten aus Tabellenkalkulationen in eine Bilddatei: Schritt-für-Schritt-Anleitung"
linktitle: "Arbeitsblatt in Bild konvertieren"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, Arbeitsblatt in Bild konvertieren, Excel zu PNG, Excel zu SVG, Excel zu TIFF, Excel zu JPEG, Excel zu BMP, Bildkonvertierungs-API, REST-API, Tabellenkalkulations-Bildexport, SDK-Beispiele"
description: "Schritt-für-Schritt-Anleitung zur Konvertierung eines Excel-Arbeitsblatts in Bildformate (PNG, SVG, TIFF, JPEG, BMP usw.) mithilfe der Aspose.Cells Cloud API, einschließlich Anforderungsparameter, Antwortdetails, Fehlercodes, Anwendungsszenarien und SDK-Codebeispielen."
weight: 100
---

Exportieren Sie Daten aus einem Arbeitsblatt einer lokalen Excel-Datei in eine [Bilddatei](https://docs.fileformat.com/image/) mithilfe der Aspose.Cells Cloud API. Dieser Vorgang unterstützt mehrere Bildformate und eignet sich ideal, um visuelle Schnappschüsse von Tabellendaten zu erstellen.

**UNTERSTÜTZTE BILDFORMATE**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Arbeitsblatt in Bild konvertieren – API**

### Web-API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                      |
| :---------------- | :----- | :---------------------------------- | :------------------------------------------------------------------------------------------------ |
| Spreadsheet       | Datei  | FormData                            | Hochladen der Tabellenkalkulationsdatei.                                                        |
| worksheet         | String | Abfrage                             | Name des zu konvertierenden Arbeitsblatts.                                                       |
| format            | String | Abfrage                             | Gewünschtes Bildformat (`svg`, `png`, `tiff`, `jpeg`, `bmp`, usw.).                             |
| outPath           | String | Abfrage                             | _(Optional)_ Ordnerpfad, in dem das Ausgabebild gespeichert wird; Standardwert ist `null`.       |
| outStorageName    | String | Abfrage                             | Name des Speicherorts für die Ausgabedatei.                                                      |
| fontsLocation     | String | Abfrage                             | Pfad zu einem benutzerdefinierten Schriftartenordner, falls Schriftarten verwendet werden sollen, die nicht auf dem Server verfügbar sind. |
| region            | String | Abfrage                             | Tabellenkalkulationsregionseinstellung (z. B. `de-DE`).                                          |
| password          | String | Abfrage                             | Passwort zum Öffnen einer passwortgeschützten Tabellenkalkulationsdatei.                        |

### **Antwort**

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

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                           |
| ---- | --------------------- | ---------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.       |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                  |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.          |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                            |

## **Wann sollte die Arbeitsblatt-in-Bild konvertieren API verwendet werden?**

- **Statische Berichtsschnappschüsse** – Konvertieren Sie Finanztabellen, Berechnungen oder andere Daten in Bilder, die in PDF-Berichte, PowerPoint-Folien oder gedruckte Dokumente eingebunden werden sollen, wo keine Bearbeitung erforderlich ist.
- **Datenvisualisierung in Präsentationen** – Wandeln Sie komplexe Tabellentabellen (einschließlich bedingter Formatierungen oder einfacher Diagramme) in Bilder um, die in Präsentationen (PPTX, Google Slides) eingebettet werden können.
- **Dokumentation und Schulungsmaterialien** – Erfassen Sie Tabellenkalkulationsbeispiele, -vorlagen oder Eingabeformulare als Bilder für Benutzerhandbücher, Tutorials oder Knowledge-Base-Artikel.
- **Vorschaubilder (Thumbnails)** – Erstellen Sie kleine Bildvorschaubilder wichtiger Tabellensektionen für Dateibrowser, Dokumentenbibliotheken oder Suchergebnisse.

## **Warum sollte man die Arbeitsblatt-in-Bild konvertieren API verwenden?**

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken für mehrere Programmiersprachen, was eine schnelle Entwicklung ermöglicht, und ist umfassend dokumentiert. Im Vergleich zur Erstellung einer benutzerdefinierten Diagramm-Rendering-Lösung reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient** – Sie können Tabellendaten konvertieren, ohne die Arbeitsmappe dauerhaft speichern zu müssen, was Speicherplatz spart und Kosten senkt.
- **Pixelgenaue Wiedergabe** – Repliziert zuverlässig das Erscheinungsbild von Excel – einschließlich Zellformatierung, Formeln (als angezeigte Werte), Rahmen, Farben und bedingter Formatierung – im Ausgabebild.
- **Universelle Kompatibilität** – Bildformate (PNG, JPEG, TIFF, BMP, SVG usw.) sind auf jedem Gerät oder Betriebssystem ohne spezielle Software darstellbar und gewährleisten so maximale Zugänglichkeit.

## **Wie verwendet man die Arbeitsblatt-in-Bild konvertieren API mit SDKs?**

### Spezifikation der Arbeitsblatt-in-Bild konvertieren API

Die [Spezifikation der Arbeitsblatt-in-Bild konvertieren API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-codiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahiert und es ermöglicht, Arbeitsblattdaten mit minimalem Code in ein Bild zu konvertieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}