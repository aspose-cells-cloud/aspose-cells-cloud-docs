---
title: "Aspose.Cells Cloud Web API – Convertir les données locales d’un tableau Excel en fichier JSON"
second_title: "Document"
articleTitle: "Comment convertir les données de tableau d’une feuille de calcul locale en fichier JSON : guide étape par étape"
linktype: "Convertir un tableau en JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel, API, JSON, conversion, cloud, fichier, feuille de calcul"
description: "Utilisez l’API Aspose.Cells Cloud pour transformer un tableau Excel local en fichier JSON via une seule requête PUT. Inclut un exemple cURL, les paramètres et des extraits de code SDK pour C#, Java, Python, etc."
weight: 100
---

Convertissez un tableau de feuille de calcul/Excel local en fichier **JSON** à l’aide de l’API Web Aspose.Cells Cloud.

## **API Convertir un tableau en JSON**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre   | Type   | Emplacement | Description                                                                                      |
| -------------------- | ------ | ----------- | ------------------------------------------------------------------------------------------------ |
| **Spreadsheet**      | Fichier | FormData    | Le fichier Excel à télécharger.                                                                  |
| **worksheet**        | Chaîne  | Query       | Nom de la feuille contenant le tableau.                                                          |
| **tableName**        | Chaîne  | Query       | Nom du tableau à convertir.                                                                      |
| **outPath**          | Chaîne  | Query       | (Facultatif) Chemin du dossier où le fichier JSON résultant sera stocké ; valeur par défaut : **null**. |
| **outStorageName**   | Chaîne  | Query       | (Facultatif) Nom du stockage dans lequel le fichier de sortie sera placé.                       |
| **fontsLocation**    | Chaîne  | Query       | (Facultatif) Chemin vers les polices personnalisées utilisées lors de la conversion.           |
| **region**           | Chaîne  | Query       | (Facultatif) Paramètres régionaux du classeur.                                                  |
| **password**         | Chaîne  | Query       | (Facultatif) Mot de passe permettant d’ouvrir un classeur protégé.                             |

### Réponse

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

**Codes de statut HTTP**

| Code | Signification           | Description                                                           |
| ---- | ----------------------- | --------------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête        | Paramètres manquants ou invalides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                       |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.                  |
| 500  | Erreur interne du serveur | Erreur inattendue sur le serveur.                                    |

## **À quoi sert l’API Convertir un tableau en JSON ?**

- **Tableaux de bord en temps réel** – Convertissez les données Excel en direct en JSON pour les bibliothèques de graphiques comme Chart.js ou D3.js.
- **Feuilles de calcul comme service (Spreadsheet-as-a-Service)** – Exposez les tableaux Excel sous forme de points de terminaison JSON pour d’autres microservices.
- ** Charges utiles de webhooks** – Transformez les données de feuilles de calcul en JSON pour les notifications par webhook.
- **Prototypage rapide de données** – Convertissez rapidement des données Excel nettoyées en JSON pour une analyse en Python ou R.
- **Pipelines d’apprentissage automatique** – Pré-traitez les données d’entraînement stockées dans des feuilles de calcul métier.
- **Opérations e‑commerce** – Synchronisez les catalogues produits ou les feuilles tarifaires avec des sites web via JSON.
- **Automatisation des rapports** – Générez des flux JSON à partir de modèles financiers pour des rapports automatisés.
- **Configuration d’applications** – Gérez les drapeaux fonctionnels, les paramètres ou les paramètres d’A/B tests dans Excel → JSON.
- **Support multilingue** – Convertissez les feuilles de calcul de localisation en JSON pour les bibliothèques i18n.
- **Menus/navigations dynamiques** – Stockez la structure de navigation d’un site web dans Excel et déployez-la en tant que JSON.

## Pourquoi utiliser l’API Convertir un tableau en JSON ?

- **Adaptée aux développeurs** – Aspose.Cells Cloud fournit des SDK pour de nombreux langages, réduisant ainsi l’effort de développement et offrant une documentation complète.
- **Économique** – Convertissez les données de tableau sans avoir à télécharger préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.
- **Compatibilité web et mobile moderne** – JSON est le langage natif des données sur le Web ; cette API permet d’alimenter directement vos données de feuille de calcul en direct vers React, Vue, Angular, des applications mobiles ou des applications monopages, sans traitement complexe.
- **Large compatibilité linguistique** – JSON fonctionne avec pratiquement tous les langages de programmation, bases de données et services web.
- **Préservation de la structure des données**
  - **Détection intelligente de la structure** – Convertit automatiquement les données tabulaires en tableaux/objets JSON adaptés.
  - **Mappage des en-têtes** – Utilise la première ligne comme clés JSON pour des structures d’objets propres.
  - **Préservation des types de données** – Conserve les nombres, les dates et les booléens (pas seulement du texte).

_Historique des versions :_ Le point de terminaison Convertir un tableau en JSON a été introduit avec la version **v4.0** de l’API (2024) et constitue toujours la version stable actuelle. Les points de terminaison antérieurs v3.x sont obsolètes.

## Comment utiliser l’API Convertir un tableau en JSON avec les SDK ?

### Spécification de l’API Convertir un tableau en JSON

La [spécification de l’API Convertir un tableau en JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} fournit une interface de programmation accessible publiquement, permettant d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
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

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK permet d’abstraire les détails de bas niveau, vous permettant ainsi de convertir un tableau de feuille de calcul en fichier JSON avec un code minimal. Reportez-vous au dépôt GitHub officiel pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}