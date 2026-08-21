---
title: "Arbeitsblatt in CSV konvertieren – Aspose.Cells Cloud API-Dokumentation"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie ein Tabellenkalkulationsarbeitsblatt mit der Aspose.Cells Cloud API in CSV"
linktitle: "Arbeitsblatt in CSV konvertieren"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, CSV-Konvertierung, Arbeitsblatt in CSV, REST-API, Cloud-Tabellenkalkulation, Excel in CSV"
description: "Erfahren Sie, wie Sie ein bestimmtes Arbeitsblatt aus einer Excel-Datei mithilfe der Aspose.Cells Cloud API (v4.0) in CSV konvertieren. Enthält Endpunkt, Parameter, Beispiel-cURL, SDK-Code und Fehlerbehandlung."
weight: 100
---

Der Endpunkt **ConvertWorksheetToCsv** wandelt ein einzelnes Arbeitsblatt aus einer lokalen Tabellenkalkulationsdatei vollständig auf den Aspose.Cells Cloud-Servern in ein CSV-Dokument um. Durch das Hochladen der Quelldatei und die Angabe des Zielarbeitsblatts erhalten Entwickler einen binären CSV-Stream zurück, ohne die Datei im Cloud-Speicher speichern zu müssen. Diese API eignet sich ideal für die Automatisierung der Datenextraktion, die Integration von Tabellenkalkulationsdaten in nachgelagerte Systeme und die Reduzierung des Speicheraufwands.

## API zum Konvertieren von Arbeitsblättern in CSV

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter

| Parametername   | Typ    | Speicherort | Erforderlich/Optional | Beschreibung                                                                                                                               |
| :-------------- | :----- | :---------- | :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Datei  | FormData    | **Erforderlich**      | Binärdatei der Quell-Tabellenkalkulation (z. B. `.xlsx`, `.xls`). Beispiel: `myWorkbook.xlsx`.                                             |
| worksheet       | String | Query       | **Erforderlich**      | Name des zu konvertierenden Arbeitsblatts (Groß-/Kleinschreibung beachten). Wird dieser Parameter weggelassen, wird das erste Arbeitsblatt verwendet. Beispiel: `Sheet1`. |
| outPath         | String | Query       | Optional              | Zielpfad im Cloud-Speicher, in dem die generierte CSV-Datei gespeichert wird. Wird dieser Parameter weggelassen, wird die CSV direkt im Antwortstream zurückgegeben. |
| outStorageName  | String | Query       | Optional              | Name des Speicherdiensts (z. B. Azure, AWS S3), in dem die Ausgabedatei abgelegt werden soll. Erforderlich, nur wenn `outPath` verwendet wird. |
| fontsLocation   | String | Query       | Optional              | Pfad zu einem benutzerdefinierten Schriftartenordner auf dem Server, sodass die Konvertierungsmaschine nicht standardmäßige Schriftarten verwenden kann. |
| region          | String | Query       | Optional              | Gebietsschemabezeichner, der die Zahlen-/Datumsformatierung im CSV beeinflusst (z. B. `de-DE`, `fr-FR`).                                 |
| password        | String | Query       | Optional              | Passwort zum Öffnen einer geschützten Tabellenkalkulation. Muss mit dem Verschlüsselungspasswort der Quelldatei übereinstimmen.           |

### Antwort

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

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## Wann sollte die API zum Konvertieren von Arbeitsblättern in CSV verwendet werden?

- **Datenextraktion für BI-Pipelines** – Extrahieren Sie ein bestimmtes Arbeitsblatt aus einem Excel-Bericht und übertragen Sie das resultierende CSV direkt an Power BI oder Tableau, ohne Zwischendateien zu verwalten.
- **Automatisierte Rechnungsverarbeitung** – Konvertieren Sie das Arbeitsblatt mit Rechnungszeilen in CSV für einen schnellen Import in Buchhaltungssysteme.
- **Integration in veraltete Systeme** – Exportieren Sie Arbeitsblattdaten in CSV für die Verwendung durch ältere Anwendungen, die nur durch Trennzeichen getrennte Textdateien akzeptieren.
- **On-the-fly-Berichtserstellung** – Generieren Sie CSV-Snapshots von Live-Tabellenkalkulationsdaten in einem Webservice und geben Sie die Datei sofort an den Clientbrowser zurück.

## Warum sollte die API zum Konvertieren von Arbeitsblättern in CSV verwendet werden?

- **Kein permanenter Cloud-Speicher erforderlich** – Die Datei wird direkt an die Konvertierungsmaschine übertragen und nach der Konvertierung verworfen, was Bandbreite und Speicherkosten spart.
- **Hochperformante Cloud-Ausführung** – Die Konvertierung erfolgt auf Asposes optimierten Servern und dauert in der Regel höchstens 2 Sekunden für Dateien bis zu 100 MB.
- **Feingliedrige Steuerung** – Wählen Sie ein einzelnes Arbeitsblatt aus, wenden Sie benutzerdefinierte Schriftarten, regionale Formatierungen und Passwortschutz in einer Anforderung an.
- **Konsistente plattformübergreifende Ausgabe** – Garantiert identische CSV-Ausgaben über .NET, Java, Python und andere SDKs hinweg, die denselben REST-Endpunkt verwenden.

## Verwendung der API zum Konvertieren von Arbeitsblättern in CSV mit SDKs

### API-Spezifikation zum Konvertieren von Arbeitsblättern in CSV

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">API-Spezifikation zum Konvertieren von Arbeitsblättern in CSV</a> bietet eine öffentlich zugängliche Programmierschnittstelle, um REST-Interaktionen direkt aus einem Webbrowser auszuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

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

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung des SDK vereinfacht die Entwicklung, indem niedrigere Ebenen abstrahiert werden, sodass Sie Tabellenkalkulationen mit prägnantem Code miteinander fusionieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs auf die Aspose.Cells-Webservices zugreifen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}