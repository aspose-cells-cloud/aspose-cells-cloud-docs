---
title: "Aspose.Cells Cloud – Convertir une plage Excel en HTML"
description: "Convertir une plage spécifique d’un fichier Excel (par exemple, A1:C10) en fichier HTML à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’authentification, des exemples de requêtes, la gestion des réponses, des extraits de code SDK et les codes d’erreur."
keywords: "Aspose.Cells, Excel vers HTML, conversion de plage, API cloud, feuille de calcul"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Convertissez une plage sélectionnée d’un classeur Excel local en fichier HTML directement via Aspose.Cells Cloud. La conversion a lieu entièrement sur le serveur cloud, de sorte que vous n’avez jamais besoin de télécharger l’ensemble du classeur ni d’avoir Excel installé localement.

## API Convertir une plage en HTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

Le corps de la requête est de type `multipart/form-data` contenant le fichier de feuille de calcul. Toutes les autres options sont fournies sous forme de paramètres de requête.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de requête

| Nom                | Type    | Emplacement | Obligatoire | Description                                                                 |
|--------------------|---------|-------------|-------------|-----------------------------------------------------------------------------|
| **Spreadsheet**    | Fichier | FormData    | Oui         | Le classeur Excel à convertir.                                              |
| **worksheet**      | Chaîne  | Query       | Oui         | Nom de la feuille de calcul contenant la plage.                             |
| **range**          | Chaîne  | Query       | Oui         | Zone de cellules à convertir, par exemple `A1:C10`.                         |
| **outPath**        | Chaîne  | Query       | Non         | Chemin du dossier où le fichier HTML résultat doit être enregistré (par défaut `null`). |
| **outStorageName** | Chaîne  | Query       | Non         | Nom du service de stockage pour le fichier de sortie.                      |
| **fontsLocation**  | Chaîne  | Query       | Non         | Chemin vers un dossier personnalisé de polices.                             |
| **AutoRowsFit**    | Booléen | Query       | Non         | Ajuster automatiquement la hauteur de toutes les lignes de la feuille.      |
| **AutoColumnsFit** | Booléen | Query       | Non         | Ajuster automatiquement la largeur de toutes les colonnes de la feuille.    |
| **region**         | Chaîne  | Query       | Non         | Identifiant de paramètres régionaux (par exemple, `en-US`, `fr-FR`). Affecte le format des nombres et des dates. |
| **password**       | Chaîne  | Query       | Non         | Mot de passe pour ouvrir un classeur protégé.                              |
| **fontsLocation**  | Chaîne  | Query       | Non         | Emplacement personnalisé des polices.                                       |
| **region**         | Chaîne  | Query       | Non         | Paramètre de région/langue de la feuille de calcul.                        |
| **password**       | Chaîne  | Query       | Non         | Mot de passe pour ouvrir le fichier de feuille de calcul.                  |

## Réponse

L’API renvoie le fichier HTML converti sous forme de **flux binaire** (`application/octet-stream`).

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

### Exemple de réponse réussie (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

Enregistrez le corps de la réponse dans un fichier (par exemple, `report.html`) pour visualiser le tableau rendu dans un navigateur.

---

**Codes de statut HTTP**

| Code | Signification         | Description                                                     |
|------|-----------------------|-----------------------------------------------------------------|
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la taille limite.               |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                    |

## Comment utiliser l’API Convertir une plage en HTML avec les SDK ?

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) décrit une API publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet de convertir une plage de données en fichier HTML avec un minimum de code.  
Consultez la liste complète des SDK Aspose.Cells Cloud sur notre [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK. Si le chargement depuis Gist est bloqué, vous pouvez télécharger directement les exemples depuis le dépôt.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}