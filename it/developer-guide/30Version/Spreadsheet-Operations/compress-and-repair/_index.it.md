---
title: "Comprimi e Ripara File Excel"
second_title: "Documento"
type: docs
url: /compress-and-repair-excel-files/
linktitle: "Comprimi e Ripara"
keywords: "Aspose.Cells, compressione Excel, riparazione Excel, API cloud, ridurre dimensione file Excel, ripristinare cartella di lavoro danneggiata, comprimere file Excel, riparare cartella di lavoro Excel"
description: "Scopri come comprimere grandi cartelle di lavoro Excel e riparare file danneggiati utilizzando l'API Aspose.Cells Cloud. Esempi passo-passo, linguaggi supportati e best practice."
weight: 100
ArticleTitle: "Comprimi e Ripara File Excel – API Aspose.Cells Cloud"
---

Comprimere una cartella di lavoro Excel riduce la sua dimensione rimuovendo stili, immagini e stringhe condivise non utilizzati, mentre la riparazione ripristina l'integrità delle cartelle di lavoro danneggiate. L'API Aspose.Cells Cloud fornisce endpoint dedicati per entrambe le operazioni.

- **[Comprimi i dati in un file Excel](https://docs.aspose.cloud/cells/compress-excel-files/).**
- **[Ripara file Excel](https://docs.aspose.cloud/cells/repair-excel-files/).**

**API Comprimi Cartella di Lavoro**  
L'operazione **Comprimi** utilizza una semplice richiesta POST. Di seguito è riportata una specifica completa della richiesta/risposta:

| Metodo | Endpoint | Parametri Richiesti | Corpo della Richiesta | Risposta di Esempio | Codici di Stato Tipici |
|--------|----------|---------------------|-----------------------|-------------------|------------------------|
| POST   | `/cells/compress` | `file` (binario) – la cartella di lavoro da comprimere; `outPath` opzionale (stringa) – percorso di destinazione | *Nessuno* (il file viene inviato come multipart/form‑data) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**API Ripara Cartella di Lavoro**  
Anche l'operazione **Ripara** utilizza una richiesta POST. La sua specifica è la seguente:

| Metodo | Endpoint | Parametri Richiesti | Corpo della Richiesta | Risposta di Esempio | Codici di Stato Tipici |
|--------|----------|---------------------|-----------------------|-------------------|------------------------|
| POST   | `/cells/repair` | `file` (binario) – la cartella di lavoro danneggiata; `outPath` opzionale (stringa) – posizione in cui salvare il file riparato | *Nessuno* (il file viene inviato come multipart/form‑data) | `{ "isRepaired": true, "message": "Cartella di lavoro riparata con successo." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

Queste tabelle forniscono agli sviluppatori i dettagli essenziali per chiamare direttamente le API senza dover cercare altrove.

**Risorse Aggiuntive**  
- Consulta la guida completa **[Comprimi file Excel](/compress-excel-files/)** per opzioni avanzate, come la rimozione di righe e colonne non utilizzate.  
- Esamina la documentazione **[Ripara file Excel](/repair-excel-files/)** per suggerimenti sulla risoluzione dei problemi e spiegazioni dei codici di errore.  
- Esplora operazioni correlate come **[Ottieni Informazioni sul File](/file-info/)** e **[Operazioni su Fogli di Calcolo](/spreadsheet-operations/)** per una comprensione più ampia dell'API Aspose.Cells Cloud.