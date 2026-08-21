---
title: "Aspose.Cells Cloud – API de détection de liens rompus dans Excel – Analyser et valider les liens dans des classeurs distants"
second_title: "Document"
ArticleTitle: "Trouver et corriger les liens rompus dans Excel distant – Vérificateur de liens de classeur cloud"
linktitle: "Rechercher les liens rompus dans les classeurs distants"
type: docs
url: /fr/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, liens rompus, API, cloud, classeur, validation, Aspose.Cells"
description: "Utilisez l’API Aspose.Cells Cloud pour analyser les classeurs Excel distants à la recherche de liens externes rompus, de formules invalides et de sources de données manquantes."
weight: 100
---

## **Rechercher les liens rompus dans l’API de classeur distant**

Détectez automatiquement les liens rompus dans les fichiers Excel stockés dans le stockage cloud. Notre API analyse les plages spécifiées afin de repérer les références externes rompues, les formules invalides et les sources de données manquantes. Elle prend en charge l’audit de classeurs distants, les contrôles automatiques de qualité et l’intégration avec les fournisseurs de stockage cloud. Utilisez l’API REST pour automatiser des flux de travail au niveau entreprise.

### **API Web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                               |
| :--------------- | :----- | :-------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Chemin                                  | **Obligatoire.** Nom du fichier classeur Excel à analyser pour détecter les liens rompus (par exemple, `Rapport_trimestriel.xlsx`).                     |
| worksheet        | String | Chaîne de requête                        | **Obligatoire.** Nom de la feuille de calcul dans laquelle l’opération de recherche sera effectuée. Indiquez le nom exact de la feuille tel qu’il apparaît dans le classeur. |
| cellArea         | String | Chaîne de requête                        | **Obligatoire.** Plage de cellules à analyser pour les liens rompus, exprimée en notation A1 (par exemple, `C5:J50`). L’API ne recherche que dans cette zone. |
| folder           | String | Chaîne de requête                        | **Facultatif.** Chemin du répertoire contenant le classeur dans votre stockage cloud. Si omis, le répertoire racine est considéré par défaut.            |
| storageName      | String | Chaîne de requête                        | **Facultatif.** Nom de votre configuration personnalisée de stockage cloud. Si omis, le stockage par défaut du système est utilisé.                    |
| region           | String | Chaîne de requête                        | **Facultatif.** Paramètre de configuration régionale appliqué pendant le traitement (par exemple, `fr-FR`). Peut influencer l’interprétation de la syntaxe ou des références spécifiques à la région. |
| password         | String | Chaîne de requête                        | **Facultatif.** Mot de passe requis pour ouvrir un classeur chiffré. Omettez-le si le fichier n’est pas protégé par un mot de passe.                    |

**Exemple de requête cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Réponse**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**Exemple de réponse JSON**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "Fichier introuvable"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "Référence externe non prise en charge en mode cloud"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Codes d’erreur

- **400 Bad Request** – URI invalide pour l’API Aspose.Cells Cloud.  
- **401 Unauthorized** – Jeton d’accès, ID client ou secret client invalide.  
- **404 Not Found** – Le fichier de classeur n’est pas accessible.  
- **500 Server Error** – Une erreur s’est produite lors de l’obtention des données de calcul.

## Où utiliser l’API de recherche de liens rompus dans les classeurs ?

- **Audit régulier de grands modèles financiers** – Avant la diffusion des rapports mensuels ou trimestriels, analysez automatiquement les zones de calcul clés (par exemple, `Dashboard!B5:K50`) contenant de nombreuses références externes afin de vous assurer que tous les liens pointent vers des fichiers sources valides.  
- **Intégration de données lors de fusions et acquisitions** – Lors de la fusion de plusieurs classeurs représentant des unités métier, analysez la feuille « Vue d’ensemble » après intégration afin d’identifier les liens devenus invalides en raison de modifications de chemins de fichiers ou de problèmes de permissions.  
- **Préparation de dossiers pour les investisseurs** – Avant la finalisation des supports de présentation contenant des graphiques et tableaux liés à des bases de données externes ou des sources de données de marché, vérifiez la validité de tous les liens.

## Pourquoi utiliser l’API de recherche de liens rompus dans les classeurs ?

- **Adaptée aux développeurs** – Aspose.Cells Cloud fournit des SDK dans plusieurs langages, permettant un développement rapide grâce à une documentation complète. Comparé à la construction d’une solution personnalisée, cela réduit considérablement l’effort de développement.  
- **Réduction des coûts de main-d’œuvre** – Automatise la validation des liens, éliminant le besoin de personnel dédié pour consolider manuellement les documents.  
- **Paiement à l’utilisation** – Aucun investissement initial ; vous ne payez que pour les appels API effectivement réalisés.  
- **Coûts de maintenance nuls** – Aucun serveur à maintenir, aucune mise à jour logicielle, aucune préoccupation de compatibilité.

## Comment utiliser l’API de recherche de liens rompus dans les classeurs à l’aide des SDK

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus efficace pour accélérer le développement. Le SDK masque les détails HTTP sous-jacents, vous permettant d’implémenter la détection de liens rompus avec un code minimal. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}