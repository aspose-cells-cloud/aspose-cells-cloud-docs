---
title: "Aspose.Cells Cloud PHP SDK – Converti, unisci, dividi, proteggi file Excel"  
second_title: "Documento"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Converti, unisci, dividi, proteggi file Excel"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /available-sdks/aspose-cells-cloud-php/  
description: "Scarica Aspose.Cells Cloud PHP SDK (v24.3). Scopri come installarlo tramite Composer, autenticarti, convertire XLSX in PDF/CSV, unire cartelle di lavoro, proteggere fogli e molto altro — tutto senza installare Office."  
keywords: "Aspose.Cells, Cloud, PHP, SDK, Excel, Converti, Unisci, Dividi, Proteggi"  
weight: 30  
---  

L'SDK è open-source e concesso in licenza con la licenza MIT. Puoi accedere al codice sorgente della libreria PHP per Aspose.Cells Cloud <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">qui</a>.

# **Come utilizzare Aspose.Cells Cloud SDK per PHP**

Aspose.Cells Cloud SDK per PHP è una potente libreria che consente agli sviluppatori di manipolare e processare file di Microsoft Excel utilizzando il **linguaggio di programmazione PHP**. Con questo SDK è possibile creare, modificare e convertire documenti Excel nel cloud, senza dover installare software aggiuntivi o dipendenze sul proprio computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK per PHP per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Per iniziare

Prima di poter utilizzare Aspose.Cells Cloud SDK per **PHP**, è necessario configurare l'ambiente di sviluppo e installare le dipendenze necessarie. Consulta <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">l'articolo</a> sul sito web Aspose per ottenere il proprio client ID e client secret.

**Prerequisiti**

- PHP 7.4 o versione successiva  
- Composer installato sulla macchina di sviluppo  
- Client ID e client secret validi per Aspose Cloud  
- Accesso a una posizione di archiviazione Aspose Cloud (predefinita o personalizzata)  

## Come installare il pacchetto PHP per Aspose.Cells Cloud

Puoi installare Aspose.Cells Cloud SDK per PHP. Di seguito sono riportati i passaggi:

- Aggiungi Aspose.Cells Cloud come dipendenza nel file `composer.json`:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Esegui Composer update per installare l'SDK:

   ```bash
   composer install
   ```

- Includi l'autoloader di Composer nel tuo codice PHP:

   ```php
   require 'vendor/autoload.php';
   ```

## Come utilizzare il pacchetto PHP per convertire Xlsx in altri formati

- Importa la libreria Aspose.Cells Cloud  
  Inizia importando il pacchetto necessario dell'SDK Aspose.Cells Cloud per PHP nel tuo progetto.

- Configura il client API con le credenziali  
  Autentica il tuo client API con il tuo unico client ID e client secret.

- Prepara i parametri per la conversione  
  Definisci i parametri per l'attività di conversione, inclusi il nome del file sorgente, il formato di output desiderato e il percorso della cartella di archiviazione.

- Esegui la conversione della cartella di lavoro  
  Richiama il processo di conversione utilizzando il metodo `PostConvertWorkbook` e gestisci la risposta.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### Riferimento API per `PostConvertWorkbook`

| Parametro      | Descrizione                                   | Tipo   | Obbligatorio |
|----------------|-----------------------------------------------|--------|--------------|
| `file`         | Nome del file Excel sorgente (ad esempio, `sample.xlsx`). | string | Sì |
| `format`       | Formato di output desiderato (`pdf`, `csv`, `png`, ecc.). | string | Sì |
| `storage`      | Nome dell'archiviazione o percorso della cartella in cui si trova il file sorgente. | string | No |
| `outPath`      | Percorso facoltativo per salvare direttamente nel cloud il file convertito. | string | No |

**Metodo HTTP:** POST  
**Endpoint:** `/cells/convert/{format}`  

**Esempio di risposta (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**Codici di stato**

- `200` – Conversione riuscita.  
- `400` – Richiesta non valida (parametri mancanti o non validi).  
- `401` – Autenticazione non riuscita.  
- `500` – Errore del server.  
---