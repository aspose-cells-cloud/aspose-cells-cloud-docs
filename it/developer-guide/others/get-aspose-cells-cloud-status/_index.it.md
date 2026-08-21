---
---
title: "Aspose.Cells Cloud Web API - Ottieni lo stato di Aspose Cells Cloud"
second_title: "Documento"
ArticleTitle: "Ottieni lo stato di Aspose Cells Cloud"
linktitle: "Ottieni lo stato di Aspose Cells Cloud"
type: docs
url: /it/get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Cloud API, Controllo integrità, Excel, REST"
description: "Monitora in tempo reale lo stato di integrità del servizio Aspose.Cells Cloud."
weight: 100
---

Ottieni in tempo reale lo stato di integrità del servizio Aspose.Cells Cloud.

**Prerequisiti:** Per chiamare questa API è necessario ottenere un token di accesso Bearer utilizzando le credenziali del client Aspose Cloud. Includi il token nell'intestazione `Authorization` come `Bearer {access_token}`.

## **Ottieni lo stato di Aspose.Cells Cloud**

### **API Web**

L'endpoint utilizza il metodo HTTP **GET** e non richiede un corpo della richiesta.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                      |
| -------------- | ------ | ------------------------------------ | ------------------------------------------------ |
| Authorization  | String | Intestazione                         | Token Bearer per l'autenticazione (obbligatorio). |
| format         | String | Query                                | Formato di risposta desiderato, ad esempio `json`. |

### **Risposta**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Schema della risposta**

| Campo     | Tipo              | Descrizione                                    |
| --------- | ----------------- | ---------------------------------------------- |
| status    | stringa           | Stato del servizio (`OK`, `Degraded`, ecc.).  |
| service   | stringa           | Nome del servizio.                             |
| timestamp | stringa (ISO‑8601) | Ora del controllo dello stato.                 |

L'API restituisce un payload JSON standard che include la **status** corrente dell'integrità del servizio Aspose.Cells Cloud.

**Codici di stato HTTP**

- **200 OK** – Il servizio è integro e la risposta contiene le informazioni sullo stato.
- **401 Unauthorized** – Token di autenticazione mancante o non valido.
- **503 Service Unavailable** – Il servizio è attualmente disattivato per manutenzione o presenta problemi.

## Come utilizzare l'API "Ottieni lo stato di Aspose.Cells Cloud" con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) definiscono un'interfaccia di programmazione accessibile pubblicamente che consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK semplifica l'integrazione e riduce il codice boilerplate. L'SDK gestisce i dettagli sottostanti, consentendo di recuperare facilmente lo stato di esecuzione di Aspose.Cells Cloud con il minimo sforzo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.