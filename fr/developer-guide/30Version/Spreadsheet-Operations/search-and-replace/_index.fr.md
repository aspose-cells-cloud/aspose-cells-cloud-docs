---
title: "Rechercher et remplacer du contenu texte dans des fichiers Excel"
second_title: "Documentation"
linktype: "Rechercher et remplacer"
type: docs
url: /fr/search-and-replace/
aliases: [  /fr/working-with-text/ , /fr/text/ ]
description: "Découvrez comment rechercher et remplacer du texte dans des classeurs et des feuilles de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut le format de requête, des exemples de code pour .NET, Java, Python et la gestion des erreurs."
keywords: "Aspose.Cells Cloud, Excel, recherche et remplacement, API REST, .NET, Java, Python"
weight: 20
ArticleTitle: "Rechercher et remplacer du texte dans des fichiers Excel à l’aide de l’API Aspose.Cells Cloud"
---

Les opérations sur le texte sont des processus complexes pour les fichiers Excel. De nombreux facteurs contribuent à cette complexité et doivent être pris en compte lors du traitement. Aspose.Cells Cloud fournit une méthode fiable pour rechercher et remplacer du texte dans une grande variété de formats de classeurs.

Travailler avec du texte dans des classeurs Excel nécessite souvent de localiser des chaînes spécifiques et de les mettre à jour sur plusieurs feuilles. L’API Aspose.Cells Cloud simplifie cette tâche en proposant une opération unifiée de **recherche et remplacement** fonctionnant sur n’importe quel format de classeur pris en charge.

## Vue d’ensemble

La fonctionnalité de recherche et remplacement permet de localiser des chaînes spécifiques dans un classeur ou une feuille de calcul particulière, puis de les remplacer par de nouvelles valeurs. Cette opération fonctionne avec tous les formats pris en charge par Aspose.Cells Cloud, notamment **XLS, XLSX, XLSM, XLSB, ODS, CSV**, et d’autres. Grâce à cette fonctionnalité, vous pouvez rapidement nettoyer vos données, corriger des fautes de frappe répétées ou appliquer des conventions de nommage en masse sur l’ensemble d’un classeur.

## Conditions préalables

- Un compte Aspose.Cloud actif avec un **Client‑Id** et un **Client‑Secret** valides.
- Un jeton d’accès obtenu via le flux d’authentification OAuth 2.0.
- Le classeur cible doit être stocké dans le stockage Aspose Cloud ou accessible via une URL publique.
- Le SDK requis doit être installé (par exemple, Aspose.Cells‑Cloud pour .NET, Java ou Python).

## Référence de l’API

**Méthode :** `POST`  
**Point de terminaison**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| Paramètre         | Type    | Obligatoire | Description                                                                              |
| ----------------- | ------- | ----------- | ---------------------------------------------------------------------------------------- |
| `fileName`        | string  | Oui         | Nom du classeur (avec extension).                                                        |
| `folder`          | string  | Non         | Chemin du dossier dans le stockage cloud.                                                |
| `storage`         | string  | Non         | Nom du stockage, si différent du stockage par défaut.                                   |
| `sheetName`       | string  | Non         | Nom de la feuille de calcul spécifique ; si omis, l’opération s’applique à l’ensemble du classeur. |
| `searchString`    | string  | Oui         | Texte à rechercher.                                                                      |
| `replaceString`   | string  | Oui         | Texte à utiliser pour remplacer les occurrences trouvées.                               |
| `ignoreCase`      | boolean | Non         | Définir sur `true` pour effectuer une recherche insensible à la casse.                  |
| `matchWholeCell`  | boolean | Non         | Définir sur `true` pour ne remplacer que les correspondances de cellules entières.     |

**En‑têtes**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**Corps de la requête (JSON)**

```json
{
  "searchString": "AncienneValeur",
  "replaceString": "NouvelleValeur",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Feuil1"
}
```

**Réponse réussie (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/classeurMisÀJour.xlsx"
}
```

## Formats pris en charge

| Format                                | Extension                 |
| ------------------------------------- | ------------------------- |
| Classeur Excel                        | .xls, .xlsx, .xlsm, .xlsb |
| Classeur OpenDocument                 | .ods                      |
| CSV                                   | .csv                      |
| Autres (selon la prise en charge par Aspose.Cells) | —                         |

## Exemples de code

Ci‑dessous figurent des exemples minimaux pour trois SDK populaires. Remplacez `{clientId}`, `{clientSecret}` et autres espaces réservés par vos propres valeurs réelles. Ces exemples illustrent comment effectuer une opération de **recherche et remplacement** par programmation.

## Gestion des erreurs et cas limites

| Code HTTP | Signification                                            | Action recommandée                                                  |
| --------- | -------------------------------------------------------- | ------------------------------------------------------------------- |
| 400       | Requête incorrecte – paramètres manquants ou non valides | Vérifiez les champs obligatoires et les types de données.         |
| 401       | Non autorisé – jeton invalide ou expiré                 | Actualisez le jeton d’accès.                                        |
| 404       | Introuvable – le classeur ou la feuille de calcul n’existe pas | Vérifiez le nom du fichier, le chemin du dossier et `sheetName`. |
| 415       | Type de support non pris en charge – format de fichier invalide | Assurez-vous que le fichier envoyé est au format Excel ou CSV pris en charge. |
| 202       | Accepté – requête acceptée pour traitement              | Interrogez l’état de l’opération si un traitement asynchrone est utilisé. |
| 204       | Aucun contenu – opération réussie, sans corps de réponse | Le remplacement a été appliqué ; aucune donnée supplémentaire renvoyée. |
| 500       | Erreur interne du serveur – défaillance inattendue      | Réessayez après un court délai ; contactez le support Aspose si le problème persiste. |

**Notes :**  
- Les classeurs volumineux peuvent dépasser les limites de taille de requête ; pensez à d’abord télécharger le fichier dans le stockage cloud.  
- Lorsque `ignoreCase` est défini sur `true`, notez que les correspondances de casse peuvent être affectées par les règles locales.  
- L’utilisation de `matchWholeCell` avec des formules ne remplacera pas les correspondances partielles à l’intérieur du texte de la formule.

## Rechercher et remplacer dans des fichiers Excel

- [Comment obtenir les éléments texte d’un classeur Excel.](/cells/workbook/get-text-items/)  
- [Comment obtenir les éléments texte d’une feuille de calcul Excel.](/cells/worksheets/get-text-items/)  
- [Comment rechercher du texte dans un classeur Excel.](/cells/workbook/find-text/)  
- [Comment rechercher du texte dans une feuille de calcul Excel.](/cells/worksheets/find-text/)  
- [Comment rechercher du texte dans des fichiers Excel sans télécharger le fichier.](/cells/search/)  
- [Comment remplacer du texte dans un classeur Excel.](/cells/workbook/replace-text/)  
- [Comment remplacer du texte dans une feuille de calcul Excel.](/cells/worksheets/replace-text/)  
- [Comment remplacer du texte dans des fichiers Excel sans télécharger le fichier.](/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Rechercher et remplacer du texte dans des fichiers Excel à l’aide de l’API Aspose.Cells Cloud",
  "description": "Documentation relative au point de terminaison de recherche et remplacement d’Aspose.Cells Cloud, incluant le format de requête, les paramètres, les exemples et la gestion des erreurs.",
  "url": "https://docs.aspose.cloud/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, recherche et remplacement, API, REST"
}
</script>