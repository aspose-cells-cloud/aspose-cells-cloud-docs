---
title: "Aspose.Cells Cloud – Remplacer du texte dans des fichiers Excel locaux (API Rechercher & Remplacer)"
second_title: "Document"
ArticleTitle: "Remplacement en masse de texte dans des fichiers Excel locaux – API Rechercher & Remplacer"
linktitle: "Remplacer le contenu d'une feuille de calcul"
type: docs
url: /replace-spreadsheet-content/
keywords: "remplacer du texte dans Excel, Aspose.Cells Rechercher et Remplacer, API de feuille de calcul locale, remplacement de fichier Excel, API de remplacement de contenu"
description: "Remplacer du texte dans des classeurs Excel locaux sans les téléverser vers le cloud. Utilisez l’API Rechercher & Remplacer d’Aspose.Cells Cloud pour mettre à jour des plages spécifiques, des feuilles de calcul ou des fichiers entiers en une seule appel."
weight: 100
---

Remplacez du texte spécifié dans des fichiers de feuille de calcul Excel locaux sans téléversement vers le cloud. Mettez à jour le contenu des classeurs efficacement à l’aide de l’API Rechercher & Remplacer d’Aspose.Cells Cloud pour une édition hors ligne.

## **API de remplacement du contenu d'une feuille de calcul**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                                                           |
| :--------------- | :----- | :----------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | Le fichier de feuille de calcul local à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                                                       |
| searchText       | Chaîne  | Chaîne de requête                                     | La chaîne de texte à rechercher dans la feuille de calcul et la zone de cellules spécifiées.                                                                                                           |
| replaceText      | Chaîne  | Chaîne de requête                                     | La chaîne de texte qui remplacera toutes les occurrences de `searchText` dans la plage spécifiée.                                                                                                         |
| worksheet        | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ Le nom de la feuille de calcul dans laquelle l’opération de recherche et remplacement sera effectuée. Si omis, l’opération s’applique à la première feuille de calcul.                              |
| cellArea         | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ La plage spécifique de cellules (par ex., `"A1:D20"`, `"B5:F15"`) dans laquelle la recherche et le remplacement de texte auront lieu. Si omis, l’opération s’applique à toutes les cellules utilisées de la feuille de calcul spécifiée. |
| region           | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ Définit la locale pour la gestion du texte, ce qui peut affecter la sensibilité à la casse et l’encodage des caractères dans les opérations de recherche (par ex., `"en-US"`, `"fr-FR"`).           |
| password         | Chaîne  | Chaîne de requête                                     | _(Facultatif)_ Si la feuille de calcul téléversée est protégée par mot de passe, fournissez le mot de passe pour ouvrir et traiter le fichier.                                                                                    |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

La réponse est un flux binaire contenant le classeur mis à jour. Enregistrez-le avec l’extension appropriée (par ex., `.xlsx`).

### **Codes d’erreur**

- **400 Bad Request (Requête incorrecte)** – URI de l’API Aspose.Cells Cloud invalide ou paramètres mal formés.
- **401 Unauthorized (Non autorisé)** – Jeton d’accès invalide ou manquant ; obtenez un nouveau jeton.
- **404 Not Found (Non trouvé)** – Le fichier de feuille de calcul n’est pas accessible ou la feuille de calcul spécifiée n’existe pas.
- **500 Server Error (Erreur serveur)** – Une erreur interne de traitement s’est produite dans la feuille de calcul ; contactez le support si le problème persiste.

## Où utiliser l’API de remplacement du contenu d'une feuille de calcul ?

- **Traitement par lots de fichiers Excel locaux** – Automatisez les opérations de recherche et remplacement sur plusieurs classeurs stockés localement.
- **Pipelines de données en local** – Intégrez l’API dans des tâches planifiées permettant de modifier les rapports avant leur archivage ou leur distribution.
- **Génération locale de rapports** – Insérez dynamiquement des valeurs dans des modèles de classeurs sans les téléverser vers le cloud.

## Pourquoi utiliser l’API de remplacement du contenu d'une feuille de calcul ?

- **Adaptée aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide et une documentation complète. Comparé à la création de solutions personnalisées, cela réduit considérablement l’effort de développement.
- **Réduction des coûts en main-d’œuvre** – Réduit la nécessité d’avoir du personnel dédié à la consolidation manuelle des documents.
- **Paiement à l’usage** – Aucun investissement initial ; vous ne payez que pour les appels d’API effectivement utilisés.
- **Coûts de maintenance nuls** – Aucun serveur à maintenir, aucune mise à jour logicielle à gérer, aucune préoccupation de compatibilité.
- **Préservation du formatage complexe Excel** – Le formatage, les formules et les graphiques d’origine du classeur restent intacts après le remplacement.

## Comment utiliser l’API de remplacement du contenu d'une feuille de calcul avec les SDK

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) définit une interface de programmation accessible publiquement, vous permettant d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d’implémenter les opérations de remplacement de contenu avec un minimum de code. Consultez le dépôt officiel **Aspose.Cells Cloud SDK sur GitHub** pour obtenir la liste complète des langages pris en charge.

Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}