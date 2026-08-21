---
title: "Aspose.Cells Cloud SDK pour Node.js : convertir, fusionner, diviser, protéger, rechercher, remplacer, et plus encore."
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK pour Node.js : convertir, fusionner, diviser, protéger, rechercher, remplacer, et plus encore."
linktitle: "Aspose.Cells Cloud SDK pour Node.js"
type: docs
url: /available-sdks/aspose-cells-cloud-node/
description: "L’SDK Aspose.Cells Cloud pour Node.js offre une puissance véritablement multiplateforme : une seule importation met à disposition des développeurs Windows, Linux et macOS la même API fluide pour créer, convertir, fusionner, diviser, protéger et manipuler tous les objets Excel — aucune installation d’Office n’est requise, et aucune adaptation spécifique à la plateforme n’est nécessaire."
weight: 30
kwords: Node.js, SDK Node.js, SDK Excel pour Node.js, SDK Cloud pour Node.js, REST, Graphique, Tableau croisé dynamique, Objet Tableau/Liste, Convertir feuille de calcul, PDF, CSV, JSON, Markdown, Fusionner, Diviser, Protéger, Rechercher, Remplacer
---

L’SDK est open source et distribué sous licence MIT. Vous pouvez consulter le code source de la bibliothèque Node.js pour Aspose.Cells Cloud [ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Comment utiliser la bibliothèque Node de Aspose.Cells Cloud**

L’SDK Aspose.Cells Cloud pour Node est une bibliothèque puissante qui permet aux développeurs de manipuler et traiter des fichiers Microsoft Excel à l’aide du langage de programmation Node. Grâce à cet SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans avoir à installer de logiciels ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser l’SDK Aspose.Cells Cloud pour Node afin d’accomplir certaines tâches courantes, telles que la création d’un nouveau classeur Excel, l’insertion de données dans des cellules, et l’enregistrement du classeur modifié dans le cloud.

## Premiers pas

Avant de pouvoir utiliser l’SDK Aspose.Cells Cloud pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Reportez-vous à [cet article](https://docs.aspose.cloud/cells/quickstart/) sur le site web d’Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Node pour Aspose.Cells Cloud

Vous pouvez installer l’SDK Aspose.Cells Cloud pour Node à l’aide de npm. Voici les étapes à suivre pour npm :

```Powershell

npm install asposecellscloud

```

## Comment ajouter les dépendances dans la configuration du package pour Aspose.Cells Cloud

Fichier de configuration Node : package.json

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

- Importer la bibliothèque Aspose.Cells Cloud  
  Commencez par importer le package nécessaire depuis le SDK NodeJS d’Aspose.Cells Cloud dans votre projet.
- Configurer le client API avec les identifiants  
  Authentifiez votre client API à l’aide de votre identifiant client et de votre secret client uniques.
- Préparer les paramètres de conversion  
  Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur  
  Invoquez le processus de conversion à l’aide de la méthode PostConvertWorkbook et gérez la réponse.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}