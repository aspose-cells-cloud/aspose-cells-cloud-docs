---
title: "Elaborazione in batch di file Excel: convertire, bloccare, proteggere, dividere e sbloccare"
second_title: "Documento"
linktype: "Elaborazione in batch di file Excel"
type: docs
url: /it/batch/
keywords: "Elaborazione in batch, Excel, conversione, blocco, protezione, divisione, sblocco, Aspose.Cells Cloud API, riferimento API, operazioni in batch"
description: "L'API Aspose.Cells Cloud consente l'elaborazione in batch di più file Excel per la conversione, il blocco, la protezione, la divisione e lo sblocco. Include specifiche API dettagliate e supporto SDK per Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift."
weight: 35
ArticleTitle: "Elaborazione in batch di file Excel – Convertire, Bloccare, Proteggere, Dividere, Sbloccare con Aspose.Cells Cloud API"
---

L'API Aspose.Cells Cloud fornisce endpoint per l'elaborazione in batch che consentono di eseguire operazioni comuni su più file Excel in una singola richiesta. Di seguito è riportata una rapida panoramica delle operazioni in batch disponibili, accompagnata da concise specifiche API per ciascuna.

- **["Convertire file Excel in batch"](https://docs.aspose.cloud/cells/batch/convert "Convertire file Excel in batch")**  
  *Convertire più file Excel in un formato di output scelto in una singola richiesta.*  

  **Dettagli API**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **Parametri**  

  | Nome          | Tipo     | Descrizione                                    |
  |---------------|----------|------------------------------------------------|
  | files         | file[]   | Uno o più file Excel da convertire.            |
  | outputFormat  | string   | Formato di output desiderato (es. pdf, csv, html). |
  | storage       | string   | (Opzionale) Nome dello storage cloud.          |

  **Risposte**  

  | Codice | Descrizione                                 |
  |--------|---------------------------------------------|
  | 200    | Conversione riuscita; restituisce i file.   |
  | 400    | Parametri forniti non validi.               |
  | 401    | Non autorizzato – token mancante o non valido. |
  | 500    | Errore interno del server.                  |

- **["Bloccare file Excel in batch"](https://docs.aspose.cloud/cells/batch/lock "Bloccare file Excel in batch")**  
  *Applicare contemporaneamente un blocco con password a più file Excel.*  

  **Dettagli API**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametri**  

  | Nome     | Tipo   | Descrizione                              |
  |----------|--------|------------------------------------------|
  | files    | array  | Elenco di identificatori di file o URL.  |
  | password | string | Password con cui bloccare i workbook.    |
  | storage  | string | (Opzionale) Nome dello storage cloud.     |

  **Risposte**  

  | Codice | Descrizione                                 |
  |--------|---------------------------------------------|
  | 200    | File bloccati con successo.                 |
  | 400    | Parametri mancanti o non validi.            |
  | 401    | Accesso non autorizzato.                    |
  | 500    | Errore del server.                          |

- **["Proteggere file Excel in batch"](https://docs.aspose.cloud/cells/batch/protect "Proteggere file Excel in batch")**  
  *Aggiungere impostazioni di protezione (es. sola lettura, struttura) a più workbook.*  

  **Dettagli API**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametri**  

  | Nome          | Tipo   | Descrizione                                          |
  |---------------|--------|------------------------------------------------------|
  | files         | array  | Elenco di identificatori di file o URL.              |
  | protection    | object | Opzioni di protezione (es. readOnly, structure).    |
  | storage       | string | (Opzionale) Nome dello storage cloud.                |

  **Risposte**  

  | Codice | Descrizione                                 |
  |--------|---------------------------------------------|
  | 200    | Protezione applicata con successo.          |
  | 400    | Dati della richiesta non validi.            |
  | 401    | Autenticazione fallita.                     |
  | 500    | Errore imprevisto del server.               |

- **["Dividere in batch"](https://docs.aspose.cloud/cells/batch/split "Dividere in batch")**  
  * suddividere workbook Excel di grandi dimensioni in file più piccoli in base ai fogli di lavoro o a intervalli di righe.*  

  **Dettagli API**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametri**  

  | Nome        | Tipo   | Descrizione                                      |
  |-------------|--------|--------------------------------------------------|
  | files       | array  | File da dividere.                                |
  | splitBy     | string | Criterio: "worksheet" o "rowRange".              |
  | criteria    | object | Dettagli per il metodo di suddivisione scelto.  |
  | storage     | string | (Opzionale) Nome dello storage cloud.            |

  **Risposte**  

  | Codice | Descrizione                                 |
  |--------|---------------------------------------------|
  | 200    | Operazione di suddivisione completata; restituisce le parti. |
  | 400    | Parametri di suddivisione errati.            |
  | 401    | Richiesta non autorizzata.                   |
  | 500    | Errore durante l'elaborazione.               |

- **["Sbloccare in batch"](https://docs.aspose.cloud/cells/batch/unlock "Sbloccare in batch")**  
  *Rimuovere la protezione con password da più file Excel in una singola chiamata.*  

  **Dettagli API**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametri**  

  | Nome     | Tipo   | Descrizione                              |
  |----------|--------|------------------------------------------|
  | files    | array  | Elenco di identificatori di file bloccati o URL. |
  | password | string | Password corrente dei file.              |
  | storage  | string | (Opzionale) Nome dello storage cloud.     |

  **Risposte**  

  | Codice | Descrizione                                 |
  |--------|---------------------------------------------|
  | 200    | File sbloccati con successo.                |
  | 400    | Password errata o file mancanti.            |
  | 401    | Accesso non autorizzato.                    |
  | 500    |Errore lato server.                           |
---