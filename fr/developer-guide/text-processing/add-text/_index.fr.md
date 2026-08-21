---
title: "Aspose.Cells Cloud API AddText – Ajouter du texte à plusieurs cellules Excel simultanément – Insérer des préfixes, suffixes et libellés"
second_title: "Document"
ArticleTitle: "Insertion groupée de texte dans Excel – Ajouter des préfixes, suffixes et texte personnalisé aux cellules – Guide étape par étape"
linktype: "AddText"
type: docs
url: /add-text/
keywords: "API Aspose Cells, ajouter du texte à Excel, insertion groupée de texte, préfixe suffixe Excel, remplacement de texte dans feuille de calcul, automatisation Excel, API feuille de calcul cloud"
description: "Insérez des préfixes, suffixes ou libellés personnalisés dans de nombreuses cellules Excel en une seule opération avec Aspose.Cells Cloud. Choisissez l’insertion en début, fin, avant ou après un texte spécifique. Prend en charge les plages, les feuilles de calcul et le traitement des cellules vides."
weight: 100
---

Insérez du texte dans plusieurs cellules Excel en une seule opération. Ajoutez des préfixes, suffixes, libellés ou caractères personnalisés en début, en fin, ou avant/après un texte spécifique dans les cellules à l’aide de l’API Aspose.Cells.

## Vue d’ensemble

Insertion groupée en une seule requête de préfixes, suffixes ou chaînes ancrées dans chaque cellule d’une plage cible — aucune formule, aucune colonne d’aide.

- Insérez du texte personnalisé à **n’importe quelle position** dans chaque cellule

| Valeur           | Description                                                                     |
| ---------------- | ------------------------------------------------------------------------------- |
| `None`           | Remplace le contenu original                                                    |
| `AtTheBeginning` | Insère au début (préfixe)                                                       |
| `AtTheEnd`       | Insère en fin (suffixe)                                                         |
| `BeforeText`     | Insère **avant** la première occurrence de `selectText` ; saute si non trouvé |
| `AfterText`      | Insère **après** la première occurrence de `selectText` ; saute si non trouvé  |

- Quatre modes d’emplacement : préfixe, suffixe, avant/après une sous-chaîne.
- Ignore les cellules vides pour éviter tout encombrement.
- L’API modifie uniquement les valeurs de type **chaîne** ; les nombres, booléens et formules sont d’abord convertis en texte.
- **Cellules vides**
  - `skipEmptyCells = true` → les cellules vides sont ignorées.
  - `skipEmptyCells = false` → du texte est ajouté aux cellules vides (la cellule devient de type texte).

- **Ancre introuvable** : si `position = BeforeText | AfterText` et que `selectText` **n’existe pas**, la valeur de la cellule reste inchangée.

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête de l’API **AddText**

| Nom du paramètre | Type    | Emplacement (Chemin/Requête/Corps HTTP) | Description                                                                                                                                                      | Obligatoire |
| :--------------- | :------ | :--------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
| Spreadsheet      | Fichier | FormData                                 | Le fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                       | Oui         |
| text             | Chaîne  | Requête                                  | Le contenu textuel à ajouter dans les cellules spécifiées de la feuille de calcul.                                                                             | Oui         |
| position         | Chaîne  | Requête                                  | Indique où insérer le texte par rapport au contenu existant de la cellule. Options : `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`.         | Oui         |
| selectText       | Chaîne  | Requête                                  | _(Facultatif)_ Si fourni, le texte sera ajouté uniquement dans les cellules contenant exactement cette sous-chaîne. À utiliser conjointement avec `position`. | Non         |
| skipEmptyCells   | Booléen | Requête                                  | Si `true`, les cellules vides sont ignorées ; si `false`, du texte est ajouté aux cellules vides.                                                             | Non         |
| worksheet        | Chaîne  | Requête                                  | _(Facultatif)_ Le nom de la feuille de calcul dans laquelle le texte sera ajouté. Par défaut, l’opération s’applique à la première feuille.                   | Non         |
| range            | Chaîne  | Requête                                  | _(Facultatif)_ La plage de cellules dans laquelle le texte sera ajouté (ex. `"A1:C10"`). Par défaut, l’opération s’applique à toutes les cellules utilisées. | Non         |
| outPath          | Chaîne  | Requête                                  | _(Facultatif)_ Le chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Par défaut, le fichier est enregistré dans le dossier source. | Non         |
| outStorageName   | Chaîne  | Requête                                  | Le nom du stockage cloud dans lequel le fichier de sortie sera stocké.                                                                                        | Non         |
| region           | Chaîne  | Requête                                  | _(Facultatif)_ Définit la locale pour le formatage des nombres, dates et devises dans le fichier de sortie (ex. `"en-US"`, `"zh-CN"`, `"de-DE"`).             | Non         |
| password         | Chaîne  | Requête                                  | _(Facultatif)_ Si la feuille de calcul uploadée est protégée par mot de passe, fournissez ce mot de passe pour l’ouvrir et la traiter.                          | Non         |

