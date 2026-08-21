---
title: "Aspose.Cells Cloud SDK pour Perl – Convertir, fusionner, diviser, protéger et plus encore"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK pour Perl – Convertir, fusionner, diviser, protéger et plus encore"
linktitle: "Aspose.Cells Cloud SDK pour Perl"
type: docs
url: /available-sdks/aspose-cells-cloud-perl/
description: "Découvrez le SDK Aspose.Cells Cloud pour Perl – une bibliothèque multiplateforme permettant de créer, convertir, fusionner, diviser, protéger, rechercher et remplacer des fichiers Excel sans avoir besoin d’installer Office. Inclut un guide d’installation, des exemples de code et une référence API."
weight: 30
keywords: "Perl, Aspose.Cells Cloud, SDK Excel, conversion, PDF, API, manipulation Excel, SDK Perl, traitement Excel dans le cloud"
---

_Dernière mise à jour : 30 juillet 2026_

Le SDK est open-source et distribué sous la licence MIT. Vous pouvez accéder au code source de la bibliothèque Perl pour Aspose.Cells Cloud [ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **Comment utiliser la bibliothèque Perl d’Aspose.Cells Cloud**

Le SDK Aspose.Cells Cloud pour Perl est une bibliothèque puissante permettant aux développeurs de manipuler et traiter des fichiers Microsoft Excel à l’aide du langage de programmation Perl. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciels ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser le SDK Aspose.Cells Cloud pour Perl afin d’accomplir certaines tâches courantes, telles que la création d’un nouveau classeur Excel, l’insertion de données dans des cellules, et l’enregistrement du classeur modifié dans le cloud.

## Premiers pas

Avant de pouvoir utiliser le SDK Aspose.Cells Cloud pour **Perl**, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Reportez-vous au guide **[Démarrage rapide Aspose.Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)** sur le site d’Aspose pour obtenir votre identifiant client (client ID) et votre secret client (client secret).

## Comment installer le paquet Perl pour Aspose.Cells Cloud

**Prérequis**  
- Perl 5.10 ou version ultérieure  
- CPAN (Comprehensive Perl Archive Network) installé  
- Identifiant client et secret client valides pour Aspose.Cells Cloud  

Vous pouvez installer le SDK Aspose.Cells Cloud pour Perl à l’aide de la commande suivante :

```perl
perl -MCPAN -e shell
install AsposeCellsCloud::CellsApi
```

## Comment utiliser le paquet Perl pour convertir Xlsx vers d’autres formats

- **Importer la bibliothèque Aspose.Cells Cloud**  
  Commencez par importer le paquet nécessaire du SDK Aspose.Cells Cloud pour Perl dans votre projet.

- **Configurer le client API avec les identifiants**  
  Authentifiez votre client API à l’aide de votre identifiant client unique et de votre secret client.

- **Préparer les paramètres de conversion**  
  Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité, et le chemin du dossier de stockage.

- **Exécuter la conversion du classeur**  
  Déclenchez le processus de conversion à l’aide de la méthode `PostConvertWorkbook`, puis gérez la réponse.

Voici une référence concise concernant l’opération `PostConvertWorkbook` :

| Méthode HTTP | Endpoint                         | Paramètres requis                                      | Exemple de requête (Perl)                                                                                      | Exemple de réponse (JSON)                                 | Codes de statut possibles                     |
|--------------|----------------------------------|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------------|
| POST         | `/cells/convert`                 | `file` (classeur source), `outputFormat`, `storage`   | ```perl\nmy $result = $api_instance->post_convert_workbook({ file => 'Book1.xlsx', outputFormat => 'pdf', storage => 'MyStorage' });\n``` | `{ "File": "Book1.pdf", "Url": "https://.../Book1.pdf" }` | 200 OK, 400 Requête incorrecte, 401 Non autorisé, 500 Erreur serveur |

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}