---
---
title: "Aspose.Cells Cloud SDK per Node.js: convertire, unire, dividere, proteggere, cercare, sostituire e molto altro."
second_title: "Documento"
ArticleTitle: "Aspose.Cells Cloud SDK per Node.js: convertire, unire, dividere, proteggere, cercare, sostituire e molto altro."
linktitle: "Aspose.Cells Cloud SDK per Node.js"
type: docs
url: /available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK per Node.js offre un vero potere multipiattaforma: un'unica importazione fornisce agli sviluppatori Windows, Linux e macOS la stessa API fluida per creare, convertire, unire, dividere, proteggere e manipolare ogni oggetto Excel—nessuna installazione di Office è richiesta e non sono necessarie modifiche specifiche per piattaforma."
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK per Node.js, Cloud SDK per Node.js, REST, Grafico, Tabella Pivot, Oggetto Tabella/Elenco, Convertire Foglio Elettronico, PDF, CSV, Json, Markdown, Unire, Dividere, Proteggere, Cercare, Sostituire
---

L'SDK è open-source e rilasciato sotto licenza MIT. Puoi accedere al codice sorgente della libreria Node per Aspose.Cells Cloud [qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Come usare la libreria Node di Aspose.Cells Cloud**

Aspose.Cells Cloud SDK per Node è una potente libreria che consente agli sviluppatori di manipolare e processare file Microsoft Excel utilizzando il linguaggio di programmazione Node. Con questo SDK è possibile creare, modificare e convertire documenti Excel nel cloud, senza dover installare software o dipendenze aggiuntive sul proprio computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK per Node per svolgere alcune attività comuni, come la creazione di un nuovo workbook Excel, l'inserimento di dati nelle celle e il salvataggio del workbook modificato nel cloud.

## Per iniziare

Prima di poter iniziare a utilizzare Aspose.Cells Cloud SDK per Go, è necessario configurare l'ambiente di sviluppo e installare le dipendenze necessarie. Consulta [questo articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito web di Aspose per ottenere il proprio client ID e client secret.

## Come installare il pacchetto Node per Aspose.Cells Cloud

È possibile installare Aspose.Cells Cloud SDK per Node tramite npm. Di seguito sono riportati i passaggi per npm:

```Powershell

npm install asposecellscloud

```

## Come aggiungere le dipendenze nel file di configurazione del pacchetto per Aspose.Cells Cloud

File di configurazione node: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Come utilizzare il pacchetto Node per convertire Xlsx in altri formati

- Importa la libreria Aspose.Cells Cloud
  Inizia importando il pacchetto necessario dall'SDK NodeJS di Aspose.Cells Cloud nel tuo progetto.
- Configura il client API con le credenziali
  Autentica il tuo client API con il tuo unico client ID e client secret.
- Prepara i parametri per la conversione
  Definisci i parametri per l'attività di conversione, inclusi il nome del file sorgente, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui la conversione del workbook
  Invoca il processo di conversione utilizzando il metodo PostConvertWorkbook e gestisci la risposta.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}

---