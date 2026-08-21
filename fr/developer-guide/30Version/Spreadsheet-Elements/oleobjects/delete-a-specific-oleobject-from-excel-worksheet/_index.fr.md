---
title: "Supprimer un objet OLE dans une feuille Excel"
second_title: "Document"
linktitle: "Supprimer"
type: docs
url: /fr/oleobjects/delete/
aliases: [  /fr/delete-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "Aspose.Cells, Cloud, Supprimer, OLE, Objet, Excel, feuille de calcul, REST, API, SDK"
description: "Découvrez comment supprimer un objet OLE d'une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud (v4.0). Inclut l’endpoint HTTPS, les étapes d’authentification, un exemple cURL, des extraits de code SDK, des conseils sur la gestion des erreurs et des liens vers les prochaines étapes."
weight: 50
ArticleTitle: "Supprimer un objet OLE d’une feuille Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette page explique comment supprimer un objet OLE spécifique d’une feuille de calcul dans un classeur Excel à l’aide de **Aspose.Cells Cloud**. Un objet OLE peut être une image liée, un graphique ou tout autre objet intégré que Excel stocke comme entité distincte.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                           |
|------------------|---------|-------------|-------------------------------------------------------|
| name             | string  | path        | Le nom du classeur.                                   |
| sheetName        | string  | path        | Le nom de la feuille de calcul.                       |
| oleObjectIndex   | integer | path        | Index de l’objet OLE à supprimer.                     |
| folder           | string  | query       | Le dossier contenant le classeur. (facultatif)       |
| storageName      | string  | query       | Le nom du service de stockage. (facultatif)          |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer cet appel avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
  -X DELETE \
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

### Détails de la réponse

| Statut HTTP          | Description                                                              | Exemple JSON                                                          |
|----------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **200 OK**           | L’objet OLE a été supprimé avec succès.                                  | `{ "Code": 200, "Status": "OK" }`                                     |
| **401 Unauthorized** | Le jeton JWT est manquant ou invalide.                                   | `{ "Code": 401, "Message": "Le jeton d’accès est manquant ou invalide." }` |
| **404 Not Found**    | Le classeur, la feuille de calcul ou l’index d’objet OLE spécifié n’existe pas. | `{ "Code": 404, "Message": "L’index de l’objet OLE est hors limites." }` |
| **400 Bad Request**  | Les paramètres requis sont manquants ou mal formés.                      | `{ "Code": 400, "Message": "Paramètres de requête invalides." }`     |

Gérez ces réponses dans votre application en vérifiant le code de statut et en affichant le message associé.

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}