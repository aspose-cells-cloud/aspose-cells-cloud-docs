---
title: "Aspose.Cells Cloud Web-API – Konvertieren Sie Tabellendaten einer Tabellenkalkulation in eine CSV-Datei – Kostenfreies Online-Tool"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie Tabellendaten einer Tabellenkalkulation in eine CSV-Datei: Schritt-für-Schritt-Anleitung"
linktype: "docs"
url: /de/convert-table-to-csv/
keywords: "Aspose.Cells Cloud, Tabelle zu CSV, Tabellenkalkulationskonvertierung, Excel zu CSV, API, REST, Datenexport"
description: "Konvertieren Sie eine Tabelle aus einer Excel-Tabellenkalkulation schnell in eine CSV-Datei mithilfe der Aspose.Cells Cloud API."
weight: 100
---

Exportieren Sie Tabellendaten aus einer lokalen Excel-Datei in eine CSV-Datei mithilfe der Cloud-API.

## **Konvertieren einer Tabelle in CSV per API**

### Web-API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                           |
|-----------------|--------|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet     | Datei  | FormData                            | Laden Sie die Tabellendatei hoch.                                                                                                     |
| worksheet       | String | Abfrage                             | Name des Arbeitsblatts in der Tabellendatei.                                                                                         |
| tableName       | String | Abfrage                             | Name der zu konvertierenden Tabelle.                                                                                                  |
| outPath         | String | Abfrage                             | (Optional) Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; Standardwert ist null.                                               |
| outStorageName  | String | Abfrage                             | Name des Speichers für die Ausgabedatei.                                                                                             |
| fontsLocation   | String | Abfrage                             | Pfad für benutzerdefinierte Schriftarten.                                                                                             |
| region          | String | Abfrage                             | Regionale/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und regionsabhängiges Verhalten. |
| password        | String | Abfrage                             | Passwort zum Öffnen der Tabellendatei.                                                                                                |

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

| Code | Bedeutung             | Beschreibung                                                              |
|------|-----------------------|---------------------------------------------------------------------------|
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails.       |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                                     |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                   |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                               |

## **Wann sollten Sie die Konvertieren einer Tabelle in CSV API verwenden?**

- **Datenbankmigration**: Konvertieren Sie Excel-Tabellen in CSV für den Massenimport in SQL-Datenbanken (MySQL, PostgreSQL, SQL Server).
- **Data-Warehouse-Ladeprozesse**: Wandeln Sie Excel-basierte Berichtstabellen in CSV um, um sie in Snowflake, Redshift oder BigQuery zu laden.
- **Massen-API-Payloads**: Konvertieren Sie Excel-Tabellendaten in CSV für Massen-Uploads an REST-Dienste.
- **Dienst-zu-Dienst-Kommunikation**: Verwenden Sie CSV als leichtes Datenformat für den Austausch zwischen Microservices.
- **Maschinelles Lernen – Datenvorbereitung**: Konvertieren Sie Feature-Tabellen aus Excel in CSV für Python-/R-Maschinenlern-Bibliotheken.
- **Statistische Analyse**: Wandeln Sie Forschungsdatentabellen in CSV um, um sie in SPSS, SAS oder Stata zu importieren.
- **Inhaltsmigration**: Übertragen Sie strukturierte Inhalte aus Excel mithilfe von CSV in CMS-Systeme.

## Warum sollten Sie die Konvertieren einer Tabelle in CSV API verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Programmiersprachen an, was eine schnelle Entwicklung ermöglicht, und wird von einer umfassenden Dokumentation begleitet. Im Vergleich zur Erstellung eigener Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient**: Sie können Tabellendaten konvertieren, ohne die Arbeitsmappe zuerst hochzuladen, was Speicherplatz spart und Kosten senkt.
- **Reine Datenextraktion ohne Formatierung**.
- **CSV wird von praktisch jedem System unterstützt**:
  - Datenbanken (alle gängigen RDBMS)
  - Programmiersprachen (integrierte Parser in allen)
  - Business-Intelligence-Tools (Tableau, Power BI, Looker)
  - Tabellenkalkulationssoftware (Excel, Google Sheets, LibreOffice)
  - Kommandozeilenwerkzeuge (awk, sed, grep)

## Wie verwenden Sie die Konvertieren einer Tabelle in CSV API mit SDKs?

### API-Spezifikation „Konvertieren einer Tabelle in CSV“

Die [API-Spezifikation „Konvertieren einer Tabelle in CSV“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) bietet eine öffentlich zugängliche Programmierschnittstelle, über die REST-Aufrufe direkt aus einem Webbrowser durchgeführt werden können.
Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist die schnellste Möglichkeit zur Entwicklung, da sie low-Level-Details abstrahiert und es Ihnen ermöglicht, Tabellendaten mit minimalem Codeaufwand in eine CSV-Datei zu konvertieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webservices durchführen:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}