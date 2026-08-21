---
title: "Datenimport ohne Speicherung – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Datenimport ohne Speicherung"
type: docs
url: /de/import/without-using-storage/
aliases: [  /de/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, Cloud API, Datenimport ohne Speicherung, Excel-Import-API, REST-Import"
description: "Erfahren Sie, wie Sie Daten mithilfe der Aspose.Cells Cloud API in eine Excel-Arbeitsmappe importieren, ohne Speicherung zu verwenden. Enthält Anforderungsformat, Parameter, cURL-Beispiel, SDK-Code und Fehlerbehandlung."
weight: 10
ArticleTitle: "Datenimport ohne Speicherung – Aspose.Cells Cloud API"
---

Der Excel-Datenimport kann komplex sein, da viele Faktoren das Ergebnis beeinflussen. Alle diese Faktoren müssen während des **Importvorgangs** berücksichtigt werden. Aspose.Cells Cloud vereinfacht den Import verschiedener Formate und Datentypen in eine Excel-Datei mit Qualität auf Profiniveau.

Diese REST-API importiert **Daten** in eine Excel-Datei.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername | Typ          | Speicherort  | Beschreibung                                                                                                                                     |
| -------------- | ------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| file           | Datei          | formData  | Die hochzuladende Excel-Datei.                                                                                                                       |
| ImportOption   | ImportOption  | JSON-Textkörper | JSON-Objekt, das die zu importierenden Daten, deren Typ (z. B. `IntArray`, `DoubleArray`, `StringArray`) sowie die Platzierung im Arbeitsblatt definiert. |

Die **ImportOption**-Parameter werden in der **ImportData-Option-Referenz** unter [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter) beschrieben.

**Voraussetzungen:**  
Ein gültiges JWT-Token muss zuvor generiert werden, und die Dateigröße darf das Dienstlimit (typischerweise 100 MB) nicht überschreiten. Unterstützte Dateiformate sind XLS, XLSX, CSV und ODS. Falls Sie programmgesteuerten Zugriff bevorzugen, stellen Sie sicher, dass das entsprechende SDK installiert ist.

### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                     | Beschreibung                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request (Ungültige Anforderung)                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized (Nicht autorisiert)                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large (Nutzdaten zu groß)           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error (Interner Serverfehler)       | Unerwarteter Serverfehler. |

**Hinweise:**  
Beim Senden der Anforderung wird der Header `Content-Type: multipart/form-data` automatisch durch den `-F`-Schalter gesetzt. Bei großen Nutzdaten sollten Sie die Daten vor dem Import komprimieren und eine Wiederholungslogik für vorübergehende Fehler implementieren.

## Verwendung der PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*Der `-F`-Schalter setzt automatisch `Content-Type: multipart/form-data`.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}