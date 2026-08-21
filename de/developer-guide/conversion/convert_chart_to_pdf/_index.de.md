---
title: "Diagramm in PDF konvertieren"
ArticleTitle: "Diagramm in PDF konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "ConvertChartToPdf"
type: docs
url: /cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, Diagramm-Konvertierung"
description: "Konvertiert ein Diagramm einer Tabellendatei von einer lokalen Festplatte in PDF."
weight: 100
---

## Die Konvertierung von Diagrammen in PDF über Aspose.Cells Cloud-Webdienste

Diese Methode liest ein Diagramm aus einer Tabellendatei, die über einen lokalen Datei-Upload bereitgestellt wird, wandelt es in das PDF-Format um und gibt das konvertierte Ergebnis zurück. Sie erfolgt vollständig auf dem Cloud-Server, sodass keine Zwischenspeicherung erforderlich ist. Der Quelldateipfad und das Zielformat müssen korrekt sein, und es sind entsprechende Berechtigungen erforderlich, um die Quelldatei zu lesen. Fehler wie fehlende Dateien, Zugriffsprobleme oder Konvertierungsfehler führen zu entsprechenden HTTP-Fehlerantworten.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|------------------|--------|------------------------------------|--------------|
| Spreadsheet      | Datei  | FormData                           | Hochzuladende Tabellendatei. |
| worksheet        | String | Abfrage                            | Name des Arbeitsblatts der Tabellendatei. |
| chartIndex       | Integer| Abfrage                            | Diagrammindex innerhalb des Arbeitsblatts. |
| outPath          | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| outStorageName   | String | Abfrage                            | Speichername für die Ausgabedatei. |
| fontsLocation    | String | Abfrage                            | Verwendung benutzerdefinierter Schriftarten. |
| region           | String | Abfrage                            | Regionale/lokale Einstellung der Tabellendatei (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und regionsbezogenes Verhalten. |
| password         | String | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ  | Beschreibung                  |
|---------------|------|-------------------------------|
| Spreadsheet   | Datei | Hochzuladende Tabellendatei. |

### **Antwort**

```json
{
  "ResponseFile": "binärer PDF-Dateistream"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Diagramm erfolgreich in PDF konvertiert; binäre PDF-Datei zurückgegeben. |
| 400 | Ungültige Anforderung | Ungültige Anforderungsparameter oder fehlerhafte URL. |
| 401 | Nicht autorisiert | Authentifizierung fehlgeschlagen oder keine Anmeldedaten bereitgestellt. |
| 404 | Nicht gefunden | Quelldatei nicht zugänglich. |
| 413 | Anforderungstext zu groß | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Interner Serverfehler | Beim Verarbeiten der Konvertierung ist ein Fehler aufgetreten. |

## Verwendung der Konvertierung von Diagrammen in PDF mit SDKs

### Spezifikation für die Konvertierung von Diagrammen in PDF

Die [API-Spezifikation für die Konvertierung von Diagrammen in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}
{< tab tabNum="1" >}
```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "binärer PDF-Dateistream"
}
```
{< /tab >}
{< /tabs >}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstractiert die low-Level-Details, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---