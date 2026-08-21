---
title: "Aspose.Cells Cloud Web API – Convertir un classeur en CSV"
second_title: "Document"
ArticleTitle: "Comment convertir un classeur en CSV à l’aide de l’API Aspose.Cells Cloud"
linktitle: "Convertir un classeur en CSV"
type: docs
url: /fr/convert-spreadsheet-to-csv/
keywords: "Aspose Cells, conversion CSV, API Excel, conversion cloud"
description: "Découvrez comment convertir des fichiers Excel (XLS, XLSX, XLSM, etc.) en CSV à l’aide de l’API Aspose.Cells Cloud. Inclut les étapes d’authentification, un exemple cURL, des extraits de code SDK et la gestion des erreurs."
weight: 100
---

Le point de terminaison **ConvertSpreadsheetToCsv** lit un fichier de classeur téléchargé depuis un disque local, effectue la conversion entièrement sur les serveurs Aspose.Cells Cloud, puis renvoie le fichier CSV résultant sous forme de flux binaire. Cette opération native cloud élimine la nécessité de téléverser le fichier source vers le stockage cloud, réduit les coûts de stockage et simplifie le flux de travail pour les développeurs ayant besoin de conversions rapides de classeurs vers CSV. Les formats pris en charge dépendent des bibliothèques sous-jacentes, et des autorisations adéquates sont nécessaires pour lire le fichier source. Les erreurs telles que les fichiers manquants, les requêtes invalides ou les échecs de conversion sont renvoyées avec des codes de statut HTTP standard.

## **API Convertir un classeur en CSV**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement | Obligation | Description                                                                                                                                                         |
| :--------------- | :----- | :---------- | :--------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | Fichier | FormData    | Obligatoire | Le fichier de classeur à convertir. Prend en charge les formats courants tels que .xls, .xlsx, .xlsm. Doit être fourni en tant que multipart/form‑data. Exemple : `monClasseur.xlsx`. |
| outPath          | Chaîne  | Query       | Facultatif  | Chemin du dossier de destination où le CSV converti doit être enregistré. Si omis, le CSV est renvoyé directement dans le corps de la réponse. Exemple : `/sortie/rapports/`.     |
| outStorageName   | Chaîne  | Query       | Facultatif  | Nom du service de stockage cloud où le fichier de sortie sera stocké. Si non fourni, le stockage par défaut configuré pour le compte Aspose.Cells est utilisé.              |
| fontsLocation    | Chaîne  | Query       | Facultatif  | Chemin vers un dossier contenant les polices personnalisées nécessaires au classeur. Permet un rendu correct des cellules utilisant des polices non standard.                  |
| region           | Chaîne  | Query       | Facultatif  | Paramètre de région/langue du classeur (par exemple, `fr-FR`, `en-US`). Influence le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale.         |
| password         | Chaîne  | Query       | Facultatif  | Mot de passe utilisé pour ouvrir les classeurs protégés par mot de passe. Si le fichier est chiffré et que le mot de passe est omis ou incorrect, une erreur HTTP 400/401 est renvoyée. |

### **Réponse**

En cas de succès, l’API renvoie **HTTP 200** (ou **202** pour un traitement asynchrone) avec l’en-tête `Content-Type: application/octet-stream`. Le corps de la réponse contient le fichier CSV généré sous forme de flux binaire.

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

| Code | Signification             | Description                                                      |
| ---- | ------------------------- | ---------------------------------------------------------------- |
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte        | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop volumineuse | Le fichier téléversé dépasse la limite de taille.                   |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                       |

## Où faut-il utiliser l’API Convertir un classeur en CSV ?

- **Exportation de données pour les systèmes de rapports** – Générer des extraits CSV à partir de rapports Excel afin d’alimenter des outils BI ou des entrepôts de données, sans manipulation manuelle des fichiers.
- **Traitement par lots automatisé** – Convertir un grand nombre de classeurs stockés localement en CSV au sein d’un travail côté serveur, puis diffuser directement les résultats vers les services aval.
- **Applications web avec téléchargement de fichiers** – Permettre aux utilisateurs finaux de télécharger un fichier Excel et de recevoir instantanément une version CSV pour une analyse ultérieure ou une importation dans d’autres plateformes.
- **Intégration de systèmes hérités** – Traduire les formats hérités de classeurs en CSV pour les systèmes ne prenant en charge que les fichiers texte délimités simples.

## Pourquoi utiliser l’API Convertir un classeur en CSV ?

- **Architecture sans téléversement vers le cloud** – Aucune nécessité de stocker le fichier source dans le stockage cloud ; la conversion a lieu directement à partir du flux téléversé, ce qui fait gagner du temps et réduit les coûts de stockage.
- **Traitement cloud haute performance** – Exploite le moteur de conversion optimisé d’Aspose.Cells sur des serveurs cloud évolutifs, fournissant une sortie CSV rapide même pour de grands classeurs.
- **Intégration simple** – Une seule requête PUT avec des paramètres de requête facultatifs ; renvoie le CSV sous forme de flux binaire prêt au téléchargement, éliminant les étapes de post-traitement.
- **Prise en charge complète des fonctionnalités** – Gère les fichiers protégés par mot de passe, les polices personnalisées et les paramètres spécifiques à la locale, garantissant une conversion précise même pour des classeurs complexes.

## Comment utiliser l’API Convertir un classeur en CSV avec les SDK

### Spécification de l’API Convertir un classeur en CSV

La [Spécification de l’API Convertir un classeur en CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv) fournit une interface de programmation accessible publiquement permettant d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant ainsi de travailler avec les classeurs à l’aide d’un code concis. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud. Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}