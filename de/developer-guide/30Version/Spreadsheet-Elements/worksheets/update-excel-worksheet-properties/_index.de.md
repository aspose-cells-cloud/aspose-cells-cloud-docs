---
title: "Arbeitsblatt-Eigenschaften aktualisieren – Aspose.Cells Cloud API-Referenz (v3.0)"
second_title: "Dokument"
linktitle: "Aktualisieren"
type: docs
url: /worksheets/update-properties/
aliases: [/update-excel-worksheet-properties/]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "Arbeitsblatt",
    "Eigenschaften aktualisieren",
    "REST API",
    "Cloud",
    "v3.0",
  ]
description: "Erfahren Sie, wie Sie Basiseigenschaften (z. B. Nullen anzeigen, Lineal-Sichtbarkeit) eines Excel-Arbeitsblatts mithilfe der Aspose.Cells Cloud REST API v3.0 aktualisieren. Enthält cURL-Anforderung, SDK-Beispiele, Parameter und Fehlerbehandlung."
ArticleTitle: "Arbeitsblatt-Eigenschaften aktualisieren – Aspose.Cells Cloud API-Referenz (v3.0)"
---

Diese REST-API aktualisiert die Basiseigenschaften eines Arbeitsblatts.

## REST API

**Voraussetzungen:** Sie benötigen einen gültigen Aspose Cloud-Account, erhalten ein JWT-Zugriffstoken und stellen sicher, dass die Zielarbeitsmappe in einem unterstützten Speicherort gespeichert ist. Alle Anforderungen müssen über **HTTPS** erfolgen.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Anforderungsparameter**

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                         |
| -------------- | ------ | -------------------------- | --------------------------------------------------------------------------------------------------- |
| name           | string | path                       | Dateiname der Arbeitsmappe (einschließlich Erweiterung).                                            |
| sheetName      | string | path                       | Name des zu aktualisierenden Arbeitsblatts.                                                         |
| sheet          | object | body                       | JSON-Objekt mit Schlüssel-Wert-Paaren für Arbeitsblatt-Eigenschaften (z. B. `DisplayZeros`, `IsRulerVisible`). |
| folder         | string | query                      | Ordnerpfad im Speicher, in dem sich die Arbeitsmappe befindet.                                      |
| storageName    | string | query                      | Name des zu verwendenden Speichers.                                                                 |

Das **sheet**-Objekt wird als JSON im Anforderungstext gesendet. Zu den Beispieleigenschaften, die geändert werden können, zählen `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible` und weitere, wie in der API-Spezifikation definiert.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

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

Typische Antwortcodes:

- **200** – Erfolgreich. Die Arbeitsblatt-Eigenschaften wurden aktualisiert.
- **400** – Ungültige Anforderung (z. B. fehlerhaftes JSON oder fehlender erforderlicher Parameter).
- **401** – Nicht autorisiert – fehlendes oder ungültiges JWT-Token.
- **404** – Arbeitsmappe oder Arbeitsblatt nicht gefunden.
- **500** – Interner Serverfehler.

| Code | Bedeutung |
|------|-----------|
| 200 | Erfolg – die Arbeitsblatt-Eigenschaften wurden aktualisiert. |
| 400 | Ungültige Anforderung – fehlerhaftes JSON oder fehlender erforderlicher Parameter. |
| 401 | Nicht autorisiert – fehlendes oder ungültiges JWT-Token. |
| 404 | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht. |
| 500 | Interner Serverfehler. |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}