---
title: "Object Exists API – Überprüfen der Datei-/Ordnerpräsenz in Aspose.Cells Cloud"
second_title: "Dokument"
ArticleTitle: "Object Exists API – Überprüfen der Datei- oder Ordnerpräsenz in Aspose.Cells Cloud"
linktype: "docs"
url: "/object-exists/"
keywords: "Aspose.Cells, Cloud-Speicher, Objekt vorhanden, Dateivorhandensein, Ordnervorhandensein, API"
description: "Verwenden Sie die Object Exists API, um schnell zu überprüfen, ob eine Datei oder ein Ordner im Aspose.Cells Cloud-Speicher vorhanden ist. Unterstützt optional den Speichernamen und die Version-ID sowie versionierte Objekte."
weight: 100
---

Die **Object Exists API** ermöglicht Entwicklern, festzustellen, ob eine bestimmte Datei oder ein bestimmter Ordner im Aspose.Cells Cloud-Speicher vorhanden ist. Sie gibt einen einfachen Boolean-Wert zurück, der die Existenz angibt, sowie einen weiteren Boolean-Wert, der angibt, ob der Pfad auf einen Ordner verweist.

## **Excel-API: Object Exists**

### Web-API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ ist der vollständige Pfad zur Datei oder zum Ordner im Speicher.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ    | Ort     | Erforderlich | Beschreibung                                                                 |
| ----------------- | ------ | ------- | ------------ | ---------------------------------------------------------------------------- |
| `path`            | string | Pfad    | Ja           | Vollständiger Pfad zur Datei oder zum Ordner.                               |
| `storageName`     | string | Abfrage | Nein         | Name des Speichers; standardmäßig wird der primäre Speicher verwendet, wenn ausgelassen. |
| `versionId`       | string | Abfrage | Nein         | Spezifische Versions-ID der Datei (falls Versionierung aktiviert ist).     |

**HTTP-Statuscodes**

| HTTP-Code | HTTP-Status            | Beschreibung                                                          |
| --------- | ---------------------- | --------------------------------------------------------------------- |
| 200       | OK                     | Die Web-API wurde erfolgreich aufgerufen; die Antwort enthält die Vorgangsdetails. |
| 400       | Bad Request            | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401       | Unauthorized           | Ungültiges oder fehlendes JWT-Token.                                 |
| 413       | Payload Too Large      | Die hochgeladene Datei überschreitet das Größenlimit.                |
| 500       | Internal Server Error  | Unerwarteter Serverfehler.                                            |

### **Antwort**

Ein erfolgreicher Aufruf gibt eine JSON-Antwort mit zwei Eigenschaften zurück:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true`, wenn die Datei oder der Ordner vorhanden ist; andernfalls `false`.
- **IsFolder** – `true`, wenn der Pfad auf einen Ordner verweist; `false` für eine Datei.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
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

Die Verwendung eines SDK ist der beste Weg, um die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden. Falls ein Gist nicht geladen wird, wird jeweils unten unterhalb des Tabs ein statisches Beispiel bereitgestellt.

---