**Exemple cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Report&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
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

### Codes d’erreur

| Code | Description |
| ---- | ----------- |
| **400** Bad Request | URI invalide de l’API Aspose.Cells Cloud ou paramètres obligatoires manquants. |
| **401** Unauthorized | Jeton d’accès invalide ou identifiant/secret client incorrect. |
| **404** Not Found | Le fichier de feuille de calcul est inaccessible. |
| **500** Server Error | Une anomalie est survenue lors de la récupération des données de calcul dans la feuille de calcul. |

## Où utiliser l’API Add Text pour les feuilles de calcul ?

- **Libellés dynamiques pour rapports** : Ajouter des titres dynamiques, des libellés de date ou des notes à des états financiers et rapports de ventes générés automatiquement.
- **Tamponnage groupé de fichiers** : Ajouter des logos d’entreprise, des mentions de confidentialité ou des informations de version à un lot de fichiers Excel.
- **Remplissage automatique de modèles** : Remplir automatiquement les noms clients, montants et autres textes dans des positions prédéfinies de modèles de contrats ou factures.
- **Étiquetage par classification des données** : Ajouter automatiquement des tags de classification ou libellés de statut (ex. « En attente de validation », « Approuvé ») aux lignes de données selon les résultats d’analyse.
- **Annotation de qualité des données** : Ajouter des notes sur les données problématiques lors du nettoyage des données.
- **Formatage textuel groupé** : Ajouter uniformément des préfixes ou suffixes aux noms de produits ou clients.

## Pourquoi utiliser l’API Add Text pour les feuilles de calcul ?

- **Ajout groupé de texte** : Ajoutez du texte à des centaines de cellules ou fichiers en une seule fois, économisant jusqu’à 95 % du temps par rapport au travail manuel.
- **Contrôle précis de la position** : Prend en charge l’insertion précise du texte à six positions : début, fin, ou avant/après un texte spécifique dans une cellule.
- **Gestion intelligente conditionnelle** : Décidez si le texte doit être ajouté selon que la cellule est vide ou contient un texte spécifique.
- **Support de stratégies multi-position** :
  - `AtTheBeginning` : Ajouter le même texte avant le contenu de toutes les cellules sélectionnées.
  - `AtTheEnd` : Ajouter du texte après le contenu de toutes les cellules sélectionnées.
  - `BeforeText` / `AfterText` : Ajouter du texte uniquement avant ou après les cellules contenant un texte spécifique.
  - `None` : Remplacer le contenu original.
- **Contrôle précis de la plage** : Permet de spécifier des feuilles ou plages de cellules particulières pour les opérations.
- **Option conditionnelle de saut** : Prend en charge l’ignorance des cellules vides pour éviter l’ajout inutile de texte.
- **Convivial pour les développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant un développement rapide, avec une documentation complète. Comparé à la création de solutions personnalisées de rendu graphique, cela réduit considérablement la charge de développement.
- ** rentable** : Vous pouvez ajouter du texte dans une cellule sans avoir à uploader préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d’implémenter simplement l’ajout de texte aux cellules avec un minimum de code. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---