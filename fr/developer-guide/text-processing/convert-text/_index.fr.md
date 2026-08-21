---
title: "Aspose.Cells Cloud Web API – Convertir du texte en nombres dans Excel et nettoyer les caractères spéciaux"
second_title: "Document"
ArticleTitle: "Excel Data Cleaner – Convertir du texte en nombres et supprimer les caractères indésirables"
linktitle: "Convertir du texte"
type: docs
url: /convert-text/
keywords: "Aspose.Cells convertir du texte, texte Excel en nombres, supprimer les caractères spéciaux dans Excel, remplacer les sauts de ligne dans Excel, normaliser les caractères accentués, API de nettoyage de données Excel"
description: "Convertir des nombres au format texte en valeurs numériques, remplacer les caractères et sauts de ligne indésirables, et normaliser les caractères accentués dans des fichiers Excel à l’aide de l’API Aspose.Cells Cloud."
weight: 100
---

Nettoyez les données Excel en convertissant des nombres au format texte en valeurs numériques, en remplaçant les caractères et sauts de ligne indésirables, et en normalisant les caractères accentués en lettres standards à l’aide de l’API Aspose.Cells.

## Vue d’ensemble

**Convertir les nombres au format texte, éliminer les caractères indésirables, remplacer les accents – tout cela en une seule requête, sans formule.**

- **Convertir les nombres stockés en tant que texte en nombres** : transformer des données numériques stockées sous forme de texte en vrais nombres, garantissant ainsi des calculs précis et une représentation correcte des données.
- **Remplacer des caractères spécifiques** : remplacer toutes les occurrences de caractères spécifiés dans les cellules sélectionnées en une seule opération afin d’uniformiser vos données.
- **Convertir les sauts de ligne en espace, virgule ou point-virgule** : améliorer la lisibilité en remplaçant les sauts de ligne par des espaces, des virgules ou des points-virgules, offrant ainsi une présentation plus organisée et visuellement plus attrayante.
- **Remplacer les caractères accentués** : si vos données proviennent de différentes langues, vous pouvez remplacer les caractères accentués tels que « é » ou « ü » par leurs équivalents non accentués, ce qui améliore la cohérence et la clarté.

## API **ConvertText**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de requête de l’API **convertText**

| Nom du paramètre | Type   | Emplacement (Chemin / Chaîne de requête / Corps HTTP) | Description                                                                                                                                                         |
| ---------------- | ------ | ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | Le fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                           |
| convertTextType  | Chaîne  | Chaîne de requête                                     | Spécifie le type de conversion de texte à appliquer, par exemple convertir des nombres au format texte en valeurs numériques ou convertir des caractères accentués en leurs équivalents non accentués. |
| sourceCharacters | Chaîne  | Chaîne de requête                                     | Spécifie les caractères, chaînes ou motifs à remplacer ou supprimer du texte (par exemple : `"é,è,ê"`, `"#N/A"`, `"\\n"` pour les sauts de ligne).                 |
| targetCharacters | Chaîne  | Chaîne de requête                                     | Spécifie les caractères ou chaînes de remplacement destinés à remplacer les caractères sources (par exemple : `"e"` pour les lettres accentuées, `""` pour suppression, `" "` pour les sauts de ligne). |
| worksheet        | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ Le nom de la feuille de calcul sur laquelle la conversion de texte sera appliquée. Si omis, l’opération s’applique à la première feuille.         |
| range            | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ La plage de cellules sur laquelle la conversion de texte sera appliquée (par exemple : `"A1:C10"`). Si omis, l’opération s’applique à toutes les cellules utilisées de la feuille spécifiée. |
| outPath          | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ Le chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Si omis, le fichier est enregistré dans le dossier source.     |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Le nom du stockage cloud où le fichier de sortie sera stocké.                                                                                                     |
| region           | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ Définit la locale pour les règles de conversion de texte, particulièrement pertinente pour la gestion des caractères spécifiques aux langues (par exemple : `"en-US"`, `"fr-FR"`). |
| password         | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ Si le fichier de feuille de calcul uploadé est protégé par un mot de passe, fournir ce mot de passe pour l’ouvrir et le traiter.                   |

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

### Codes d’erreur

- **400 Bad Request** : URI d’API Aspose.Cells Cloud invalide.
- **401 Unauthorized** : Jeton d’accès invalide, ou ID client et secret invalides.
- **404 Not Found** : Le fichier de feuille de calcul n’est pas accessible.
- **500 Server Error** : Une anomalie s’est produite lors de l’obtention des données de calcul par le fichier de feuille de calcul.

## Où utiliser l’API Convert Text ?

- **Correction du format numérique** : convertir des nombres stockés en tant que texte (par exemple : « 123,45 ») en un format numérique adapté aux calculs.
- **Nettoyage des caractères spéciaux** : supprimer les symboles inutiles, les espaces supplémentaires ou les caractères invisibles des données.
- **Gestion des sauts de ligne** : remplacer les sauts de ligne dans les cellules par des espaces ou d’autres délimiteurs.
- **Normalisation des caractères accentués** : convertir les lettres accentuées (par exemple : « é », « ñ ») en lettres standard (« e », « n »).
- **Prétraitement des fichiers CSV** : standardiser le format texte avant l’importation des fichiers CSV dans Excel.

## Pourquoi utiliser l’API Convert Text ?

- **Conversion automatique de format** : convertir en masse des nombres au format texte en valeurs calculables en une seule requête.
- **Uniformisation des caractères** : gérer de manière uniforme les caractères spéciaux, les diacritiques et les problèmes d’encodage.
- **Cohérence des données** : garantir une uniformité complète du format texte sur l’ensemble du jeu de données.
- **Adapté aux développeurs** : Aspose.Cells Cloud propose des SDK dans plusieurs langages, facilitant un développement rapide et offrant une documentation complète. Comparé à la création de solutions de traitement de texte personnalisées, cela réduit considérablement la charge de développement.
- **Économique** : vous pouvez convertir du texte sans avoir à uploader préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de simplement implémenter la conversion de texte dans les cellules avec un minimum de code.  
Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---