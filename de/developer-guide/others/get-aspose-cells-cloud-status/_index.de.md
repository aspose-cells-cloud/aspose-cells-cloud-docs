---
title: "Aspose.Cells Cloud Web-API – Abrufen des Aspose.Cells Cloud-Status"
second_title: "Dokument"
ArticleTitle: "Abrufen des Aspose.Cells Cloud-Status"
linktitle: "Abrufen des Aspose.Cells Cloud-Status"
type: docs
url: /de/get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Cloud-API, Gesundheitsprüfung, Excel, REST"
description: "Überwachen Sie den Gesundheitsstatus des Aspose.Cells Cloud-Diensts in Echtzeit."
weight: 100
---

Rufen Sie den Gesundheitsstatus des Aspose.Cells Cloud-Diensts in Echtzeit ab.

**Voraussetzungen:** Um diese API aufzurufen, müssen Sie ein Bearer-Zugriffstoken mithilfe Ihrer Aspose-Cloud-Client-Anmeldeinformationen erhalten. Fügen Sie das Token im `Authorization`-Header als `Bearer {access_token}` ein.

## **Abrufen des Aspose.Cells Cloud-Status**

### **Web-API**

Der Endpunkt verwendet die HTTP-Methode **GET** und erfordert keinen Anforderungstext.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                |
| ------------- | ----- | ---------------------------------- | ------------------------------------------- |
| Authorization | String | Header                             | Bearer-Token zur Authentifizierung (erforderlich). |
| format        | String | Abfrage                            | Gewünschtes Antwortformat, z. B. `json`.   |

### **Antwort**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Antwort-Schema**

| Feld       | Typ               | Beschreibung                                  |
| ---------- | ----------------- | --------------------------------------------- |
| status     | string            | Gesundheitszustand des Diensts (`OK`, `Degraded`, usw.). |
| service    | string            | Name des Diensts.                             |
| timestamp  | string (ISO‑8601) | Zeitpunkt der Statusprüfung.                  |

Die API gibt eine standardmäßige JSON-Payload zurück, die den aktuellen Gesundheitsstatus **status** des Aspose.Cells Cloud-Diensts enthält.

**HTTP-Statuscodes**

- **200 OK** – Der Dienst ist funktionsfähig, und die Antwort enthält die Statusinformationen.
- **401 Unauthorized** – Fehlendes oder ungültiges Authentifizierungstoken.
- **503 Service Unavailable** – Der Dienst ist derzeit zur Wartung oder aufgrund von Problemen nicht verfügbar.

## Verwendung der Get Aspose.Cells Cloud Status-API mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) definiert eine öffentlich zugängliche Programmierschnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung des SDKs vereinfacht die Integration und reduziert den Boilerplate-Code. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie den Laufstatus von Aspose.Cells Cloud mit minimalem Aufwand abrufen können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).