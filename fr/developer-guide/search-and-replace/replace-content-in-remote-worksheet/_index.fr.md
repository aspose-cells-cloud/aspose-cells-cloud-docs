---
title: "Aspose.Cells Cloud – API Web de remplacement – Mettre à jour le texte dans une feuille de calcul distante"
second_title: "Document"
articleTitle: "Rechercher et remplacer du texte dans une feuille de calcul distante avec l’API Aspose.Cells Cloud"
linktitle: "Remplacer le contenu d’une feuille de calcul distante"
type: docs
url: /fr/replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, remplacer du texte, feuille de calcul distante, API Excel, feuille de calcul cloud, recherche et remplacement, API REST"
description: "Remplacer du texte dans une feuille de calcul spécifique d’un fichier Excel stocké dans Aspose Cloud. Prend en charge les classeurs protégés par mot de passe, la recherche sensible à la région et les mises à jour en masse."
weight: 100
---

Remplacer du texte spécifié dans une feuille de calcul spécifique de fichiers Excel distants. Mettez à jour efficacement le contenu des feuilles de calcul ciblées à l’aide de l’API Aspose.Cells Rechercher et Remplacer pour un édition précise des feuilles de calcul.

## **API de remplacement du contenu d’une feuille de calcul distante**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Chemin / Chaîne de requête / Corps HTTP | Description                                                                                                                                                                  |
| :--------------- | :----- | :--------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Chemin                                   | Nom du fichier de classeur stocké dans le stockage cloud à modifier (par ex. `"rapport_ventes.xlsx"`, `"budget_2024.xls"`).                                               |
| worksheet        | String | Chemin                                   | Nom de la feuille de calcul spécifique dans laquelle l’opération de recherche et remplacement sera effectuée (par ex. `"Ventes_T1"`, `"Feuille1"`).                       |
| searchText       | String | Chaîne de requête                        | Chaîne de texte à rechercher dans la feuille de calcul spécifiée. La recherche s’applique à toutes les cellules de la feuille de calcul, sauf si elle est davantage limitée. |
| replaceText      | String | Chaîne de requête                        | Chaîne de texte qui remplacera toutes les occurrences de `searchText` trouvées dans la feuille de calcul spécifiée.                                                       |
| folder           | String | Chaîne de requête                        | Chemin du dossier dans le stockage cloud où le classeur source est situé (par ex. `"/rapports/mensuels/"`, `"/finance/"`).                                                 |
| storageName      | String | Chaîne de requête                        | _(Facultatif)_ Nom du stockage cloud personnalisé (par ex. `"CorporateS3"`, `"AzureArchive"`). Si omis, le stockage cloud par défaut de votre compte est utilisé.         |
| region           | String | Chaîne de requête                        | _(Facultatif)_ Définit la locale pour la gestion du texte, ce qui peut affecter l’encodage des caractères et le comportement de recherche spécifique à la langue dans la feuille de calcul (par ex. `"fr-FR"`, `"en-US"`). |
| password         | String | Chaîne de requête                        | _(Facultatif)_ Si le classeur est protégé par mot de passe, fournissez le mot de passe pour ouvrir et modifier le fichier.                                                 |

**Exemple de requête (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/rapport_ventes.xlsx/worksheets/Feuille1/replace/content?searchText=AncienneValeur&replaceText=NouvelleValeur&folder=/rapports" \
     -H "Authorization: Bearer {access_token}"
```

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### **Codes d’erreur**

| Code | Description                              | Quand cela se produit                                              |
|------|------------------------------------------|--------------------------------------------------------------------|
| 400  | Mauvaise requête                         | L’URI de la requête est mal formée ou les paramètres requis sont absents. |
| 401  | Non autorisé                             | Le jeton d’accès est manquant, invalide ou les identifiants client sont incorrects. |
| 404  | Introuvable                              | Le classeur ou la feuille de calcul spécifié ne peut être trouvé. |
| 500  | Erreur interne du serveur                | Une erreur inattendue s’est produite lors du traitement de la requête. |

## Où utiliser l’API de remplacement du contenu d’une feuille de calcul dans une feuille de calcul distante ?

- **Mise à jour en masse de fichiers cloud** : Modifier le contenu de plusieurs fichiers Excel stockés dans un stockage cloud tel qu’AWS S3 ou Azure Blob.
- **Remplissage dynamique de modèles cloud** : Remplir en lot des données dynamiques pour des modèles de rapports stockés dans le cloud.
- **Synchronisation inter-régions des fichiers** : Synchroniser la cohérence du contenu des fichiers Excel dans le stockage cloud entre différentes régions géographiques.

## Pourquoi utiliser l’API de remplacement du contenu d’une feuille de calcul dans une feuille de calcul distante ?

- **Adaptée aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide et accompagnée d’une documentation complète. Comparé à la création de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Réduction des coûts en personnel** : Diminue la nécessité de personnel dédié à la consolidation de documents.
- **Paiement à l’usage** : Aucun investissement initial ; vous ne payez que pour les appels API effectivement utilisés.
- **Coûts de maintenance nuls** : Aucune nécessité de maintenir des serveurs, de mettre à jour des logiciels ou de gérer des problèmes de compatibilité.

## Comment utiliser l’API de remplacement du contenu d’une feuille de calcul dans une feuille de calcul distante à l’aide des SDK

### **Spécification OpenAPI**

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) définit une interface de programmation accessible publiquement et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

### **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant simplement d’implémenter le remplacement du contenu d’une feuille de calcul dans des classeurs avec un minimum de code.  
Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :