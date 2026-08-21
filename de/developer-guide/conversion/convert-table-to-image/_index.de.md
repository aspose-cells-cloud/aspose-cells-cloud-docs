---
title: "Aspose.Cells Cloud Web API – Lokale Excel-Tabellendaten in eine Bilddatei konvertieren – Kostenloses Online-Tool"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie Tabellendaten lokaler Tabellendateien in eine Bilddatei: Schritt-für-Schritt-Anleitung"
linktitle: "Tabelle in Bild konvertieren"
type: docs
url: /de/convert-table-to-image/
keywords: "Aspose.Cells, Cloud API, Tabelle in Bild konvertieren, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Konvertieren Sie lokal gespeicherte Excel-Tabellendaten mithilfe der Aspose.Cells Cloud API schnell in eine Bilddatei. Unterstützt PNG, JPEG, TIFF, BMP, SVG und weitere Formate."
weight: 100
---

Exportieren Sie Tabellendaten aus einer lokalen Excel-Datei in eine [Bilddatei](https://docs.fileformat.com/image/) mithilfe der Cloud API.

**UNTERTÜTZTE BILDFORMATE:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API zur Konvertierung von Tabellen in Bilder**

Bevor Sie diesen Endpunkt verwenden, stellen Sie sicher, dass folgende Voraussetzungen erfüllt sind:

- Ein gültiges JWT-Zugriffstoken, das über die Aspose.Cells Cloud-Authentifizierung erhalten wurde.
- Ein zugänglicher Speicherkonto, falls Sie die Parameter `outPath` oder `outStorageName` verwenden möchten.
- Die Quelldatei (lokale Excel-Datei) muss lesbar sein; bei passwortgeschützten Dateien ist das korrekte Passwort anzugeben.

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                            |
| :-------------- | :----- | :------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Datei  | FormData                        | Hochladen der Tabellendatei.                                                                                                            |
| worksheet       | String | Abfrage                         | Name des Arbeitsblatts der Tabelle/Excel.                                                                                               |
| tableName       | String | Abfrage                         | Name der zu konvertierenden Tabelle.                                                                                                    |
| format          | String | Abfrage                         | Gewünschtes Bilddateiformat (z. B. png, svg).                                                                                           |
| outPath         | String | Abfrage                         | (Optional) Der Ordnerpfad, in dem das konvertierte Bild gespeichert wird. Standardwert ist null.                                       |
| outStorageName  | String | Abfrage                         | Name des Ausgabespeichers.                                                                                                              |
| fontsLocation   | String | Abfrage                         | Verwenden Sie benutzerdefinierte Schriftarten, sofern erforderlich.                                                                    |
| region          | String | Abfrage                         | Regionaleinstellung/Sprache der Tabelle (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst Zahlenformatierung, Datumsverarbeitung und regionsabhängiges Verhalten. |
| password        | String | Abfrage                         | Passwort zum Zugriff auf die Tabellendatei.                                                                                             |

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

| Code | Bedeutung             | Beschreibung                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes JWT-Token.                              |
| 413  | Anforderung zu groß   | Die hochgeladene Datei überschreitet die Größeinschränkung.       |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler.                                        |

## **Wann sollten Sie die API zur Konvertierung von Tabellen in Bilder verwenden?**

- **Statische Berichtssnapshots**: Konvertieren Sie Finanztabellen, Berechnungsergebnisse oder andere formatierte Daten in Bilder, um sie in PDF-Berichten, PowerPoint-Folien oder gedruckten Dokumenten einzubinden, wo keine Bearbeitung erforderlich ist.
- **Datenvisualisierung in Präsentationen**: Wandeln Sie komplexe Tabellendaten – einschließlich bedingter Formatierungen oder einfacher Visualisierungen – in Bilder um, die in Präsentationen (PPTX, Google Slides) eingebettet werden können.
- **Dokumentation und Schulungsmaterialien**: Erfassen Sie Beispiele, Vorlagen oder Eingabeformulare aus Tabellendateien als Bilder für Benutzerhandbücher, Tutorials oder Knowledge-Base-Artikel.
- **Vorschaubilder**: Erzeugen Sie kleine Vorschaubilder wichtiger Tabellensektionen für Dateibrowser, Dokumentenbibliotheken oder Suchergebnisse.

## **Warum sollten Sie die API zur Konvertierung von Tabellen in Bilder verwenden?**

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken für mehrere Sprachen, die eine schnelle Entwicklung ermöglichen und umfangreiche Dokumentation bereitstellen. Im Vergleich zum Aufbau eigener Renderingsysteme reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient**: Sie können Tabellendaten konvertieren, ohne die gesamte Arbeitsmappe hochladen zu müssen – dies spart Speicherplatz und Kosten.
- **Pixelgenaue Wiedergabe**: Reproduziert das Erscheinungsbild von Excel treu – einschließlich Zellformatierung, Formeln (als angezeigte Werte), Rändern, Farben und bedingter Formatierung – in der Ausgabebilddatei.
- **Universelle Kompatibilität**: Bildformate (PNG, JPEG, TIFF, BMP, SVG usw.) lassen sich auf jedem Gerät oder Betriebssystem ohne spezielle Software anzeigen – somit ist maximale Zugänglichkeit gewährleistet.

## **Wie verwenden Sie die API zur Konvertierung von Tabellen in Bilder mit SDKs?**

### Spezifikation der API zur Konvertierung von Tabellen in Bilder

Die [Spezifikation der API zur Konvertierung von Tabellen in Bilder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) stellt eine öffentlich zugängliche Programmierschnittstelle für REST-basierte Interaktionen direkt aus einem Webbrowser bereit.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
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

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie detaillierte Low-Level-Details abstrahieren und es Ihnen ermöglichen, Tabellendaten mit minimalem Codeaufwand in Bilder umzuwandeln. Weitere Informationen und eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}