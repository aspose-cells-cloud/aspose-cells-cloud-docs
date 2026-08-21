---
title: "Spalten in einer Excel-Datei automatisch anpassen"
second_title: "Dokument"
linktitle: "Spalten"
type: docs
url: /de/autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "Spalten automatisch anpassen, Excel, Aspose.Cells Cloud, REST-API, SDK, cURL, API"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST-API Spalten in einer Excel-Arbeitsmappe automatisch anpassen können. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Codebeispiele für mehrere Sprachen."
weight: 90
---

Diese REST-API unterstützt das automatische Anpassen von Spalten in einer Excel-Arbeitsmappe.

## PostAutofitWorkbookColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

Die Anforderungsparameter sind:

| Parametername         | Typ     | Ort      | Beschreibung                                         |
| --------------------- | ------- | -------- | ---------------------------------------------------- |
| **name**              | string  | path     | Der Name der Arbeitsmappe-Datei.                     |
| **autoFitterOptions** | object  | body     | Optionen zur Steuerung des automatischen Anpassens. |
| **startColumn**       | integer | query    | Nullbasierter Index der ersten Spalte zur Anpassung. |
| **endColumn**         | integer | query    | Nullbasierter Index der letzten Spalte zur Anpassung. |
| **folder**            | string  | query    | Der Ordner, der die Arbeitsmappe enthält.           |
| **storageName**       | string  | query    | Der Name des Speicherdienstes.                      |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **Hinweis:** Verwenden Sie in der Produktion immer den HTTPS-Endpunkt und halten Sie Ihr JWT-Token vertraulich.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Voraussetzungen
Bevor Sie diesen Vorgang aufrufen, stellen Sie sicher, dass Sie über einen gültigen Aspose-Cloud-API-Schlüssel, ein generiertes JWT-Token verfügen und die Zielarbeitsmappe bereits am angegebenen Speicherort vorhanden ist.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

Die API kann folgende HTTP-Statuscodes zurückgeben:

| Code | Beschreibung                           |
|------|----------------------------------------|
| 200  | Erfolg – Spalten wurden automatisch angepasst |
| 400  | Bad request – fehlende oder ungültige Parameter |
| 401  | Unauthorized – ungültiges oder abgelaufenes JWT |
| 500  | Serverfehler – interner Verarbeitungsfehler |

## Cloud SDK-Familie

Die Verwendung eines SDK ist die effizienteste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektlogik konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}