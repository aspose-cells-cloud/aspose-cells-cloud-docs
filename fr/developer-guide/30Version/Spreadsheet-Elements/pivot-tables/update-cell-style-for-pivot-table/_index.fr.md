---
title: "Mettre à jour le style de cellule pour un tableau croisé dynamique"
second_title: "Document"
linktype: "Format"
type: docs
url: /fr/pivot-tables/format/
aliases: [/fr/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, style de tableau croisé dynamique, API de mise à jour du style de cellule, API REST, API Excel, formatage de feuille de calcul, SDK cloud, style de cellule, tableau croisé dynamique"
description: "Découvrez comment mettre à jour le style d’une cellule spécifique dans un tableau croisé dynamique Aspose.Cells Cloud via l’API REST. Inclut le point de terminaison, les paramètres, l’authentification, un exemple cURL, un extrait de code Go SDK et des conseils optimisés pour le référencement."
weight: 90
ArticleTitle: "Mettre à jour le style de cellule pour un tableau croisé dynamique - Documentation de l’API Aspose.Cells Cloud"
---

Cette API REST met à jour le **style** d'une cellule dans un tableau croisé dynamique.

**Conditions préalables / Authentification**  
Pour appeler ce point de terminaison, vous devez disposer d’un jeton d’accès JWT Aspose Cloud valide. Obtenez le jeton via le flux OAuth 2.0 décrit dans le [Guide d’authentification](/fr/authentication/). Incluez le jeton dans l’en-tête de la requête :

```http
Authorization: Bearer <jeton JWT>
```

Le jeton JWT est requis pour toutes les appels à l’API Aspose.Cells Cloud.

## API PostPivotTableCellStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                                                             |
| ----------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------------- |
| name              | string  | path        | Nom du document (obligatoire).                                                                          |
| sheetName         | string  | path        | Nom de la feuille de calcul (obligatoire).                                                             |
| pivotTableIndex   | integer | path        | Index du tableau croisé dynamique (obligatoire).                                                       |
| column            | integer | query       | Index de colonne (à partir de zéro) de la cellule à formater (obligatoire).                            |
| row               | integer | query       | Index de ligne (à partir de zéro) de la cellule à formater (obligatoire).                              |
| style             | object  | body        | Objet DTO de style (objet de transfert de données) définissant le nouveau style de cellule.            |
| needReCalculate   | boolean | query       | Indique si le tableau croisé dynamique doit être recalculé après le formatage. La valeur par défaut est **false**. |
| folder            | string  | query       | Dossier dans lequel le document est stocké (facultatif).                                               |
| storageName       | string  | query       | Nom du stockage (facultatif).                                                                          |
| Method            | string  | N/A         | Méthode HTTP utilisée pour la requête (**POST**).                                                      |

La <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Réponse**  
En cas de succès, le service renvoie un code HTTP 200 avec un corps vide, indiquant que le style a été appliqué. En cas d’erreur, une charge utile JSON contenant un code et un message d’erreur est renvoyée.

| Statut HTTP | Description                                            |
|-------------|--------------------------------------------------------|
| 200         | Style appliqué avec succès.                            |
| 400         | Requête incorrecte – par exemple, index de colonne/ligne invalide. |
| 401         | Non autorisé – jeton JWT manquant ou invalide.         |
| 404         | Introuvable – le document, la feuille ou le tableau croisé dynamique spécifié n’existe pas. |
| 500         | Erreur interne du serveur – condition inattendue.      |

Le corps de la réponse est vide en cas de succès.

Pour plus d’informations, consultez la documentation de l’API **Get Pivot Table**.

## Famille de SDK Cloud

Utiliser un SDK est la méthode la plus rapide pour développer. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

L’exemple de code suivant illustre comment appeler les services web Aspose.Cells à l’aide du **SDK Go** :

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Mettre à jour le style de cellule pour un tableau croisé dynamique",
  "description": "Guide pour mettre à jour le style d’une cellule spécifique dans un tableau croisé dynamique Aspose.Cells Cloud à l’aide de l’API REST.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, tableau croisé dynamique, style de cellule, API REST, SDK Go",
  "url": "https://docs.aspose.cloud/fr/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---