---
title: "Mehrere Zeilen aus einem Excel-Arbeitsblatt löschen"
second_title: "Dokument"
linktitle: "Zeilen"
type: docs
url: /de/rows/delete/rows/
keywords: "Aspose.Cells Cloud, Zeilen löschen, mehrere Zeilen löschen, Excel-Arbeitsblatt, REST-API, SDK"
description: "Erfahren Sie, wie Sie eine oder mehrere Zeilen aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API löschen. Enthält Endpunkt-Details, Parameter, ein cURL-Beispiel und SDK-Codebeispiele für verschiedene Sprachen."
weight: 80
ArticleTitle: "Mehrere Zeilen aus einem Excel-Arbeitsblatt mit der Aspose.Cells Cloud API löschen"
---

Diese REST-API löscht mehrere Zeilen **aus** einem Excel-Arbeitsblatt.

**Voraussetzungen:** Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges JWT-Zugriffstoken, das Sie über die Aspose-Cloud-Authentifizierung erhalten haben, sowie entsprechende Speicherberechtigungen für die Arbeitsmappe.

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Pfad / Abfragezeichenfolge / HTTP-Body | Beschreibung                                                                 |
| ---------------- | ------- | -------------------------------------- | ----------------------------------------------------------------------------- |
| name             | string  | path                                   | Der Name der Arbeitsmappe.                                                    |
| sheetName        | string  | path                                   | Der Name des Arbeitsblatts.                                                   |
| startrow         | integer | query                                  | Nullbasierter Index der ersten zu löschenden Zeile (z. B. `0` = erste Zeile). |
| totalRows        | integer | query                                  | Die Anzahl der zu löschenden Zeilen.                                          |
| updateReference  | boolean | query                                  | Gibt an, ob Verweise nach dem Löschen aktualisiert werden sollen (`true`/`false`). |
| folder           | string  | query                                  | Der Dokumentordner.                                                           |
| storageName      | string  | query                                  | Der Speichername.                                                             |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden. **Alle Endpunkte erfordern HTTPS; HTTP ist veraltet.**

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
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

**Mögliche Antwortcodes**

| HTTP-Status | Beschreibung                                      |
|-------------|---------------------------------------------------|
| 200         | Zeilen erfolgreich gelöscht.                      |
| 400         | Ungültige Anforderung – ungültige Parameter.     |
| 401         | Nicht autorisiert – fehlendes oder ungültiges JWT-Token. |
| 404         | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht. |
| 500         | Interner Serverfehler – unerwarteter Zustand.    |

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Bitte schauen Sie sich das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}