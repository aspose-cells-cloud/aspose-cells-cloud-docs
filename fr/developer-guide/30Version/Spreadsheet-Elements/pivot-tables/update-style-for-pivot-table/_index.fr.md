---
title: "Mettre à jour le style d'un tableau croisé dynamique"
second_title: "Document"
linktype: "Mettre en forme tout"
type: docs
url: /fr/pivot-tables/format-all/
aliases: [  /fr/update-style-for-pivot-table/ ]
keywords: "tableau croisé dynamique, mise à jour du style, Aspose.Cells Cloud, API REST, Excel, feuille de calcul, API, style de tableau croisé dynamique, mettre en forme tout"
description: "Découvrez comment mettre à jour le style d’un tableau croisé dynamique entier à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails de la requête, un exemple cURL et des extraits de code SDK pour plusieurs langages de programmation."
weight: 100
ArticleTitle: "Mettre à jour le style d'un tableau croisé dynamique - Aspose.Cells Cloud API"
---

Cette API REST met à jour le style d’un tableau croisé dynamique.

## API PostPivotTableStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**Conditions préalables / Authentification**  
Un jeton d’accès JWT valide doit être fourni dans l’en-tête `Authorization` (par exemple, `Bearer <jeton jwt>`). Assurez-vous que le jeton dispose des autorisations nécessaires pour accéder au classeur et à la feuille de calcul spécifiés.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------ |
| name             | string  | chemin      | Le nom du fichier du classeur.                                                                   |
| sheetName        | string  | chemin      | La feuille de calcul contenant le tableau croisé dynamique.                                      |
| pivotTableIndex  | integer | chemin      | Index à base zéro du tableau croisé dynamique à mettre en forme.                                 |
| style            | object  | corps       | Un DTO de style définissant la mise en forme à appliquer.                                        |
| needReCalculate  | boolean | requête     | Définir sur **true** pour recalculer le tableau croisé dynamique après la mise en forme ; la valeur par défaut est **false**. |
| folder           | string  | requête     | Le dossier dans lequel le classeur est stocké.                                                  |
| storageName      | string  | requête     | Le nom du service de stockage.                                                                   |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                             |
|------|-----------------------------|-------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                         |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                     |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                              |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer avec l’API. Le SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

L’exemple de code suivant illustre comment appeler l’API à l’aide du SDK Go :

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}