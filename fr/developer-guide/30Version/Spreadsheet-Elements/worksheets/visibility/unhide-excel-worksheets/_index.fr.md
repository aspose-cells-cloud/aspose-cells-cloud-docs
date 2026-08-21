---
title: "Révéler une feuille Excel"
second_title: "Document"
linktitle: "Révéler"
type: docs
url: /worksheets/unhide/
aliases: [/unhide-excel-worksheets/]
keywords: "Aspose.Cells, révéler une feuille, API Excel, classeur cloud, REST, visibilité de feuille, classeur Excel"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour révéler une feuille dans un classeur Excel. Inclut les détails de la requête, des exemples cURL et des extraits de code SDK pour plusieurs langages de programmation."
weight: 60
---

Cette API REST fournit un point de terminaison pour **révéler une feuille** dans un classeur Excel.

**Conditions préalables**  
Avant d’appeler cette opération, vous devez disposer de :

* Un jeton d’accès Aspose Cloud valide (JWT) inclus dans l’en-tête `Authorization`.  
* Le classeur stocké dans un emplacement de stockage pris en charge que vous spécifiez à l’aide des paramètres de requête `folder` et `storageName`.  
* Le classeur doit être au format pris en charge par Aspose.Cells (par exemple, `.xls`, `.xlsx`, `.xlsm`).  

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                               |
| ---------------- | ------- | ----------- | ----------------------------------------- |
| name             | string  | path        | Nom du document.                          |
| sheetName        | string  | path        | Nom de la feuille.                        |
| isVisible        | boolean | query       | Nouvelle valeur de visibilité de la feuille (`true`). |
| folder           | string  | query       | Dossier du document.                      |
| storageName      | string  | query       | Nom du stockage.                          |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) définit une interface de programmation accessible publiquement qui permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler facilement les services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer une requête avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"   # remplacer <jeton jwt> par votre jeton d’accès
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de réponse possibles**

| Code HTTP | Signification                                              | Corps d’exemple (le cas échéant)                           |
|-----------|------------------------------------------------------------|-------------------------------------------------------------|
| 200       | Visibilité de la feuille mise à jour avec succès         | `{ "Code": 200, "Status": "OK" }`                           |
| 400       | Requête incorrecte – paramètres manquants ou non valides | `{ "Code": 400, "Message": "Paramètres de requête non valides." }` |
| 401       | Non autorisé – jeton JWT manquant ou non valide          | `{ "Code": 401, "Message": "Échec de l’authentification." }` |
| 404       | Non trouvé – classeur ou feuille inexistante             | `{ "Code": 404, "Message": "Fichier ou feuille non trouvé." }` |
| 500       | Erreur interne du serveur                                 | `{ "Code": 500, "Message": "Une erreur inattendue s'est produite." }` |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}