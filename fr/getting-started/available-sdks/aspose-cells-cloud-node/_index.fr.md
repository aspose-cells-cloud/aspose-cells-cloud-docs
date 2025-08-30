---
title: Aspose.Cells Cloud SDK pour Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, effectuer des opérations sur des objets internes, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Node
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Node pour Aspose.Cells Cloud.[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Comment utiliser la bibliothèque Node du Cloud Aspose.Cells**

Le SDK Cloud pour Node est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers à l'aide du langage de programmation Node. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser Aspose.Cells Cloud SDK pour Node pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Node pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud Aspose.Cells pour Node avec npm. Voici la procédure à suivre :

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

## Comment utiliser le package Node pour convertir Xlsx vers d'autres formats

- Importer la bibliothèque Cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Cloud NodeJS Aspose.Cells dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l’aide de la méthode PostConvertWorkbook et gérez la réponse.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
