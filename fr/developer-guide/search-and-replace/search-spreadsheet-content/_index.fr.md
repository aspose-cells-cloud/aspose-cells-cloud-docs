---
title: "Rechercher dans le contenu d'une feuille de calcul – API Aspose.Cells Cloud (rechercher du texte dans Excel)"
second_title: "Document"
articleTitle: "Rechercher du texte dans des feuilles de calcul Excel locales – Trouver des données spécifiques"
linktitle: "Rechercher dans le contenu d'une feuille de calcul"
type: docs
url: /search-spreadsheet-content/
keywords: "Aspose.Cells, API de recherche Excel, recherche de contenu de feuille de calcul, API de feuille de calcul cloud, recherche de texte"
description: "Utilisez l’API Aspose.Cells Cloud pour rechercher du texte, des nombres ou des formules dans des fichiers Excel locaux. Prend en charge les requêtes insensibles à la casse, la portée au niveau de la feuille de calcul et une authentification sécurisée."
weight: 100
---

## **API de recherche dans le contenu d'une feuille de calcul**

Recherchez de manière programmatique du texte spécifique dans n’importe quelle feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud. L’API permet de localiser du texte, des nombres ou des formules dans des fichiers locaux stockés dans le cloud, facilitant ainsi les flux de travail d’automatisation de la découverte de données, d’analyse de contenu et d’audit des feuilles de calcul.

### **API Web**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

Si vous préférez utiliser du HTTP brut, l’exemple cURL suivant illustre la même requête :

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête**

| Paramètre     | Type    | Emplacement | Description                                                                                                         |
| ------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------------------------- |
| spreadsheet   | Fichier | FormData    | Le fichier Excel à rechercher.                                                                                      |
| searchText    | Chaîne  | Requête     | Le texte (ou la valeur numérique) à localiser dans le classeur.                                                    |
| ignoringCase  | Booléen | Requête     | Mettre à `true` pour effectuer une recherche insensible à la casse.                                                 |
| worksheet     | Chaîne  | Requête     | Nom de la feuille de calcul dans laquelle limiter la recherche. Si omis, toutes les feuilles sont balayées.        |
| cellArea      | Chaîne  | Requête     | Plage au format A1 (par ex. `A1:C10`) limitant la zone de recherche.                                               |
| region        | Chaîne  | Requête     | Région géographique du service (par ex. `us-east-1`).                                                              |
| password      | Chaîne  | Requête     | Mot de passe requis pour ouvrir un classeur protégé.                                                              |

### **Réponse**

L’API renvoie un objet `SearchResult` contenant un tableau des cellules correspondantes. Chaque élément fournit le nom de la feuille de calcul, l’adresse de la cellule et le texte correspondant.

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### Codes d’erreur

- **400 Bad Request** – L’URI ou les paramètres de la requête sont invalides.
- **401 Unauthorized** – Jeton d’accès manquant ou invalide, ou identifiants client incorrects.
- **404 Not Found** – La feuille de calcul spécifiée est inaccessible.
- **500 Internal Server Error** – Une erreur serveur inattendue s’est produite lors du traitement du classeur.

## Où faut-il utiliser l’API de recherche dans le contenu d’une feuille de calcul ?

- **Audit complet de conformité du classeur** – Balayez l’ensemble du classeur pour localiser des termes sensibles (par ex. « Clause confidentielle », « Données internes ») dans le cadre de vérifications de sécurité des données et de conformité.
- **Requête d’association de données intersheets** – Trouvez un numéro de projet ou un nom de client apparaissant sur plusieurs feuilles de calcul, permettant une intégration rapide intersheets.
- **Vérification par lot du contenu des modèles** – Après génération des rapports, vérifiez que tous les espaces réservés tels que `{{Date}}` ont été correctement remplacés dans un lot de fichiers Excel.
- **Archivage et exploitation de données historiques** – Recherchez dans les fichiers Excel hérités des codes d’événement spécifiques ou des termes métier afin d’accélérer l’archéologie et l’analyse de données.

## Pourquoi utiliser l’API de recherche dans le contenu d’une feuille de calcul ?

- **Adaptée aux développeurs** – Des SDK sont disponibles pour de nombreux langages, réduisant l’effort de développement par rapport à la création d’une solution sur mesure.
- **Réduction des coûts de main-d’œuvre** – Automatise des tâches qui autrement nécessiteraient une inspection manuelle des feuilles de calcul.
- **Paiement à l’usage** – Vous ne payez que pour les appels d’API que vous effectuez réellement.
- **Aucune maintenance** – Aucun serveur à gérer, aucune mise à jour logicielle, aucune préoccupation de compatibilité.
- **Préservation du formatage complexe** – Les résultats peuvent être exportés vers PDF tout en conservant la mise en page Excel d’origine.

## Comment utiliser la recherche de liens brisés dans l’API de recherche dans le contenu d’une feuille de calcul à l’aide des SDK ?

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour intégrer la fonctionnalité de recherche. Le SDK abstrait la couche HTTP, vous permettant d’appeler l’API avec un minimum de code. Consultez la liste complète des SDK dans le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants illustrent comment invoquer l’opération de recherche dans le contenu d’une feuille de calcul à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
---