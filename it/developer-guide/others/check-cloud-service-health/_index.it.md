---
title: "Aspose.Cells Cloud – Verifica la salute del servizio (API)"
second_title: "Documento"
ArticleTitle: "Verifica della salute di Aspose.Cells Cloud"
linktitle: "Verifica la salute del servizio cloud"
type: docs
url: /it/check-cloud-service-health/
keywords: "Aspose.Cells Cloud, controllo della salute dell'API, stato REST, monitoraggio del servizio cloud"
description: "Monitora in tempo reale la salute di Aspose.Cells Cloud. Scopri l'endpoint GET /v4.0/cells/status/check, i parametri, il formato della risposta e gli esempi con SDK."
weight: 100
---

Verifica lo stato di salute dei servizi Aspose.Cells Cloud.

**Prerequisiti**  
Per chiamare questo endpoint è necessario disporre di un token di accesso valido di Aspose Cloud. Ottieni il token registrando un'applicazione nella dashboard di Aspose Cloud e utilizzando client-id e client-secret per richiedere un token Bearer tramite l'endpoint OAuth2 per i token. Includi il token nell'intestazione `Authorization`, come mostrato di seguito.

## **Verifica la salute del servizio cloud**

### **API Web**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Parametro     | Tipo   | Obbligatorio | Descrizione                                                         |
| ------------- | ------ | ------------ | ------------------------------------------------------------------- |
| Authorization | header | Sì           | Token Bearer per l'autenticazione (`Authorization: Bearer <token>`). |
| detail        | query  | No           | Impostare su `true` per includere informazioni dettagliate sui componenti. |
| Accept        | header | No           | Formato della risposta desiderato; il valore predefinito è `application/json`. |

### **Risposta**

Il servizio restituisce un payload JSON quando la richiesta ha esito positivo.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Operativo",
    "storage": "Operativo",
    "database": "Operativo"
  }
}
```

**Codici di stato HTTP**

| Codice | significato           | Descrizione                                             |
| ------ | --------------------- | ------------------------------------------------------- |
| 200    | OK                    | Il servizio è sano; vedere l'esempio JSON sopra.       |
| 401    | Non autorizzato       | Token di autenticazione non valido o mancante.          |
| 503    | Servizio non disponibile | Il servizio attualmente non è sano o in manutenzione. |
| 4xx    | Errore client         | Parametri della richiesta errati o richiesta malformata. |
| 5xx    | Errore server         | Errore imprevisto sul server; riprovare più tardi.      |

## Come utilizzare l'API di stato di Aspose.Cells Cloud con gli SDK

### Specifica OpenAPI

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo più rapido per accelerare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendo di implementare un controllo della salute per Cells con un numero minimo di righe di codice.  
Consultare il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per l'elenco completo degli SDK di Aspose.Cells Cloud.

Di seguito sono riportati frammenti di esempio che mostrano come chiamare l'endpoint di controllo della salute con gli SDK più diffusi.

---