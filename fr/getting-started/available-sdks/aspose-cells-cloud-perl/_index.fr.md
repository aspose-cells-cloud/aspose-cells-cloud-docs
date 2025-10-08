---
title: "Aspose.Cells Cloud SDK pour Perl : Convertir, fusionner, diviser, protéger, rechercher, remplacer et bien plus encore"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Perl: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Cloud SDK pour Per
type: docs
url: /fr/available-sdks/aspose-cells-cloud-perl/
description: "Aspose.Cells Cloud SDK pour Perl offre une véritable puissance multiplateforme : une seule importation fournit aux développeurs Windows, Linux et macOS la même fluidité API pour créer, convertir, fusionner, diviser, protéger et manipuler chaque Excel objet — aucune installation Office n'est requise et aucun ajustement spécifique à la plateforme n'est nécessaire"
weight: 30
kwords: Perl, Perl SDK, Excel SDK pour Perl, Cloud SDK pour Perl, REST, Graphique, Tableau croisé dynamique, Objet Table/Liste, Convertir une feuille de calcul, PDF, CSV, Json, Markdown, Fusionner, Fractionner, Protéger, Rechercher, Remplacer
---
Le SDK est open source et sous licence MIT. Vous pouvez y accéder.[le code source de la bibliothèque Perl pour Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **Comment utiliser la bibliothèque Perl du Cloud Aspose.Cells**

Le SDK Cloud Aspose.Cells pour Perl est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft et Excel à l'aide du langage de programmation Perl. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons découvrir comment utiliser Aspose.Cells Cloud SDK pour Perl pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Perl pour Aspose.Cells Cloud

Vous pouvez installer Aspose.Cells Cloud SDK pour Perl avec la commande ci-dessous :

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## Comment utiliser le package Perl pour convertir un fichier Xlsx vers d'autres formats

- Importer la bibliothèque Cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud Perl dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l’aide de la méthode PostConvertWorkbook et gérez la réponse.

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}
