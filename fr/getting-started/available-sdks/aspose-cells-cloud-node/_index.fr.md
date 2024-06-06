---
title: Aspose.Cells SDK cloud pour Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, feuille de calcul, PDF, CSV, Json, Markdwon, nœud
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Node pour Aspose.Cells Cloud[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **Comment utiliser la bibliothèque Node de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Node est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter Microsoft Excel fichiers à l'aide du langage de programmation Node. Avec ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ou de dépendances supplémentaires sur votre ordinateur local.


Dans cet article, nous verrons comment utiliser le SDK Cloud Aspose.Cells pour Node pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Faire référence à[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Node pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud Aspose.Cells pour Node à l'aide de npm. Voici les étapes pour npm :


```Powershell

npm install asposecellscloud

```

## Comment ajouter des dépendances dans la configuration du package pour Aspose.Cells Cloud

fichier de configuration du nœud : package.json

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

## Comment utiliser le package Node pour convertir Xlsx en PDF

- Importer la bibliothèque cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Cloud NodeJS Aspose.Cells dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l'aide de la méthode PostConvertWorkbook et gérez la réponse.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```
