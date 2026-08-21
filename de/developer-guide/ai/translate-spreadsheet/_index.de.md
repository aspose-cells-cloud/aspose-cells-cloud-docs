---
title: "Aspose.Cells Cloud Web API – Übersetzen einer Tabellendatei in die Zielsprache"
second_title: "Dokument"
ArticleTitle: "So übersetzen Sie eine gesamte Tabellendatei mithilfe der Aspose.Cells Cloud KI-Übersetzung-API"
linktitle: "Tabellendatei übersetzen"
type: docs
url: /de/translate-spreadsheet/
keywords: "Aspose.Cells Cloud, Übersetzungs-API für Tabellendateien, KI-Übersetzung, Übersetzung von Tabellendateien, targetLanguage, Übersetzung mehrerer Arbeitsblätter, Cloud-basierte Verarbeitung von Tabellendateien, Aspose.Cells Cloud-Übersetzung"
description: "Übersetzen Sie eine gesamte Excel-Arbeitsmappe mit Aspose.Cells Cloud KI. Beibehaltung von Formeln, Diagrammen und Formatierungen bei der Umwandlung von Text in jede unterstützte Sprache. Erfahren Sie mehr über Endpunkt, Parameter, SDK-Beispiele, Einschränkungen und Fehlerbehandlung."
weight: 100
---

Der **TranslateSpreadsheet**-Endpunkt, Teil der **Übersetzungs-API für Tabellendateien**, liest jedes Textelement einer Arbeitsmappe ein, sendet den Inhalt an einen KI-gestützten Übersetzungsdienst und gibt eine neue Tabellendatei zurück, in der alle Textdaten in der angegebenen **targetLanguage** wiedergegeben werden. Der Vorgang behält das ursprüngliche Layout, die Zellstile, Formeln und **die** Struktur mit mehreren Arbeitsblättern bei, wodurch er sich ideal für die Internationalisierung von Berichten, Dashboards und datengetriebenen Dokumenten eignet. Unterstützte Dateiformate sind XLS, XLSX, XLSM, CSV und ODS. Fehler werden bei ungültigen Sprachcodes, Authentifizierungsfehlern oder Ausfällen des Übersetzungsdienstes zurückgegeben.

## **Übersetzungs-API für Tabellendateien**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **Anforderungsparameter:**

| Parametername | Typ    | Speicherort | Erforderlich/Optional | Beschreibung                                                                                                                                                                                                 |
| :------------ | :----- | :---------- | :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | Datei  | Erforderlich | FormData              | Die zu übersetzende Excel-Arbeitsmappe. Zulässige Erweiterungen: .xls, .xlsx, .xlsm, .csv, .ods. Maximale Dateigröße: 50 MB. Beispiel: `budget.xlsx`.                                                        |
| targetLanguage | Zeichenfolge | Erforderlich | Abfrage | ISO-639-1-Sprachcode für die gewünschte Ausgabesprache (z. B. „es“ für Spanisch, „fr“ für Französisch, „de“ für Deutsch). Muss eine Sprache sein, die vom zugrunde liegenden KI-Dienst unterstützt wird. |
| region        | Zeichenfolge | Optional   | Abfrage | Regionenkennung der Tabellendatei, die länderspezifische Formatierungen wie Daten, Zahlen und Währungen beeinflusst. Gängige Werte: „US“, „EU“, „CN“. Bei Weglassung wird die ursprüngliche Regioneneinstellung der Arbeitsmappe verwendet. |
| password      | Zeichenfolge | Optional   | Abfrage | Passwort zum Öffnen einer geschützten Arbeitsmappe. Leer lassen, wenn die Datei nicht passwortgeschützt ist.                                                                                                 |

### **Antwort**

Erfolgreiche Antwort (200 OK)  
Header:  
Content-Type: application/octet-stream // bzw. text/csv, wenn CSV-Ausgabe angefordert wurde  
Content-Disposition: attachment; filename="translated.xlsx"  
Content-Length: <Größe in Bytes>

Body:  
<Binärstream, der die übersetzte Tabellendatei enthält>

Fehlerantworten folgen dem standardmäßigen Aspose.Cells Cloud-Fehlermodell (application/json) mit den Feldern `code`, `message` und optional `details`.

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wann sollte die Übersetzungs-API für Tabellendateien verwendet werden?

- **Internationale Finanzberichterstattung** – Konvertieren Sie quartalsweise Excel-Berichte in mehrere Sprachen für regionale Niederlassungen, während Formeln und Diagrammlayouts beibehalten werden.
- **Mehrsprachige Marketing-Dashboards** – Automatisch lokalisierte Versionen von Verkaufsleistungs-Dashboards für globale Teams generieren.
- **Verteilung von Bildungsinhalten** – Übersetzen von Notenbüchern, Aufgabenblättern oder Lehrplänen in Tabellenform für Schüler in verschiedenen Ländern, ohne manuelles Kopieren und Einfügen.
- **Regulatorische Compliance** – Erstellung sprachspezifischer Compliance-Tabellen, die Validierungsregeln und Datenvalidierungslisten beibehalten.

## Warum sollte man die Übersetzungs-API für Tabellendateien verwenden?

- **KI-gesteuerte Genauigkeit** – Nutzt modernste neuronale Übersetzungsmodelle für kontextbewusste, qualitativ hochwertige Sprachumwandlung.
- **Keine Layout-Störung** – Behält Zellformeln, bedingte Formatierungen, Diagramme und Reihenfolge der Arbeitsblätter exakt wie in der Originaldatei bei.
- **Mehrfacharbeitsblattverarbeitung mit einem einzigen Aufruf** – Übersetzt jedes Arbeitsblatt in einer einzigen Anforderung, sodass Schleifen pro Arbeitsblatt entfallen.
- **Nahtlose Cloud-Integration** – Funktioniert mit der Aspose.Cells Cloud-Authentifizierung und ermöglicht automatisierte Workflows in CI/CD, serverlosen Funktionen oder Unternehmens-Backends.

## Wie verwendet man die Übersetzungs-API für Tabellendateien mit SDKs

### Spezifikation der Übersetzungs-API für Tabellendateien

Die [Spezifikation der Übersetzungs-API für Tabellendateien](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) stellt eine öffentlich zugängliche Programmierschnittstelle zur Ausführung von REST-Interaktionen direkt aus einem Webbrowser bereit.

## Excel-API-SDK

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist der schnellste Weg zur Entwicklung, da sie die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, eine Tabellendatei mit kurzem Code in eine andere zu zusammenzufügen.  
Bitte überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.  
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs mit den Aspose.Cells-Webdiensten interagieren:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}