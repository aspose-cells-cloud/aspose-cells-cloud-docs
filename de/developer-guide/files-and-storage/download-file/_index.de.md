---
title: "Aspose.Cells Cloud Download File API – Schnittstelle zum schnellen Dateidownload in der Cloud"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Download File API – Schnittstelle zum schnellen Dateidownload in der Cloud"
linktitle: "Download File API"
type: docs
url: /de/download-file/
keywords: "Aspose.Cells, Download File API, Excel Cloud-Speicher, REST API, Dateidownload, PDF, CSV, SDK"
description: "Laden Sie Excel-Dateien, PDFs, CSVs und andere Formate aus dem Aspose.Cells Cloud-Speicher mithilfe der Download File API (v4.0) herunter. Enthält Endpunkt, Parameter, Authentifizierungsdetails und Codebeispiele."
weight: 100
---

Die **DownloadFile** API ermöglicht es Ihnen, in Aspose.Cells Cloud gespeicherte Dateien abzurufen. Die Download File API ist entscheidend, um direkt aus der Cloud auf Excel-Arbeitsblätter, PDFs, CSVs und andere unterstützte Formate zuzugreifen.

## **Excel API: Datei herunterladen**

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anforderungsparameter der **DownloadFile** API sind

| Parametername | Typ   | Speicherort (Pfad / Abfrage) | Beschreibung                                                        |
| ------------- | ----- | ---------------------------- | ------------------------------------------------------------------- |
| path          | String | Pfad                         | Der virtuelle Pfad zur Datei, die Sie herunterladen möchten.       |
| storageName   | String | Abfrage                      | Der Name des Speichers, aus dem die Datei abgerufen werden soll.   |
| versionId     | String | Abfrage                      | Die Versionskennung der herunterzuladenden Datei (falls zutreffend). |

### **Antwort**

Die API gibt einen **binären Dateistream** zurück. Der `Content-Type`-Header entspricht dem Dateiformat (z. B. `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` für XLSX). Es wird kein JSON-Payload zurückgegeben.

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                       |
| ---- | --------------------- | ------------------------------------------------------------------ |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                              |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.             |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                        |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}