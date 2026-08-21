---
title: "Opzioni di salvataggio"
second_title: "Documento"
linktitle: "Opzioni di salvataggio"
type: docs
url: /it/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Workbook, REST API, Formati file, PDF, CSV, JSON, Compressione HTTP, Cache grafici, Nomi definiti, Creazione directory"
description: "Descrive le proprietà SaveOptions dell'API REST di Aspose.Cells Cloud, consentendo agli sviluppatori di configurare il comportamento di salvataggio del workbook tra diversi formati file e opzioni come la compressione HTTP, l'aggiornamento della cache dei grafici e la creazione automatica delle directory."
weight: 79
ArticleTitle: "Opzioni di salvataggio – Documentazione dell'API REST di Aspose.Cells Cloud"
---

# Proprietà SaveOptions

Le opzioni SaveOptions consentono di controllare il modo in cui un workbook viene salvato quando si utilizza l'API REST di Aspose.Cells Cloud. Configurando queste opzioni è possibile abilitare la compressione HTTP, specificare il formato di output, gestire l'archiviazione temporanea e controllare comportamenti aggiuntivi come l'aggiornamento della cache dei grafici e la creazione automatica delle directory.

**Prerequisiti**  
- Una sessione autenticata di Aspose.Cells Cloud (OAuth 2.0 o JWT).  
- Il workbook di destinazione deve essere caricato o creato tramite l'API prima del salvataggio.

| Nome                      | Tipo       | Descrizione                                                                                                        | Note       |
| ------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------ | ---------- |
| **EnableHTTPCompression** | **bool?**  | Abilita la compressione HTTP per la risposta.                                                                      | [opzionale] |
| **SaveFormat**            | **string** | Specifica il formato file di destinazione per il salvataggio del workbook.                                         | [opzionale] |
| **ClearData**             | **bool?**  | Rende il workbook vuoto dopo il salvataggio del file.                                                              | [opzionale] |
| **CachedFileFolder**      | **string** | La directory di file memorizzati temporaneamente utilizzata per archiviare dati di grandi dimensioni.              | [opzionale] |
| **ValidateMergedAreas**   | **bool?**  | Indica se convalidare le aree unite prima del salvataggio del file. Il valore predefinito è false.                 | [opzionale] |
| **RefreshChartCache**     | **bool?**  | Aggiorna i dati della cache dei grafici prima del salvataggio.                                                     | [opzionale] |
| **CreateDirectory**       | **bool?**  | Se true e la directory non esiste già, verrà creata automaticamente prima del salvataggio del file.                | [opzionale] |
| **SortNames**             | **bool?**  | Ordina alfabeticamente i nomi definiti durante il salvataggio.                                                     | [opzionale] |

**Richiesta**  
- **Metodo:** `POST` (o `PUT` a seconda dell'operazione)  
- **Endpoint:** `/cells/workbook/save`  
- **Intestazioni:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **Corpo:** Rappresentazione JSON del modello `SaveOptions` (tabella sopra) combinata con i dati o il riferimento al workbook.

**Esempio di risposta**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "Workbook salvato correttamente."
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                     |
|--------|-----------------------------|-----------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                               |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.              |
| 500    | Errore interno del server   | Errore imprevisto del server.                                  |

**Note / Osservazioni**  
- Quando **CreateDirectory** è impostato su `true`, l'API crea automaticamente la cartella di destinazione se non esiste già.  
- Abilitare **EnableHTTPCompression** può ridurre la dimensione del payload per workbook di grandi dimensioni, ma il client deve supportare la decodifica gzip/deflate.  
- **RefreshChartCache** deve essere utilizzato quando i grafici si basano su dati dinamici che potrebbero essere cambiati dal momento della generazione del workbook.