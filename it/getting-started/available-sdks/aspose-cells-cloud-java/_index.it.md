---
title: Aspose.Cells Cloud SDK per Jav
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-java/
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Java
---
 L'SDK è open source e concesso in licenza con la licenza MIT. Puoi accedere al codice sorgente della libreria Java per Aspose.Cells Cloud[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **Come utilizzare la libreria Java di Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Java è una potente libreria che consente agli sviluppatori di manipolare ed elaborare i file Microsoft Excel utilizzando il linguaggio di programmazione Java. Con questo SDK puoi creare, modificare e convertire i documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK for Java per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Iniziare

 Prima di poter iniziare a utilizzare Aspose.Cells Cloud SDK for Go, devi configurare il tuo ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito web Aspose per ottenere l'ID cliente e il segreto cliente.

## Come utilizzare Maven per aggiungere dipendenze per Aspose.Cells Cloud

Nel tuo progetto Maven, aggiungi le dipendenze per Aspose.Cells Cloud SDK. Includere le seguenti dipendenze nel file pom.xml:

**Aspose Maven Deposito**

```java

<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>

```

**Maven Dipendenza**

```java

<dependency>
      <groupId>com.aspose</groupId>
      <artifactId>aspose-cloud-cells</artifactId>
      <version>24.5</version>
</dependency>

```

## Come utilizzare il pacchetto Java per convertire Xlsx in PDF

- Importa libreria cloud Aspose.Cells
 Inizia importando il pacchetto necessario dall'SDK Aspose.Cells Cloud Java nel tuo progetto.
- Configurare Cliente API con Credenziali
 Autentica il tuo client API con il tuo ID client univoco e il segreto client.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, incluso il nome del file di origine, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui la conversione della cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

### **Codice d'esempio**

```java
package com.aspose.cloud.cells.api;

import com.aspose.cloud.cells.client.*;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.request.*;

import org.junit.Test;
import java.util.ArrayList;
import java.util.List;
import java.io.File;
import java.util.HashMap;

public class ExamplePutConvertWorkbook {
    private  CellsApi api;
    public ExamplePutConvertWorkbook(){
        try {
            api = new CellsApi(
                System.getenv("CellsCloudClientId"),
                System.getenv("CellsCloudClientSecret"),
                "v3.0",
                System.getenv("CellsCloudApiBaseUrl")
            );
        } catch (ApiException e) {
            e.printStackTrace();
        }
    }

    public void Run(){
        try{
            String remoteFolder = "TestData/In";

            String localName = "Book1.xlsx";
            String remoteName = "Book1.xlsx";

            String format = "pdf";

            UploadFileRequest  uploadFileRequest = new UploadFileRequest();
            uploadFileRequest.setPath( remoteFolder + "/" + remoteName );
            uploadFileRequest.setStorageName( "");
            HashMap<String,File> files = new HashMap<String,File>();
            files.put( localName , new File(localName ));
            uploadFileRequest.setUploadFiles(files);
            cellsApi.uploadFile(uploadFileRequest);
   
            PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();
            request.setFormat(format);
             

            HashMap<String,File> fileMap = new HashMap<String,File>(); 
            fileMap.put(localName ,CellsApiUtil.GetFileHolder(localName) ); 
            request.setFile(fileMap);
            this.api.putConvertWorkbook(request);

        } catch (ApiException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        }
    }
}

```
