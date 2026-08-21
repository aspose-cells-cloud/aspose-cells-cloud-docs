---
title: "Alle Änderungen in einer Remote-Tabelle akzeptieren"
ArticleTitle: "Alle Änderungen in einer Remote-Tabelle akzeptieren – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Alle Änderungen in einer Remote-Tabelle akzeptieren"
type: docs
url: /cells/accept-all-revisions
aliases: ["/cells/accept-all-revisions"]
keywords: "Aspose.Cells, AcceptAllRevisions, Remote-Tabelle"
description: "Akzeptiert alle Änderungen (Überarbeitungen) in einer Remote-Tabelle und gibt die aktualisierte Arbeitsmappe als Datei zurück."
weight: 1000
---

## Die Funktion „Alle Änderungen in einer Remote-Tabelle akzeptieren“ der Aspose.Cells Cloud-Webdienste

Akzeptiert alle verfolgten Änderungen (Überarbeitungen) in der angegebenen Arbeitsmappe, die im Remote-Speicher gespeichert ist. Der Vorgang kann optional die resultierende Arbeitsmappe an einem anderen Speicherort oder in einem anderen Speicher speichern und gibt die aktualisierte Datei als Binärstream zurück.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|----------------|------|-------------------------------------|--------------|
| name | string | Pfad | Der Name der im Remote-Speicher gespeicherten Arbeitsmappendatei. |
| folder | string | Abfrage | (Optional) Der Ordner im Speicher, in dem sich die Arbeitsmappe befindet. |
| storageName | string | Abfrage | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Standardmäßig wird der Standard-Speicher verwendet, wenn dieser Parameter weggelassen wird. |
| outPath | string | Abfrage | (Optional) Der Ordnerpfad, in dem die aktualisierte Arbeitsmappe gespeichert werden soll. Der Standardwert ist null. |
| outStorageName | string | Abfrage | (Optional) Speichername für die Ausgabedatei. |
| fontsLocation | string | Abfrage | (Optional) Pfad zu einem benutzerdefinierten Schriftartenordner. |
| region | string | Abfrage | (Optional) Region/Spracheinstellung der Tabelle (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password | string | Abfrage | (Optional) Das Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| *Keine* | *Keine* | Dieser Vorgang erfordert keinen Anforderungstext. |

### **Antwort**

```json
{
  "File": "Binärstream der aktualisierten Arbeitsmappe (z. B. .xlsx), der im Antworttext zurückgegeben wird."
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Arbeitsmappe mit akzeptierten Änderungen wird als Binärdateistream zurückgegeben. |
| 400 | Ungültige Anfrage | Fehlende erforderliche Parameter oder ungültiges Anfrageformat. |
| 401 | Nicht autorisiert | Ungültiges oder fehlendes JWT-Token. |
| 413 | Anforderungstext zu groß | Die Anfrage überschreitet die zulässigen Größenbegrenzungen. |
| 500 | Interner Serverfehler | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

## Verwendung von „Alle Änderungen in einer Remote-Tabelle akzeptieren“ mit SDKs

### Spezifikation für „Alle Änderungen in einer Remote-Tabelle akzeptieren“

Die [API-Spezifikation für „Alle Änderungen in einer Remote-Tabelle akzeptieren“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die direkte Durchführung von REST-Interaktionen über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "Binärstream der aktualisierten Arbeitsmappe (z. B. .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Methode, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Details auf niedriger Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
 `[TBD]`
---