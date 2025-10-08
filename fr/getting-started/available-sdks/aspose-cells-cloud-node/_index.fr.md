---
title: "Aspose.Cells Cloud SDK pour Node.js : conversion, fusion, division, protection, recherche, remplacement, etc."
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Cloud SDK pour Node.j
type: docs
url: /fr/available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK pour Node.js offre une véritable puissance multiplateforme : une seule importation fournit aux développeurs Windows, Linux et macOS la même fluidité API pour créer, convertir, fusionner, diviser, protéger et manipuler chaque Excel objet — aucune Office installation n'est requise et aucun ajustement spécifique à la plateforme n'est nécessaire"
weight: 30
kwords: Node.js, SDK Node.js, Excel SDK pour Node.js, SDK Cloud pour Node.js, REST, Graphique, Tableau croisé dynamique, Objet tableau/liste, Conversion de feuille de calcul, PDF, CSV, Json, Markdown, Fusion, Division, Protection, Recherche, Remplacement
---
Le SDK est open source et sous licence MIT. Vous pouvez y accéder.[le code source de la bibliothèque Node pour Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Comment utiliser la bibliothèque Node du Cloud Aspose.Cells**

Le SDK Cloud pour Node est une puissante bibliothèque permettant aux développeurs de manipuler et de traiter des fichiers à l'aide du langage de programmation Node. Ce SDK vous permet de créer, modifier et convertir des documents dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons découvrir comment utiliser Aspose.Cells Cloud SDK for Node pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

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
