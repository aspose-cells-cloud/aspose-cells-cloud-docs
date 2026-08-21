---
title: "Funzionalità principali di Aspose.Cells Cloud Docker: conversione di fogli di calcolo, unione, suddivisione, protezione, elaborazione dati e altro."
second_title: "Documento"
ArticleTitle: "Funzionalità principali di Aspose.Cells Cloud Docker"
linktype: "Features"
type: docs
url: /docker-container-features/
description: "Esegui l'API Aspose.Cells Cloud in locale grazie al contenitore Docker di Aspose.Cells Cloud — un servizio basato su Docker e contenurizzato che fornisce l'elaborazione completa dei fogli di calcolo, privacy e funzionalità offline, senza utilizzare il cloud pubblico di Aspose."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - Conversione foglio di calcolo
  - Elaborazione Excel
  - Esportazione PDF
  - Gestione CSV
  - API REST
  - Servizio contenurizzato
  - Cloud privato
  - Elaborazione offline
---

## Cos'è il contenitore Docker di Aspose.Cells Cloud?

Il contenitore Docker di Aspose.Cells Cloud è un servizio contenurizzato fornito da Aspose, basato su Docker, che consente di distribuire le funzionalità dell'API Aspose.Cells Cloud in ambienti locali o in cloud privati, senza dover fare affidamento sui servizi cloud pubblici di Aspose.

## Perché utilizzare il contenitore Docker di Aspose.Cells Cloud?

Il contenitore Docker di Aspose.Cells Cloud è un servizio potente per l'elaborazione di fogli di calcolo, che supporta:

### Funzionalità principali

- Lettura e scrittura di file Excel (XLS, XLSX, CSV, ODS, ecc.)
- Calcolo di formule, grafici, formattazione condizionale, tabelle pivot, ecc.
- Conversione di formati (ad esempio, da Excel a PDF, HTML, immagini, ecc.)
- Operazioni sulle celle, impostazioni di stile, gestione dei fogli di lavoro, ecc.

Il contenitore Docker di Aspose.Cells Cloud incapsula queste funzionalità come API RESTful e le raggruppa in un'immagine Docker, consentendoti di eseguirla sulla tua infrastruttura.

### Vantaggi principali

| Benefici                         | Descrizione                                                                 |
| -------------------------------- | --------------------------------------------------------------------------- |
| Privacy e sicurezza dei dati     | L'elaborazione dei file avviene interamente all'interno della tua rete privata; non è necessario caricare i dati su un cloud di terze parti. |
| Disponibilità offline            | Non richiede il cloud pubblico di Aspose; ideale per reti interne o ambienti isolati. |
| Scalabilità                      | Facilmente scalabile tramite Docker/Kubernetes.                             |
| API unificata                    | Completamente compatibile con l'API pubblica di Aspose.Cells Cloud; non sono necessarie modifiche al codice. |
| Controllo della licenza          | Supporta due tipi di autorizzazione; scegli quella più adatta al tuo caso d'uso. |

## Come utilizzare il contenitore Docker di Aspose.Cells Cloud

Fai riferimento alla guida utente — [Come utilizzare il contenitore Docker di Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**Prerequisiti**

- Docker Engine 20.10 o versione successiva installata sulla macchina host.  
- Almeno 2 GB di RAM e 2 core CPU assegnati al contenitore per carichi di lavoro tipici.  
- Un file di licenza Aspose.Cells Cloud valido (o un token di accesso) collocato in una directory che verrà montata all'interno del contenitore.

**Avvio rapido**

1. Estrai l'immagine Docker: `docker pull aspose/cells-cloud`.  
2. Esegui il contenitore, montando le directory per la licenza e per i dati, ad esempio:  
   ```bash
   docker run -d -p 8080:80 \
     -v /percorso/alla/license:/app/license \
     -v /percorso/ai/dati:/app/data \
     aspose/cells-cloud
   ```  
3. Accedi all'API REST all'indirizzo `http://localhost:8080/v3.0/`. Per ulteriori informazioni sull'utilizzo dell'API, consulta il [riferimento all'API Aspose.Cells Cloud](https://docs.aspose.cloud/cells/api-reference/).

## Documentazione di riferimento

- [Come configurare l'archiviazione del contenitore Docker di Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)