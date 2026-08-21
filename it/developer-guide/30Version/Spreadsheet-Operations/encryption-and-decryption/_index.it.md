---
title: "Crittografa, decrittografa e firma digitalmente file Excel"
second_title: "Documento"
linktype: "Proteggi Excel"
type: docs
url: /it/protect/
aliases: [/it/workbook/password/]
keywords: "Excel, proteggi, crittografa, decrittografa, firma digitale, Aspose.Cells Cloud, API REST, password, sicurezza"
description: "Scopri come proteggere, crittografare, decrittografare e firmare digitalmente cartelle di lavoro Excel con l'API REST di Aspose.Cells Cloud – esempi di codice per Android, C#, Java, Python e altro."
ArticleTitle: "Crittografa, decrittografa, firma digitalmente e proteggi file Excel utilizzando l'API Aspose.Cells Cloud"
weight: 36
---

## **Protezione e rimozione della protezione dei file Excel**

**Cos’è la “protezione” in Aspose.Cells Cloud?**  
L'operazione **Proteggi** protegge una cartella di lavoro Excel applicando una password che impedisce l'apertura, la modifica o la modifica della struttura del file. L'API supporta anche la crittografia della cartella di lavoro, la sua decrittografia e l'aggiunta di una firma digitale per una verifica resistente contraffazione.

**Riferimento API**

| Metodo HTTP | Endpoint | Parametri obbligatori (query/body) | Corpo della richiesta di esempio | Risposte tipiche |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (percorso), `password` (query) | `{ "password": "LaMiaSegreta123" }` | `200 OK` – protezione applicata, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (percorso), `password` (query) | N/A | `200 OK` – protezione rimossa, codici di errore come sopra |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (percorso), `password` (query) | N/A | `200 OK` – file crittografato |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (percorso), `password` (query) | N/A | `200 OK` – file decrittografato |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (percorso) | `{ "certificatePath": "/certs/miacert.pfx", "certificatePassword": "passCert" }` | `200 OK` – firma digitale aggiunta |

**Esempio di codice (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Inizializza il client API
var config = new Configuration
{
    AppSid = "IL_TUO_APP_SID",
    AppKey = "LA_TUA_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Proteggi la cartella di lavoro
var protectRequest = new PostProtectWorkbookRequest(
    name: "Esempio.xlsx",
    password: "LaMiaSegreta123"
);
api.PostProtectWorkbook(protectRequest);
```

**Prerequisiti**  
- Una sottoscrizione attiva ad Aspose.Cells Cloud.  
- `AppSid` e `AppKey` per l'autenticazione.  

**Autenticazione**  
Tutte le richieste devono includere l'intestazione `Authorization` con un token JWT valido ottenuto dall'endpoint di autenticazione di Aspose Cloud.

**Gestione degli errori**  
Verifica il codice di stato HTTP e l'oggetto `Error` restituito nel corpo della risposta. Gli errori comuni includono password non valida (`400`), file mancante (`404`) e errori di autenticazione (`401`).

**Note**  
- Lo stesso endpoint può essere utilizzato per **crittografare** o **decrittografare** modificando la parte relativa all'azione (`/encrypt`, `/decrypt`).  
- Le firme digitali richiedono un file di certificato valido accessibile all'API.

- [Crittografare un file Excel con Aspose.Cells Cloud API](/it/cells/excel-file-encrypt/)
- [Proteggere un file Excel con Aspose.Cells Cloud API](/it/cells/protect-excel-file/)
- [Aggiungere una firma digitale a un file Excel](/it/cells/excel-digital-signature/)
- [Proteggere i file Excel – guida dettagliata](/it/cells/protect-excel-files/)
- [Impostare una password per un file Excel](/it/cells/workbook/password/modify/)
- [Decrittografare un file Excel](/it/cells/excel-file-decrypt/)
- [Rimuovere la protezione da un file Excel](/it/cells/excel-file-unprotect/)
- [Sbloccare file Excel](/it/cells/unlock-excel-files/)
- [Rimuovere la password da un file Excel](/it/cells/clear-excel-files-password/)
---