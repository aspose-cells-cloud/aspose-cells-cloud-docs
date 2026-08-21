---
title: "Ajouter un tableau croisé dynamique dans une feuille de calcul Excel"
second_title: "Document"
linktitle: Ajouter
type: docs
url: /fr/pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "ajouter un tableau croisé dynamique, feuille de calcul Excel, Aspose.Cells Cloud, API REST, SDK, tableau croisé dynamique Excel"
description: "Utilisez l’API REST Aspose.Cells Cloud pour ajouter un tableau croisé dynamique dans une feuille de calcul Excel. Disponible via les SDK pour C#, Java, PHP, Python, Node.js, Android, Swift, Perl, Go."
weight: 30
ArticleTitle: "Comment ajouter un tableau croisé dynamique dans une feuille de calcul Excel à l’aide d’Aspose.Cells Cloud"
---

Cette API REST ajoute un tableau croisé dynamique dans une feuille de calcul.

**Prérequis :**  
- Un compte Aspose.Cells Cloud disposant d’un jeton d’accès JWT valide.  
- Le classeur cible doit être stocké dans un emplacement pris en charge (stockage par défaut ou un stockage spécifié par l’utilisateur).  
- La feuille de calcul spécifiée par `sheetName` doit exister dans le classeur.  

## API PutWorksheetPivotTable

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                                                                                         |
| ---------------- | ------- | ----------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| name             | string  | path        | Le nom du document Excel.                                                                                                          |
| sheetName        | string  | path        | Le nom de la feuille de calcul dans laquelle le tableau croisé dynamique sera créé.                                               |
| request          | object  | body        | DTO `CreatePivotTableRequest` contenant la définition du tableau croisé dynamique.                                                |
| folder           | string  | query       | Le dossier contenant le document.                                                                                                  |
| storageName      | string  | query       | Le nom du stockage dans lequel le document est situé.                                                                              |
| sourceData       | string  | query       | La plage fournissant les données sources pour le nouveau cache de tableau croisé dynamique (par exemple, `A5:E10`).              |
| destCellName     | string  | query       | L’adresse de la cellule en haut à gauche de la plage de destination pour le rapport du tableau croisé dynamique.                  |
| tableName        | string  | query       | Le nom attribué au nouveau tableau croisé dynamique.                                                                               |
| useSameSource    | boolean | query       | Si `true`, le nouveau tableau croisé dynamique réutilise une source de données existante, économisant ainsi de la mémoire si un autre tableau croisé dynamique a déjà utilisé cette source. |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST à partir d’un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL.

**Note de sécurité :** Utilisez toujours `https://` lors de l’appel de l’API et gardez votre jeton JWT confidentiel ; sa transmission en clair via HTTP expose le jeton à une interception.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

{{< /tab >}}

{{< /tabs >}}

**Codes de statut HTTP**

| Code | Signification                | Description                                                        |
|------|------------------------------|--------------------------------------------------------------------|
| 200  | OK                           | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                 | Jeton JWT invalide ou manquant.                                    |
| 413  | Charge utile trop grande      | Le fichier envoyé dépasse la limite de taille.                   |
| 500  | Erreur interne du serveur    | Erreur inattendue du serveur.                                      |

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

Pour plus d’opérations, consultez les pages API associées : **[Obtenir un tableau croisé dynamique](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[Supprimer un tableau croisé dynamique](https://docs.aspose.cloud/cells/pivot-tables/delete/)** et **[Mettre à jour un tableau croisé dynamique](https://docs.aspose.cloud/cells/pivot-tables/update/)**.