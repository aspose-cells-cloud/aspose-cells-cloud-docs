---
title: Aspose.Cells Cloud Web API - Post Access Toke
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: Post Access Toke
type: docs
url: /it/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: Recupera un token di accesso utilizzando il token di accesso cloud Cells API, che funge da servizio proxy inoltrando le richieste degli utenti al server di autenticazione cloud Aspose e restituisce il token di accesso risultante al client in modo sicuro
weight: 100
kwords: Excel, Office Cloud, REST API, Autenticazione, Gestione token, Integrazione middleware, Sicuro API, Aspose Cloud
---
Recupera un token di accesso utilizzando il Cloud Get Token Cells API con ID client e segreto.

## **Token di accesso postale API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| ID cliente| corda| domanda| ID cliente|
| Segreto del cliente| corda| domanda| Segreto del cliente|

### **Risposta**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## Come utilizzare la chiave pubblica Get API con gli SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) definisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice il token di accesso per le celle con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDKs.nt. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
