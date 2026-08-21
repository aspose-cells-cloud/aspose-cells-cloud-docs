---
title: "API Web Aspose.Cells Cloud pour supprimer des caractères par position – Supprimer du texte à des emplacements spécifiques dans Excel"
second_title: "Document"
articleTitle: "Supprimateur de caractères basé sur la position dans Excel – Supprimer du texte à des emplacements spécifiques – Shortcode en ligne"
linktitle: "Supprimer des caractères par position"
type: docs
url: /remove-characters-by-position/
keywords: "Aspose.Cells Cloud, supprimer des caractères par position, nettoyage de texte dans Excel, supprimer les N premiers caractères, supprimer les N derniers caractères, supprimer le texte avant un marqueur, supprimer le texte après un marqueur, suppression entre deux valeurs"
description: "Utilisez l’API Web Aspose.Cells Cloud pour supprimer des caractères dans des cellules Excel selon leur position : supprimez les N premiers/derniers caractères ou le texte avant/après des marqueurs spécifiques avec une grande précision."
weight: 100
---

Supprimez des caractères dans des cellules Excel selon leur position : supprimez les N premiers/derniers caractères, ou supprimez le texte avant/après des marqueurs spécifiés. Nettoyage précis du texte grâce à l’API Web Aspose.Cells Cloud.


## **Introduction** : Supprimer des caractères indésirables par position

**Modes de position**

- `theFirstNCharacters` – supprime les N caractères depuis le début
- `theLastNCharacters` – supprime les N caractères depuis la fin
- `allCharactersBeforeText` – supprime tout ce qui précède la première occurrence de la sous-chaîne fournie
- `allCharactersAfterText` – supprime tout ce qui suit la première occurrence
- `BetweenValues` – supprime la sous-chaîne (et éventuellement les délimiteurs eux-mêmes) située entre deux valeurs définies par l’utilisateur

**Options**

- `caseSensitive` – détermine si les recherches pour `BeforeText`, `AfterText` et `BetweenValues` sont sensibles à la casse

## **API RemoveCharactersByPosition**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une authentification basée sur <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête de l’API **RemoveCharactersByPosition**

| Nom du paramètre        | Type    | Emplacement (chemin/chaîne de requête Corps HTTP) | Description                                                                                                                                                             |
| ----------------------- | ------- | --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet             | Fichier | FormData                                            | Fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                                  |
| Authorization           | Chaîne  | En-tête                                             | Jeton « Bearer » pour l’authentification (obligatoire).                                                                                                                 |
| theFirstNCharacters     | Entier  | Chaîne de requête                                   | Nombre de caractères à supprimer depuis le début du texte dans chaque cellule sélectionnée (par exemple, `3` supprime les 3 premiers caractères).                     |
| theLastNCharacters      | Entier  | Chaîne de requête                                   | Nombre de caractères à supprimer depuis la fin du texte dans chaque cellule sélectionnée (par exemple, `2` supprime les 2 derniers caractères).                        |
| allCharactersBeforeText | Chaîne  | Chaîne de requête                                   | Supprime tous les caractères situés avant la chaîne de texte spécifiée dans chaque cellule. Si la chaîne apparaît plusieurs fois, la suppression porte sur la première occurrence. |
| allCharactersAfterText  | Chaîne  | Chaîne de requête                                   | Supprime tous les caractères situés après la chaîne de texte spécifiée dans chaque cellule. Si la chaîne apparaît plusieurs fois, la suppression porte sur la première occurrence. |
| worksheet               | Chaîne  | Chaîne de requête                                   | _(Facultatif)_ Nom de la feuille de calcul où la suppression de caractères sera appliquée. Si omis, l’opération s’applique à la première feuille.                     |
| range                   | Chaîne  | Chaîne de requête                                   | _(Facultatif)_ Plage de cellules où la suppression de caractères sera appliquée (par exemple, `"A1:C10"`). Si omis, l’opération s’applique à toutes les cellules utilisées dans la feuille spécifiée. |
| outPath                 | Chaîne  | Chaîne de requête                                   | _(Facultatif)_ Chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Si omis, le fichier est enregistré dans le dossier source.             |
| outStorageName          | Chaîne  | Chaîne de requête                                   | Nom du stockage cloud où le fichier de sortie sera stocké.                                                                                                             |
| region                  | Chaîne  | Chaîne de requête                                   | _(Facultatif)_ Définit la locale pour le traitement du texte, particulièrement utile pour les positions de caractères spécifiques aux langues et l’encodage (par exemple, `"en-US"`, `"zh-CN"`). |
| password                | Chaîne  | Chaîne de requête                                   | _(Facultatif)_ Si le fichier de feuille de calcul uploadé est protégé par mot de passe, fournir le mot de passe pour l’ouvrir et le traiter.                            |

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

- **200 OK** – La requête a réussi et le fichier traité est renvoyé.
- **400 Bad Request** : URI invalide pour l’API Aspose.Cells Cloud.
- **401 Unauthorized** : jeton d’accès invalide ou ID client/mot de passe invalide.
- **404 Not Found** : le fichier de feuille de calcul n’est pas accessible.
- **500 Server Error** : une anomalie est survenue dans la feuille de calcul lors de l’obtention des données de calcul.

## Où utiliser l’API Remove Characters by Position ?

- **Standardisation des données** : Nettoyer les codes produits (supprimer les zéros initiaux ou les suffixes), les numéros de téléphone (supprimer les codes pays)
- **Extraction de texte** : Extraire des informations clés à partir de fichiers journaux (supprimer les horodatages ou préfixes)
- **Traitement de fichiers** : Organiser les noms de fichiers (supprimer les préfixes ou suffixes de date uniformes)
- **Analyse de données** : Traiter du texte structuré (extraire le contenu entre crochets ou marqueurs spécifiques)
- **Gestion de base de données** : Nettoyer les données importées (supprimer les caractères fixes d’en-tête/de pied de page)

## Pourquoi utiliser l’API Remove Characters by Position ?

- **Précis et efficace** : La suppression directe par position élimine le besoin d’expressions régulières complexes.
- **Configuration flexible** : Cinq modes de positionnement plus une option de sensibilité à la casse couvrent de nombreux scénarios.
- **Traitement par lots** : Nettoyer des colonnes entières en une seule requête, augmentant l’efficacité jusqu’à 10 fois.
- **Analyse intelligente** : Facilite l’extraction de contenu située entre deux délimiteurs.
- **Facile à utiliser pour les développeurs** : Aspose.Cells Cloud fournit des SDK pour de nombreux langages, accélérant le développement et offrant une documentation complète. Comparé à la création de logique personnalisée de traitement de texte, cela réduit considérablement la charge de développement.
- **Économique** : Les caractères peuvent être supprimés sans avoir à uploader préalablement le classeur, économisant de l’espace de stockage et réduisant les coûts.

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK est le moyen optimal d’accélérer le développement. Les SDK gèrent les détails sous-jacents, vous permettant d’implémenter simplement la suppression de caractères par position dans les cellules avec un minimum de code.  
Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---