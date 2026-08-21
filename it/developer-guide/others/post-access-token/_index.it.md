---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "Documento"
ArticleTitle: "Ottieni il token di accesso con Client ID e Secret"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, Cloud, Token di accesso, OAuth2, API, Autenticazione, REST, Excel, Office Cloud"
description: "Ottieni un token di accesso OAuth2 per Aspose.Cells Cloud chiamando l'endpoint POST /cells/connect/token con il tuo Client ID e secret."
weight: 100
---

Recupera un token di accesso utilizzando l'API Cells Cloud Get Token con un Client ID e un secret.

## API Post Access Token

Prima di chiamare l'endpoint, assicurati di avere:

* Un account Aspose Cloud registrato.  
* Un **Client ID** e un **Client Secret** generati nel portale Aspose Cloud.  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione                     | Descrizione                                          |
| -------------- | ------ | ---------------------------- | ---------------------------------------------------- |
| grant_type     | string | body (form‑url‑encoded)      | Valore fisso `client_credentials` richiesto per OAuth. |
| client_id      | string | body (form‑url‑encoded)      | L'identificativo client rilasciato a te.             |
| client_secret  | string | body (form‑url‑encoded)      | Il secret associato al Client ID.                    |

**Esempio di richiesta (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=IL_TUO_CLIENT_ID&client_secret=IL_TUO_CLIENT_SECRET"
```

### Risposta

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

**Esempio di gestione dell’errore**

```json
{
  "error": "invalid_client",
  "error_description": "Autenticazione client non riuscita."
}
```

## Come utilizzare l’API Get public key con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) definiscono un'interfaccia di programmazione accessibile pubblicamente, consentendoti di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per iniziare. L'SDK nasconde i dettagli HTTP sottostanti, consentendoti di ottenere un token di accesso per Cells con un numero minimo di righe di codice.

Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:  
---