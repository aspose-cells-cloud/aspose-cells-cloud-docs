---
title: "Options d'enregistrement"
second_title: "Document"
linktitle: "Options d'enregistrement"
type: docs
url: /fr/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Classeur, API REST, Formats de fichiers, PDF, CSV, JSON, Compression HTTP, Cache de graphiques, Noms de plages, Création de répertoires"
description: "Décrit les propriétés SaveOptions de l'API REST Aspose.Cells Cloud, permettant aux développeurs de configurer le comportement d'enregistrement des classeurs pour plusieurs formats de fichiers et options telles que la compression HTTP, l'actualisation du cache de graphiques et la création automatique de répertoires."
weight: 79
ArticleTitle: "Options d'enregistrement – Documentation de l'API REST Aspose.Cells Cloud"
---

# Propriétés SaveOptions

Les SaveOptions vous permettent de contrôler la manière dont un classeur est enregistré lors de l'utilisation de l'API REST Aspose.Cells Cloud. En configurant ces options, vous pouvez activer la compression HTTP, spécifier le format de fichier cible, gérer le stockage temporaire et contrôler des comportements supplémentaires tels que l'actualisation du cache de graphiques et la création automatique de répertoires.

**Prérequis**  
- Une session Aspose.Cells Cloud authentifiée (OAuth 2.0 ou JWT).  
- Le classeur cible doit être chargé ou créé via l'API avant l'enregistrement.

| Nom                        | Type       | Description                                                                                              | Notes      |
| -------------------------- | ---------- | -------------------------------------------------------------------------------------------------------- | ---------- |
| **EnableHTTPCompression**  | **bool?**  | Active la compression HTTP pour la réponse.                                                              | [optionnel] |
| **SaveFormat**             | **string** | Spécifie le format de fichier cible pour l’enregistrement du classeur.                                  | [optionnel] |
| **ClearData**              | **bool?**  | Vide le classeur après l’enregistrement du fichier.                                                      | [optionnel] |
| **CachedFileFolder**       | **string** | Le dossier de fichiers mis en cache utilisé pour stocker temporairement de grandes quantités de données. | [optionnel] |
| **ValidateMergedAreas**    | **bool?**  | Indique s’il faut valider les zones fusionnées avant l’enregistrement du fichier. La valeur par défaut est false. | [optionnel] |
| **RefreshChartCache**      | **bool?**  | Actualise les données du cache des graphiques avant l’enregistrement.                                    | [optionnel] |
| **CreateDirectory**        | **bool?**  | Si la valeur est true et que le répertoire n’existe pas, il est automatiquement créé avant l’enregistrement du fichier. | [optionnel] |
| **SortNames**              | **bool?**  | Trie les noms de plages par ordre alphabétique lors de l’enregistrement.                                 | [optionnel] |

**Requête**  
- **Méthode :** `POST` (ou `PUT`, selon l’opération)  
- **Point de terminaison :** `/cells/workbook/save`  
- **En-têtes :**  
  - `Authorization: Bearer <jeton_d_accès>`  
  - `Content-Type: application/json`  
- **Corps :** Représentation JSON du modèle `SaveOptions` (tableau ci-dessus), combinée aux données ou à la référence du classeur.

**Exemple de réponse**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "Le classeur a été enregistré avec succès."
}
```

**Codes d’état HTTP**

| Code | Signification               | Description                                                     |
|------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant.                              |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue.                                      |

**Notes / Remarques**  
- Lorsque **CreateDirectory** est défini sur `true`, l’API crée automatiquement le dossier cible s’il n’existe pas déjà.  
- L’activation de **EnableHTTPCompression** peut réduire la taille de la charge utile pour les classeurs volumineux, mais le client doit prendre en charge le décodage gzip/deflate.  
- **RefreshChartCache** doit être utilisé lorsque les graphiques reposent sur des données dynamiques qui ont pu changer depuis la génération du classeur.