---
title: "Aspose.Cells Cloud – Spalten, Zeilen und Bereiche tauschen (v4.0)"
second_title: "Dokument"
ArticleTitle: "Daten zwischen Spalten, Zeilen und Zellen in Excel austauschen/täuschen"
linktitle: "Bereich tauschen"
type: docs
url: /de/swap-range/
keywords: "Aspose Cells, Excel API, Bereich tauschen, Cloud-Tabellenkalkulation"
description: "Tauschen Sie Spalten, Zeilen oder Bereiche in Excel-Dateien mit der Aspose.Cells Cloud API aus. Behalten Sie Formatierung, Formeln und Zellbezüge in einem einzigen Aufruf bei."
weight: 100
---

Tauschen Sie Daten zwischen beliebigen zwei Spalten, Zeilen, Bereichen oder Zellen in Excel-Dateien automatisch mit der Aspose.Cells Cloud API aus. Die API „Bereich tauschen“ ermöglicht präzises Austauschen von Daten, wobei alle Formatierungen, Formeln und Zellbezüge erhalten bleiben. Sie unterstützt komplexe Neuanordnungen von Daten, Stapelverarbeitung und nahtlose Cloud-Integration für Unternehmensworkflows.

## **API „Bereich tauschen“**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anfrageparameter**

| Parametername      | Typ    | Ort      | Beschreibung                                                                                                                                  |
| ------------------ | ------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Datei  | FormData | **Erforderlich.** Die Quell-Excel-Arbeitsmappe (`.xlsx`, `.xls`).                                                                           |
| **worksheet1**     | String | Query    | **Erforderlich.** Name des Arbeitsblatts, das den ersten Datenbereich enthält.                                                              |
| **range1**         | String | Query    | **Erforderlich.** Zellbereich (z. B. `A1:D10`) in `worksheet1`, der ausgetauscht werden soll.                                                |
| **worksheet2**     | String | Query    | **Erforderlich.** Name des Arbeitsblatts, das den zweiten Datenbereich enthält (kann identisch mit `worksheet1` sein).                      |
| **range2**         | String | Query    | **Erforderlich.** Zellbereich (z. B. `F1:I10`) in `worksheet2`, der ausgetauscht werden soll. **Wichtig:** `range1` und `range2` müssen die gleiche Abmessung haben. |
| **outPath**        | String | Query    | **Optional.** Cloud-Speicherordner, in dem die bearbeitete Arbeitsmappe gespeichert wird.                                                   |
| **outStorageName** | String | Query    | **Erforderlich.** Name des konfigurierten Cloud-Speicherdienstes (z. B. `MyCompanyStorage`).                                                |
| **region**         | String | Query    | **Optional.** Gebietsschema-Einstellung (z. B. `de-DE`, `en-US`, `ja-JP`), die die Formatierung beeinflussen kann.                           |
| **password**       | String | Query    | **Optional.** Passwort zur Entschlüsselung einer geschützten Tabellendatei. Weglassen, falls nicht verschlüsselt.                            |

**Beispielanfrage (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

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

**Hinweise:**  
- Die API gibt die bearbeitete Arbeitsmappe als Dateistream zurück. Falls `outPath` angegeben ist, wird die Datei zusätzlich am angegebenen Cloud-Speicherort gespeichert.  
- Eine Abweichung in den Abmessungen der Bereiche führt zu einem Fehler **400 Bad Request**.

### Fehlercodes

| Code                 | Beschreibung                                                               |
| -------------------- | -------------------------------------------------------------------------- |
| **400 Bad Request**  | Ungültige Anforderungs-URI oder nicht übereinstimmende Bereichsabmessungen. |
| **401 Unauthorized** | Ungültiges oder abgelaufenes Zugriffstoken; Client-ID oder Geheimnis falsch. |
| **404 Not Found**    | Die angegebene Tabellendatei ist nicht erreichbar.                         |
| **500 Server Error** | Beim Verarbeiten der Arbeitsmappe ist ein interner Fehler aufgetreten.     |

## Wofür sollte die API „Bereich tauschen“ verwendet werden?

- **Neustrukturierung von Finanzmodellen** – Datenblöcke neu anordnen (z. B. Q3-Prognose nach Q4 verschieben), ohne Formeln und bedingte Formatierungen zu verlieren.
- **Datenpipelines und ETL-Prozesse** – Rohdatenbereiche mit bereinigten Bereichen in einer Zwischentabelle austauschen, bevor die endgültige Ausgabe erfolgt.
- **Fehlerkorrektur und Datenwiederherstellung** – Falsch platzierte Daten schnell korrigieren, ohne manuelles Kopieren und Einfügen.

## Warum die API „Bereich tauschen“ verwenden?

- **Entwicklerfreundlich** – SDKs stehen für mehrere Programmiersprachen zur Verfügung und reduzieren den Entwicklungs-Aufwand im Vergleich zur Erstellung eigener Lösungen.
- **Kosteneinsparung** – Automatisiert das Neuanordnen von Daten und reduziert den Bedarf an manueller Konsolidierung.
- **Pay-per-Use** – Sie zahlen nur für die tatsächlich getätigten API-Aufrufe.
- **Kein Wartungsaufwand** – Keine Server zu verwalten, keine Softwareupdates und keine Kompatibilitätsprobleme.

## Verwendung der API „Bereich tauschen“ mit SDKs

### Spezifikation der API „Bereich tauschen“

Die [Spezifikation der API „Bereich tauschen“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie detaillierte Low-Level-Details abstrahiert und so das Tauschen von Bereichen mit kurzen Codezeilen ermöglicht. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}