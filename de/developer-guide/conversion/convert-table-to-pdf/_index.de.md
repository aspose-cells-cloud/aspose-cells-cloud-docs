---
title: "Aspose.Cells Cloud Web-API – Lokale Excel-Tabellendaten in eine PDF-Datei konvertieren – Kostenloses Online-Tool"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie Tabellendaten aus lokalen Tabellenkalkulationen in eine PDF-Datei: Schritt-für-Schritt-Anleitung"
linktitle: "Tabelle in PDF konvertieren"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells, Excel zu PDF, Tabellenkonvertierung, Cloud-API"
description: "Konvertieren Sie lokale Excel-Tabellen schnell mithilfe der Aspose.Cells Cloud REST-API in eine PDF-Datei."
weight: 100
---

Exportieren Sie Tabellendaten aus einer lokalen Excel-Datei in eine PDF-Datei mithilfe der Cloud-API.

## **API zur Konvertierung von Tabellen in PDF**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                             |
| :-------------- | :----- | :---------------------------------- | :------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Datei  | FormData                            | Laden Sie die zu konvertierende Tabellenkalkulationsdatei hoch.                                         |
| worksheet       | String | Abfrage                             | Der Name des Arbeitsblatts der Tabellenkalkulation.                                                     |
| tableName       | String | Abfrage                             | Der Name der zu konvertierenden Tabelle.                                                                |
| outPath         | String | Abfrage                             | (Optional) Der Ordnerpfad, in dem die konvertierte PDF gespeichert wird. Der Standardwert ist null.    |
| outStorageName  | String | Abfrage                             | Geben Sie den Namen des Ausgabespeichers an.                                                            |
| fontsLocation   | String | Abfrage                             | Verwenden Sie benutzerdefinierte Schriftarten für die PDF.                                              |
| region          | String | Abfrage                             | Gibt die Regionseinstellung für die Tabellenkalkulation an.                                            |
| password        | String | Abfrage                             | Passwort zum Zugriff auf die Tabellenkalkulationsdatei.                                                |

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

**Beispiel für Antwort-Header**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                       |
| ---- | --------------------- | ------------------------------------------------------------------ |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                              |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Dateigrößenbeschränkung. |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                         |

## **Wann sollten Sie die API zur Konvertierung von Tabellen in PDF verwenden?**

- **Finanzberichte**: Konvertieren Sie Bilanzen, Gewinn- und Verlustrechnungen (bestimmte Tabellen) in PDF für prüfungskonforme Dokumentation.
- **Verkaufsberichte**: Wandeln Sie Verkaufs-Dashboards oder Provisionsberechnungen in verteilbare PDFs um.
- **Betriebskennzahlen**: Exportieren Sie KPI-Tabellen und Leistungsmetriken als formelle PDF-Berichte.
- **Vertragsdaten**: Exportieren Sie Preislisten und Service-Level-Vereinbarungen aus Tabellenkalkulationen als PDF-Anhänge.
- **Audit-Logs**: Bewahren Sie Tabellen mit Finanzdaten als nicht bearbeitbare PDF-Beweise auf.
- **Portfoliobeschreibungen**: Exportieren Sie Tabellen zur Anlageperformance als kundenfertige PDF-Aussagen.
- **Qualitätskontrollberichte**: Exportieren Sie Inspektionsdatentabellen als PDF für Compliance-Aufzeichnungen.
- **Bestandsübersichten**: Wandeln Sie Bestandslevel-Tabellen in PDF für die Führungskräfterezension um.

## **Warum sollten Sie die API zur Konvertierung von Tabellen in PDF verwenden?**

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Programmiersprachen an, die eine schnelle Entwicklung ermöglichen, und wird von einer umfassenden Dokumentation begleitet. Im Vergleich zur Erstellung eigener Lösungen zur Diagrammerstellung reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient**: Sie können Tabellendaten konvertieren, ohne zunächst die gesamte Arbeitsmappe hochzuladen, was Speicherplatz spart und Kosten reduziert.
- **Erhält komplexe Excel-Formatierungen** in einem universell zugänglichen PDF-Format.

## **Wie verwenden Sie die API zur Konvertierung von Tabellen in PDF mit SDKs?**

### Spezifikation der API zur Konvertierung von Tabellen in PDF

Die [Spezifikation der API zur Konvertierung von Tabellen in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) bietet eine öffentlich zugängliche Programmierschnittstelle, um REST-Interaktionen direkt aus einem Webbrowser durchzuführen.
Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahieren und es Ihnen ermöglichen, Tabellendaten aus Tabellenkalkulationen mit minimalem Codeaufwand in PDF-Dateien zu konvertieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufrufen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}