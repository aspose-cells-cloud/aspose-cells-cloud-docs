---
title: "Aspose.Cells Cloud Excel Web-API zum Hinzufügen von Arbeitsblättern – Einfügen neuer Blätter mit Typ- und Positionssteuerung"
second_title: "Dokument"
ArticleTitle: "So fügen Sie Arbeitsblätter zu Excel hinzu – Einfügen neuer Blätter an spezifischen Positionen"
linktitle: "Arbeitsblatt zu Tabellendokument hinzufügen"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "Excel, Arbeitsblatt hinzufügen, Aspose Cells API, Tabellendokument, Cloud-API, Blatttyp, Blattposition"
description: "Erfahren Sie, wie Sie programmgesteuert ein neues Arbeitsblatt, Diagrammblatt oder Makroblatt in eine Excel-Arbeitsmappe mit der Aspose.Cells Cloud API hinzufügen. Steuern Sie Blatttyp, Name und Einfügeposition mit einem einzigen REST-Aufruf."
weight: 100
---

Fügen Sie programmgesteuert Arbeitsblätter zu Excel-Dateien hinzu und behalten Sie volle Kontrolle über den Blatttyp und die Position. Fügen Sie Standardarbeitsblätter, Diagrammblätter oder Makroblätter an beliebigen Positionen in der Arbeitsmappe ein. Dieser REST-basierte Vorgang ermöglicht die automatisierte Verwaltung und Organisation von Excel-Arbeitsmappen.

**Voraussetzungen**

- Ein aktiver Aspose.Cells Cloud-Account mit einem gültigen JWT-Zugriffstoken.
- Ein konfigurierter Cloud-Speichername (z. B. `CompanyOneDrive`), in dem die Arbeitsmappe gespeichert werden soll.
- Die Zielarbeitsmappe muss im angegebenen Speicher zugänglich sein; bei passwortgeschützten Dateien ist das korrekte Passwort anzugeben.

| **Blatttyp**             | Beschreibung                                           |
| :----------------------- | :----------------------------------------------------- |
| **VB**                   | Visual-Basic-Modul                                     |
| **Worksheet**            | Normales Arbeitsblatt                                  |
| **Chart**                | Diagrammblatt                                          |
| **BIFF4Macro**           | BIFF4-Makroblatt                                       |
| **InternationalMacro**   | Internationales Makroblatt                             |
| **Other**                | Benutzerdefiniertes oder seltenerer Blatttyp (nicht oben aufgeführt) |
| **Dialog**               | Dialogarbeitsblatt                                     |

## **API zum Hinzufügen eines Arbeitsblatts zu einem Tabellendokument**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername      | Typ    | Speicherort | Beschreibung                                                                                                                                                                                                 |
| :----------------- | :----- | :---------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Datei  | FormData    | **Erforderlich.** Die Excel-Arbeitsmappe (.xlsx, .xls usw.), zu der ein neues Arbeitsblatt hinzugefügt werden soll.                                                                                          |
| **sheetType**      | String | Query       | **Optional.** Der Typ des zu erstellenden Blatts. Zulässige Werte sind `worksheet` (Standard), `chartsheet`, `macrosheet`, `vbmodule` und `dialog`.                                                       |
| **position**       | Integer| Query       | **Optional.** Nullbasierter Index, an dem das neue Blatt eingefügt werden soll. `0` fügt es vor dem ersten Blatt ein; `2` fügt es als drittes Blatt ein. Weglassen, um das Blatt am Ende anzuhängen.       |
| **sheetName**      | String | Query       | **Optional.** Name für das neue Arbeitsblatt. Muss innerhalb der Arbeitsmappe eindeutig sein. Bei Weglassen wird ein Standardname wie „SheetX“ generiert.                                                   |
| **outPath**        | String | Query       | **Optional.** Zielverzeichnis im Cloud-Speicher, in dem die bearbeitete Arbeitsmappe gespeichert wird. Bei `null` oder Weglassen wird die Arbeitsmappe am gleichen Speicherort wie die Quelldatei oder in einem Standardpfad gespeichert. |
| **outStorageName** | String | Query       | **Erforderlich.** Bezeichner des konfigurierten Cloud-Speichers (z. B. `CompanyOneDrive`), in den die Ausgabedatei geschrieben werden soll.                                                                 |
| **region**         | String | Query       | **Optional.** Gebietsschema-Einstellung (z. B. `de-DE`), die das Formatieren und regionale Regeln im neuen Arbeitsblatt beeinflussen kann.                                                                   |
| **password**       | String | Query       | **Optional.** Passwort zur Entschlüsselung und Bearbeitung einer passwortgeschützten Arbeitsmappe. Weglassen, falls die Datei nicht verschlüsselt ist.                                                        |

### Antwort

Bei Erfolg gibt die API **HTTP 200 OK** (oder **201 Created**, falls eine neue Datei erzeugt wird) mit der aktualisierten Arbeitsmappe zurück.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                                 |
| ---- | --------------------- | ---------------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                                  |

## Wofür sollte die API zum Hinzufügen eines Arbeitsblatts zu einem Tabellendokument verwendet werden?

- **Automatisierte Berichterstellung** – Erstellen und Einfügen monatlicher Arbeitsblätter (z. B. `2024‑05`) dynamisch bei der Erstellung von Finanzberichten.
- **Stapelweise Vorlageninitialisierung** – Hinzufügen eines dedizierten Analysearbeitsblatts für jeden neuen Kunden oder jedes neue Projekt bei der Massenerstellung von Verkaufsangeboten oder Vorschlägen.
- **Dynamische Dashboard-Erweiterung** – Einfügen neuer Diagrammblätter in Echtzeit, sobald neue Datenmerkmale verfügbar sind.
- **Compliance und Audit-Archivierung** – Automatisches Hinzufügen von Nachweissammlungsblättern während jährlicher Audits, um jeden Prüfpunkt isoliert zu halten.
- Zum Entfernen eines Blatts siehe den Vorgang **[Arbeitsblatt löschen](/delete-worksheet/)**.
- Zum Verschieben eines Blatts siehe den Vorgang **[Arbeitsblatt verschieben](/move-worksheet/)**.

## Warum sollte man die API zum Hinzufügen eines Arbeitsblatts zu einem Tabellendokument verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud stellt SDKs für mehrere Sprachen zur Verfügung, reduziert den Entwicklungsaufwand und bietet umfangreiche Dokumentation.
- **Reduzierte Arbeitskosten** – Entfällt das manuelle Erstellen von Arbeitsblättern und wiederholtes Kopieren-Einfügen.
- **Pay-per-Use** – Sie zahlen nur für die tatsächlich durchgeführten API-Aufrufe.
- **Kein Wartungsaufwand** – Keine Server zu verwalten, keine Software-Updates und keine Kompatibilitätsprobleme.

## Wie verwendet man die API zum Hinzufügen eines Arbeitsblatts zu einem Tabellendokument mit SDKs

### Spezifikation der API zum Hinzufügen eines Arbeitsblatts zu einem Tabellendokument

Die [Spezifikation der API zum Hinzufügen eines Arbeitsblatts zu einem Tabellendokument](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encodiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs abstrahiert die niederwertigen Details und ermöglicht das Hinzufügen eines Arbeitsblatts mit minimalem Codeaufwand. Die vollständige Liste der SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie der Dienst mit verschiedenen SDKs aufgerufen wird:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}