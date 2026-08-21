---
title: "Aspose.Cells Cloud Web-API – Post Access Token"
second_title: "Dokument"
ArticleTitle: "Zugriffstoken mit Client-ID und Geheimnis abrufen"
linktype: "docs"
url: /de/post-access-token/
keywords: "Aspose.Cells, Cloud, Zugriffstoken, OAuth2, API, Authentifizierung, REST, Excel, Office Cloud"
description: "Rufen Sie ein OAuth2-Zugriffstoken für Aspose.Cells Cloud ab, indem Sie den Endpoint POST /cells/connect/token mit Ihrer Client-ID und Ihrem Geheimnis aufrufen."
weight: 100
---

Rufen Sie ein Zugriffstoken mithilfe der Cells Cloud Get Token API mit einer Client-ID und einem Geheimnis ab.

## API „Post Access Token“

Bevor Sie den Endpoint aufrufen, stellen Sie sicher, dass Folgendes vorliegt:

* Ein registriertes Aspose Cloud-Konto.  
* Eine **Client-ID** und ein **Clientgeheimnis**, die im Aspose Cloud-Portal generiert wurden.  

### Web-API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Standort                     | Beschreibung                                         |
| --------------- | ------ | ---------------------------- | ---------------------------------------------------- |
| grant_type      | string | body (form‑url‑encoded)      | Erforderlicher fester Wert `client_credentials` für OAuth. |
| client_id       | string | body (form‑url‑encoded)      | Die Ihnen ausgestellte Client-Identifikationsnummer. |
| client_secret   | string | body (form‑url‑encoded)      | Das mit der Client-ID verknüpfte Geheimnis.         |

**Beispielanfrage (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=IHRE_CLIENT_ID&client_secret=IHRE_CLIENT_GEHEIMNIS"
```

### Antwort

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

**Beispiel für Fehlerbehandlung**

```json
{
  "error": "invalid_client",
  "error_description": "Client-Authentifizierung fehlgeschlagen."
}
```

## Verwendung der Get public key API mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) definiert eine öffentlich zugängliche Programmierschnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, loszulegen. Das SDK abstractiert die zugrundeliegenden HTTP-Details und ermöglicht es Ihnen, mit minimalem Code ein Zugriffstoken für Cells abzurufen.

Bitte überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
---