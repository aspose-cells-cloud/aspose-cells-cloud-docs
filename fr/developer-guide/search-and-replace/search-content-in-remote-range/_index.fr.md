---
title: "API de recherche de texte Aspose.Cells Cloud Excel – Rechercher du texte dans des plages de classeurs distants"
second_title: "Document"
articleTitle: "Rechercher du texte dans des classeurs Excel distants – Trouver des données dans des plages spécifiques"
linkTitle: "Rechercher le contenu dans une plage distante"
type: docs
url: /fr/search-content-in-remote-range/
keywords: "Aspose.Cells, API Excel, recherche de texte, plage distante, classeur cloud, API REST, découverte de données"
description: "Recherchez du texte, des nombres ou des formules dans une plage spécifique d’un classeur Excel stocké dans Aspose Cloud."
weight: 100
---

## **Rechercher le contenu dans une plage distante**

Recherchez dynamiquement du texte spécifique dans n’importe quelle plage de classeurs Excel à l’aide de l’API Aspose.Cells Cloud. Localisez du texte, des nombres ou des formules dans des fichiers distants stockés dans le stockage cloud. API RESTful pour des workflows automatisés de découverte de données, d’analyse de contenu et d’audit de feuilles de calcul.

### **API Web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


**Exemple cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### Paramètres de la requête

| Nom du paramètre | Type    | Path/Query/String/HTTPBody | Description                                                                                                                                              |
| :--------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String  | Path                       | **Obligatoire**. Le nom du fichier (avec extension) du classeur Excel à analyser, par exemple `customer_data.xlsx`.                                   |
| worksheet        | String  | Path                       | **Obligatoire**. Le nom exact de la feuille de calcul à l’intérieur du classeur dans laquelle effectuer la recherche, par exemple `Orders_2024`.      |
| cellArea         | String  | Path                       | **Obligatoire**. La plage cible de cellules pour la recherche, spécifiée en notation A1 (par exemple `B2:H100`). La recherche est limitée à cette zone. |
| searchText       | String  | Query                      | **Obligatoire**. La chaîne de texte, le nombre ou le contenu partiel spécifique à rechercher dans la plage de cellules définie.                       |
| ignoreCase       | Boolean | Query                      | **Facultatif**. Si défini sur `true`, la recherche ignore la casse (par exemple, « Report » correspond à « report »). Par défaut : `false` (sensible à la casse). |
| folder           | String  | Query                      | **Facultatif**. Le chemin du répertoire dans votre stockage cloud où se trouve le classeur. Si omis, le répertoire racine est utilisé.                |
| storageName      | String  | Query                      | **Facultatif**. L’identifiant d’une configuration personnalisée de stockage cloud. Si non spécifié, le stockage par défaut du compte est utilisé.    |
| region           | String  | Query                      | **Facultatif**. Le paramètre de culture/région (par exemple `fr-FR`) pouvant affecter l’interprétation des caractères ou formats spécifiques à une région pendant la recherche. |
| password         | String  | Query                      | **Facultatif**. Le mot de passe nécessaire pour déchiffrer et accéder à un fichier de feuille de calcul protégé par mot de passe. À omettre si le fichier n’est pas chiffré. |

### Réponse

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

### Codes d’erreur

- **400 Bad Request** – URI de l’API Aspose.Cells Cloud invalide.  
- **401 Unauthorized** – Jeton d’accès, client ID ou client secret invalide.  
- **404 Not Found** – Le fichier de feuille de calcul n’est pas accessible.  
- **500 Server Error** – Une condition inattendue a empêché le serveur de traiter la requête.

## Où utiliser la fonctionnalité de recherche de contenu dans une plage de la feuille de calcul ?

- **Vérification à grande échelle de la qualité des données** – Lors de la phase d’acceptation du processus ETL dans un entrepôt de données, recherchez des descriptions de champs manquantes, des abréviations non définies ou du texte générique (par exemple, `« TDB »` ou `« NULL »`) dans la table de correspondance des données (`DataDictionary!B2:F1000`) afin d’identifier les définitions de données incomplètes.  
- **Génération dynamique de rapports et extraction de contenu** – Dans les systèmes automatisés de génération de rapports, recherchez et extrayez intelligemment les blocs de données de la période en cours identifiés par des marqueurs spécifiques (par exemple, `« [KPI] »`) à partir de feuilles modèles contenant des données hétérogènes (`Monthly_Metrics!C10:G50`) afin de constituer le rapport final.  
- **Analyse de contrats et de documents juridiques** – Lors de l’examen d’annexes sous forme de feuilles de calcul comportant de nombreuses clauses, localisez efficacement des termes juridiques précis (par exemple, `« limite de responsabilité »`), des noms de parties ou des dates dans une plage définie (`Contract_Terms!A:A`) pour accélérer le processus d’instruction.

## Pourquoi utiliser la fonctionnalité de recherche de contenu dans une plage de la feuille de calcul ?

- **Adapté aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant un développement rapide et bénéficiant d’une documentation complète, ce qui réduit considérablement la charge de développement par rapport à la création de solutions sur mesure.  
- **Réduction des coûts de main-d’œuvre** – Élimine le besoin de postes dédiés à la consolidation de documents.  
- **Paiement à l’usage** – Aucun investissement initial ; vous ne payez que les appels à l’API effectivement utilisés.  
- **Coûts de maintenance nuls** – Aucun serveur à entretenir, aucune mise à jour logicielle à gérer, aucune préoccupation de compatibilité.

## Comment utiliser la recherche de contenu dans une plage de la feuille de calcul à l’aide des SDK

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utilisation des SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de mettre en œuvre simplement la recherche de contenu dans une plage de feuilles de calcul avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}