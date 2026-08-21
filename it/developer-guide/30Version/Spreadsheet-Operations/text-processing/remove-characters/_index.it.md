---
title: "Rimuovi caratteri da Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "Documento"
linktitle: "Rimuovi caratteri"
type: docs
url: /it/excel-remove-characters/
keywords: "rimuovi caratteri, Aspose.Cells, API Excel, elaborazione testo, cloud"
description: "Scopri come rimuovere caratteri, set di caratteri o sottostringhe dai fogli di calcolo Excel utilizzando l'API Aspose.Cells Cloud. Include schema della richiesta, esempio cURL, codice SDK e gestione degli errori."
weight: 100
ArticleTitle: "Rimuovi caratteri da Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)"
---

## Rimuovi caratteri da Excel tramite API Web

Un insieme completo di strumenti per pulire il contenuto di testo all'interno delle celle selezionate. L'API rimuove caratteri specifici, set di caratteri predefiniti o sottostringhe, garantendo che il testo nei fogli di calcolo sia standardizzato e privo di simboli indesiderati.

**Prerequisiti**

- Un account Aspose Cloud attivo.  
- Un token di accesso JWT valido ottenuto come descritto nella guida all'autenticazione.  
- Il file Excel deve essere caricato nello storage prima di chiamare questo endpoint.  
- I formati di file supportati includono `.xlsx`, `.xls`, `.xlsm` e altri tipi Excel comuni.

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Descrizione della funzione

- **Rimuovi caratteri personalizzati** – Specifica i caratteri che desideri eliminare. Inserisci ciascun carattere nel campo _Rimuovi caratteri personalizzati_; l'API eliminerà ogni occorrenza di tali caratteri nelle celle selezionate.  
- **Rimuovi set di caratteri** – Scegli dai set predefiniti:  
  - **Caratteri non stampabili** – Elimina i ritorni a capo e i primi 32 caratteri ASCII non stampabili (0‑31) oltre ai codici aggiuntivi (127, 129, 141, 143, 144, 157).  
  - **Caratteri di testo** – Rimuove tutte le lettere.  
  - **Caratteri numerici** – Elimina tutte le cifre.  
  - **Simboli** – Rimuove simboli matematici, geometrici, tecnici, valutari e simboli simili a lettere come “?”, “1” e “™”.  
  - **Segni di punteggiatura** – Elimina tutti i segni di punteggiatura.  
- **Rimuovi una sottostringa** – Elimina qualsiasi sottostringa specificata (ad esempio, una parola) dalle celle selezionate.

### Parametri della richiesta

| Nome del parametro      | Tipo  | Posizione | Descrizione                                                                    |
| ----------------------- | ----- | -------- | ------------------------------------------------------------------------------ |
| removeCharactersOptions | Classe | Corpo    | Opzioni che definiscono quali caratteri, set di caratteri o sottostringhe rimuovere. |

**Schema di `removeCharactersOptions`**

| Proprietà        | Tipo    | Obbligatoria | Descrizione                                                                                                    |
| ---------------- | ------- | ------------ | -------------------------------------------------------------------------------------------------------------- |
| Range            | string  | Sì           | Notazione A‑1 o nome di intervallo che identifica le celle da elaborare (ad esempio, `"A1:C10"`).             |
| CustomCharacters | string  | No           | Stringa contenente ciascun carattere personalizzato da eliminare (ad esempio, `"@#$"`).                        |
| CharacterSet     | string  | No           | Valore di enum che specifica un set predefinito (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring        | string  | No           | La sottostringa esatta da rimuovere (ad esempio, `"USD"`).                                                     |
| IgnoreCase       | boolean | No           | Se `true`, la rimozione dei caratteri avviene senza distinzione tra maiuscole e minuscole.                      |

**Esempio di corpo della richiesta JSON**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**Esempio di richiesta cURL**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nome file unito]",
    "Filesize" : [dimensione file],
    "FileContent" : "[Base64String]"
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

## Come utilizzare l'API PostRemoveCharacters con gli SDK

### Specifica dell'API PostRemoveCharacters

La <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">specifica OpenAPI completa dell'endpoint PostRemoveCharacters</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli a basso livello e consente di concentrarsi sulle attività del progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:
---