---
title: "Aspose.Cells Cloud Remove Characters Web API – Supprimer des caractères personnalisés et des sous‑chaînes d’Excel (Short‑Code en ligne)"
second_title: "Document"
ArticleTitle: "Nettoyeur de texte Excel – Supprimer des caractères et des sous‑chaînes dans une plage sélectionnée"
linktype: "docs"
url: /remove-characters/
keywords: "Aspose.Cells, supprimer des caractères, API Excel, nettoyage de texte, feuille de calcul"
description: "Supprimer des caractères personnalisés, des jeux de caractères et des sous‑chaînes des cellules Excel d’une plage sélectionnée. Supprimer du texte à des positions spécifiques à l’aide de l’API Aspose.Cells pour un nettoyage de données précis."
weight: 100
---

Nettoyez vos données Excel en supprimant des caractères personnalisés, des jeux de caractères ou des sous‑chaînes d’une plage de cellules sélectionnée. Supprimez du texte à des positions précises à l’aide de l’API Aspose.Cells pour un formatage de données précis.

## Introduction

Nettoyez et standardisez facilement vos données Excel en supprimant des caractères spécifiques indésirables. Notre complément propose plusieurs méthodes ciblées pour assainir vos cellules :

- **Supprimer des caractères personnalisés**  
  Supprimez n’importe quels symboles spécifiques que vous définissez. Il suffit d’entrer chaque caractère dans le champ, et le complément supprimera instantanément toutes les occurrences dans les cellules sélectionnées. Idéal pour éliminer des délimiteurs uniques, des fautes de frappe ou des marques spéciales.

- **Supprimer des jeux de caractères (nettoyage en masse)**
  - **Caractères non imprimables** – Nettoyez vos données des caractères invisibles qui perturbent l’analyse et le formatage (sauts de ligne, retours chariot, tabulations et autres caractères de contrôle tels que ASCII 0‑31, 127, 129, 141, 143, 144, 157).
  - **Caractères textuels (toutes les lettres)** – Isolez les nombres et symboles en supprimant toutes les lettres (A‑Z, a‑z) de la plage sélectionnée.
  - **Caractères numériques (tous les chiffres)** – Extraisez du texte pur en supprimant tous les chiffres (0‑9), idéal pour nettoyer des noms de produits ou descriptions textuelles.
  - **Symboles** – Supprimez un large éventail de symboles parasites, notamment mathématiques (ex. : ±, √), géométriques (ex. : ∆, °), techniques, monétaires (ex. : £, ¢) et symboliques ressemblant à des lettres (ex. : ™, ®, ©).
  - **Signes de ponctuation** – Obtenir un texte propre et sans ponctuation en supprimant tous les signes de ponctuation tels que points, virgules, guillemets et tirets.

- **Supprimer une sous‑chaîne spécifique**  
  Allez au‑delà des caractères simples et supprimez des mots entiers ou des séquences spécifiques de caractères. Éliminez sans effort les préfixes, suffixes courants ou toute expression textuelle redondante de vos jeux de données.

**Version 4.0 – Mise à jour du 2024‑11‑15**

## API RemoveCharacters

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de requête

| Nom du paramètre | Type   | Emplacement           | Description                                                                                                                                                                                                                      |
| ---------------- | ------ | --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | File   | FormData              | Le fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                                                                                        |
| removeTextMethod | String | Query                 | Spécifie la méthode de suppression de texte. Options : `None`, `RemoveCustomCharacter`, `RemoveCharacterSets`, `RemoveSubString`. Par défaut : `None`.                                                                           |
| characterSets    | String | Query                 | Jeu(x) de caractères prédéfini(s) à supprimer lorsque `RemoveCharacterSets` est sélectionné. Options : `NonPrintingCharacters`, `TextCharacters`, `NumericCharacters`, `Symbols`, `PunctuationMarks`. Plusieurs jeux peuvent être combinés par des virgules. |
| removeCustomValue | String | Query              | Caractère(s) personnalisé(s) ou sous‑chaîne(s) à supprimer lors de l’utilisation de `RemoveCustomCharacter` ou `RemoveSubString`.                                                                                               |
| worksheet        | String | Query _(facultatif)_  | Le nom de la feuille de calcul où la suppression de texte sera appliquée. **Si omis, l’API traite la première feuille du classeur.**                                                                                           |
| range            | String | Query _(facultatif)_  | La plage de cellules où la suppression de texte sera appliquée (ex. : `"A1:C10"`). **Si omis, l’opération s’applique à toutes les cellules utilisées de la feuille spécifiée.**                                                  |
| outPath          | String | Query _(facultatif)_  | Chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Si omis, le fichier est enregistré dans le dossier source.                                                                                      |
| outStorageName   | String | Query _(facultatif)_  | Nom du stockage cloud où le fichier de sortie sera stocké.                                                                                                                                                                      |
| region           | String | Query _(facultatif)_  | Définit la locale pour les définitions des jeux de caractères (ex. : `"en-US"`, `"ja-JP"`).                                                                                                                                      |
| password         | String | Query _(facultatif)_  | Mot de passe pour un classeur protégé, le cas échéant.                                                                                                                                                                           |

### Réponse

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

### Codes d’erreur

- **400 Bad Request** – URI de l’API Aspose.Cells Cloud invalide.
- **401 Unauthorized** – Jeton d’accès invalide, ou ID client et secret incorrects.
- **404 Not Found** – Le fichier de feuille de calcul n’est pas accessible.
- **500 Server Error** – La feuille de calcul a rencontré une anomalie lors de l’obtention des données de calcul.

## Où utiliser l’API Remove Characters ?

- **Import/Export de données** – Nettoyez les CSV ou données importés en supprimant les caractères invisibles et les erreurs de formatage.
- **Gestion de bases de données** – Standardisez les codes produits, ID et noms en supprimant les symboles ou signes de ponctuation indésirables.
- **Analyse financière** – Extraire des nombres purs en supprimant les symboles monétaires et les caractères textuels.
- **Traitement de texte** – Supprimer les sauts de ligne et tabulations pour une analyse et un rapport textuels propres.
- **Gestion des stocks** – Nettoyer les noms de produits en éliminant les préfixes ou suffixes redondants.

## Pourquoi utiliser l’API Remove Characters ?

- **Gagner du temps** – Supprimez instantanément plusieurs types de caractères en bloc, contrairement au nettoyage manuel.
- **Garantir la précision** – Éliminez les caractères cachés responsables d’erreurs d’analyse et de problèmes de formatage.
- **Standardiser les données** – Obtenez un formatage cohérent à travers les jeux de données et les systèmes.
- **Améliorer l’analyse** – Obtenez des données propres et prêtes à l’analyse en isolant nombres ou texte selon les besoins.
- **Corriger les erreurs d’import** – Supprimez les caractères problématiques qui interrompent les bases de données et les formules.
- **Adapté aux développeurs** – Aspose.Cells Cloud fournit des bibliothèques SDK dans plusieurs langages, permettant un développement rapide avec une documentation complète. Comparé à la création de solutions sur mesure, cela réduit considérablement la charge de développement.
- **Économique** – Supprimez des caractères sans avoir à télécharger préalablement le classeur, économisant ainsi de l’espace de stockage et réduisant les coûts.

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK constitue la meilleure manière d’accélérer le développement. Les SDK gèrent les détails sous‑jacent, vous permettant d’implémenter la fonctionnalité **Remove Characters** pour les cellules avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}

---