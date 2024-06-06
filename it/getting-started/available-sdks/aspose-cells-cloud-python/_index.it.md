---
title: Aspose.Cells Cloud SDK per Pytho
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-python/
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Python
---
 L'SDK è open source e concesso in licenza con la licenza MIT. Puoi accedere al codice sorgente della libreria Python per Aspose.Cells Cloud[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

# **Come utilizzare Aspose.Cells Cloud SDK per Python**

Aspose.Cells Cloud SDK per Python è una potente libreria che consente agli sviluppatori di manipolare ed elaborare i file Microsoft Excel utilizzando il linguaggio di programmazione Python. Con questo SDK puoi creare, modificare e convertire i documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK per Python per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Iniziare

 Prima di poter iniziare a utilizzare Aspose.Cells Cloud SDK for Go, devi configurare il tuo ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito web Aspose per ottenere l'ID cliente e il segreto cliente.

## Come installare il pacchetto Python per Aspose.Cells Cloud

Puoi installare Aspose.Cells Cloud SDK per Python con il comando seguente:

```bash

    pip3 install AsposeCellsCloud
  
 ```

## Come utilizzare il pacchetto Python per convertire Xlsx in PDF

- Importa libreria cloud Aspose.Cells
 Inizia importando il pacchetto necessario dall'SDK Aspose.Cells Cloud Python nel tuo progetto.
- Configurare Cliente API con Credenziali
 Autentica il tuo client API con il tuo ID client univoco e il segreto client.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, incluso il nome del file di origine, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui la conversione della cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

```python
import os
import sys
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import *
from asposecellscloud.requests import *

api  = CellsApi(os.getenv('CellsCloudClientId'),os.getenv('CellsCloudClientSecret'),"v3.0",os.getenv('CellsCloudApiBaseUrl'))
remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = 'csv'

mapFiles = { 
    local_name: os.path.dirname(os.path.realpath(__file__)) + "/../TestData/" +local_name             
}
mapFiles = { 
    local_name:  local_name             
}
request =  UploadFileRequest( mapFiles, remote_folder + '/' + remote_name,storage_name= '')
api.upload_file(request)
 
request =  PutConvertWorkbookRequest( mapFiles,format= format)
api.put_convert_workbook(request)

```
