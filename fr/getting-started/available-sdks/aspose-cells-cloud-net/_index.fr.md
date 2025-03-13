---
title: Aspose.Cells SDK Cloud pour Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdwon, Net
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Net pour Aspose.Cells Cloud[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **Comment utiliser la bibliothèque Net de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Net est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter Microsoft Excel fichiers à l'aide du langage de programmation Net. Avec ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ou de dépendances supplémentaires sur votre ordinateur local.

Dans cet article, nous verrons comment utiliser le SDK Cloud Aspose.Cells pour Net pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Faire référence à[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Net pour Aspose.Cells Cloud

Vous pouvez installer Aspose.Cells Cloud SDK for Net à l'aide de nuget. Vous trouverez ci-dessous les étapes pour nuget :

```nuget

Install-Package Aspose.Cells-Cloud

```

Vous pouvez également installer le SDK Cloud Aspose.Cells pour Net à l'aide de dotnet. Voici les étapes pour dotnet :

```powershell

dotnet add package Aspose.Cells-Cloud 

```

## Comment utiliser le package Net pour convertir Xlsx en PDF

- Importer la bibliothèque cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Cloud DotNet Aspose.Cells dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l'aide de la méthode PostConvertWorkbook et gérez la réponse.

### **Exemple de code**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Convert-Excel-To-PDF.cs" >}}
