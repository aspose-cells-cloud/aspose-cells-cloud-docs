---
title: Aspose.Cells Cloud SDK pour Python
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-python/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, effectuer des opérations sur des objets internes, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Python
---
Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Python pour Aspose.Cells Cloud.[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

# **Comment utiliser le SDK Cloud Aspose.Cells pour Python**

Le SDK Cloud Aspose.Cells pour Python est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Python. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser Aspose.Cells Cloud SDK pour Python pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Python pour Aspose.Cells Cloud

Vous pouvez installer Aspose.Cells Cloud SDK pour Python avec la commande ci-dessous :

```bash

    pip3 install AsposeCellsCloud
  
 ```

## Comment utiliser le package Python pour convertir Xlsx en PDF

- Importer la bibliothèque Cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud Python dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l’aide de la méthode PostConvertWorkbook et gérez la réponse.

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_AvailableSDKs.py" >}}
