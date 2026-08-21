---
title: "Informations sur le fichier"
second_title: "Document"
linktitle: "Informations sur le fichier"
type: docs
url: /fr/file-info/
keywords: "Fichier, Informations, Excel, Aspose.Cells, API Cloud, Métadonnées, Base64"
description: "Récupérer le nom, la taille et le contenu Base64 d’un fichier Excel à l’aide de l’API Aspose.Cells Cloud. Inclut la syntaxe des requêtes, du code d’exemple et la gestion des erreurs."
weight: 79
ArticleTitle: "Informations sur le fichier – Métadonnées et contenu Base64 d’un fichier Excel (API Aspose.Cells Cloud)"
---

## Propriétés de FileInfo


| Nom               | Type   | Description                                               |
| ----------------- | ------ | --------------------------------------------------------- |
| **FileName**      | string | Le nom du fichier, y compris son extension.               |
| **FileSize**      | long   | La taille du fichier en octets.                           |
| **FileContent**   | string | Contient les données brutes du fichier Excel codées en Base64. |

La réponse est renvoyée au format JSON avec les trois mêmes propriétés indiquées dans le tableau ci-dessus, par exemple :

```json
{
  "FileName": "MonClasseur.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### Erreurs

| Code HTTP | Signification                | Moment de survenue                          |
| --------- | ---------------------------- | ------------------------------------------- |
| 200       | OK – requête réussie.        | Réponse normale.                            |
| 401       | Non autorisé                 | Jeton d’authentification manquant ou invalide. |
| 404       | Introuvable                  | Le fichier spécifié n’existe pas.           |
| 500       | Erreur interne du serveur    | Échec inattendu côté serveur.               |

Pour chaque erreur, assurez-vous que le jeton d’authentification est valide (401), vérifiez le chemin du fichier (404) ou consultez le guide général de gestion des erreurs pour des stratégies de nouvelle tentative (500).

## Voir aussi

- [Obtenir un classeur](https://docs.aspose.cloud/cells/get-workbook) – récupérer un objet classeur et ses feuilles de calcul.  
- [Télécharger un fichier](https://docs.aspose.cloud/cells/download-file) – télécharger les octets bruts du fichier sans codage Base64.  
- [Vue d’ensemble de l’authentification](https://docs.aspose.cloud/cells/authentication) – comment obtenir et utiliser des jetons d’accès.  
---