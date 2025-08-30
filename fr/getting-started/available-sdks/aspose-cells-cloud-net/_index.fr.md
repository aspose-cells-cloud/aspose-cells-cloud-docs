---
title: Aspose.Cells Cloud SDK pour Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, effectuer des opérations sur des objets internes, etc.
weight: 30
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Net
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Net pour Aspose.Cells Cloud.[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **Comment utiliser la bibliothèque Net du Cloud Aspose.Cells**

Aspose.Cells Cloud SDK for Net est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Net. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser Aspose.Cells Cloud SDK for Net pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Net pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud pour Net Aspose.Cells à l'aide de nuget. Voici les étapes pour nuget :

```nuget

Install-Package Aspose.Cells-Cloud

```

Vous pouvez également installer le SDK Cloud Aspose.Cells pour Net avec dotnet. Voici la procédure pour dotnet :

```powershell

dotnet add package Aspose.Cells-Cloud

```

## Comment utiliser le package Net pour convertir Xlsx en PDF

- Importer la bibliothèque Cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Cloud DotNet Aspose.Cells dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l’aide de la méthode PostConvertWorkbook et gérez la réponse.

### **Exemple de code**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}
