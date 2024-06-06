---
title: Aspose.Cells SDK cloud pour Java
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-java/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdwon, Java
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Java pour Aspose.Cells Cloud[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **Comment utiliser la bibliothèque Java de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Java est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Java. Avec ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ou de dépendances supplémentaires sur votre ordinateur local.

Dans cet article, nous verrons comment utiliser le SDK Cloud Aspose.Cells for Java pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Faire référence à[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment utiliser Maven pour ajouter des dépendances pour Aspose.Cells Cloud

Dans votre projet Maven, ajoutez des dépendances pour le SDK Cloud Aspose.Cells. Incluez les dépendances suivantes dans le fichier pom.xml :

**Aspose Maven Dépôt**

```java

<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>

```

**Maven Dépendance**

```java

<dependency>
      <groupId>com.aspose</groupId>
      <artifactId>aspose-cloud-cells</artifactId>
      <version>24.5</version>
</dependency>

```

## Comment utiliser le package Java pour convertir Xlsx en PDF

- Importer la bibliothèque cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud Java dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l'aide de la méthode PostConvertWorkbook et gérez la réponse.

### **Exemple de code**

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
