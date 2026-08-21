---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "FlipData"
type: docs
url: /cells/flip
aliases: []
keywords: "FlipData, Transformieren, Aspose.Cells"
description: "Transponiert einen angegebenen Datenbereich in einer Tabellendatei."
weight: 100
---

## FlipData von Aspose.Cells Cloud-Webdiensten

Diese API kehrt die Ausrichtung einer gegebenen Datenmatrix um. Beispielsweise wird ein Bereich von 3×2 (3 Zeilen, 2 Spalten) zu einem Bereich von 2×3 (2 Zeilen, 3 Spalten) in der Ausgabe. Dies wird häufig verwendet, um Daten neu zu strukturieren, um die Eingabeanforderungen unterschiedlicher Diagramme, Berichte oder Datenmodelle zu erfüllen.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|---------------|--------|------------------------------------|--------------|
| Spreadsheet   | Datei  | FormData                           | Hochladen der Tabellendatei. |
| worksheet     | String | Abfrage                            | Der Name des Arbeitsblatts. |
| cellArea      | String | Abfrage                            | Ein angegebener Datenbereich. |
| Horizontal    | Boolean | Abfrage                           | Horizontales/Vertikales Umkehren. Standardwert: true |
| outPath       | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| outStorageName| String | Abfrage                            | Speichername für die Ausgabedatei. |
| region        | String | Abfrage                            | Regions-/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password      | String | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| *Keine*       | *N/V* | *Kein zusätzliches JSON-Body erforderlich; die Datei wird als multipart/form-data gesendet.* |

### **Antwort**

```json
{
  "File": "<binärer Stream der transformierten Arbeitsmappe>"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200  | OK        | Der Vorgang wurde erfolgreich abgeschlossen, und die transformierte Tabellendatei wird zurückgegeben. |
| 400  | Bad Request | Ein oder mehrere erforderliche Parameter fehlen oder sind ungültig. |
| 401  | Unauthorized | Authentifizierung fehlgeschlagen – fehlender oder ungültiger JWT-Token. |
| 413  | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500  | Internal Server Error | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

## Verwendung von FlipData mit SDKs

### FlipData-Spezifikation

Die [FlipData-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=de-DE&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<binärer Stream der transformierten Arbeitsmappe>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Methode, um die Entwicklung zu beschleunigen. Ein SDK abstractiert die niederleveligen Details und ermöglicht es Ihnen, sich auf Ihre Projektanforderungen zu konzentrieren. Bitte prüfen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
 `[TBD]`
---