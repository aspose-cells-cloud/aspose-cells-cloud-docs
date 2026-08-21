---
title: "Aspose.Cells Cloud File Copy API – Eine Schnittstelle zum schnellen Kopieren und Stapelverarbeitung von Excel-Dateien in der Cloud"
second_title: "Dokument"
ArticleTitle: "Cloud-basierte Excel-Dateiverwaltungslösung – Detaillierte Erklärung der Stapelkopierfunktion der Aspose.Cells Copy File API"
linktype: "docs"
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel-Dateikopie, Cloud-Speicher, REST API"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud CopyFile API verwenden, um Excel-Dateien effizient zu duplizieren und diese über verschiedene Speicherorte hinweg zu verwalten."
weight: 100
---

Die **copyFile** API ermöglicht es Benutzern, eine Excel-Datei von einem angegebenen Quellpfad in einen Zielpfad zu kopieren und unterstützt verschiedene Speicheroptionen.

## **Excel API: Datei kopieren**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Die Anforderungsparameter der **copyFile** API sind

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                          |
| ----------------- | ------ | ---------------------------------- | ----------------------------------------------------- |
| srcPath           | String | Pfad                               | Der Quellpfad der zu kopierenden Datei.              |
| destPath          | String | Abfrage                            | Der Zielpfad, an dem die Datei gespeichert wird.     |
| srcStorageName    | String | Abfrage                            | Der Name des Quellspeichers.                         |
| destStorageName   | String | Abfrage                            | Der Name des Zielspeichers.                          |
| versionId         | String | Abfrage                            | Optionale Version-ID der zu kopierenden Datei.       |

### **Antwort**

Der Vorgang gibt bei Erfolg keinen Inhalt zurück. Typische HTTP-Statuscodes sind:

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                      |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.  |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                              |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.     |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                        |

## Wie verwendet man die Copy File API mit SDKs?

### Copy File API-Spezifikation

Die [Copy File API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) stellt eine öffentlich zugängliche Programmierschnittstelle für REST-basierte Interaktionen bereit, die direkt aus einem Webbrowser durchgeführt werden können.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer IHR_ZUGRIFFSTOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung, da sie detaillierte Low-Level-Details abstrahiert und es Ihnen ermöglicht, Tabellendaten aus Tabellenkalkulationen mit minimalem Code in Bilder umzuwandeln. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden: