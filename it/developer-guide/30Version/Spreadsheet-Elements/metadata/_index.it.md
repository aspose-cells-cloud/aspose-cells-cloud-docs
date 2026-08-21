---
title: "Lavorare con i metadati e le proprietà di Excel"
second_title: "Documento"
linktitle: "Metadati e proprietà"
type: docs
url: /it/metadata/
aliases:
  - /document-properties/
  - /working-with-document-properties/
keywords: "Aspose.Cells Cloud, metadati Excel, API delle proprietà dei documenti, API REST, recupero metadati, aggiornamento delle proprietà di Excel, eliminazione dei metadati di Excel"
description: "Scopri come leggere, aggiungere, aggiornare ed eliminare i metadati dei file Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi in cURL e SDK per Java, .NET, Python, Node.js e altro ancora."
ArticleTitle: "Lavorare con i metadati e le proprietà dei documenti di Excel – Aspose.Cells Cloud"
weight: 100
---

I file Excel possono memorizzare una varietà di metadati utili per identificare, organizzare e gestire i documenti. Aspose.Cells Cloud fornisce una semplice API REST per leggere, aggiungere, aggiornare ed eliminare tali metadati, consentendo agli sviluppatori di integrare la gestione delle proprietà dei documenti nelle proprie applicazioni. Questa guida illustra le due principali categorie di proprietà—standard e personalizzate—spiega come lavorarvi e fornisce link diretti alle rispettive API endpoint. Troverai inoltre una concisa tabella di riferimento API con i dettagli delle richieste per accelerare l'implementazione.

**Ultimo aggiornamento:** 8 luglio 2026  

**Tipi di proprietà dei documenti**

Prima di imparare a utilizzare le API di Aspose.Cells Cloud per visualizzare, modificare ed eliminare le proprietà dei documenti (metadati) in Excel, chiariamo i tipi di proprietà che un documento Excel può contenere.

- **Proprietà standard** sono comuni a Excel. Contengono informazioni di base come Titolo, Oggetto, Autore, Categoria, ecc. È possibile assegnare valori di testo personalizzati a queste proprietà per facilitarne la individuazione.

- **Proprietà personalizzate** sono definite dall'utente. Consentono di aggiungere metadati aggiuntivi al proprio documento Excel.

**Come lavorare con le proprietà dei documenti in un file Excel**

- [Come ottenere una particolare proprietà del documento utilizzando lo storage](/cells/document-properties/get/)
- [Come ottenere le proprietà del documento senza utilizzare lo storage](/cells/metadata/get/)
- [Come ottenere tutte le proprietà del documento utilizzando lo storage](/cells/document-properties/get-all/)
- [Come aggiornare una particolare proprietà del documento utilizzando lo storage](/cells/document-properties/update/)
- [Come aggiornare una particolare proprietà del documento senza utilizzare lo storage](/cells/metadata/update/)
- [Come eliminare una particolare proprietà del documento utilizzando lo storage](/cells/document-properties/delete/)
- [Come eliminare le proprietà del documento senza utilizzare lo storage](/cells/metadata/delete/)
- [Come eliminare tutte le proprietà del documento utilizzando lo storage](/cells/document-properties/clear/)

**Riferimento API (senza storage)**  

| Metodo | Endpoint | Descrizione |
|--------|----------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | Recupera tutte le proprietà del documento del workbook memorizzato nel cloud. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Recupera il valore di una proprietà specifica (standard o personalizzata) identificata da `propertyName`. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Aggiorna il valore di una proprietà esistente. Il corpo della richiesta contiene il nuovo valore in formato JSON. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Elimina una proprietà specifica dal workbook. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | Rimuove tutte le proprietà standard e personalizzate dal workbook. |

*Le richieste richiedono un token di accesso OAuth 2.0 e possono includere parametri di query opzionali come `storage` e `folder` quando viene utilizzato uno storage specifico.*