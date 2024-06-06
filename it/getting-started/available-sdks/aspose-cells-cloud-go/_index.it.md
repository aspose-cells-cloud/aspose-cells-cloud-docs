---
title: Aspose.Cells Cloud SDK per G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-go/
description: Aspose.Cells Cloud SDK for Go fornisce un forte supporto multipiattaforma per gli sviluppatori Go, semplificando l'integrazione e l'utilizzo per Windows, Linux o macOS. Supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Vai, Excel, Office Cloud, REST API, Grafico, Tabella pivot, Tabella, Foglio di calcolo, PDF, CSV, Json, Markdown
---
 L'SDK è open source e concesso in licenza con la licenza MIT. Puoi accedere al codice sorgente della libreria Go per Aspose.Cells Cloud[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **Come utilizzare la libreria Go di Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Go è una potente libreria che consente agli sviluppatori di manipolare ed elaborare file Microsoft Excel utilizzando il linguaggio di programmazione Go. Con questo SDK puoi creare, modificare e convertire i documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK for Go per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## **Iniziare**

 Prima di poter iniziare a utilizzare Aspose.Cells Cloud SDK for Go, devi configurare il tuo ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito web Aspose per ottenere l'ID cliente e il segreto cliente.

## Come installare il pacchetto Go per Aspose.Cells Cloud

Puoi installare Aspose.Cells Cloud SDK for Go utilizzando il comando `go get`. Apri il terminale o il prompt dei comandi ed esegui il seguente comando:

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

Verrà scaricata e installata la versione più recente dell'SDK nell'area di lavoro Go.


## Come importare la libreria Go nel tuo progetto


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## Come utilizzare il pacchetto Go per convertire Xlsx in PDF

- Importa libreria cloud Aspose.Cells
Inizia importando il pacchetto necessario dall'SDK Cloud Go Aspose.Cells nel tuo progetto.
- Configurare Cliente API con Credenziali
 Autentica il tuo client API con il tuo ID client univoco e il segreto client.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, incluso il nome del file di origine, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui la conversione della cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

### **Codice d'esempio**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```
