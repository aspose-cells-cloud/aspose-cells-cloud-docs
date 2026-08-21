---
title: "Zeilen in einer Excel-Arbeitsmappe automatisch anpassen"
second_title: "Dokument"
linktitle: "Zeilen"
type: docs
url: /de/autofit-rows-on-an-excel-file/
aliases: [  /de/auto-fit-rows-in-excel-workbooks/ , /de/workbook/autofit/rows/ ]
keywords: "Zeilen automatisch anpassen, Excel-Arbeitsmappe, Aspose.Cells Cloud, REST-API, Auto-Fitter-Optionen"
description: "Erfahren Sie, wie Sie die Zeilenhöhe in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST-API automatisch anpassen können. Enthält Endpunkt, Parameter, cURL-Beispiel und SDK-Snippets für C#, Java, Python und mehr."
weight: 90
ArticleTitle: "Zeilen in einer Excel-Arbeitsmappe automatisch anpassen – Aspose.Cells Cloud API"
---

**Voraussetzungen**  
Bevor Sie die API aufrufen, beschaffen Sie ein gültiges Bearer-JWT-Token vom Aspose-Authentifizierungsdienst und stellen sicher, dass die Ziel-Arbeitsmappe in einem unterstützten Speicherort gespeichert ist (Standardspeicher oder ein benutzerdefinierter Speicher, den Sie konfiguriert haben).

Diese REST-API ermöglicht es Ihnen, **Zeilen in einer Excel-Arbeitsmappe automatisch anzupassen**, wobei die Zeilenhöhe nach dem Einfügen oder Ändern von Daten automatisch angepasst wird.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

Die Anforderungsparameter sind wie folgt definiert:

| Parametername     | Typ               | Ort     | Beschreibung                                                                                   |
| ----------------- | ----------------- | ------- | ---------------------------------------------------------------------------------------------- |
| name              | string            | path    | Name der Arbeitsmappen-Datei.                                                                  |
| autoFitterOptions | AutoFitterOptions | body    | Optionen, die das Verhalten der automatischen Anpassung steuern.                              |
| startRow          | integer           | query   | Index der ersten Zeile, die automatisch angepasst werden soll.                                |
| endRow            | integer           | query   | Index der letzten Zeile, die automatisch angepasst werden soll.                               |
| firstColumn       | integer           | query   | Index der ersten Spalte, die bei der automatischen Anpassung berücksichtigt wird.             |
| lastColumn        | integer           | query   | Index der letzten Spalte, die bei der automatischen Anpassung berücksichtigt wird.            |
| onlyAuto          | boolean           | query   | Falls **true**, werden nur Zeilen mit aktiviertem AutoFit-Flag verarbeitet (Standard: **false**). |
| folder            | string            | query   | Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.                                           |
| storageName       | string            | query   | Name des Speicherdiensts.                                                                      |

**AutoFitterOptions** ist ein Objekt, das festlegt, wie der Vorgang der automatischen Anpassung ausgeführt wird (z. B. `AutoFitMergedCells`, `IgnoreHidden`).

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.        |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die maximale Größe.                    |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste aufzurufen. Ersetzen Sie `<jwt token>` durch ein gültiges Bearer-JWT-Token, das Sie vom Aspose-Authentifizierungsdienst erhalten haben.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Beispiel einer Fehlerantwort (z. B. fehlende Arbeitsmappe):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "Die angegebene Arbeitsmappe 'myWorkbook.xlsx' ist nicht vorhanden."
}
```

{{< /tab >}}

{{< /tabs >}}

**Hinweise**  
- Wenn `AutoFitMergedCells` auf **true** gesetzt ist, werden verschmelzte Zellen bei der automatischen Anpassung als einzelnes Element betrachtet.  
- Wenn `IgnoreHidden` auf **true** gesetzt ist, werden ausgeblendete Zeilen und Spalten ignoriert, wodurch ihre aktuellen Abmessungen beibehalten werden.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}