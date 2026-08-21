---
title: "Aspose.Cells Cloud – Prüfung des Service-Status (API)"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Statusprüfung"
linktitle: "Status des Cloud-Service prüfen"
type: docs
url: /check-cloud-service-health/
keywords: "Aspose.Cells Cloud, API-Statusprüfung, REST-Status, Cloud-Service-Monitoring"
description: "Überwachen Sie den Status von Aspose.Cells Cloud in Echtzeit. Erfahren Sie mehr über den GET /v4.0/cells/status/check-Endpunkt, Parameter, Antwortformat und SDK-Beispiele."
weight: 100
---

Prüfen Sie den Status der Aspose.Cells Cloud-Dienste.

**Voraussetzungen**  
Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges Aspose Cloud-Zugriffstoken. Holen Sie sich das Token, indem Sie eine Anwendung im Aspose Cloud Dashboard registrieren und mit client-id und client-secret über den OAuth2-Token-Endpunkt ein Bearer-Token anfordern. Geben Sie das Token im `Authorization`-Header wie unten gezeigt an.

## **Status des Cloud-Service prüfen**

### **Web-API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parameter     | Typ    | Erforderlich | Beschreibung                                                         |
| ------------- | ------ | ------------ | -------------------------------------------------------------------- |
| Authorization | Header | Ja           | Bearer-Token für die Authentifizierung (`Authorization: Bearer <token>`). |
| detail        | Query  | Nein         | Auf `true` setzen, um detaillierte Komponenteninformationen einzuschließen. |
| Accept        | Header | Nein         | Gewünschtes Antwortformat, Standard ist `application/json`.         |

### **Antwort**

Der Service gibt bei erfolgreicher Anforderung eine JSON-Payload zurück.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Betriebsbereit",
    "storage": "Betriebsbereit",
    "database": "Betriebsbereit"
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung            | Beschreibung                                               |
| ---- | -------------------- | ---------------------------------------------------------- |
| 200  | OK                   | Der Service ist funktionsfähig; siehe obenstehendes JSON-Beispiel. |
| 401  | Nicht autorisiert    | Ungültiges oder fehlendes Authentifizierungstoken.        |
| 503  | Service nicht verfügbar | Der Service ist derzeit nicht funktionsfähig oder wird gewartet. |
| 4xx  | Clientfehler         | Falsche Anforderungsparameter oder fehlerhafte Anforderung. |
| 5xx  | Serverfehler         | Unerwarteter Serverfehler; später erneut versuchen.       |

## Verwendung der Aspose.Cells Cloud Status-API mit SDKs

### OpenAPI-Spezifikation

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen direkte REST-Interaktionen aus einem Webbrowser heraus.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie eine Cloud-Statusprüfung für Cells mit minimalem Codeaufwand implementieren können.  
Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Im Folgenden finden Sie Beispielcodesnippets, die zeigen, wie der Status-Prüf-Endpunkt mit den gängigsten SDKs aufgerufen wird.

---