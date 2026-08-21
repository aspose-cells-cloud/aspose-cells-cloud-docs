---
title: "Aspose.Cells Cloud Web API – Convertir une feuille de calcul en JSON"
second_title: "Document"
ArticleTitle: "Comment convertir une feuille de calcul locale en JSON à l’aide de l’API Aspose.Cells Cloud"
linktype: "Convert Spreadsheet to JSON"
type: docs
url: /fr/convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, convertir une feuille de calcul en JSON, API Excel vers JSON, API Aspose.Cells Cloud, API REST, conversion de feuilles de calcul"
description: "Découvrez comment convertir des fichiers Excel locaux en JSON à l’aide de l’API Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, un exemple de code et la gestion des erreurs pour une intégration fluide."
weight: 100
---

L’**endpoint ConvertSpreadsheetToJson** convertit une feuille de calcul stockée sur un disque local en fichier JSON entièrement côté serveur Aspose.Cells Cloud. En envoyant la feuille de calcul sous la forme `multipart/form-data`, le service renvoie un flux JSON prêt à être téléchargé ou traité ultérieurement. Cette conversion native cloud élimine la nécessité de télécharger d’abord le fichier vers le stockage, réduit les coûts de stockage et simplifie le flux de travail des applications exigeant des données de feuille de calcul au format JSON pour l’analyse, les rapports ou l’échange de données.

**Prérequis** : Vous devez disposer d’un compte Aspose Cloud, d’un jeton d’accès JWT valide, ainsi que du SDK ou de la clé API Aspose.Cells Cloud configurés.

**Contexte** : La conversion de feuilles de calcul en JSON est une étape fréquente lors de l’intégration des données Excel avec des services web, des bases de données NoSQL ou des applications JavaScript côté client. L’API Convert Spreadsheet to JSON propose une conversion rapide côté serveur, sans avoir à conserver le fichier original.

## API Convert Spreadsheet to JSON

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type                       | Emplacement | Obligatoire/Optionnel | Description                                                                                                                                                                     |
| :--------------- | :------------------------- | :--------- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | Fichier (multipart/form-data) | FormData | Obligatoire          | Le fichier source de la feuille de calcul (par ex. .xls, .xlsx, .xlsm). Exemple : `curl -F "Spreadsheet=@monFichier.xlsx"`                                                     |
| outPath          | String                     | Query    | Optionnel            | Chemin du dossier cible dans le stockage cloud où le fichier JSON converti sera enregistré. Si omis, le JSON est renvoyé directement dans le flux de réponse. Exemple : `outPath=/output/`. |
| outStorageName   | String                     | Query    | Optionnel            | Nom du stockage cloud (par ex. Amazon S3, Azure Blob) dans lequel le fichier de sortie doit être écrit. Obligatoire uniquement si `outPath` est utilisé avec un stockage non par défaut. |
| fontsLocation    | String                     | Query    | Optionnel            | Chemin vers un dossier personnalisé contenant des polices sur le serveur. À utiliser lorsque la feuille de calcul fait référence à des polices non disponibles dans la bibliothèque par défaut. |
| region           | String                     | Query    | Optionnel            | Paramètre de région/langue de la feuille de calcul (par ex. `fr-FR`, `en-US`). Affecte le formatage des nombres, des dates et des devises durant la conversion.               |
| password         | String                     | Query    | Optionnel            | Mot de passe pour ouvrir une feuille de calcul protégée par mot de passe. À omettre pour les fichiers non protégés.                                                           |

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

| Code | Signification         | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Le filtre a été appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête      | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite autorisée.         |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                        |

## Où utiliser l’API Convert Spreadsheet to JSON ?

- **Pipelines de migration de données** – Convertir des rapports Excel hérités en JSON afin de les ingérer dans des bases de données NoSQL modernes ou des lacs de données.
- **Applications mobiles ou web** – Transformer rapidement les feuilles de calcul uploadées par les utilisateurs en JSON pour un rendu côté client, sans stocker le fichier original dans le cloud.
- **Rapport automatisé** – Générer des charges utiles JSON pour des services d’analyse en aval (par ex. Power BI, Tableau) directement à partir d’entrées de feuilles de calcul.
- **Fonctions sans serveur** – Utiliser l’API dans AWS Lambda ou Azure Functions pour effectuer des conversions à la volée sans gérer de stockage temporaire.

## Pourquoi utiliser l’API Convert Spreadsheet to JSON ?

- Conversion native cloud : élimine le besoin de télécharger de gros fichiers vers le stockage avant traitement, réduisant ainsi la latence et les coûts de stockage.
- Flux de travail en une seule requête : téléchargez la feuille de calcul et recevez le JSON dans le même appel HTTP, simplifiant la logique d’intégration.
- Prend en charge les feuilles de calcul protégées par mot de passe et celles spécifiques à une région, garantissant une représentation précise des données selon les localisations.
- Évolutif sur l’infrastructure Aspose : gère de gros classeurs et des formules complexes sans impacter les ressources de votre propre serveur.

## Comment utiliser l’API Convert Spreadsheet to JSON avec les SDK

### Spécification de l’API Convert Spreadsheet to JSON

La [spécification de l’API Convert Spreadsheet to JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) fournit une interface de programmation publiquement accessible permettant d’exécuter directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels vers l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/resultat.json" \
     -H "Authorization: Bearer {jeton_d'accès}" \
     -F "Spreadsheet=@monClasseur.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et permet de convertir une feuille de calcul en JSON en quelques lignes de code.  
Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.  
Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}