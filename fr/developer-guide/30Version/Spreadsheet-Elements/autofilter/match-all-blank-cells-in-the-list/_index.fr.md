---
title: "Correspondre à toutes les cellules vides dans une feuille de calcul Excel"
ArticleTitle: "Correspondre à toutes les cellules vides dans une feuille de calcul Excel – Guide de l’API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, cellules vides, AutoFilter, API REST, Excel"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour filtrer et correspondre à toutes les cellules vides dans une feuille de calcul Excel. Inclut le point de terminaison, les paramètres, les étapes d’authentification, un exemple cURL et des extraits de code SDK pour C#, Java, Python, et plus encore."
weight: 100
---

Cette API REST permet de correspondre à toutes les **cellules vides** dans la liste de filtrage d’une feuille de calcul Excel.

**Prérequis :** Avant d’appeler ce point de terminaison, assurez-vous d’avoir un jeton d’accès JWT valide, que le classeur ait été téléchargé dans le stockage Aspose Cloud, et que vous connaissiez le dossier de stockage (le cas échéant). Fournissez les paramètres `folder` et `storageName` si le fichier ne se trouve pas dans le dossier racine par défaut.

## API PostWorksheetMatchBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                             |
|------------------|---------|-------------|-------------------------------------------------------------------------|
| name             | string  | chemin      | Le nom du fichier du classeur.                                          |
| sheetName        | string  | chemin      | Le nom de la feuille de calcul contenant le filtre.                    |
| fieldIndex       | integer | requête     | Indice (à partir de zéro) de la colonne à laquelle le filtre est appliqué. |
| folder           | string  | requête     | Le chemin du dossier dans le stockage où se trouve le classeur.        |
| storageName      | string  | requête     | Le nom du stockage Aspose Cloud.                                        |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                              |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                          |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la taille limite.                        |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                            |

## Comment utiliser l’API PostWorksheetMatchBlanks avec les SDK

### Spécification de l’API PostWorksheetMatchBlanks

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```
{{< /tab >}}

{{< tab tabNum="12" >}}
```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Un SDK masque les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}