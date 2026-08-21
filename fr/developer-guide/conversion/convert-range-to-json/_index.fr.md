---
title: "Aspose.Cells Cloud Web API - Convertir les données locales d'une plage Excel en fichier JSON - Outil gratuit en ligne"
second_title: "Document"
ArticleTitle: "Comment convertir les données d'une plage de feuille de calcul locale en fichier JSON : guide étape par étape"
linktitle: "Convertir une plage en JSON"
type: docs
url: /convert-range-to-json/
keywords: "convertir une plage en json, Aspose.Cells Cloud, Excel vers JSON, conversion de feuille de calcul, API"
description: "Convertir une plage spécifique d'une feuille de calcul Excel locale en JSON à l'aide de l'API Aspose.Cells Cloud."
weight: 100
---

Exporter les données d'une plage à partir d'un fichier Excel local vers un fichier JSON à l'aide de l'API Cloud.

## **API Convertir une plage en JSON**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                 |
|------------------|--------|-------------------------------------------------------|-----------------------------------------------------------------------------|
| Spreadsheet      | Fichier | FormData                                              | Télécharger le fichier de feuille de calcul.                                |
| worksheet        | Chaîne  | Chaîne de requête                                     | Nom de la feuille de calcul dans le classeur.                               |
| range            | Chaîne  | Chaîne de requête                                     | Zone de cellules à convertir, par exemple A1:C10.                           |
| outPath          | Chaîne  | Chaîne de requête                                     | (Facultatif) Chemin du dossier où le classeur est stocké ; la valeur par défaut est null. |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Nom du stockage de sortie.                                                  |
| fontsLocation    | Chaîne  | Chaîne de requête                                     | Emplacement pour stocker les polices personnalisées à usage personnel.      |
| region           | Chaîne  | Chaîne de requête                                     | Paramètre de région de la feuille de calcul.                                |
| password         | Chaîne  | Chaîne de requête                                     | Mot de passe pour ouvrir le fichier de feuille de calcul.                   |

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

**Codes de statut HTTP**

| Code | Signification           | Description                                                          |
|------|-------------------------|----------------------------------------------------------------------|
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                      |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la taille limite.                     |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                          |

## **À quoi servir l’API Convertir une plage en JSON ?**

- **Tableaux de bord en temps réel** : Convertir les données Excel en direct en JSON pour les bibliothèques de visualisation comme Chart.js ou D3.js.
- **Feuille de calcul en tant que service (Spreadsheet-as-a-Service)** : Exposer des plages Excel sous forme de points de terminaison JSON pour d'autres services.
- ** Charges utiles de webhook** : Transformer les données de feuilles de calcul en JSON pour les notifications webhook.
- **Prototypage rapide des données** : Convertir rapidement des données Excel nettoyées en JSON pour une analyse avec Python ou R.
- **Pipelines d’apprentissage automatique (machine learning)** : Prétraiter les données d’entraînement provenant de feuilles de calcul maintenues par des utilisateurs métier.
- **Opérations e‑commerce** : Synchroniser des catalogues produits ou des feuilles de tarification avec des sites web via JSON.
- **Automatisation des rapports** : Générer des flux de données JSON à partir de modèles financiers pour des rapports automatisés.
- **Configuration d’applications** : Gérer les drapeaux de fonctionnalités, les paramètres ou les paramètres des tests A/B dans Excel → JSON.
- **Prise en charge multilingue** : Convertir des feuilles de calcul de localisation en JSON pour les bibliothèques i18n.
- **Menus/navigation dynamiques** : Stocker les structures de navigation de site web dans Excel et les déployer en tant que JSON.

_Pour d'autres options de conversion, consultez le guide [Convertir une plage en CSV](/convert-range-to-csv/)._

## Pourquoi utiliser l’API Convertir une plage en JSON ?

- **Support des SDK** : Aspose.Cells Cloud fournit des bibliothèques pour plusieurs langages, réduisant ainsi la quantité de code personnalisé nécessaire.
- **Réduction des coûts de stockage** : La plage peut être convertie sans avoir à télécharger préalablement l’ensemble du classeur, économisant ainsi de l’espace de stockage.
- **Compatibilité avec les applications web et mobiles** : JSON est le format de données natif des frameworks JavaScript modernes comme React, Vue et Angular.
- **Large support des langages** : Presque tous les langages de programmation et bases de données peuvent consommer du JSON.
- **Préservation de la structure des données**
  - **Détection intelligente de la structure** : Convertit automatiquement les données tabulaires en tableaux ou objets JSON appropriés.
  - **Cartographie des en-têtes** : Utilise la première ligne comme clés JSON pour des structures d'objets propres.
  - **Préservation des types de données** : Conserve les types nombres, dates et booléens au lieu de les convertir en texte brut.

## Comment utiliser l’API Convertir une plage en JSON à l’aide des SDK ?

### Spécification de l’API Convertir une plage en JSON

La [Spécification de l’API Convertir une plage en JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant ainsi de convertir une plage de données en fichier JSON à l’aide d’un code concis.  
Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}