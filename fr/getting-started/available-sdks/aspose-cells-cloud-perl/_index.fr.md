---
title: Aspose.Cells SDK Cloud pour Per
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdwon, Perl
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Perl pour Aspose.Cells Cloud[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).


# **Comment utiliser la bibliothèque Perl de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK pour Perl est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Perl. Avec ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ou de dépendances supplémentaires sur votre ordinateur local.

Dans cet article, nous verrons comment utiliser le SDK Cloud Aspose.Cells pour Perl afin d'effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Faire référence à[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Perl pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud Aspose.Cells pour Perl à l'aide de la commande ci-dessous :

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## Comment utiliser le package Perl pour convertir Xlsx en PDF

- Importer la bibliothèque cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud Perl dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l'aide de la méthode PostConvertWorkbook et gérez la réponse.

```Perl
use lib 'lib';
use strict;
use warnings;
use File::Slurp;
use MIME::Base64;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'CellsCloudClientId'}, client_secret => $ENV{'CellsCloudClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $remoteFolder = 'TestData/In';
  
my $localName = 'Book1.xlsx';
my $remoteName = 'Book1.xlsx';

my $upload_file_request = AsposeCellsCloud::Request::UploadFileRequest->new( 'UploadFiles'=>{ $localName => $localName  }  ,'path'=>$remoteFolder . '/' . $remoteName );
 
my $format = 'csv';

my $mapFiles = {};           

 $mapFiles->{$localName}= "TestData/".$localName ;

my $request = AsposeCellsCloud::Request::PutConvertWorkbookRequest->new();
$request->{file} =  $mapFiles;
$request->{format} =  $format;
$instance->put_convert_workbook(request=> $request);
```
