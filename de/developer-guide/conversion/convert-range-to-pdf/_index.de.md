---
title: "Excel-Bereich mit Aspose.Cells Cloud API in PDF konvertieren"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie lokalen Tabellendatenbereich in eine PDF-Datei: Schritt-für-Schritt-Anleitung"
linktitle: "Bereich in PDF konvertieren"
type: docs
url: /de/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, Excel-Bereich in PDF konvertieren, Excel zu PDF, Cloud-Konvertierung"
description: "Konvertieren Sie einen bestimmten Bereich aus einer lokalen Excel-Tabelle mit der REST-API von Aspose.Cells Cloud in PDF."
weight: 100
---

Exportieren Sie einen Datenbereich aus einer lokalen Excel-Datei in eine [PDF](https://docs.fileformat.com/pdf/)-Datei mithilfe der Cloud-API.

**Voraussetzungen**: Vor der Verwendung dieser API benötigen Sie ein gültiges Aspose.Cells Cloud-Konto, ein JWT-Zugriffstoken und optional ein Aspose.Cells Cloud SDK für Ihre Programmiersprache. Stellen Sie sicher, dass das Ziel-Storage (Standard oder benutzerdefiniert) konfiguriert ist, falls Sie den Parameter `outStorageName` verwenden möchten.

## **Bereich in PDF konvertieren – API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                 |
| ----------------- | ------ | ---------------------------------- | ---------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData                           | Hochladen der Tabellendatei.                                                 |
| worksheet         | String | Abfrage                            | Der Name des Arbeitsblatts innerhalb der Tabelle.                           |
| range             | String | Abfrage                            | Der zu konvertierende Zellbereich, z. B. A1:C10.                            |
| outPath           | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| outStorageName    | String | Abfrage                            | Name des Speichers für die Ausgabedatei.                                    |
| fontsLocation     | String | Abfrage                            | Speicherort für benutzerdefinierte Schriftarten für die private Nutzung.    |
| region            | String | Abfrage                            | Die Regionseinstellung der Tabelle.                                         |
| password          | String | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei.                                  |

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

_Die typische Antwort ist ein binärer PDF-Stream, der als Dateidownload zurückgegeben wird._

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## **Wann sollten Sie die „Bereich in PDF konvertieren“-API verwenden?**

- **Finanzaussagen**: Konvertieren Sie Bilanzen, Gewinn- und Verlustrechnungen (spezifische Bereiche) in PDF für prüfungsfähige Dokumente.
- **Verkaufsberichte**: Wandeln Sie Verkaufs-Dashboards oder Provisionberechnungen in verteilbare PDFs um.
- **Betriebskennzahlen**: Exportieren Sie KPI-Tabellen und Leistungsmetriken als formelle PDF-Berichte.
- **Vertragsdaten**: Exportieren Sie Preislisten und Service-Level-Vereinbarungen aus Tabellen als PDF-Anhänge.
- **Audit-Protokolle**: Speichern Sie Finanzdatenbereiche als nicht bearbeitbare PDF-Beweise.
- **Portfolio-Zusammenfassungen**: Exportieren Sie Anlageperformancerbereiche als kundenfertige PDF-Auszüge.
- **Qualitätskontrollberichte**: Exportieren Sie Prüfdatenbereiche als PDF für Compliance-Aufzeichnungen.
- **Inventarzusammenfassungen**: Wandeln Sie Bestandslisten in PDF für das Management-Review um.

## **Warum sollten Sie die „Bereich in PDF konvertieren“-API verwenden?**

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung und umfassende Dokumentation ermöglicht. Im Vergleich zum Aufbau eigener Diagramm-Rendering-Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient**: Sie können Datenbereiche konvertieren, ohne zuerst die gesamte Arbeitsmappe hochzuladen – dies spart Speicherplatz und reduziert Kosten.
- **Beibehaltung komplexer Excel-Formatierungen** in einem allgemein zugänglichen PDF-Format.

## **Wie verwenden Sie die „Bereich in PDF konvertieren“-API mit SDKs?**

### **Spezifikation der „Bereich in PDF konvertieren“-API**

Die [Spezifikation der „Bereich in PDF konvertieren“-API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### **Verwendung der Aspose.Cells Cloud SDKs**

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung, da sie niedrigere Details abstrahiert und es Ihnen ermöglicht, einen Datenbereich mit kurzem Code in eine PDF-Datei zu konvertieren. Sehen Sie sich das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}