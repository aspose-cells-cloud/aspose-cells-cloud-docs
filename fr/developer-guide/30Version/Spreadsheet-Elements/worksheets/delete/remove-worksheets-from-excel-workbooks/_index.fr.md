---
title: "Supprimer une feuille de calcul"
second_title: "Document"
linktype: "Une feuille de calcul"
type: docs
url: /worksheets/delete-worksheet/
aliases: [/remove-worksheets-from-excel-workbooks/]
keywords: "Aspose.Cells Cloud, Supprimer une feuille de calcul, Excel, Classeur, API REST"
description: "Supprimer une feuille de calcul d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud. Prend en charge les SDK pour C#, Java, PHP, Ruby, Node.js, Python, Perl, Go et cURL."
weight: 20
ArticleTitle: "Supprimer une feuille de calcul – API Aspose.Cells Cloud"
---

Cette API REST permet de supprimer une feuille de calcul.  
Prérequis : Pour appeler cette API, vous devez fournir un jeton d’authentification JWT valide dans l’en-tête **Authorization** et avoir accès à l’emplacement de stockage où se trouve le classeur.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*Remarque : L’API utilise la version **v3.0**, qui est la version stable actuelle. Toute évolution future de la version sera annoncée dans les notes de version.*

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description              |
| ---------------- | ------ | ----------- | ------------------------ |
| name             | string | path        | Nom du document.         |
| sheetName        | string | path        | Nom de la feuille de calcul. |
| folder           | string | query       | Dossier du document.     |
| storageName      | string | query       | Nom du stockage.         |

Réponses HTTP possibles :

| Code d’état | Description |
| ----------- | ----------- |
| 200 OK | Feuille de calcul supprimée avec succès. |
| 400 Bad Request | Paramètres de requête invalides. |
| 401 Unauthorized | Échec de l’authentification ou jeton manquant. |
| 404 Not Found | Le classeur ou la feuille de calcul spécifié n’existe pas. |
| 500 Internal Server Error | Erreur inattendue du serveur. |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

*Toutes les requêtes doivent être effectuées via HTTPS ; l’API ne prend pas en charge les connexions non TLS.*

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

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}