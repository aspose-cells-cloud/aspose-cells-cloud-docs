---
title: "Travail avec les images Excel"
second_title: "Document"
linktitle: "Images"
type: docs
url: /fr/pictures/
aliases: [  /fr/working-with-pictures/ ]
keywords: "Excel, image, Aspose.Cells Cloud, API REST, gestion d'images, images Excel"
description: "Découvrez comment récupérer, ajouter, mettre à jour et supprimer des images dans les feuilles de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut des exemples de code en C#, Java, Python, et plus encore."
weight: 100
ArticleTitle: "Travail avec les images Excel – Documentation Aspose.Cells Cloud"
---

## Travail avec des images dans un fichier Excel

Ce guide explique comment manipuler les **images** (également appelées illustrations) dans les feuilles de calcul Excel via l'API REST Aspose.Cells Cloud. Il couvre les principales opérations liées aux images — récupération, ajout, mise à jour et suppression d'images Excel — et vous oriente vers des exemples détaillés pour chaque tâche.

**Prérequis** : un compte Aspose.Cells Cloud, une clé API valide, et le SDK approprié installé pour le langage de votre choix.

- [Comment obtenir une image spécifique d’une feuille de calcul Excel.](/cells/pictures/get/) – Récupérer une seule image dans le format demandé (PNG, JPEG, etc.) à partir d’une feuille de calcul.  
- [Comment obtenir toutes les informations relatives aux images d’une feuille de calcul Excel.](/cells/pictures/get-all/) – Lister les métadonnées de chaque image contenue dans une feuille de calcul.  
- [Comment ajouter une image à une feuille de calcul Excel.](/cells/pictures/add/) – Insérer une nouvelle image dans une feuille de calcul, en spécifiant sa position et sa taille.  
- [Comment mettre à jour une image spécifique d’une feuille de calcul Excel.](/cells/pictures/update/) – Modifier les propriétés (par exemple, dimensions, position) d’une image existante.  
- [Comment supprimer toutes les images d’une feuille de calcul Excel.](/cells/pictures/clear/) – Supprimer tous les objets image d’une feuille de calcul en une seule opération.  
- [Comment supprimer une image d’une feuille de calcul Excel.](/cells/pictures/delete/) – Supprimer une seule image identifiée par son index.  

**Référence de l'API**

**Obtenir une image dans un format spécifique**

| Méthode HTTP | Endpoint | Paramètres requis | Exemple de requête | Exemple de réponse | Codes de statut |
|-------------|----------|-------------------|-------------------|------------------|----------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (chemin), `sheetName` (chemin), `pictureIndex` (chemin), `format` (paramètre de requête) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | Données binaires de l’image (PNG, JPEG, etc.) | 200 OK, 400 Requête incorrecte, 401 Non autorisé, 404 Non trouvé, 500 Erreur serveur |

**Obtenir toutes les informations relatives aux images**

| Méthode HTTP | Endpoint | Paramètres requis | Exemple de requête | Exemple de réponse | Codes de statut |
|-------------|----------|-------------------|-------------------|------------------|----------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (chemin), `sheetName` (chemin) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | Tableau JSON contenant les métadonnées des images (index, nom, position, taille) | 200 OK, 400, 401, 404, 500 |

**Ajouter une image**

| Méthode HTTP | Endpoint | Paramètres requis | Corps de la requête d’exemple | Exemple de réponse | Codes de statut |
|-------------|----------|-------------------|------------------------------|------------------|----------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (chemin), `sheetName` (chemin) | `{ "image": "<image-encodée-en-base64>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Créé, 400, 401, 404, 500 |

**Mettre à jour une image**

| Méthode HTTP | Endpoint | Paramètres requis | Corps de la requête d’exemple | Exemple de réponse | Codes de statut |
|-------------|----------|-------------------|------------------------------|------------------|----------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (chemin), `sheetName` (chemin), `pictureIndex` (chemin) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Supprimer toutes les images**

| Méthode HTTP | Endpoint | Paramètres requis | Exemple de requête | Exemple de réponse | Codes de statut |
|-------------|----------|-------------------|-------------------|------------------|----------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (chemin), `sheetName` (chemin) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "Toutes les images ont été supprimées." }` | 200 OK, 400, 401, 404, 500 |

**Supprimer une image spécifique**

| Méthode HTTP | Endpoint | Paramètres requis | Exemple de requête | Exemple de réponse | Codes de statut |
|-------------|----------|-------------------|-------------------|------------------|----------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (chemin), `sheetName` (chemin), `pictureIndex` (chemin) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Image supprimée." }` | 200 OK, 400, 401, 404, 500 |

**Sujets connexes**

Explorez d'autres opérations liées aux images dans Aspose.Cells Cloud :  
- [Travail avec les formes](/cells/shapes/) – ajouter, modifier et supprimer des formes graphiques.  
- [Travail avec les graphiques](/cells/charts/) – créer et manipuler des objets graphiques.  
- [Travail avec les images dans les feuilles de calcul](/cells/images/) – intégrer et gérer des fichiers image bruts.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Travail avec les images Excel – Documentation Aspose.Cells Cloud",
  "description": "Guide pour récupérer, ajouter, mettre à jour et supprimer des images Excel via l'API REST Aspose.Cells Cloud.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "images Excel, Aspose.Cells Cloud, API REST, gestion d'images",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>