---
title: Aspose.Cells SDK Cloud pour PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdwon, PHP
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque PHP pour Aspose.Cells Cloud[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Comment utiliser le SDK Cloud Aspose.Cells pour PHP**

Aspose.Cells Cloud SDK pour PHP est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter Microsoft Excel fichiers à l'aide du langage de programmation Go. Avec ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ou de dépendances supplémentaires sur votre ordinateur local.

Dans cet article, nous verrons comment utiliser le SDK Cloud Aspose.Cells pour PHP afin d'effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Faire référence à[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package PHP pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud Aspose.Cells pour PHP. Voici les étapes :

- Ajoutez Aspose.Cells Cloud comme dépendance à votre fichier `composer.json` :

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Exécutez la mise à jour de Composer pour installer le SDK :

   ```bash

   composer install

   ```

- Incluez le chargeur automatique de Composer dans votre code PHP :

   ```php

   require 'vendor/autoload.php';

   ```

## Comment utiliser le package PHP pour convertir Xlsx en PDF

- Importer la bibliothèque cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud PHP dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l'aide de la méthode PostConvertWorkbook et gérez la réponse.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```
