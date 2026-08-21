---
title: "Aspose.Cells Cloud Excel : déplacement d’onglet via l’API Web – modifier la position d’une feuille de calcul de manière programmatique"
second_title: "Document"
ArticleTitle: "Comment déplacer des feuilles de calcul dans Excel – réorganiser l’ordre et la position des onglets"
linktype: "docs"
url: /fr/move-worksheet-in-spreadsheet/
keywords: "API de déplacement d’onglet, API de réorganisation des feuilles, API de modification de l’ordre des feuilles, API de gestion des onglets Excel, API REST Aspose Cells, automatisation de la position des feuilles, API d’organisation de classeurs, API de structure de feuille de calcul, automatisation Excel dans le cloud, réorganisation par lots des feuilles"
description: "Découvrez comment déplacer des feuilles de calcul à l’intérieur des classeurs Excel afin de réorganiser l’ordre des feuilles et optimiser la structure du classeur. Modifiez les positions des feuilles, réorganisez les onglets pour améliorer votre flux de travail et automatisez l’organisation des feuilles pour une gestion professionnelle des feuilles de calcul."
weight: 100
---

Déplacez de manière programmatique des feuilles de calcul au sein des classeurs Excel à l’aide de l’API Aspose.Cells Cloud. Modifiez les positions des feuilles, réorganisez les onglets et optimisez la structure du classeur grâce à des appels RESTful à l’API. Idéal pour automatiser l’organisation des feuilles de calcul et créer des dispositions standardisées des classeurs.

## **Déplacer une feuille de calcul via l’API**

### API Web

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                        |
| :--------------- | :----- | :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | Fichier | FormData                                | **Obligatoire**. Fichier du classeur Excel source (.xlsx, .xls, etc.) contenant la feuille de calcul à repositionner.                                              |
| worksheet        | Chaîne  | Query                                   | **Obligatoire**. Nom exact de la feuille de calcul à déplacer (par exemple, `Résumé`, `DonnéesBrutes_2024`).                                                     |
| position         | Entier  | Query                                   | **Obligatoire**. Nouvelle position d’index à zéro de la feuille de calcul. Par exemple, `0` la place en première position, `2` la place en troisième position. |
| outPath          | Chaîne  | Query                                   | **Facultatif**. Chemin du dossier cible dans le stockage cloud où le classeur réorganisé sera enregistré. Si `null` ou omis, le dossier source est utilisé.     |
| outStorageName   | Chaîne  | Query                                   | **Obligatoire**. Nom identifiant votre service de stockage cloud configuré (par exemple, `TeamDrive`) où le fichier de sortie sera stocké.                      |
| region           | Chaîne  | Query                                   | **Facultatif**. Paramètre de localisation (par exemple, `fr-FR`) à appliquer, pouvant influencer certaines règles de formatage lors de l’enregistrement.       |
| password         | Chaîne  | Query                                   | **Facultatif**. Mot de passe de déchiffrement nécessaire pour ouvrir et modifier un classeur protégé par mot de passe. À omettre si le fichier n’est pas chiffré. |

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

**Codes d’état HTTP**

| Code | Signification          | Description                                                        |
| ---- | ---------------------- | ------------------------------------------------------------------ |
| 200  | OK                     | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte     | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé           | Jeton JWT invalide ou manquant.                                    |
| 413  | Charge utile trop grande | Fichier téléchargé dépassant la taille limite.                   |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                        |

## Où utiliser l’API de déplacement de feuille de calcul dans une feuille de calcul ?

- **Génération standardisée de rapports** : après la génération automatique des rapports mensuels ou trimestriels, la feuille `Résumé` ou `Vue d’ensemble exécutive` est déplacée en première position du classeur afin que les conclusions principales soient immédiatement visibles à l’ouverture du fichier.
- **Pipeline de traitement des données** : après le traitement des feuilles brutes issues de différentes sources dans le cadre du processus ETL, la feuille `DonnéesTraitées`, une fois nettoyée et transformée, est placée à une position logique dans le classeur (par exemple, au milieu), ce qui crée une structure claire avec les données d’origine et les résultats d’analyse.
- **Livraison de fichiers personnalisés selon les préférences utilisateur** : après qu’un utilisateur a sélectionné une mise en page préférée via une interface de configuration (par exemple, en plaçant la page de graphique en premier), le système réorganise automatiquement l’ordre des feuilles dans le classeur selon la sélection et livre le fichier personnalisé.

## Pourquoi utiliser l’API de déplacement de feuille de calcul dans une feuille de calcul ?

- **Adaptée aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions sur mesure, cela réduit considérablement la charge de développement.
- **Réduction des coûts de main-d’œuvre** : diminue la nécessité de personnel dédié à la consolidation de documents.
- **Paiement à l’usage** : pas d’investissement initial ; vous ne payez que les appels à l’API effectivement utilisés.
- **Coûts de maintenance nuls** : pas besoin de maintenir des serveurs, mettre à jour des logiciels ou gérer des problèmes de compatibilité.

## Comment utiliser l’API de déplacement de feuille de calcul dans une feuille de calcul avec les SDK ?

### Spécification de l’API de déplacement de feuille de calcul dans une feuille de calcul

La [spécification de l’API de déplacement de feuille de calcul dans une feuille de calcul](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) fournit une interface de programmation accessible publiquement pour faciliter les interactions REST directes depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Feuil1&destIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/chemin/vers/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de déplacer des feuilles de calcul dans une feuille de calcul à l’aide d’un code concis. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.  
Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}