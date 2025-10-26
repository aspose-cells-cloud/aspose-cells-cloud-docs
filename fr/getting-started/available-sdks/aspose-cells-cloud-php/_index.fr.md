---
title: "Aspose.Cells Cloud SDK pour PHP : Convertir, fusionner, diviser, protéger, rechercher, remplacer et bien plus encore"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for PHP: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Cloud SDK pour PH
type: docs
url: /fr/available-sdks/aspose-cells-cloud-php/
description: "Aspose.Cells Cloud SDK pour PHP offre une véritable puissance multiplateforme : une seule importation fournit aux développeurs Windows, Linux et macOS la même fluidité API pour créer, convertir, fusionner, diviser, protéger et manipuler chaque Excel objet — aucune installation Office n'est requise et aucun ajustement spécifique à la plateforme n'est nécessaire"
weight: 30
kwords: SDK PHP, SDK Excel pour PHP, SDK Cloud pour PHP, REST, Graphique, Tableau croisé dynamique, Objet Table/Liste, Conversion de feuille de calcul, PDF, CSV, Json, Markdown, Fusion, Fractionnement, Protection, Recherche, Remplacement
---
Le SDK est open source et sous licence MIT. Vous pouvez y accéder.[le code source de la bibliothèque PHP pour Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Comment utiliser le SDK Cloud Aspose.Cells pour PHP**

Le SDK Cloud Aspose.Cells pour PHP est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Go. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons découvrir comment utiliser Aspose.Cells Cloud SDK pour PHP pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package PHP pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud Aspose.Cells pour PHP. Voici les étapes à suivre :

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

## Comment utiliser le package PHP pour convertir un fichier Xlsx vers d'autres formats

- Importer la bibliothèque Cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud PHP dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l’aide de la méthode PostConvertWorkbook et gérez la réponse.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}
