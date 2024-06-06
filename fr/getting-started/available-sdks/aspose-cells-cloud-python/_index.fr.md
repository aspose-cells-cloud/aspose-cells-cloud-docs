---
title: Aspose.Cells SDK Cloud pour Python
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-python/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdwon, Python
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Python pour Aspose.Cells Cloud[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

# **Comment utiliser le SDK Cloud Aspose.Cells pour Python**

Aspose.Cells Cloud SDK pour Python est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Python. Avec ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ou de dépendances supplémentaires sur votre ordinateur local.

Dans cet article, nous verrons comment utiliser le SDK Cloud Aspose.Cells pour Python afin d'effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Faire référence à[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Python pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud Aspose.Cells pour Python à l'aide de la commande ci-dessous :

```bash

    pip3 install AsposeCellsCloud
  
 ```

## Comment utiliser le package Python pour convertir Xlsx en PDF

- Importer la bibliothèque cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud Python dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l'aide de la méthode PostConvertWorkbook et gérez la réponse.

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
