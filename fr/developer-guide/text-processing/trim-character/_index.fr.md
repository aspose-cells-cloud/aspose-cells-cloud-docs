---
title: "Aspose.Cells Cloud Text Trimming Web API – Supprimer les espaces et sauts de ligne supplémentaires"
second_title: "Document"
ArticleTitle: "Nettoyeur de données Excel – Supprimer automatiquement les caractères, les espaces et les sauts de ligne – En ligne, avec shortcode"
linktitle: "Suppression de caractères"
type: docs
url: /fr/trim-character/
keywords: "Excel, suppression de texte, suppression d’espaces, sauts de ligne, Aspose.Cells, nettoyage de données, feuille de calcul, normalisation du formatage des cellules"
description: "Supprimez les espaces, sauts de ligne et caractères indésirables supplémentaires des cellules Excel à l’aide de l’API Aspose.Cells Cloud. Assurez-vous que vos données de feuille de calcul soient propres et cohérentes."
weight: 100
---

Supprimez automatiquement les caractères inutiles, les espaces superflus et les sauts de ligne des cellules Excel à l’aide de l’API Aspose.Cells Trim Character. Nettoyez vos entrées de données et maintenez une mise en forme cohérente dans vos feuilles de calcul.

## **Vue d’ensemble**

- **Suppression des espaces en début et en fin**
  - Supprime les espaces superflus au début et à la fin du texte
  - Améliore l’aspect, la propreté et la lisibilité des données
- **Traitement des espaces supplémentaires entre les mots**
  - Élimine les espaces superflus entre les mots
  - Résout les problèmes de formatage causés par des données provenant de plusieurs sources

- **Suppression des espaces spéciaux**
  - Supprime clairement les espaces insécables
  - Garantit l’exactitude et la cohérence des données

- **Gestion des sauts de ligne**
  - Supprime les sauts de ligne supplémentaires ou tous les sauts de ligne
  - Maintient le contenu des cellules organisé et professionnel

## **API TrimCharacter**

Avant d’appeler l’API, assurez-vous d’avoir un compte Aspose Cloud valide, un `client_id`/`client_secret` et un jeton d’accès portant la portée **Cells**.

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de requête de l’API **trimCharacter**

| Nom du paramètre        | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                         |
| :---------------------- | :------ | :----------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet             | Fichier | FormData                                               | Le fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                          |
| trimContent             | Chaîne  | Chaîne de requête                                       | Spécifie les caractères ou chaînes spécifiques à supprimer du contenu des cellules. Peut s’agir d’un seul caractère, de plusieurs caractères ou d’un motif personnalisé. |
| trimLeading             | Booléen | Chaîne de requête                                       | Si `true`, supprime les caractères spécifiés au début du contenu de chaque cellule.                                                                               |
| trimTrailing            | Booléen | Chaîne de requête                                       | Si `true`, supprime les caractères spécifiés à la fin du contenu de chaque cellule.                                                                                |
| trimSpaceBetweenWordTo1 | Booléen | Chaîne de requête                                       | Si `true`, réduit plusieurs espaces consécutifs entre mots à un seul espace dans chaque cellule.                                                                  |
| trimNonBreakingSpaces   | Booléen | Chaîne de requête                                       | Si `true`, supprime les caractères d’espace insécable (Unicode U+00A0) du contenu des cellules.                                                                   |
| removeExtraLineBreaks   | Booléen | Chaîne de requête                                       | Si `true`, réduit plusieurs sauts de ligne consécutifs à un seul saut de ligne dans chaque cellule.                                                               |
| removeAllLineBreaks     | Booléen | Chaîne de requête                                       | Si `true`, supprime tous les caractères de saut de ligne du contenu des cellules.                                                                                 |
| worksheet               | Chaîne  | Chaîne de requête                                       | _(Optionnel)_ Le nom de la feuille de calcul sur laquelle la suppression de texte sera appliquée. Si omis, l’opération s’applique à la première feuille.          |
| range                   | Chaîne  | Chaîne de requête                                       | _(Optionnel)_ La plage de cellules sur laquelle la suppression de texte sera appliquée (par ex. `"A1:C10"`). Si omis, l’opération s’applique à toutes les cellules utilisées de la feuille spécifiée. |
| outPath                 | Chaîne  | Chaîne de requête                                       | _(Optionnel)_ Le chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Si omis, le fichier est enregistré dans le dossier source.        |
| outStorageName          | Chaîne  | Chaîne de requête                                       | Le nom du stockage cloud dans lequel le fichier de sortie sera enregistré.                                                                                        |
| region                  | Chaîne  | Chaîne de requête                                       | _(Optionnel)_ Définit la localisation pour le traitement du texte, ce qui peut affecter la gestion des espaces et sauts de ligne selon la langue (par ex. `"fr-FR"`, `"ar-SA"`). |
| password                | Chaîne  | Chaîne de requête                                       | _(Optionnel)_ Si la feuille de calcul importée est protégée par mot de passe, fournissez le mot de passe pour l’ouvrir et la traiter.                               |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Exemple de réussite (HTTP 200) :** L’API renvoie un flux de fichier contenant le classeur nettoyé.

### Codes d’erreur

- **400 Bad Request** : URI d’API Aspose.Cells Cloud invalide.
- **401 Unauthorized** : Jeton d’accès invalide ou identifiant client / secret invalide.
- **404 Not Found** : Le fichier de feuille de calcul est inaccessible.
- **500 Server Error** : Une anomalie s’est produite lors de l’obtention des données de calcul dans la feuille de calcul.

## Où utiliser l’API Trim Character ?

- **Normalisation des entrées utilisateur** : Nettoyer les données de tables saisies manuellement, en supprimant les espaces et sauts de ligne superflus.
- **Maintenance de bases de clients** : Nettoyer les espaces redondants et les problèmes de mise en forme dans les noms, adresses et coordonnées des clients.
- **Nettoyage automatique des rapports** : Nettoyer le formatage des sources de données avant la génération de rapports automatisés.
- **Préparation à la migration de données** : Corriger les problèmes de formatage avant la migration des données vers le nouveau système.

## Pourquoi utiliser l’API Trim Character ?

- **Réduction des coûts de main-d’œuvre** : Élimine les tâches manuelles chronophages de nettoyage de données.
- **Réduction des coûts d’erreur** : Évite les erreurs d’analyse causées par des problèmes de formatage.
- **Payant à l’utilisation** : Aucune frais fixes, seul le débit réel est facturé.
- **Aucun investissement en infrastructure** : Aucune nécessité de maintenir des serveurs ou des logiciels.
- **Support multi-formats** : Prend en charge le traitement de plusieurs formats tels que XLSX, XLS, CSV, ODS, etc.
- **Adapté aux développeurs** : Aspose.Cells Cloud propose des SDK dans plusieurs langages, permettant un développement rapide et accompagné d’une documentation complète. Comparé à la création de solutions personnalisées de rendu graphique, cela réduit considérablement la charge de travail de développement.
- **Économique** : Vous pouvez supprimer les caractères redondants sans d’abord uploader le classeur, ce qui économise de l’espace de stockage et réduit les coûts.

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK est le meilleur moyen d’accélérer le développement. Les SDK gèrent les détails sous-jacents, vous permettant d’implémenter simplement la fonctionnalité de suppression de caractères dans les cellules avec un minimum de code.
Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}