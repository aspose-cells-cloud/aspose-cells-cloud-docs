---
title: "API Web Aspose.Cells Cloud de suppression des sous-chaînes dupliquées – Nettoyer le texte répété dans Excel"
second_title: "Document"
ArticleTitle: "Outil de suppression de sous-chaînes dupliquées dans Excel – Nettoyer le texte répété dans les cellules"
linktitle: "Supprimer les sous-chaînes dupliquées"
type: docs
url: /fr/remove-duplicate-substrings/
keywords: "Aspose.Cells, sous-chaînes dupliquées, API Excel, nettoyage de texte, cloud"
description: "Supprimez les sous-chaînes dupliquées dans les cellules Excel via l’API Aspose.Cells Cloud tout en conservant le formatage et les validations."
weight: 100
---

Supprimez les sous-chaînes dupliquées dans les cellules Excel grâce à une détection intelligente. Conservez le formatage original tout en éliminant le texte redondant à l’aide de l’API de déduplication d’Aspose.Cells.

## **Introduction** : Supprimer les caractères indésirables avec précision

L’API *Repeat Substring Cleaner* (nettoyeur de sous-chaînes répétées) supprime les sous-chaînes dupliquées dans les cellules individuelles d’une plage Excel, tout en conservant le formatage des cellules, la validation des données et les autres structures du classeur. Elle traite chaque cellule de façon indépendante, en ne conservant que la première occurrence de chaque sous-chaîne dupliquée.

### **Options de la source de données**

| Champ        | Type   | Obligatoire | Description                                                      |
| ------------ | ------ | ----------- | ---------------------------------------------------------------- |
| `workbook`   | fichier | Oui         | Fichier de classeur Excel (.xlsx, .xlsm)                        |
| `range`      | chaîne | Oui         | Plage cible à traiter (par ex. : "A1:D100", "Feuil1!A:D")       |

### **Options de délimiteur**

| Champ                                | Type    | Valeur par défaut | Description                                                                                                                                                 |
| ------------------------------------ | ------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                         | chaîne  | `"preset"`        | Options : `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break`, ou une chaîne de délimiteur personnalisée (plusieurs caractères sont traités comme un délimiteur composite) |
| `treatConsecutiveDelimitersAsOne`   | booléen | `false`           | Réduit les délimiteurs adjacents en un seul séparateur                                                                                                      |
| `caseSensitive`                      | booléen | `false`           | Détermine si la comparaison est sensible à la casse. Si `false`, la casse est ignorée lors de la détection des doublons.                                |

## **API RemoveDuplicateSubstrings**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête de l’API **RemoveDuplicateSubstrings**

| Nom du paramètre                | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                                       |
| :------------------------------ | :------ | :----------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | Fichier | FormData                                               | Fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                                            |
| delimiters                      | Chaîne  | Chaîne de requête                                      | Spécifie un ou plusieurs caractères délimiteurs utilisés pour découper le contenu des cellules en sous-chaînes, afin de détecter et supprimer les doublons. Plusieurs délimiteurs peuvent être spécifiés (par ex. `",;"`). |
| treatConsecutiveDelimitersAsOne | Booléen | Chaîne de requête                                      | Si défini à `true`, les caractères délimiteurs consécutifs sont traités comme un seul séparateur. Si `false`, chaque délimiteur est traité individuellement.                       |
| caseSensitive                   | Booléen | Chaîne de requête                                      | Si `true`, la détection des doublons tient compte de la casse (par ex. : "Texte" ≠ "texte"). Si `false`, la casse est ignorée lors de la comparaison des doublons.                |
| worksheet                       | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Nom de la feuille de calcul sur laquelle la suppression des sous-chaînes dupliquées sera appliquée. Si omis, l’opération s’applique à la première feuille.          |
| range                           | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Plage de cellules sur laquelle la suppression des sous-chaînes dupliquées sera appliquée (par ex. : `"A1:C10"`). Si omis, l’opération s’applique à toutes les cellules utilisées de la feuille spécifiée. |
| outPath                         | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Si omis, le fichier est enregistré dans le dossier source.                         |
| outStorageName                  | Chaîne  | Chaîne de requête                                      | Nom du stockage cloud dans lequel le fichier de sortie sera stocké.                                                                                                              |
| region                          | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Définit la locale pour le traitement du texte, ce qui peut affecter l’interprétation des délimiteurs et les règles de sensibilité à la casse pour certaines langues (par ex. : `"fr-FR"`, `"en-US"`). |
| password                        | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Si la feuille de calcul envoyée est protégée par un mot de passe, fournissez ce mot de passe pour ouvrir et traiter le fichier.                                    |

**Exemple de requête (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

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

### **Codes de statut**

| Code | Signification               | Description                                                                                     |
|------|-----------------------------|-------------------------------------------------------------------------------------------------|
| 200  | OK                          | La requête a abouti et le classeur traité est renvoyé.                                         |
| 202  | Accepté                     | La requête est acceptée pour traitement asynchrone.                                            |
| 400  | Requête incorrecte          | La requête est mal formée ou contient des paramètres invalides.                                |
| 401  | Non autorisé                | L’authentification a échoué ou le jeton est manquant/ invalide.                                |
| 404  | Non trouvé                  | Le classeur ou la ressource spécifiée est introuvable.                                        |
| 500  | Erreur interne du serveur   | Une erreur inattendue s’est produite côté serveur.                                             |

## Où utiliser l’API Remove Duplicate Substrings ?

- **Scénarios de nettoyage et de normalisation des données** : Nettoyer des tags comme `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **Données techniques et opérationnelles** : Nettoyer les entrées de journal avec des codes d’erreur répétés, supprimer les identifiants de bac/étagère redondants, etc.
- **Gestion de contenu et de médias** : Dé-dupliquer les tags de compétences, supprimer les entrées de certification redondantes.

## Pourquoi utiliser l’API Remove Duplicate Substrings ?

- **Automatisation des tâches manuelles** : Élimine les modifications fastidieuses et réduit les erreurs humaines.  
- **Préservation de l’intégrité des données** : Les couleurs, polices, bordures et mises en forme conditionnelles restent inchangées ; les listes déroulantes et les règles de validation sont conservées.  
- **Traitement flexible** : Indépendant des délimiteurs, avec contrôle optionnel de la sensibilité à la casse et protection des en-têtes.  
- **Adapté aux développeurs** : Aspose.Cells Cloud fournit des SDK dans plusieurs langages, permettant un développement rapide grâce à une documentation complète.  
- **Solution économique** : L’opération est exécutée dans le cloud, évitant la nécessité de stocker localement des fichiers intermédiaires.  

## Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK est le moyen optimal d’accélérer le développement. Les SDK gèrent les détails sous-jacents, vous permettant ainsi de mettre en œuvre simplement la suppression des sous-chaînes dupliquées dans les cellules avec un minimum de code. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

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