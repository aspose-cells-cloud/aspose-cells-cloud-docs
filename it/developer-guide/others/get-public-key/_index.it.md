---
---
title: "Aspose.Cells Cloud API – Ottieni la Chiave Pubblica (v4.0) | Documentazione REST"
second_title: "Documento"
ArticleTitle: "Ottieni la Chiave Pubblica"
linktitle: "Ottieni la Chiave Pubblica"
type: docs
url: /it/get-public-key/
keywords: "Aspose.Cells, Chiave Pubblica, RSA, API, Cloud"
description: "Recupera la chiave pubblica RSA utilizzata per crittografare i dati con Aspose.Cells Cloud. Include endpoint, parametri, esempi di richiesta/risposta, codici di stato e esempi di utilizzo degli SDK."
weight: 100
---

Questa API recupera la chiave pubblica da un algoritmo di crittografia asimmetrica.

**Sommario Breve:** Utilizza l'API Aspose.Cells *Ottieni la Chiave Pubblica* per ottenere la chiave pubblica RSA (2048 bit) necessaria per crittografare i dati durante il lavoro con file Excel nel cloud. L'endpoint restituisce la chiave in formato JSON ed è protetto tramite OAuth 2.0.

## **API Ottieni la Chiave Pubblica**

**Prerequisiti:**  
Ottenere un token di accesso OAuth 2.0 valido che includa l'ambito `Cells.Read` prima di chiamare questo endpoint.

### **API Web**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**Esempio di Richiesta (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della Richiesta:**

| Nome Parametro | Tipo   | Posizione | Descrizione                                                                 |
| -------------- | ------ | --------- | --------------------------------------------------------------------------- |
| Authorization  | string | Header    | Token Bearer per l'autenticazione OAuth2 (obbligatorio).                   |
| Accept         | string | Header    | Formato di risposta desiderato, ad esempio `application/json` (opzionale, il valore predefinito è JSON). |

### **Risposta**

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

**Codici di Stato HTTP**

| Codice | Significato            | Descrizione                                                    |
| ------ | ---------------------- | -------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Non Validata | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non Autorizzato        | Token JWT non valido o mancante.                               |
| 413    | Payload Troppo Grande  | Il file caricato supera il limite di dimensione.              |
| 500    | Errore Interno del Server | Errore imprevisto del server.                                |

## Come utilizzare l'API *Ottieni la Chiave Pubblica* con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) definiscono un'interfaccia di programmazione accessibile pubblicamente, consentendo di effettuare interazioni REST direttamente dal tuo browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo migliore per velocizzare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendoti di implementare semplicemente l'ottieni chiave pubblica per le celle con un codice minimo.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Di seguito sono riportati esempi concreti per i linguaggi più comuni:

---