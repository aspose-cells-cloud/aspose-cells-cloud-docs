---
title: "Aspose.Cells Cloud – Détecter les liens brisés dans une plage Excel (API)"
second_title: "Document"
ArticleTitle: "Rechercher et corriger les liens brisés dans une plage Excel distante – Vérificateur de liens de classeur cloud"
linktype: "Search Remote Range Broken Links"
type: docs
url: /fr/search-broken-links-in-remote-range/
keywords: "Aspose, Cells, liens brisés, API, plage Excel, validation, cloud, classeur, référence externe, vérificateur"
description: "Utilisez l’API Aspose.Cells Cloud pour analyser une plage Excel spécifique à la recherche de liens externes brisés, de formules invalides ou de sources de données manquantes. Sécurisé, rapide et basé sur le cloud."
weight: 100
---

## **Rechercher des liens brisés dans une plage distante via l’API**

Détectez automatiquement les liens brisés dans les données de plage des fichiers Excel stockés dans le cloud. Notre API analyse les plages spécifiées à la recherche de références externes brisées, de formules invalides et de sources de données manquantes. Prend en charge l’audit de classeurs distants, les contrôles automatisés de qualité et l’intégration avec les fournisseurs de stockage cloud. API RESTful pour l’automatisation des flux de travail d’entreprise.


### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                                                                                                                          |
| ---------------- | ------ | ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Path        | **Obligatoire.** Le nom du fichier de classeur Excel (par exemple `financial_report.xlsx`) stocké dans le cloud que vous souhaitez analyser à la recherche de liens brisés. |
| worksheet        | String | Path        | **Obligatoire.** Le nom de la feuille de calcul spécifique (par exemple `Sheet1`, `Q4_Data`) dans le classeur où la recherche de liens brisés doit être effectuée.        |
| cellArea         | String | Path        | **Obligatoire.** L’adresse de la plage cible (par exemple `A1:F100`) dans la feuille de calcul spécifiée à analyser pour les références externes brisées, formules ou liens. |
| folder           | String | Query       | **Facultatif.** Le chemin du répertoire dans votre stockage cloud où le classeur cible est situé. Si omis, le répertoire racine est supposé.                           |
| storageName      | String | Query       | **Facultatif.** Le nom du service de stockage cloud configuré (par exemple `DropboxBusiness`, `S3Bucket`). Si non spécifié, le stockage par défaut du compte est utilisé. |
| region           | String | Query       | **Facultatif.** Le paramètre de paramètres régionaux (par exemple `fr-FR`, `de-DE`) à appliquer pour l’interprétation des données spécifiques à la région lors de l’analyse. |
| password         | String | Query       | **Facultatif.** Le mot de passe de déchiffrement nécessaire pour accéder à un classeur protégé par mot de passe. Laisser vide si le fichier n’est pas chiffré.           |

**Exemple de corps de requête**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### Réponse

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

La collection `BrokenLinks` contient des objets de type **BrokenLink**. Chaque objet fournit les propriétés suivantes :

- **CellName** – L’adresse de la cellule contenant la référence brisée (par exemple `B12`).
- **LinkType** – Le type de lien brisé (par exemple `ExternalReference`, `Formula`).
- **ErrorMessage** – Une description expliquant pourquoi le lien est considéré comme brisé.

**Remarque** : L’API est soumise à des limites de débit. Reportez-vous à la page [Tarification et limites de débit](https://www.aspose.cloud/pricing) pour plus de détails.

### Codes d’erreur

- **400 Bad Request** – URI d’API Aspose.Cells Cloud invalide.
- **401 Unauthorized** – Jeton d’accès, ID client ou secret client invalide.
- **404 Not Found** – Le fichier de classeur n’est pas accessible.
- **500 Server Error** – Le classeur a rencontré une anomalies lors de la récupération des données de calcul.

## Où utiliser la recherche de liens brisés dans une plage de classeur via l’API ?

- **Audit régulier de grands modèles financiers** – Avant la diffusion de rapports mensuels ou trimestriels, scannez automatiquement les zones clés de calcul (par exemple `Dashboard!B5:K50`) contenant de nombreuses références à des données externes afin de garantir que tous les liens pointent vers des fichiers sources valides.
- **Intégration de données dans le cadre de fusions-acquisitions** – Lors de la fusion de plusieurs fichiers de classeur représentant des unités métier, scannez la feuille « Vue d’ensemble » après l’intégration pour identifier les liens devenus invalides suite à des modifications de chemins de fichiers ou à des problèmes de permissions.
- **Préparation de dossiers pour les investisseurs** – Avant de finaliser les supports de présentation contenant des graphiques et tableaux liés à des bases de données externes ou des sources de données de marché, vérifiez la validité de tous les liens.

## Pourquoi utiliser la recherche de liens brisés dans une plage de classeur via l’API ?

- **Convivial pour les développeurs** – Aspose.Cells Cloud propose des SDK dans plusieurs langages, permettant un développement rapide avec une documentation complète. Comparé à la construction d’une solution sur mesure, cela réduit considérablement l’effort de développement.
- **Réduction des coûts de main-d’œuvre** – Élimine le besoin de personnel dédié pour consolider manuellement les documents.
- **Paiement à l’usage** – Aucun investissement initial ; vous ne payez que pour les appels API effectués.
- **Zéro coût de maintenance** – Aucun serveur à maintenir, aucune mise à jour logicielle à effectuer, aucune préoccupation de compatibilité.
- **Préservation du formatage complexe Excel** – Les résultats peuvent être exportés au format PDF universellement accessible sans perte de style.

## Comment utiliser la recherche de liens brisés dans une plage de classeur via l’API avec les SDK

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d’implémenter la fonction « recherche de liens brisés dans une plage » avec un minimum de code. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}