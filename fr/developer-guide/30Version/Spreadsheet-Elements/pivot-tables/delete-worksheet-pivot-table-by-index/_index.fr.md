---
title: "Supprimer un tableau croisé dynamique dans une feuille Excel"
second_title: "Document"
linktype: "Supprimer"
type: docs
url: /fr/pivot-tables/delete/
aliases: [  /fr/delete-worksheet-pivot-table-by-index/ ]
keywords: "Aspose.Cells, tableau croisé dynamique, suppression, Excel, API REST"
description: "Supprimer un tableau croisé dynamique d'une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut le format de requête, un exemple cURL, les codes d’erreur et des extraits de code SDK pour C#, Java, Python et Node.js."
weight: 70
ArticleTitle: "Comment supprimer un tableau croisé dynamique dans une feuille Excel avec Aspose.Cells Cloud"
---

Cette API REST supprime un tableau croisé dynamique d'une feuille à partir de son index.

**Conditions préalables** – Vous devez disposer d’un jeton d’accès JWT valide pour Aspose.Cells Cloud, ainsi que du fichier Excel cible stocké dans un emplacement pris en charge par le service de stockage. Assurez-vous que le nom du fichier, le nom de la feuille et les détails du service de stockage sont correctement spécifiés avant d’invoquer l’API.

Les tableaux croisés dynamiques constituent une méthode puissante pour résumer les données dans une **feuille Excel**. À l’aide d’Aspose.Cells Cloud, vous pouvez supprimer de façon programmatique un tableau croisé dynamique indésirable en envoyant une seule requête HTTP DELETE. Cette opération est particulièrement adaptée lorsqu’il s’agit de nettoyer des feuilles, d’automatiser la génération de rapports ou d’intégrer la manipulation Excel dans vos applications.

## API DeleteWorksheetPivotTable

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/fr/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                 |
| ------------------ | ------- | ----------- | ----------------------------------------------------------- |
| name               | string  | path        | Nom du document Excel.                                      |
| sheetName          | string  | path        | Nom de la feuille contenant le tableau croisé dynamique.   |
| pivotTableIndex    | integer | path        | Index de base zéro du tableau croisé dynamique à supprimer. |
| folder             | string  | query       | Chemin vers le dossier dans lequel le document est stocké. |
| storageName        | string  | query       | Nom du service de stockage.                                 |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/fr/#/PivotTables/DeleteWorksheetPivotTable) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Exemple de réponse**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La réponse suit un schéma JSON simple :

```json
{
  "Code": integer,   // Code de statut similaire à HTTP de l'opération
  "Status": string   // Description textuelle, par ex. « OK »
}
```

{{< /tab >}}

{{< /tabs >}}

### Gestion des erreurs

Les codes de statut de réponse courants sont répertoriés ci-dessous :

| Statut HTTP | Description                                                        |
| ----------- | ------------------------------------------------------------------ |
| 400         | Requête incorrecte – paramètres manquants ou non valides.         |
| 401         | Accès non autorisé – jeton JWT invalide ou absent.                |
| 404         | Introuvable – le fichier, la feuille ou le tableau croisé dynamique n’existe pas. |
| 500         | Erreur interne du serveur – une condition inattendue s’est produite côté serveur. |

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}
---