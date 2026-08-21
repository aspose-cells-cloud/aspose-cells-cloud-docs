---
title: "Aspose.Cells Cloud Web API – Konvertieren Sie Excel-Diagramme in Bilder – Kostenloses Online-Tool"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie Diagramme aus Tabellenkalkulationen in Bilder: Schritt-für-Schritt-Anleitung"
linktitle: "Diagramm in Bild konvertieren"
type: docs
url: /convert-chart-to-image/
keywords: "Diagramm in Bild konvertieren, Aspose.Cells, Excel-Diagramm exportieren, PNG, SVG, JPEG, BMP, TIFF"
description: "Verwenden Sie die Aspose.Cells Cloud Web API, um ein Excel-Diagramm direkt aus einer Tabellenkalkulationsdatei in PNG-, SVG-, TIFF-, JPEG- oder BMP-Bilder zu konvertieren."
weight: 100
---

Excel-Diagramme sind visuelle Darstellungen von Daten, die in Arbeitsblättern eingebettet werden können. Die Konvertierung dieser Diagramme in Bildformate ermöglicht eine einfache Wiederverwendung in Dokumenten, Webseiten und Berichten, ohne dass Excel erforderlich ist.

Konvertieren Sie ein Diagramm aus einer lokalen Tabellenkalkulation oder Excel-Datei in eine Bilddatei. Unterstützte **BILDFORMATE:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **API zum Konvertieren von Diagrammen in Bilder**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                      | Erforderlich |
| :---------------- | :----- | :--------------------------------- | :------------------------------------------------------------------------------------------------ | :----------- |
| Spreadsheet       | Datei  | FormData                           | Laden Sie die Tabellenkalkulationsdatei hoch, die das Diagramm enthält.                         | Ja           |
| worksheet         | String | Abfrage                            | Geben Sie den Namen des Arbeitsblatts an, falls zutreffend.                                      | Nein         |
| chartIndex        | Integer| Abfrage                            | Index des zu konvertierenden Diagramms.                                                           | Ja           |
| format            | String | Abfrage                            | (Erforderlich) Der gewünschte Bildtyp (z. B. svg, png, jpg).                                    | Ja           |
| outPath           | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Ausgabedatei gespeichert wird; Standardwert ist null.     | Nein         |
| outStorageName    | String | Abfrage                            | Name des Speichers für die Ausgabedatei.                                                         | Nein         |
| fontsLocation     | String | Abfrage                            | Geben Sie bei Bedarf benutzerdefinierte Schriftarten an.                                         | Nein         |
| region            | String | Abfrage                            | Legen Sie die Region der Tabellenkalkulation fest.                                               | Nein         |
| password          | String | Abfrage                            | Das Passwort zum Öffnen der Tabellenkalkulationsdatei.                                           | Nein         |

## **Antwort**

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

| Code | Bedeutung             | Beschreibung                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.      |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).   |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                      |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.             |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                                |

## Wo sollten Sie die API zum Konvertieren von Diagrammen in Bilder verwenden?

- **Berichtsgenerierung & Dashboards**: Konvertieren Sie Diagramme automatisch aus Excel-Daten in Bilder (PNG, JPEG usw.), die in PDF-Berichte, Web-Dashboards oder PowerPoint-Präsentationen eingebettet werden können.
- **Web-/E-Mail-Anwendungen**: Stellen Sie Diagrammbilder direkt in Webseiten oder E-Mails bereit, ohne dass Benutzer Excel-Dateien herunterladen oder öffnen müssen. Nützlich für dynamische Berichterstattungstools, Newsletter oder automatisierte Benachrichtigungen.
- **Dokumentenverarbeitungs-Workflows**: Integrieren Sie diese API in automatisierte Prozesse (z. B. Rechnungsstellung, Analyse), bei denen Diagramme aus Excel in andere Formate (Word, PDF, HTML) eingefügt werden müssen.
- **Mobile/Desktop-Anwendungen**: Zeigen Sie Excel-Diagramme in Anwendungen an, bei denen das Rendern der gesamten Tabellenkalkulation unnötig oder unpraktisch wäre.
- **Archivierung & Visualisierung**: Speichern Sie Diagramme als eigenständige Bilder für langfristige Speicherung, als Vorschaubilder oder schnelle Vorschauen, ohne Excel-Abhängigkeiten.

## Warum sollten Sie die API zum Konvertieren von Diagrammen in Bilder verwenden?

- **Visuelle Treue bewahren**: Behält die exakte Formatierung des Diagramms (Farben, Beschriftungen, Skalierung) bei, wie sie in Excel angezeigt wird, und gewährleistet so eine professionelle Qualität der Ausgabe.
- **Plattformunabhängig**: Keine Excel-Installation erforderlich. Funktioniert plattformübergreifend (Windows, Linux, macOS) über REST-API und eignet sich für Cloud-basierte oder serverseitige Anwendungen.
- **Automatisierung & Skalierbarkeit**: Konvertieren Sie mehrere Diagramme oder Dateien programmatisch im Batchbetrieb und sparen Sie Zeit im Vergleich zur manuellen Exportfunktion. Bewältigt große Datenmengen effizient in der Cloud.
- **Flexible Ausgabeformate**: Unterstützt gängige Bildformate (PNG, JPG, BMP, SVG usw.) und ermöglicht so die Integration in vielfältige Systeme und Medien.
- **Sicher & zuverlässig**: Verarbeiten Sie Dateien in der Cloud-Umgebung von Aspose, ohne sensible Daten Client-seitigen Tools auszusetzen. Hohe Verfügbarkeit und konsistente Leistung.
- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung ermöglicht, und kommt mit umfassender Dokumentation. Im Vergleich zum Aufbau eigener Diagramm-Rendelungslösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffektiv**: Sie können Diagramme konvertieren, ohne zuerst die Arbeitsmappe hochzuladen, was Speicherplatz spart und Kosten senkt.

## Wie verwenden Sie die API zum Konvertieren von Diagrammen in Bilder mit SDKs?

### API-Spezifikation zum Konvertieren von Diagrammen in Bilder

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">API-Spezifikation zum Konvertieren von Diagrammen in Bilder</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da dabei die Low-Level-Details abstrahiert werden, sodass Sie ein Diagramm mit nur wenigen Codezeilen in ein Bild konvertieren können.  
Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}

---