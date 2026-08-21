---
title: "Aspose.Cells Cloud PHP SDK – Convertir, fusionner, diviser, protéger des fichiers Excel"  
second_title: "Document"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Convertir, fusionner, diviser, protéger des fichiers Excel"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /available-sdks/aspose-cells-cloud-php/  
description: "Téléchargez l’Aspose.Cells Cloud PHP SDK (v24.3). Découvrez comment l’installer via Composer, s’authentifier, convertir XLSX en PDF/CSV, fusionner des classeurs, protéger des feuilles, et plus encore – le tout sans installer Office."  
keywords: "Aspose.Cells, Cloud, PHP, SDK, Excel, Convertir, Fusionner, Diviser, Protéger"  
weight: 30  
---

Le SDK est open source et publié sous la licence MIT. Vous pouvez accéder au code source de la bibliothèque PHP pour Aspose.Cells Cloud <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">ici</a>.

# **Comment utiliser Aspose.Cells Cloud SDK pour PHP**

Aspose.Cells Cloud SDK pour PHP est une bibliothèque puissante qui permet aux développeurs de manipuler et traiter des fichiers Microsoft Excel à l’aide du **langage de programmation PHP**. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans avoir à installer de logiciels ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser Aspose.Cells Cloud SDK pour PHP afin d’accomplir certaines tâches courantes, telles que la création d’un nouveau classeur Excel, l’insertion de données dans des cellules, et l’enregistrement du classeur modifié dans le cloud.

## Mise en route

Avant de pouvoir utiliser Aspose.Cells Cloud SDK pour **PHP**, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Reportez-vous à <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">cet article</a> sur le site Aspose pour obtenir votre identifiant client et votre secret client.

**Prérequis**

- PHP 7.4 ou version ultérieure  
- Composer installé sur votre machine de développement  
- Identifiant client et secret client Aspose Cloud valides  
- Accès à un emplacement de stockage Aspose Cloud (par défaut ou personnalisé)  

## Comment installer le package PHP pour Aspose.Cells Cloud

Vous pouvez installer Aspose.Cells Cloud SDK pour PHP. Voici les étapes à suivre :

- Ajoutez Aspose.Cells Cloud comme dépendance dans votre fichier `composer.json` :

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Exécutez la commande Composer pour installer le SDK :

   ```bash
   composer install
   ```

- Incluez l’autoloader de Composer dans votre code PHP :

   ```php
   require 'vendor/autoload.php';
   ```

## Comment utiliser le package PHP pour convertir Xlsx en d’autres formats

- Importez la bibliothèque Aspose.Cells Cloud  
  Commencez par importer le package nécessaire depuis le SDK PHP Aspose.Cells Cloud dans votre projet.

- Configurez le client API avec vos identifiants  
  Authentifiez votre client API à l’aide de votre identifiant client et de votre secret client uniques.

- Préparez les paramètres de conversion  
  Définissez les paramètres pour la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.

- Exécutez la conversion du classeur  
  Invoquez le processus de conversion à l’aide de la méthode `PostConvertWorkbook` et gérez la réponse.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### Référence API pour `PostConvertWorkbook`

| Paramètre      | Description                                           | Type   | Obligatoire |
|----------------|-------------------------------------------------------|--------|-------------|
| `file`         | Nom du fichier Excel source (par ex. `sample.xlsx`). | string | Oui         |
| `format`       | Format de sortie souhaité (`pdf`, `csv`, `png`, etc.). | string | Oui         |
| `storage`      | Nom du stockage ou chemin du dossier contenant le fichier source. | string | Non         |
| `outPath`      | Chemin facultatif pour enregistrer directement le fichier converti dans le stockage. | string | Non         |

**Méthode HTTP :** POST  
**Point de terminaison :** `/cells/convert/{format}`  

**Exemple de réponse (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**Codes d’état**

- `200` – Conversion réussie.  
- `400` – Requête incorrecte (paramètres manquants ou non valides).  
- `401` – Échec de l’authentification.  
- `500` – Erreur serveur.  
---