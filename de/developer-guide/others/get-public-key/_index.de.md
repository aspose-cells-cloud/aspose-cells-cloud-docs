---
title: "Aspose.Cells Cloud API – Öffentlichen Schlüssel abrufen (v4.0) | REST-Dokumentation"
second_title: "Dokument"
ArticleTitle: "Öffentlichen Schlüssel abrufen"
linktitle: "Öffentlichen Schlüssel abrufen"
type: docs
url: /de/get-public-key/
keywords: "Aspose.Cells, Öffentlicher Schlüssel, RSA, API, Cloud"
description: "Rufen Sie den RSA-öffentlichen Schlüssel ab, der für die Verschlüsselung von Daten mit Aspose.Cells Cloud verwendet wird. Enthält Endpunkt, Parameter, Beispielanfrage/-antwort, Statuscodes und SDK-Nutzungsbeispiele."
weight: 100
---

Diese API ruft den öffentlichen Schlüssel aus einem asymmetrischen Verschlüsselungsalgorithmus ab.

**Kurze Zusammenfassung:** Verwenden Sie die Aspose.Cells API „Öffentlichen Schlüssel abrufen“, um den RSA-öffentlichen Schlüssel (2048 Bit) zu erhalten, der für die Verschlüsselung von Daten bei der Arbeit mit Excel-Dateien in der Cloud erforderlich ist. Der Endpunkt gibt den Schlüssel im JSON-Format zurück und ist mit OAuth 2.0 gesichert.

## **API zum Abrufen des öffentlichen Schlüssels**

**Voraussetzungen:**  
Bevor Sie diesen Endpunkt aufrufen, müssen Sie ein gültiges OAuth 2.0-Zugriffstoken mit dem Bereich `Cells.Read` besitzen.

### **Web-API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**Beispielanfrage (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername | Typ    | Speicherort | Beschreibung                                                                     |
| ------------- | ------ | ----------- | -------------------------------------------------------------------------------- |
| Authorization | string | Header      | Bearer-Token für OAuth2-Authentifizierung (erforderlich).                       |
| Accept        | string | Header      | Gewünschtes Antwortformat, z. B. `application/json` (optional, Standard ist JSON). |

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                      |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.  |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large     | Hochgeladene Datei überschreitet die Größeinschränkung.          |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## So verwenden Sie die API „Öffentlichen Schlüssel abrufen“ mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus Ihrem Webbrowser durchführen können.

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie das Abrufen des öffentlichen Schlüssels für Cells mit minimalem Codeaufwand umsetzen können.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Nachfolgend finden Sie konkrete Beispiele für die gängigsten Sprachen:

---