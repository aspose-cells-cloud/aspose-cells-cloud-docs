---
title: "Rechercher du texte dans des classeurs Excel distants – API Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Rechercher du texte dans des classeurs Excel distants – Trouver des données spécifiques"
linktitle: "Rechercher du contenu dans un classeur distant"
type: docs
url: /fr/search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, API de recherche Excel, classeur cloud, recherche de texte, REST"
description: "Recherchez du texte, des nombres ou des formules dans des fichiers Excel stockés dans un espace de stockage cloud à l’aide d’Aspose.Cells Cloud. Prend en charge les requêtes insensibles à la casse, la sélection de dossiers et les classeurs protégés par mot de passe."
weight: 100
---

### **Rechercher du contenu dans un classeur distant via l’API**

Recherchez de manière programmatique du texte spécifique dans n’importe quel classeur Excel à l’aide de l’API Aspose.Cells Cloud. Localisez du texte, des nombres ou des formules dans des fichiers stockés dans un espace de stockage cloud. Cette API RESTful permet de mettre en place des workflows automatisés de découverte de données, d’analyse de contenu et d’audit de classeurs.

### **API Web**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                      |
| :--------------- | :------ | :----------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String  | Chemin                                                 | **Obligatoire**. Nom du fichier du classeur Excel (avec extension) dans lequel la recherche de texte sera effectuée, par exemple `sales_data.xlsx`.           |
| searchText       | String  | Chaîne de requête                                      | **Obligatoire**. Chaîne, nombre ou contenu partiel exact à localiser dans l’ensemble du classeur ou des feuilles de calcul.                                   |
| ignoringCase     | Boolean | Chaîne de requête                                      | **Facultatif**. Détermine la sensibilité à la casse. Définir sur `true` pour une recherche insensible à la casse (par exemple, « Report » correspond à « REPORT ») ; la valeur par défaut est `false`. |
| folder           | String  | Chaîne de requête                                      | **Facultatif**. Chemin du dossier dans votre espace de stockage cloud contenant le classeur cible. Si omis, le dossier racine est utilisé par défaut.          |
| storageName      | String  | Chaîne de requête                                      | **Facultatif**. Identifiant d’un service de stockage cloud personnalisé. Si non spécifié, l’API utilise le stockage par défaut associé au compte.             |
| region           | String  | Chaîne de requête                                      | **Facultatif**. Paramètre de paramètres régionaux (par exemple `fr-FR`) appliqué lors de la recherche, pouvant influencer la normalisation ou les règles de tri. |
| password         | String  | Chaîne de requête                                      | **Facultatif**. Mot de passe de déchiffrement requis pour accéder à un fichier Excel protégé par mot de passe. Omettre ce paramètre si le fichier n’est pas chiffré. |

**Glossaire**

- **searchText** – La chaîne exacte à localiser ; peut correspondre partiellement.
- **ignoringCase** – `true` rend la recherche insensible à la casse ; `false` impose la sensibilité à la casse.
- **folder** – Chemin du dossier contenant le classeur.
- **storageName** – Identifiant d’une configuration de stockage personnalisée.
- **region** – Code de paramètres régionaux influençant les règles de comparaison de texte.
- **password** – Mot de passe de déchiffrement pour les classeurs protégés.

### **Réponse**

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

La réponse contient une liste des cellules (`CellName`) dans lesquelles le texte recherché a été trouvé, accompagnée du nom de la feuille de calcul et du texte correspondant. Si aucune correspondance n’est trouvée, le tableau `TextItems` est vide, mais la requête renvoie tout de même le code HTTP 200 OK.

### Codes d’erreur

- **400 Bad Request** – URI de l’API Aspose.Cells Cloud invalide.  
  ```json
  {"code":400,"message":"URI de requête invalide"}
  ```
- **401 Unauthorized** – Jeton d’accès, ID client ou secret client invalide.  
  ```json
  {"code":401,"message":"Jeton d’accès invalide"}
  ```
- **404 Not Found** – Le fichier de classeur n’est pas accessible.  
  ```json
  {"code":404,"message":"Fichier introuvable"}
  ```
- **500 Server Error** – Une condition inattendue a empêché l’API de terminer la requête.  
  ```json
  {"code":500,"message":"Erreur interne du serveur"}
  ```

## Où utiliser l’API de recherche de contenu dans un classeur ?

- **Audit de conformité complet du classeur** – Analysez rapidement l’ensemble du fichier Excel pour identifier tous les termes sensibles (par exemple, « Clause confidentielle », « Données internes ») dans le cadre des contrôles de sécurité et de conformité des données d’entreprise.
- **Requête de corrélation inter-feuilles** – Lorsque les informations d’un projet sont réparties sur plusieurs feuilles de calcul, recherchez un numéro de projet ou un nom de client spécifique pour localiser instantanément toutes les données associées.
- **Vérification par lots du contenu des modèles** – Après génération automatique de rapports, analysez plusieurs fichiers Excel en une seule fois afin de confirmer que tous les espaces réservés prédéfinis (par exemple `{{Date}}`) ont été correctement remplacés, garantissant ainsi l’intégrité et la précision des rapports.
- **Archivage et extraction de données historiques** – Analysez les fichiers anciens, recherchez des codes d’événements spécifiques ou des termes métier, et comprenez rapidement la logique métier historique à des fins d’archéologie des données.

## Pourquoi utiliser l’API de recherche de contenu dans un classeur ?

- **Conviviale pour les développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide accompagné d’une documentation complète. Comparé à la création de solutions personnalisées, cela réduit considérablement l’effort de développement.
- **Réduction des coûts en main-d’œuvre** – Automatise les tâches de recherche répétitives, libérant ainsi les développeurs des tâches manuelles d’extraction de données.
- **Tarification à l’usage** – Aucun investissement initial requis ; vous ne payez que pour les appels d’API effectivement utilisés.
- **Aucune maintenance requise** – Aspose gère les serveurs, les mises à jour et la compatibilité, afin que vous puissiez vous concentrer sur la logique métier de votre application.
- **Préservation du formatage Excel complexe** – Les résultats peuvent être exportés au format PDF universellement accessible tout en conservant le style original.

## Comment utiliser la recherche de liens cassés dans une plage de classeurs via l’API avec les SDK ?

### Spécification OpenAPI

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant de simplement implémenter la recherche de contenu dans des classeurs avec un code minimal. Consultez le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment invoquer les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---