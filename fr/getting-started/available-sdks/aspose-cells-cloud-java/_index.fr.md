---
title: "Aspose.Cells Cloud SDK for Java : Convertir, fusionner, diviser, protéger, rechercher, remplacer et plus encore"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Java: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Cloud SDK pour Java
type: docs
url: /fr/available-sdks/aspose-cells-cloud-java/
description: "Aspose.Cells Cloud SDK for Java offre une véritable puissance multiplateforme : une seule importation fournit aux développeurs Windows, Linux et macOS la même fluidité API pour créer, convertir, fusionner, diviser, protéger et manipuler chaque Excel objet — aucune Office installation n'est requise et aucun ajustement spécifique à la plateforme n'est nécessaire"
weight: 30
kwords: Java SDK, Excel SDK for Java, Cloud SDK for Java, REST, Graphique, Tableau croisé dynamique, Objet Table/Liste, Convertir une feuille de calcul, PDF, CSV, Json, Markdown, Fusionner, Fractionner, Protéger, Rechercher, Remplacer
---
Le SDK est open source et sous licence MIT. Vous pouvez y accéder.[le code source de la bibliothèque Java pour Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **Comment utiliser la bibliothèque Java du Cloud Aspose.Cells**

Le SDK Cloud Aspose.Cells est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Java. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons découvrir comment utiliser Aspose.Cells Cloud SDK for Java pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## Commencer

 Avant de pouvoir utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment utiliser Maven pour ajouter des dépendances pour Aspose.Cells Cloud

Dans votre projet Maven, ajoutez des dépendances pour le SDK Cloud Aspose.Cells. Incluez les dépendances suivantes dans le fichier pom.xml :

**Aspose Maven Dépôt**

```java

<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>

```

**Maven Dépendance**

```java

<dependency>
      <groupId>com.aspose</groupId>
      <artifactId>aspose-cloud-cells</artifactId>
      <version>24.5</version>
</dependency>

```

## Comment utiliser le package Java pour convertir Xlsx en PDF

- Importer la bibliothèque Cloud Aspose.Cells
 Commencez par importer le package nécessaire du SDK Aspose.Cells Cloud Java dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l’aide de la méthode PostConvertWorkbook et gérez la réponse.

### **Exemple de code**

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_AvailableSDKs.java" >}}
