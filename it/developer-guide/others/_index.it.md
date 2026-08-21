---
title: "Aspise.Cells Cloud Web API – Altre funzionalità: Controllo della salute, Ottenimento della chiave pubblica"
linktitle: "Altre funzionalità"
ArticleTitle: "Altre funzionalità: Controllo della salute, Ottenimento della chiave pubblica"
second_title: "Documento"
type: docs
url: /it/other-features/
keywords: "Aspose.Cells, API cloud, controllo della salute, chiave pubblica, token di accesso, Excel, REST"
description: "Esplora le altre funzionalità di Aspose.Cells Cloud: endpoint per il controllo della salute del servizio, recupero della chiave pubblica e generazione di token per garantire la sicurezza delle integrazioni con l'API Excel."
weight: 180
---

**Prerequisiti** – Per utilizzare le funzionalità elencate di seguito è necessario disporre di una sottoscrizione valida di Aspose Cloud e di una coppia **Client ID** / **Client Secret** valida per l'autenticazione.

Queste “Altre funzionalità” forniscono operazioni di supporto essenziali per l'API Aspose.Cells Cloud, come la verifica della disponibilità del servizio, il recupero delle chiavi crittografiche e l'ottenimento dei token di accesso. Di solito vengono chiamate prima di interagire con gli endpoint relativi ai fogli di calcolo.

- **[Controllo della salute del servizio Aspose.Cells Cloud](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Verifica che il servizio Aspose.Cells Cloud sia raggiungibile e operi correttamente. Una chiamata riuscita restituisce **HTTP 200** con il JSON `{ "status": "OK" }`. Utilizza questo endpoint all'inizio del tuo flusso di lavoro per evitare errori innecessari.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Ulteriori informazioni</a>

- **[Ottenimento dello stato di esecuzione di Aspose.Cells Cloud](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Recupera lo stato corrente di esecuzione del servizio. La risposta indica se l'API è pienamente operativa, in modalità di manutenzione o se sta riscontrando problemi.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Ulteriori informazioni</a>

- **[Ottenimento della chiave pubblica](https://docs.aspose.cloud/cells/get-public-key/)**  
  Ottieni la chiave pubblica RSA (formato PEM) utilizzata per verificare i token JWT emessi da Aspose.Cells Cloud. Questa chiave è necessaria quando convalidi i token lato server.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Ulteriori informazioni</a>

- **[Ottenimento del token di accesso con Client ID e Client Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  Genera un token di accesso OAuth 2.0 utilizzando il tipo di concessione **client_credentials**. Includi il tuo **Client ID** e **Client Secret** nel corpo della richiesta; la risposta contiene `access_token`, `token_type` e `expires_in`. Questo token deve essere fornito nell'intestazione `Authorization` per tutte le chiamate API successive.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Ulteriori informazioni</a>

---