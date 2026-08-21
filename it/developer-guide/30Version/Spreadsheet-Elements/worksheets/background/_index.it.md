---
title: "Aggiungi o Rimuovi Immagine di Sfondo del Foglio di Lavoro – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Sfondo"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud, sfondo del foglio di lavoro, API Excel, aggiungi immagine di sfondo, rimuovi sfondo del foglio di lavoro, esempi SDK"
description: "Scopri come aggiungere o rimuovere un'immagine di sfondo su un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud. Include la sintassi della richiesta, esempi SDK per Java, .NET, Python, PHP e gestione degli errori."
weight: 20
ArticleTitle: "Aggiungi o Rimuovi Immagine di Sfondo del Foglio di Lavoro con Aspose.Cells Cloud API"
---

## Lavorare con lo sfondo di un foglio di lavoro Excel

**Panoramica:** Uno sfondo del foglio di lavoro è un’immagine che appare dietro le celle di un foglio di lavoro, utile per il branding o per indizi visivi. L'API Aspose.Cells Cloud consente di aggiungere o rimuovere programmaticamente questa immagine di sfondo.

**Prerequisiti:**  
- Token di accesso valido Aspose.Cells Cloud (OAuth 2.0).  
- Un libro Excel archiviato nel cloud.  
- Un file immagine (PNG, JPEG, BMP) per lo sfondo.

- **Aggiungi sfondo** – Imposta un’immagine di sfondo su un foglio di lavoro. Consulta la guida dettagliata [Come impostare lo sfondo su un foglio di lavoro Excel](/cells/worksheets/background/add/).  
- **Rimuovi sfondo** – Rimuovi un’immagine di sfondo esistente da un foglio di lavoro. Consulta la guida dettagliata [Come rimuovere lo sfondo su un foglio di lavoro Excel](/cells/worksheets/background/delete/).

L'utilizzo di uno sfondo del foglio di lavoro può migliorare il branding, evidenziare sezioni importanti o fornire indizi visivi agli utenti finali. L'API Aspose.Cells Cloud rende semplice impostare o cancellare direttamente questa immagine di sfondo dalla tua applicazione.

### Riferimento API

| Operazione | Metodo HTTP | Endpoint | Parametri del percorso | Corpo della richiesta | Risposta in caso di successo |
|-----------|-------------|----------|----------------|--------------|------------------|
| Aggiungi sfondo | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – nome del file del libro<br>`sheetName` – foglio di lavoro target | File immagine (PNG, JPEG, BMP) come multipart/form‑data | `200 OK` – sfondo applicato |
| Rimuovi sfondo | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – nome del file del libro<br>`sheetName` – foglio di lavoro target | *nessuno* | `200 OK` – sfondo rimosso |

#### Esempio (SDK Java)

```java
// Aggiungi un'immagine di sfondo
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("percorso/dello/sfondo.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Rimuovi l'immagine di sfondo
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Esempio (SDK Python)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# Aggiungi sfondo
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Rimuovi sfondo
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

Per ulteriori esempi in altri linguaggi (C#, PHP, Ruby), consulta la documentazione degli SDK.

**Argomenti correlati**  
- Scopri di più sulla gestione generale dei fogli di lavoro: [Panoramica dei fogli di lavoro](/cells/worksheets/).  
- Comprendi come autenticarti con Aspose.Cells Cloud: [Guida all'autenticazione API](/cells/authentication/).  
- Esplora altri elementi del foglio elettronico come grafici, tabelle e formule: [Indice degli elementi del foglio elettronico](/cells/elements/).
---