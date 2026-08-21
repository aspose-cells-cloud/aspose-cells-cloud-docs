---
title: "Aspose.Cells Cloud SDK pour C# : convertir, fusionner, diviser, protéger, rechercher, remplacer, etc."
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK pour C# : convertir, fusionner, diviser, protéger, rechercher, remplacer, etc."
linktitle: "Aspose.Cells Cloud SDK pour .NET"
type: docs
url: /available-sdks/aspose-cells-cloud-net/
description: "Le SDK .NET Aspose.Cells Cloud fournit une API multiplateforme pour créer, convertir, fusionner, diviser, protéger, rechercher et remplacer des fichiers Excel — aucune installation d'Office n'est requise."
keywords: "Aspose.Cells, SDK Cloud, .NET, Excel, convertir, fusionner, diviser, protéger, rechercher, remplacer, API"
weight: 30
---

Le SDK est open-source et licencié sous la licence MIT. Vous pouvez accéder au code source de la bibliothèque .NET pour Aspose.Cells Cloud [ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **Comment utiliser la bibliothèque .NET d’Aspose.Cells Cloud**

Le SDK Aspose.Cells Cloud pour .NET est une bibliothèque puissante qui permet aux développeurs de manipuler et traiter des fichiers Microsoft Excel à l’aide du langage de programmation .NET. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans avoir à installer de logiciels ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser le SDK Aspose.Cells Cloud pour .NET afin d’accomplir certaines tâches courantes, telles que la création d’un nouveau classeur Excel, l’insertion de données dans des cellules, et l’enregistrement du classeur modifié dans le cloud.

## Mise en route

Avant de pouvoir utiliser le SDK Aspose.Cells Cloud pour .NET, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Reportez-vous à [cet article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client (client ID) et votre secret client (client secret).

**Prérequis**  
- .NET 6.0 ou une version ultérieure installé.  
- Un compte Aspose Cloud disposant d’un identifiant client (client ID) et d’un secret client (client secret).  
- Accès à un emplacement de stockage (stockage Aspose Cloud ou service compatible).

## Comment installer le package .NET pour Aspose.Cells Cloud

Vous pouvez installer le SDK Aspose.Cells Cloud pour .NET via NuGet. Voici les étapes à suivre avec NuGet :

```nuget
Install-Package Aspose.Cells-Cloud
```

Vous pouvez également installer le SDK Aspose.Cells Cloud pour .NET via dotnet. Voici les étapes à suivre :

```powershell
dotnet add package Aspose.Cells-Cloud
```

## Comment utiliser le package .NET pour convertir Xlsx en PDF

- Importer la bibliothèque Aspose.Cells Cloud  
  Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud .NET dans votre projet.  
- Configurer le client API avec les identifiants  
  Authentifiez votre client API à l’aide de votre identifiant client (client ID) et de votre secret client (client secret) uniques.  
- Préparer les paramètres de conversion  
  Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.  
- Exécuter la conversion du classeur  
  Invoquez le processus de conversion à l’aide de la méthode `PostConvertWorkbook` et gérez la réponse.

### **Exemple de code**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}